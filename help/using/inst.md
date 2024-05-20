---
title: INST
description: Pattern Detector code help page.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
---
# INST {#inst}

Installed Artifact

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Installed Artifact"
>abstract="INST identifies custom and third-party packages and bundles installed in AEM by the customer. Such packages and bundles are reported to help characterize the state of the system and the general scope of an upgrade effort. Any third-party package must adhere to the AEM as a Cloud Service development and packaging guidelines."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Development Guidelines - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Packaging Guidelines - AEM as a Cloud Service"

`INST`  Identifies custom and third-party packages and bundles installed in AEM by the customer. Such packages and bundles are reported to help characterize the state of the system and the general scope of an upgrade effort.

When multiple versions of a package have been installed, only the latest version is reported.

Packages and bundles that are detected have not necessarily been optimized for AEM as a Cloud Service. Any third-party package should be verified with its creator or Adobe for compatibility with AEM as a Cloud Service.

Subtypes are used to identify different types of information:

* `custom.bundle`: A bundle that has been installed in AEM.
* `custom.package`: A package that has been installed in AEM.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Implementation Guidance"
>abstract="Customers can no longer install third-party packages using CRX Package Manager. Customers should review these installed artifacts that must be structured, and optimize them to work with AEM as a Cloud Service. Verify any third-party package with either its creator or with Adobe for compatibility with AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Embedding Subpackages in the Container Package"


* Installation of third-party packages using CRX Package Manager is not possible in AEM as a Cloud Service.
* Applications dependent on third-party packages might not work as expected until deployed correctly to work with AEM as a Cloud Service.
* Third-party vendor packages, if not optimized for AEM as a Cloud service, may result in undesired behavior.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Tools and Resources"
>abstract="Review WKND-legacy project to understand how INST violations can be made compatible with AEM Cloud Service. Also, review the INST Violation Example on GitHub to understand how this issue can be corrected and deployed in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-Legacy Project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="INST Violation Example - GitHub"

* Third-party packages should be deployed to AEM as a part of the project using the Cloud Manager [deployment process](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process).
* Review how to [embed third-party packages](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) in your project for AEM as a Cloud Service.
* Third-party packages must adhere to the AEM as a Cloud Service [development](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) and [packaging](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) guidelines.
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) project and understand how [INST violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) can be corrected and made compatible with AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
