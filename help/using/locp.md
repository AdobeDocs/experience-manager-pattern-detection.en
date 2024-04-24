---
title: LOCP
description: Pattern Detector code help page.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
---
# LOCP {#locp}

/libs Overwriting Custom Packages

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages"
>abstract="LOCP identifies the detection of a custom package that delivers content to /libs, which is an anti-pattern (except in the case ACLs)."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Sustainable Upgrades"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`LOCP`  Identifies the detection of a custom package that delivers content to `/libs`, which is an anti-pattern (except in the case ACLs).

## Possible implications and risks {#implications-and-risks}

* The customer code might be deleted or replaced for any CFP, SP, or major AEM upgrade.
* Sometimes the new content might not be installed properly.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Implementation Guidance"
>abstract="Customers should review their custom code and packages to identify if content is delivered to /libs and refactor it to rely on overlay the content under /apps and make it compatible with AEM as a Cloud Service. Contact Adobe Support for help or clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Overlays"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Customer packages should deploy content to `/apps` instead of `/libs`.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) if you need clarifications or concerns addressed.
