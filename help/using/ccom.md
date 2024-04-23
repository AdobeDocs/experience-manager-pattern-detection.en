---
title: CCOM
description: Pattern Detector code help page.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
---
# CCOM {#ccom}

Custom Component

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Custom Component"
>abstract="CCOM identifies custom components which have been installed on AEM. This information is provided for the purposes of best practices assessment"

CCOM identifies custom components which have been installed on AEM. This information is provided for the purposes of best practices assessment.

A subtype is used with this code to identify the category of component:

* `custom.core`: A supertype in the component's chain of supertypes contains "core/wcm/components/", indicating that it inherits from a core component.
* `custom.foundation`: A supertype in the component's chain of supertypes contains "core/wcm/components/", indicating that it inherits from a core component.
* `custom.overlay.foundation`: The component path contains "wcm/foundation/components/" or "foundation/components/", indicating that it overlays a foundation component.
* `custom`: The custom component does not inherit or overlay a core or foundation component.

## Possible implications and risks {#implications-and-risks}

* Best Practice is to minimize the number of custom components, use core components, and use core components with the Style System so you can reduce technical debt.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to minimize the number of custom components, use core components, and use core components with the Style System to reduce technical debt."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction" text="Core Components"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Style System"

* Find more information about Core Components at [Core Components Introduction](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction).
* Find more information about the Style System at [Using the Style System](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
