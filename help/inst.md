---
title: INST
description: Pattern Detector code help page
---

# INST {#inst}

Installed Artifact

## Background {#background}

`INST` identifies custom and third-party packages and bundles that have been installed in AEM by the customer. These are reported to help characterize the state of the system the general scope of an upgrade effort.

When multiple versions of a package have been installed, only the latest version is reported.

Packages and bundles that are detected have not necessarily been optimized for AEM as a Cloud Service. Any third-party package should be verified with its creator or Adobe for compatibility with AEM as a Cloud Service.

Subtypes are used to identify different types of information:

* `custom.bundle`: A bundle that has been installed in AEM.
* `custom.package`: A package that has been installed in AEM.

## Possible implications and risks {#implications-and-risks}

* Installation of third-party packages using CRX Package Manager is not possible in AEM as a Cloud Service.
* Applications dependent on third-party packages might not work as expected until deployed correctly to work with AEM as a Cloud Service.
* Third-party vendor packages, if not optimized for AEM as a Cloud service, may result in undesired behavior.

## Possible solutions {#solutions}

* Third-party packages should be deployed to AEM as a part of the project using the Cloud Manager [deployment process](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Review how to [embed third-party packages](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) in your project for AEM as a Cloud Service.
* Third-party packages must adhere to the AEM as a Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) and [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html) guidelines.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
