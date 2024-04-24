---
title: ECU
description: Pattern Detector code help page.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
---
# ECU {#ecu}

DEPRECATED: Extraneous Content Usage (replaced by CAV, Content Area Violation)

## Background {#background}

`ECU`  Identifies the pattern where different content areas are used in a way that violates the rules of the content classification.

Sling request processing defines how the content of a resource, its `sling:resourceType` property in particular, is used to determine the script that is used to render the content. (See [Locating the script](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) for more information.) Sling also provides techniques to access and merge resources through "Overlays" and "Overrides". These are described as part of the [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) and in [Overlays](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

To make it safer and easier for customers to understand what areas of `/libs` are safe to use and overlay the content in `/libs` has been classified with "mixin" properties: Public, Abstract, Final, and Internal. Each classification implies rules about how the content may be user, inherited, or overlaid. See [Sustainable Upgrades](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) for a detailed description.

## Possible implications and risks {#implications-and-risks}

* An AEM upgrade may lead to page rendering problems and other undesired behavior.
* Security updates are not effective.
  
## Possible solutions {#solutions}

* Minimize the use of content overlay to those cases in which it is needed.
* In particular, avoid overlaying restricted content (Final and Internal classification).
* Consider adapting changes coming from `/libs` after AEM upgrades, Service Pack, or Cumulative Fix Pack installations.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
