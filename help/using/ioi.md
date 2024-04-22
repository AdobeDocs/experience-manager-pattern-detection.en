---
title: IOI
description: Pattern Detector code help page.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
---
# IOI {#ioi}

Internal Oak Import

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import"
>abstract="IOI code identifies customer use of internal Oak packages, importing them via OSGi. They are usually exported without any particular version and are intended for consumption only by other Oak bundles or low-level AEM services."

`IOI` identifies customer use of internal Oak packages, importing them via OSGi. They are usually exported without any particular version and are intended for consumption only by other Oak bundles or low-level AEM services.

Some of these are used by `com.adobe.granite.repository`, which sets up a repository for AEM during startup. Another example is the `com.adobe.granite.maintenance.oak` Adobe bundle, which wraps and provides Oak maintenance tasks.

## Possible implications and risks {#implications-and-risks}

* In a future AEM version internal exports might be removed causing broken dependencies and inactive bundles depending directly on Oak.
* API in internal exports might change.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Implementation Guidance"
>abstract="Customers should review their custom code to identify the usage of such APIs and refactor them to be compatible with AEM as a Cloud Service. Reach out to Adobe Support for help & clarifications"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Use the Sling Resource API (or the JCR API) instead of low-level access.
* Avoid depending on internal packages that are not part of any public API or SPI.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
