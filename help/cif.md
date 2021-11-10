---
title: CIF
description: Pattern Detector code help page
---
# CIF {#cif}

Commerce Integration Framework Classic

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifies the classic version of Commerce Integration Framework usage that are incompatible with AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Content and Commerce"

`CIF` CIF identifies the classic version of Commerce Integration Framework usage that are incompatible with AEM as a Cloud Service. The message for each `CIF` finding will identify the usage and provide additional information.

Subtypes are used to identify the different types of information:

* `commerce.integration.framework.detected`: A classic version of Commerce Integration Framework incompatibility with AEM as a Cloud Service.


## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review all the classic version of Commerce Integration Framework usage."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Notable Changes to CIF"

* The classic version of Commerce Integration Framework is no longer supported on AEM as a Cloud Service. It would block the upgrade to AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Tools & Resources"
>abstract="This guide helps identify the areas you need to update for the Experience Manager Cloud Service migration."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Migration guide for CIF"

* For Experience Manager as a Cloud Service the CIF add-on is the only supported commerce integration solution for Adobe Commerce and 3rd party commerce solutions. The CIF add-on is deployed automatically for customers on Experience Manager as a Cloud Service, no manual deployment is needed. See [Getting started with AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* To support projects deploying CIF Adobe provides [AEM CIF Core Components](https://github.com/adobe/aem-core-cif-components).
* CIF add-on is available for AEM 6.5 as well via the [Software Distribution portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). It is compatible and provides the same features as the CIF add-on for Experience Manager as a Cloud Service - no adjustments are required.
* Classic CIF with its dependencies is not available anymore. Code relying on this CIF version using com.adobe.cq.commerce.api Java APIs must be adjusted to the CIF add-on and its principles.
