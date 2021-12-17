---
title: OU
description: Pattern Detector code help page
---
# OU {#ou}

Outdated Usage

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Outdated Usage"
>abstract="OU identifies the situation in which some JCR nodes, such as Sling or AEM components or API OSGi exports, are changed or removed in a non-compatible way. The customer may be not aware of this change before an upgrade. They might be upgraded to a non-compatible version or can be not available at all."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Notable Changes - AEM as a Cloud Service"

`OU` identifies the situation in which some JCR nodes, such as Sling or AEM components or API OSGi exports, are changed or removed in a non-compatible way. The customer may be not aware of this change before an upgrade. They might be upgraded to a non-compatible version or can be not available at all.

As the old versions are not installed by default, the customer application might not work correctly.

## Possible implications and risks {#implications-and-risks}

* The functionality that depends on any component that uses deprecated components or APIs can be broken and might not resolve correctly after an upgrade.
* Some features of the customer application or some AEM functionality may not work properly or might not be active after an upgrade.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Implementation Guidance"
>abstract="Best practice is to review and Adapt customer code to use the newest version of AEM components or APIs. Reach out to Adobe Support for help & clarifications."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Short-term: Installation of compatibility package might help.
* Long-term: Adapt customer code to use the newest version of AEM components or APIs.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
