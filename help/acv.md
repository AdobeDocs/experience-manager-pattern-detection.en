---
title: ACV
description: Pattern Detector code help page
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
---
# ACV {#acv}

Assets Content Validator

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifies missing mandatory nodes in assets content."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Release Notes"

`ACV`  Assets Content Validator identifies missing mandatory nodes in asset content. This could lead to failure of certain Assets features on AEM as a Cloud Service.

Subtypes are used to identify the different types of information:

* `assets.sanity.missing.jcrcontent`: Identify folders with missing mandatory jcr:content child node. This could lead to failure of certain Asset's features on AEM as a Cloud Service

## Possible implications and risks {#implications-and-risks}

*  This could lead to failure of certain Assets features that depends on property inheritance in AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review content structure to help reduce in failures of Assets contents features that depends on property inheritance . Reach out to Adobe Support for help & clarifications"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* If folders having missing child node, please analyze that. If the number of folders is manageable child nodes can be created manually or use a script for large number of folders.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
