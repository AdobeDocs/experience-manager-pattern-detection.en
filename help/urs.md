---
title: URS
description: Pattern Detector code help page
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
---
# URS {#urs}

Unsupported Repository Structure

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Unsupported Repository Structure"
>abstract="URS identifies cases of unsupported repository structure. This surfaces information to avoid conflict between AEM product code and customer code, content being restructured out of /etc to other folders in the repository and more."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Repository Restructuring"

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
* `node.name.length`: A node name with unsupported length.

## Possible implications and risks {#implications-and-risks}

* Custom code relying on older paths may cause undesired behavior and impact product functionality.
* Packages containing both mutable and immutable content will likely cause problems during deployment.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review your code project and make sure it adheres to the AEM project structure guidelines and avoid code relying on older/unsupported repository paths that may cause undesired behavior in AEM as a Cloud Service. Reach out to Adobe Support for help & clarifications"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="AEM Project Structure Guidelines"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Refer to [Repository Restructuring](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) for guidance to prepare for AEM as a Cloud Service.
* Also refer to [AEM Project Structure](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) to learn more about mutable and immutable areas of the repository.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
* Leverage the [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) to restructure existing project packages by separating content and code into discrete packages to be compatible with the project structure defined for Adobe Experience Manager as a Cloud Service.
