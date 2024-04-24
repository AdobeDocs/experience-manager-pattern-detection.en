---
title: PCX
description: Pattern Detector code help page.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
---
# PCX {#pcx}

Page Complexity

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Page Complexity"
>abstract="PCX identifies pages that contain a large number of nodes in their structure."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Release Notes"

`PCX`  Identifies pages that contain many nodes in their structure.

Subtypes are used to identify the different types of information:

* `page.complexity.medium`: A page contains a moderately high number of nodes that may affect rendering performance.
* `page.complexity.high`: A page contains a high number of nodes that likely affect rendering performance.

## Possible implications and risks {#implications-and-risks}

* Many nodes within a page may affect its rendering performance.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review content structure to reduce page complexity which in turn would help improve page rendering performance. Contact Adobe Support for help or clarifications."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Reduce the total number of nodes within a page by doing the following action:
  * Verify that there are no unnecessary containers.
  * Test whether the same layout can be achieved with fewer containers.
  * Simplify the page content.
  * Reduce the depth of the node structure.
  * Refactor any included Experience Fragments for simplicity.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
