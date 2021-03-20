---
title: URS
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# URS {#urs}

Unsupported Repository Structure

## Background {#background}

`URS` identifies cases of unsupported repository structure. Beginning in AEM 6.4, guidelines have been provided for the restructuring of repository content. By clearly delineating hierarchies for AEM product code and customer code and avoid conflict between them, content is being restructured out of `/etc` to other folders in the repository, adhering to the following high-level rules:

* AEM product code will always be placed in `/libs`, which must not be overwritten by custom code Custom code should be placed in `/apps`, `/content`, and `/conf`.
* It is highly recommended that these guidelines are followed for AEM as a Cloud Service.

Subtypes are used to identify the specific types of repository issues that should be addressed:
* `clientlibs.location`: A client library referencing `/etc` by path.
* `file.location`: A file under `/etc` that has been modified since installation.
* `node.location`: A node under `/etc` that has been modified since installation.
* `workflow.location`: A workflow model or launcher under `/etc/workflow`.
* `package.structure`: A package that contains both mutable and immutable content.

## Possible implications and risks {#implications-and-risks}

* Custom code relying on older paths may cause undesired behavior and impact product functionality.
* Packages containing both mutable and immutable content will likely cause problems during deployment.

## Possible solutions {#solutions}

* Refer to [Repository Restructuring](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) for guidance to prepare for AEM as a Cloud Service.
* Also refer to [AEM Project Structure](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) to learn more about mutable and immutable areas of the repository.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
