---
title: ASO
description: Pattern Detector code help page.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
---
# ASO {#aso}

AEM System Overview

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview"
>abstract="ASO code identifies general information about the AEM instance. Each finding provides one value of a particular type of system information that can help in your migration planning and refactoring effort."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Release Notes"

`ASO` Identifies general information about the AEM instance. Each finding provides one value of a particular type of system information.

Subtypes are used to identify different types of information:

* `aem.version`: The AEM version.
* `aem.product`: Detection of the use of an AEM product (Commerce, Forms, and so on).
* `node.count`: The approximate node count of a certain type (Page, Asset, and so on) and the grand total of nodes. 
* `node.store`: The node store implementation type (SegmentNodeStore, DocumentNodeStore) and its size.
* `data.store`: The data store implementation type (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: A maintenance task.
* `slow.query`: A slow query.
* `group.membership`: The number of users and subgroups (direct / declared members only) in a group. 
* `cqtag.count`: The number of CQ tagged assets.
* `smarttag.count`: The number of Smart tagged assets.
* `ccom.version`: The version of Core Component package.
* `instance.type`: The AEM instance type (author|publish).
* `unprocessed.asset.count`: The number of unprocessed assets.
* `vanity.url.count`: The number of vanity URLs.
* `index.size`: Total Migratable Lucene index size.
* `workflow.count`: The number of author workflows in running and stale state.
* `jvm.arguments`: The JVM arguments added to command line when starting AEM.

## Possible implications and risks {#implications-and-risks}

* The AEM version, node counts, group membership, node store, data store implementation types, CQ Tag Count, Smart Tag Count, Core Component version, AEM instance type, and Unprocessed asset count are provided for informational purposes.
* The higher number of vanity URLs (>1000) may put a load on the Dispatcher and the Publish servers with expensive queries.
* The custom application may rely on products or features not available in AEM as a Cloud Service.
* Upgrading with unsupported features may result in a failed upgrade and a non-functional application.
* A high number of author workflows in a running or stale state could degrade performance.
* Slow queries may degrade the performance of the system.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Implementation Guidance"
>abstract="Information exposed by way of ASO code provides general information for your AEM environment including version, product add-ons, and system level information. Review it for any unsupported products or features in AEM as a Cloud Service. Contact Adobe Support for help or clarifications."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* AEM upgrades with unsupported products or features are not recommended and may not be supported.
* The unprocessed assets must be processed and the `dam:assetState` property on the `jcr:content` node of the Asset must be set to "processed." Or, you should remove these assets from the migration set before migrating to AEMaaCS.
* Vanity URLs could be replaced with Apache Rewrites. 
* See [documentation](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) for troubleshooting slow queries.
* See the [release notes](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) if you want to learn more about the latest changes in AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
