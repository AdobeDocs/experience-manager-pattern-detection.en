---
title: OCU
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# OCU {#ocu}

Outdated Code Usage

## Background {#background}

`OCU` identifies the situation in which some JCR nodes, such as Sling or AEM components or API OSGi exports, are changed or removed in a non-compatible way. The customer may be not aware of this change before an upgrade. They might be upgraded to a non-compatible version or can be not available at all.

As the old versions are not installed by default, the customer application might not work correctly.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses deprecated components or APIs can be broken and might not resolve correctly after an upgrade.
* Some features of the customer application or some AEM functionality may not work properly or might not be active after an upgrade.

## Possible solutions {#solutions}

* Short-term: Installation of compatibility package might help.
* Long-term: Adapt customer code to use the newest version of AEM components or APIs.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
