---
title: DG
description: Pattern Detector code help page.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
---
# DG {#dg}

Developer Guideline

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Developer Guidelines"
>abstract="DG code identifies deviations of selected development guidelines for AEM 6.5 and AEM as a Cloud Service. Following the best practices can improve the maintainability and performance of your system. Although some of these deviations might not be a problem in other application contexts, including with previous versions of AEM, they may cause problems when used with AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM Development - Guidelines and Best Practices"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service Development Guidelines"


`DG`  Identifies deviations of selected development guidelines for [AEM 6.5](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) and [AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines). Following the best practices can improve the maintainability and performance of your system. Although some of these deviations might not be a problem in other application contexts, including with previous versions of AEM, they may cause problems when used with AEM as a Cloud Service.

Subtypes are used to identify the different types of detected violations:

* `java.io.inputstream`: The use of `java.io.InputStream` in application code.
* `maintenance.task.configuration`: The configuration of a certain periodic maintenance activity.
* `sling.commons.scheduler`: The use of the Sling Commons Scheduler API for a scheduled task.
* `unsupported.asset.api`: The use of unsupported Asset Manager APIs in application code.
* `javax.jcr.observation.EventListener`: The use of Event Listener in application code.
* `custom.guava.cache`: The use of Guava Cache in application code.
* `java.api`: Some Java APIs were removed from Java 11 to Java 17.
* `configuration.admin`: Custom code which is accessing configurations will be flagged.
* `guava.api`: Guava is not suppoerted Out of the Box on AEM 6.5 LTS.
* `com.day.cq.dam.scene7.api.model`: There is major version change for `package com.day.cq.dam.scene7.api.model`.

## Possible implications and risks {#implications-and-risks}

* `java.io.inputstream`
  * Streaming of binary data with `java.io.InputStream` can consume memory resources to the point of impacting performance. This issue is due to the limited memory available in containers used in AEM as a Cloud Service.

* `maintenance.task.configuration`
  * Some maintenance tasks that previously required explicit configuration are now automatically configured and managed within AEM as a Cloud Service.
  * Maintenance task configuration in AEM as a Cloud Service must be moved into source control.

* `sling.commons.scheduler`
  * Applications dependent on background tasks using [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) might not work as expected because execution cannot be guaranteed in AEM as a Cloud Service.
  * Guidelines for [background tasks and long-running jobs](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs) suggest that code run as a scheduled task must also assume that the instance it is running on, can be brought down at any time. Therefore, the code must be resilient and resumable.

* `unsupported.asset.api`
  * The following APIs of AssetManager are marked as unsupported on AEM as a Cloud Service.
    * createAssetForBinary
    * getAssetForBinary
    * removeAssetForBinary
    * createAsset

* `javax.jcr.observation.EventListener`
  * Applications dependent on Event Listener might not work as expected because execution cannot be guaranteed.
  
* `custom.guava.cache`
  * Usage of Guava Cache may cause performance issues on AEM.

* `java.api`
  * With AEM 6.5 LTS on JRE17, these removed Java APIs won't be available and their usage will fail.

* `configuration.admin`
  * You should look at your usage to make sure you are not using any unsupported configs like social.

* `guava.api`
  * As Guava is not supported in AEM 6.5 LTS, the custom code is using guava won't be active.

* `com.day.cq.dam.scene7.api.model`
  * Imported package `com.day.cq.dam.scene7.api.model` in custom bundles will not resolve due to a major version change.


## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Implementation Guidance"
>abstract="Review your implementations on usage of Sling Commons Scheduler. Restructure them to Sling Jobs, restructure their system maintenance tasks, review streaming of any binary data, and refactor their code to be compliant with AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling Jobs"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance" text="Maintenance Tasks in AEM as a Cloud Service"

* `java.io.inputstream`
  * Use a direct-binary upload approach in which the binary is added to the datastore directly.
  * For assets use cases, see [aem-upload](https://github.com/adobe/aem-upload). For other types of binaries, custom upload logic can be modeled after this same pattern.

* `maintenance.task.configuration`
  * Review AEM as a Cloud Service [Maintenance Task](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/maintenance) documentation.
  * Ensure that [Maintenance Task Configuration](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) is in source control.

* `sling.commons.scheduler`
  * Replace the use of [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) with [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), which have an at-least-once execution guarantee.
  * Long-running jobs should be avoided.

* `unsupported.asset.api`
  * Instead of using the unsupported APIs of Asset Manager, see [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
  * Instead of using the Event Listener, It is advised to refactor the event handling mechanism to [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) as it provides the guarantee of processing.

* `custom.guava.cache`
  * Caches, if necessary, should be created outside AEM. External caching solution might be considered.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.

* `configuration.admin`
  * Remove any config usage of non supported features like Social.

* `guava.api`
  * Either install Guava or remove usage if Guava is used in your custom code. 

* `com.day.cq.dam.scene7.api.model`
  * Update the version range for the imported package `com.day.cq.dam.scene7.api.model` to **3.0.4**.