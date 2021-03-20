---
title: ASO
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# ASO {#aso}

AEM System Overview

## Background {#background}

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

* AEM upgrades with unsupported products or features are not recommended and may not supported.
* Review the [release notes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html) to learn about the latest changes in AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
