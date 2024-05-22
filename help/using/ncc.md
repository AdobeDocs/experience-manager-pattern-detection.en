---
title: NCC
description: Pattern Detector code help page.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
---
# NCC {#ncc}

Non-Compatible Changes

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Non-Compatible Changes"
>abstract="NCC identifies the situation in which some JCR nodes or bundles are changed in a non-compatible way. The customer may not be aware of this change before an upgrade."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Release Notes - AEM as a Cloud Service"

`NCC`  Identifies the situation in which some JCR nodes or bundles are changed in a non-compatible way. The customer may not be aware of this change before an upgrade.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses non-compatible changes can be broken and might not resolve correctly.
* Some features of the customer application or some AEM functionality may not work properly after an upgrade.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review custom code and ensure that only compatible Sling components are overlaid or referenced. Contact Adobe Support for help or clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Overlays"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Overlay or reference only compatible Sling components.
* Consider adapting resources that come from `/libs` or bundles after an AEM upgrade.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
