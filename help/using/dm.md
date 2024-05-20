---
title: DM
description: Learn about how Pattern Detector code identifies usage of AEM Assets - Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
---
# DM {#dm}

Dynamic Media

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM code identifies usage of AEM Assets Dynamic Media in your current implementation. The run mode detects the Dynamic Media mode."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM Development - Guidelines and Best Practices"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service Development Guidelines"

`DM` (Dynamic Media) Identifies use of AEM Assets Dynamic Media. The run mode detects the Dynamic Media mode.

A subtype is used with this code:

* `dynamic.media.runmode`: The associated value of this subtype, if it is provided, is either:
  * `dynamicmedia`: Dynamic Media - Hybrid mode
  * `dynamicmedia_scene7`: Dynamic Media - Scene7 mode

## Possible implications and risks {#implications-and-risks}

* `dynamic.media.runmode`
  * There may be upgrade issues related to Dynamic Media.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Implementation Guidance"
>abstract="AEM as a Cloud Service only support dynamicmedia_scene7 run mode. Review the current settings and reach out to the Adobe Support Team for help and clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Setting up Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"


* `dynamic.media.runmode`
  * Find more information at [Setup Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) if you need clarifications or concerns addressed.
