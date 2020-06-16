---
title: ECU
description: Pattern Detector code help page
---

# ECU {#ecu}

DEPRECATED: Extraneous Content Usage (replaced by CAV, Content Area Violation)

## Background {#background}

`ECU` identifies the pattern where different content areas are used in a way that violates the rules of the content classification.

Sling request processing defines how the content of a resource, its `sling:resourceType` property in particular, is used to determine the script that will be used to rendering the content. (See [Locating the script](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) for more information.) Sling also provides techniques to access and merge resources through "Overlays" and "Overrides". These are described as part of the [Sling Resource Merger](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/sling-resource-merger.html) and in [Overlays](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/overlays.html).

In order to make it safer and easier for customers to understand what areas of `/libs` are safe to use and overlay the content in `/libs` has been classified with "mixin" properties: Public, Abstract, Final, and Internal. Each classification implies rules about how the content may be user, inherited, or overlaid. See [Sustainable Upgrades](https://docs.adobe.com/help/en/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) for a detailed description.

## Possible implications and risks {#implications-and-risks}

* An AEM upgrade may lead to page rendering problems and other undesired behavior.
* Security updates are not effective.
  
## Possible solutions {#solutions}

* Minimize the use of content overlay to those cases in which it is needed.
* In particular, avoid overlaying restricted content (Final and Internal classification).
* Consider adapting changes coming from `/libs` after AEM upgrades, ServicePack or CumulativeFixPack installations.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
