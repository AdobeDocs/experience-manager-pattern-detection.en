---
title: NCC
description: Pattern Detector code help page
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
---
# NCC {#ncc}

Non-Compatible Changes

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Non-Compatible Changes"
>abstract="NCC identifies to the situation in which some JCR nodes or bundles are changed in a non-compatible way. The customer may be not aware of this change before an upgrade."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Release Notes - AEM as a Cloud Service"

`NCC` identifies to the situation in which some JCR nodes or bundles are changed in a non-compatible way. The customer may be not aware of this change before an upgrade.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses non-compatible changes can be broken and might not resolve correctly.
* Some features of the customer application or some AEM functionality may not work properly after an upgrade.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Implementation Guidance"
>abstract="Best practice is review custom code and ensure only compatible Sling components are overlaid or referenced. Reach out to Adobe Support for help & clarifications"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Overlays"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Overlay or reference only compatible Sling components.
* Consider adapting resources which come from `/libs` or bundles after an AEM upgrade.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
