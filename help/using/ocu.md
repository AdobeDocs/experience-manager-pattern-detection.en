---
title: OCU
description: Pattern Detector code help page.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
---
# OCU {#ocu}

DEPRECATED: Outdated Code Usage (replaced by OU, Outdated Usage)

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Outdated Code Usage"
>abstract="OCU identifies the situation in which some JCR nodes, such as Sling or AEM components or API OSGi exports, are changed or removed in a non-compatible way. The customer may not be aware of this change before an upgrade. They might be upgraded to a non-compatible version or can be not available at all."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Notable Changes - AEM as a Cloud Service"

`OCU`  Identifies the situation in which some JCR nodes, such as Sling or AEM components or API OSGi exports, are changed or removed in a non-compatible way. The customer may not be aware of this change before an upgrade. They might be upgraded to a non-compatible version or can be not available at all.

As the old versions are not installed by default, the customer application might not work correctly.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses deprecated components or APIs can be broken and might not resolve correctly after an upgrade.
* Some features of the customer application or some AEM functionality may not work properly or might not be active after an upgrade.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Implementation Guidance"
>abstract="Best practice is to review and Adapt customer code to use the newest version of AEM components or APIs. Contact Adobe Support for help or clarifications."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Short term: Installation of a compatibility package might help.
* Long term: Adapt customer code to use the newest version of AEM components or APIs.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
