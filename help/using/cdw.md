---
title: CDW
description: Pattern Detector code help page
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
---
# CDW {#cdw}

Custom Dialog Widget

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Custom Dialog Widget"
>abstract="CDW identifies the Custom Dialog Widgets which should be updated for them to be compatible with AEM as a Cloud Service."

`CDW`  Custom Dialog Widgets identifies the custom CoralUI and Classic dialog widgets. These should be updated for them to be compatible with AEM as a Cloud Service.

Subtypes are used to identify the different types of information, such as:

* `custom.coral.widget`: Identify the custom dialog widgets based on CoralUI 2 or CoralUI 3.
* `custom.classic.widget`: Identify the custom dialog widgets based on ExtJs.

## Possible implications and risks {#implications-and-risks}

* The Classic UI is no longer available in AEM as a Cloud Service. The standard interface for authoring is the Touch-enabled UI.
 
## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Implementation Guidance"
>abstract="Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Custom Classic Dialog Widgets should to be converted from ExtJS to [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Custom Coral Dialog Widgets should be evaluated for update to CoralUI 3.
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
