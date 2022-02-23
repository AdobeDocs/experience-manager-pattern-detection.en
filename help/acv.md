---
title: ACV
description: Pattern Detector code help page
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

`ACV`  Assets' Content Validator identifies the missing mandatory nodes in asset content. This could lead to failure of certain Assets features on Experience Manager as a Cloud Service.

Subtypes are used to identify the different types of information, such as:

* `missing.jcrcontent`: Identify the folders with missing mandatory nodes in the repository. Identifying any missing content in the repository helps prevent any broken features or use cases.
* `missing.original.rendition`: Identify the assets with a missing mandatory original rendition in the repository.

## Possible implications and risks {#implications-and-risks}

* This could lead to failure of certain Assets features that depend on inherited properties in Experience Manager as a Cloud Service.
* AEM Assets depends on the existence of the original rendition. The asset processing in Cloud Service will go in a loop if the original rendition is missing.
 
## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementation Guidance"
>abstract="Adobe recommends to review content structure to prevent broken workflows that depend on inherited properties. Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Analyze a folder if it has a missing child node. Create the nodes manually if the number of folders is manageable, otherwise use a script.
* For the assets missing the original rendition, either reupload the assets or delete them before migrating.
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
