---
title: DOPI
description: Pattern Detector code help page.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
---
# DOPI {#dopi}

Deprecated Ordered Property Index

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Deprecated Ordered Property Index"
>abstract="DOPI code identifies the use of ordered property index definitions (`primaryType=oak:QueryIndexDefinition` AND type="ordered"), which have been deprecated since 6.1 and were removed in 6.2."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Ordered Index - Deprecated"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexing - AEM as a Cloud Service"

DOPI identifies the use of ordered property index definitions (`primaryType=oak:QueryIndexDefinition` AND `type="ordered"`), which have been deprecated since 6.1 and were removed in 6.2.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review all deprecated ordered indexes and move them to supported form of Lucene indexes to avoid significant performance issues or non-functional customer requirements."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Best Practices - Queries and Indexing"

* Some queries may not respond.
* Customer functionality might work incorrectly.
* Traversal warnings or even errors and significant performance penalties as the deprecated indexes have no effect.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Tools & Resources"
>abstract="Review WKND-legacy project to understand how DOPI violations can be made compatible with AEM Cloud Service. Also, Review DOPI Violation Example on GitHub to understand how legacy ordered indexes can be converted to Lucene based indexes which are supported in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-Legacy Project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="DOPI Violation Example - GitHub"

* Modify the index definition so that it becomes&mdash;or replaces the index with&mdash;a supported index definition. (See [Oak Queries and Indexing](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) project and understand how [DOPI violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) can be corrected and made compatible with AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
