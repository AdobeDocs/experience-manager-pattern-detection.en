---
title: ACV
description: Pattern Detector code help page.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
---
# ACV {#acv}

Assets Content Validator

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifies the missing mandatory nodes in assets content."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Notable Changes - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Experience Manager as a Cloud Service - Release Notes"

`ACV`  Assets' Content Validator identifies the missing mandatory nodes & violations in asset content. This could lead to failure of certain Assets features on Experience Manager as a Cloud Service.

Subtypes are used to identify the different types of information, such as:

* `missing.jcrcontent`: Identify the folders with missing mandatory nodes in the repository. Identifying any missing content in the repository helps prevent any broken features or use cases.
* `missing.original.rendition`: Identify the assets with a missing mandatory original rendition in the repository. Kindly note previewing PDF's pages does not require subassets generation in AEMaaCS. Hence for PDF assets, reporting subassets missing original rendition is suppressed.
* `metadata.descendants.violation`: Identify the assets with more than 100 descendants under metadata node of the asset in the repository.
* `conflict.node`: Identify the presence of conflict nodes in the repository under /content/dam/ path.
* `psb.file.large`: Identify Large PSB Files (dc:format : application/vnd.3gpp.pic-bw-small) having size greater than 2 gigabytes.
* `invalid.asset.name`: Identify assets with invalid characters[* / : [ \ ] | # % { } ? &] in the name.

## Possible implications and risks {#implications-and-risks}

* This could lead to failure of certain Assets features that depend on inherited properties in Experience Manager as a Cloud Service.
* AEM Assets depends on the existence of the original rendition. The asset processing in Cloud Service will go in a loop if the original rendition is missing. Subassets generation is not supported in AEMaaCS.
* High number of descendants under metadata node may slow down loading of folders consisting of assets that violate this.
* Presence of conflict nodes could lead to ingestion failure on AEM as a Cloud Service.
* Experience Manager may not process very high-resolution PSB files. Customers using ImageMagick for processing large files might face an impact on the performance if proper benchmarking of the Experience Manager server is not done.
* Invalid characters in the asset name might lead to failures while migrating to AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementation Guidance"
>abstract="Adobe recommends to review content structure to prevent broken workflows that depend on inherited properties. Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Analyze a folder if it has a missing child node. Create the nodes manually if the number of folders is manageable, otherwise use a script.
* For the assets missing the original rendition, either reupload the assets or delete them before migrating. 
* No action required for missing subassets original rendition.
* In case of conflict nodes, either they should be resolved or they might need to be deleted before migrating to AEM as a Cloud Service.
* Reach out to Adobe Customer Support if you plan to process lots of large PSD or PSB files. Experience Manager may not process very high-resolution PSB files that are more than 30000 x 23000 pixels. See [documentation](https://experienceleague.adobe.com/docs/experience-manager-65/assets/extending/best-practices-for-imagemagick.html).
* Contact the [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to address concerns.
