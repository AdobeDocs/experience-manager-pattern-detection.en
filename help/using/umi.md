---
title: UMI
description: Pattern Detector code help page
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
---
# UMI {#umi}

Upgrade Misconfiguration Issue

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Upgrade Misconfiguration Issue"
>abstract="UMI identifies modifications to certain OSGi configurations that will cause issues when upgrading, including a failed upgrade or reduced functionality."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Release Notes"

`UMI` identifies modifications to certain OSGi configurations that will cause issues when upgrading, including a failed upgrade or reduced functionality.

The following configurations are checked for modification:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` :  Identify whether the `org.apache.sling.commons.log.file` property of the custom loggers is pointing to something other than `logs/error.log` file.

## Possible implications and risks {#implications-and-risks}

* Changing or removing configurations may cause below issues:
  * Upgrade may get stuck (for example `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` was missing but present in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
  * Authorization issues may come after upgrade (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
  * Certain functionality may not work as expected. For example changing `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` may result in some JSP files not being compiled, which ultimately will result in loss of functionality.
  * The values of the externalizer config `com.day.cq.commons.impl.ExternalizerImpl` are set by cloud manager environment variables in AEM as a Cloud Service.
  * AEM as a Cloud Services does not support custom log files. Logs written to custom-named logs will not be accessible from AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review your current configurations and revert any changes made to mentioned configurations to avoid any future upgrade issues. Reach out to Adobe Support for help & clarifications"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Do not change or remove the four configurations mentioned above.
  * In case of the following violation :  
  "Required properties for the OSGi configuration 'xyz-configuration' are missing: '[property-1,property-2...]'."  
  Please confirm if these deletions are legit or not since these OSGI configurations are OOTB and might have never been modified/saved from the OSGi Config Manager.
* If configurations have been changed, they should be restored to their expected values. These values are indicated in the `UMI` messages.
* For `com.day.cq.commons.impl.ExternalizerImpl`, please refer [documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=en) for setting externalizer config using cloud manager environment variables in AEM as a Cloud Service.
* For `org.apache.sling.commons.log.LogManager.factory.config`, Change the OSGI configuration to send the customized logger to the `logs/error.log` file. Please refer [documentation](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs.html) for repointing to the `logs/error.log` file. 
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
