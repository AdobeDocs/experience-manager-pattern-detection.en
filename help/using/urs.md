---
title: URS
description: Pattern Detector code help page.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
---
# URS {#urs}

Unsupported Repository Structure

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Unsupported Repository Structure"
>abstract="URS identifies cases of URS (Unsupported Repository Structure) and node characteristics. This surfaces information to avoid conflict between AEM product code and customer code, content being restructured out of `/etc` to other folders in the repository and more."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Repository Restructuring"

## Background {#background}

`URS`  Identifies cases of URS (Unsupported Repository Structure) and node characteristics. Beginning in AEM 6.4, guidelines have been provided for the restructuring of repository content. By clearly delineating hierarchies for AEM product code, and customer code, and avoiding conflict between them all, content is being restructured out of `/etc` to other folders in the repository. Doing so adhere to the following high-level rules:

* AEM product code is always placed in `/libs` that custom code must not overwrite. 
* Custom code should be placed in `/apps`, `/content`, and `/conf`.
* It is highly recommended that these guidelines are followed for AEM as a Cloud Service.

Subtypes are used to identify the specific types of repository issues that should be addressed:

* `clientlibs.location`: A client library referencing `/etc` by path.
* `file.location`: A file under `/etc` that has been modified since installation.
* `node.location`: A node under `/etc` that has been modified since installation.
* `workflow.location`: A workflow model or launcher under `/etc/workflow`.
* `package.structure`: A package that contains both mutable and immutable content.
* `node.size`: A node with unsupported size.

## Possible implications and risks {#implications-and-risks}

* Custom code relying on older paths may cause undesired behavior and impact product functionality.
* Packages containing both mutable and immutable content can likely cause problems during deployment.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Implementation Guidance"
>abstract="Best practice is to review your code project. Make sure it adheres to the AEM project structure guidelines and avoid code relying on older or unsupported repository paths that may cause undesired behavior in AEM as a Cloud Service. Contact Adobe Support for help or clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="AEM Project Structure Guidelines"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* See [Repository Restructuring](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) for guidance to prepare for AEM as a Cloud Service.
* See also [AEM Project Structure](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) if you want to learn more about mutable and immutable areas of the repository.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
* Use the [Repository Modernizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) to restructure existing project packages by separating content and code into discrete packages to be compatible with the project structure defined for Adobe Experience Manager as a Cloud Service.
