---
title: DG
description: Pattern Detector code help page
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
---
# DG {#dg}

Developer Guideline

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Developer Guidelines"
>abstract="DG code identifies deviations of selected development guidelines for AEM 6.5 and AEM as a Cloud Service. Following the best practices can improve the maintainability and performance of your system. Although some of these deviations might not be a problem in other application contexts, including with previous versions of AEM, they may cause problems when used with AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM Development - Guidelines & Best Practices"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="AEM as a Cloud Service Development Guidelines"


`DG` identifies deviations of selected development guidelines for [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) and [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). Following the best practices can improve the maintainability and performance of your system. Although some of these deviations might not be a problem in other application contexts, including with previous versions of AEM, they may cause problems when used with AEM as a Cloud Service.

Subtypes are used to identify the different types of detected violations:

* `java.io.inputstream`: The use of `java.io.InputStream` in application code.
* `maintenance.task.configuration`: The configuration of a certain periodic maintenance activity.
* `sling.commons.scheduler`: The use of the Sling Commons Scheduler API for a scheduled task.
* `unsupported.asset.api`: The use of unsupported Asset Manager APIs in application code.

## Possible implications and risks {#implications-and-risks}

* `java.io.inputstream`
  * Streaming of binary data with `java.io.InputStream` can consume memory resources to the point of impacting performance. This is particularly an issue due to the limited memory available in containers used in AEM as a Cloud Service.

* `maintenance.task.configuration`
  * Some maintenance tasks that previously required explicit configuration are now automatically configured and managed within AEM as a Cloud Service.
  * Maintenance task configuration in AEM as a Cloud Service must be moved into source control.

* `sling.commons.scheduler`
  * Applications dependent on background tasks using [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) might not work as expected because execution cannot be guaranteed in AEM as a Cloud Service.
  * AEM as a Cloud Service development guidelines for [background tasks and long running jobs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggest that the code executed as a scheduled task must assume that the instance it is running on, can be brought down at any time. Therefore, the code must be resilient and resumable.

* `unsupported.asset.api`
  * Following APIs of AssetManager are marked as deprecated on AEM as a Cloud Service.
    * createAssetForBinary
    * getAssetForBinary
    * removeAssetForBinary
    * createAsset

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Implementation Guidance"
>abstract="Following AEM development guidelines & best practices, Customers should review their implementations on usage of Sling Commons Scheduler and restructure them to Sling Jobs, restructure their system maintenance tasks, review streaming of any binary data and refactor their code to be compliant with AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling Jobs"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html" text="Maintenance Tasks in AEM as a Cloud Service"

* `java.io.inputstream`
  * Use a direct-binary upload approach in which the binary is added to the datastore directly.
  * For assets use cases, please use [aem-upload](https://github.com/adobe/aem-upload). For other types of binaries, custom upload logic can be modeled after this same pattern.

* `maintenance.task.configuration`
  * Review AEM as a Cloud Service [Maintenance Task](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) documentation.
  * Ensure that [Maintenance Task Configuration](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) is in source control.

* `sling.commons.scheduler`
  * Replace the use of [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) with [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), which have an at-least-once execution guarantee.
  * Long running jobs should be avoided if possible.

* `unsupported.asset.api`
  * Please use [aem-upload](https://github.com/adobe/aem-upload) for the deprecated APIs of AssetManager.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
