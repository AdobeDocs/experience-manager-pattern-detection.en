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
>abstract="ACV identifies the missing mandatory nodes in assets content."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Notable Changes - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Experience Manager as a Cloud Service - Release Notes"

`ACV`  Assets' Content Validator identifies the missing mandatory nodes in asset content. This could lead to failure of certain Assets features on Experience Manager as a Cloud Service.

Subtypes are used to identify the different types of information, such as:

* `assets.sanity.missing.jcrcontent`: Identify the folders with missing mandatory nodes in the repository. Identifying any missing content in the repository helps prevent any broken features or use cases.

## Possible implications and risks {#implications-and-risks}

This could lead to failure of certain Assets features that depend on inherited properties in Experience Manager as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Implementation Guidance"
>abstract="Adobe recommends to review content structure to prevent broken workflows that depend on inherited properties. Contact Customer Care for help".
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Analyze a folder if it has a missing child node. Create the nodes manually if the number of folders is manageable, otherwise use a script.
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
