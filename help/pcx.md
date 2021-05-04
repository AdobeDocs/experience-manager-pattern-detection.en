---
title: PCX
description: Pattern Detector code help page
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
---
# PCX {#pcx}

Page Complexity

## Background {#background}

[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Page Complexity"
>abstract="PCX identifies pages that contain a large number of nodes in their structure."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Release Notes"

`PCX` identifies pages that contain a large number of nodes in their structure.

Subtypes are used to identify the different types of information:

* `page.complexity.medium`: A page contains a moderately high number of nodes that may affect rendering performance.
* `page.complexity.high`: A page contains a very high number of nodes that will likely affect rendering performance.

## Possible implications and risks {#implications-and-risks}

* A large number of nodes within a page may affect its rendering performance.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review content structure to reduce page complexity which inturn would help improve page rendering performnance. Reach out to Adobe Support for help & clarifications""
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Take steps to reduce the total number of nodes within a page, including:
  * Verify that there are no unnecessary containers.
  * Test whether the same layout can be achieved with fewer containers.
  * Simplify the page content.
  * Reduce the depth of the node structure.
  * Refactor any included Experience Fragments for simplicity.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
