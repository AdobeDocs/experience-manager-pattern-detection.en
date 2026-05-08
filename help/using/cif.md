---
title: CIF
description: Pattern Detector code help page.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
---
# CIF {#cif}

Commerce Integration Framework Classic

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifies the classic version of Commerce Integration Framework usage that is incompatible with AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF`  Identifies the classic version of Commerce Integration Framework usage that is incompatible with AEM as a Cloud Service. The message for each `CIF` finding identifies the usage and provide additional information.

Subtypes are used to identify the different types of information:

* `commerce.integration.framework.detected`: A classic version of Commerce Integration Framework incompatibility with AEM as a Cloud Service.


## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review all the classic version of Commerce Integration Framework usage."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Notable Changes to CIF"

* The classic version of Commerce Integration Framework is no longer supported on AEM as a Cloud Service. It would block the upgrade to AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Tools and Resources"
>abstract="This guide helps identify the areas you must update for the Experience Manager Cloud Service migration."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Migration guide for CIF"

* For Experience Manager as a Cloud Service, the CIF add-on is the only supported commerce integration solution for Adobe Commerce and third-party commerce solutions. The CIF add-on is deployed automatically for customers on Experience Manager as a Cloud Service, no manual deployment is needed. See [Getting started with AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* To support projects deploying CIF, Adobe provides [AEM CIF Core Components](https://github.com/adobe/aem-core-cif-components).
* CIF add-on is available for AEM 6.5 as well by way of the [Software Distribution portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). It is compatible and provides the same features as the CIF add-on for Experience Manager as a Cloud Service - no adjustments are required.
* Classic CIF with its dependencies is not available anymore. Code relying on this CIF version using com.adobe.cq.commerce.api Java&trade; APIs must be adjusted to the CIF add-on and its principles.

Also, find the possible solutions for the different subtypes below:

* `commerce.bundles.detected` - These bundles will be uninstalled during upgrade
* `commerce.packages.detected` - These packages  will be deleted during upgrade
* `commerce.packages.dependency` - Remove any dependency on Commerce from custom packages
* `commerce.nodes.detected` - Update custom code to not create CQ Commerce nodes
* `commerce.configs.detected` - Do not use CQ Commerce config properties in custom code
* `commerce.users.detected` - Do not use CQ Commerce service users in custom code
* `commerce.overlays.detected` - Remove CQ Commerce overlays usage
* `commerce.paths.detected` - Remove commerce paths after making sure that these paths are not being used on AEM
* `commerce.resource.type.detected` - Remove commerce resource type usage
* `commerce.usage` - Remove CQ Commerce APIs in your custom code.
