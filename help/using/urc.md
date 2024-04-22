---
title: URC
description: Pattern Detector code help page.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
---
# URC {#urc}

Unsupported Run mode Configuration

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Unsupported Runmode Configuration"
>abstract="URC identifies the use of configurations that are based on a run mode name that is not supported in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Supported Runmodes"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Runmodes"

URC identifies the use of configurations that are based on a run mode name that is not supported in AEM as a Cloud Service.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review if all run modes used in your application are supported and ensure they follow the runmode resolution guidelines"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Runmode Resolution Guidelines"

* The set of names that may be used for running various modes in AEM as a Cloud Service is limited.
* Configurations that are based on unsupported run mode names, have no effect when deployed to AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Tools & Resources"
>abstract="Review WKND-legacy project to understand how URC violations can be made compatible with AEM Cloud Service. Also, Review URC Violation Example on GitHub to understand how custom runmode-based OSGi configurations can be updated to adhere with AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-Legacy Project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="URC Violation Example - GitHub"

* Review the use of this configuration so you can determine if it is necessary.
* Rename the configuration using one of the supported [run mode names](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) and follow [run mode resolution guidelines](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) project and understand how [URC violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) can be corrected and made compatible with AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
