---
title: ASO
description: Pattern Detector code help page
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
---
# ASO {#aso}

AEM System Overview

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview"
>abstract="ASO code identifies general information about the AEM instance. Each finding provides one value of a particular type of system information that can help in your migration planning and refactoring effort."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Release Notes"

`ASO` identifies general information about the AEM instance. Each finding provides one value of a particular type of system information.

Subtypes are used to identify different types of information:

* `aem.version`: The AEM version.
* `aem.product`: Detection of the use of an AEM product (Commerce, Forms, etc.).
* `node.count`: The approximate node count of a certain type (Page, Asset, etc.).
* `node.store`: The node store implementation type (SegmentNodeStore, DocumentNodeStore).
* `data.store`: The data store implementation type (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: A maintenance task.
* `slow.query`: A slow query.

## Possible implications and risks {#implications-and-risks}

* The AEM version, node counts, and node store and data store implementation types are provided for informational purposes.
* The custom application may rely on products or features not available in AEM as a Cloud Service.
* Upgrading with unsupported features may result in a failed upgrade and a non-functional application.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementation Guidance"
>abstract="Information exposed via ASO code provides general information for your AEM environment including version, product add-ons, system level information and this should be reviewed for any unsupported products or features in AEM as a Cloud Service. Reach out to Adobe Support for help & clarifications."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* AEM upgrades with unsupported products or features are not recommended and may not supported.
* Review the [release notes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html) to learn about the latest changes in AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
