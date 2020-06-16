---
title: IOI
description: Pattern Detector code help page
---

# IOI {#ioi}

Internal Oak Import

## Background {#background}

`IOI` identifies customer use of internal Oak packages, importing them via OSGi. They are usually exported without any particular version and are intended for consumption only by other Oak bundles or low-level AEM services.

Some of these are used by `com.adobe.granite.repository`, which sets up a repository for AEM during startup. Another example is the `com.adobe.granite.maintenance.oak` Adobe bundle, which wraps and provides Oak maintenance tasks.

## Possible implications and risks {#implications-and-risks}

* In a future AEM version internal exports might be removed causing broken dependencies and inactive bundles depending directly on Oak.
* API in internal exports might change.

## Possible solutions {#solutions}

* Use the Sling Resource API (or the JCR API) instead of low-level access.
* Avoid depending on internal packages that are not part of any public API or SPI.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.