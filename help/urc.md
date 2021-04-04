---
title: URC
description: Pattern Detector code help page
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
---
# URC {#urc}

Unsupported Runmode Configuration

## Background {#background}

`URC` identifies identifies the use of configurations that are based on a runmode name that is not supported in AEM as a Cloud Service.

## Possible implications and risks {#implications-and-risks}

* The set of names that may be used for runmodes in AEM as a Cloud Service is limited.
* Configurations that are based on unsupported runmode names will not have any effect when deployed to AEM as a Cloud Service.

## Possible solutions {#solutions}

* Review the use of this configuration to determine if it is necessary.
* Rename the configuration to use one of the supported [runmode names](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) and follow [runmode resolution guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) project and understand how [URC violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) can be corrected and made compatible with AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
