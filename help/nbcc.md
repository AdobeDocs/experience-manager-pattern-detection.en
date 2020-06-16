---
title: NBCC
description: Pattern Detector code help page
---

# NBCC {#nbcc}

Non-Backwards Compatible Changes

## Background {#background}

`NBCC` identifies to the situation in which some JCR nodes or bundles are changed in a non-compatible way. The customer may be not aware of this change before an upgrade.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses non-backward compatible changes can be broken and might not resolve correctly.
* Some features of the customer application or some AEM functionality may not work properly after an upgrade.

## Possible solutions {#solutions}

* Overlay or reference only backward compatible Sling components.
* Consider adapting resources which come from `/libs` or bundles after an AEM upgrade.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
