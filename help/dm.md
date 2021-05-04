---
title: DM
description: Pattern Detector code help page
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
---
# DM {#dm}

Dynamic Media

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM code identifies usage of AEM Assets Dynamic Media in your current implementation. The Dynamic Media mode is detected by the run mode."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM Development - Guidelines & Best Practices"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="AEM as a Cloud Service Development Guidelines"

`DM` identifies use of AEM Assets Dynamic Media. The Dynamic Media mode is detected by the run mode.

A subtype is used with this code:

* `dynamic.media.runmode`: The associated value of this subtype, if it is provided, is either:
  * `dynamicmedia`: Dynamic Media - Hybrid mode
  * `dynamicmedia_scene7`: Dynamic Media - Scene 7 mode

## Possible implications and risks {#implications-and-risks}

* `dynamic.media.runmode`
  * There may be upgrade issues related to Dynamic Media.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementation Guidance"
>abstract="AEM as a Cloud Service only support dynamicmedia_scene7 runmode. Please review the current settings and reach out to Adobe Support Team for help & clarifications."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Setting up Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"


* `dynamic.media.runmode`
  * Find more information at [Setting Up Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html).

* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
