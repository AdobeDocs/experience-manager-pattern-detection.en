---
title: MI
description: Pattern Detector code help page

---
# MI {#mi}

Invalid Namespace

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Invalid Namespace"
>abstract="INS identifies namespace issues on AEM instance"

`INS`  Invalid Namespace identifies namespace issues on AEM instance.

Subtypes are used to identify the different types of information, such as:

* `uri`: Identify the invalid namespace URI in AEM.

## Possible implications and risks {#implications-and-risks}

* Unable to replicate content (across tier) or copy content (across env - via `/crx/packMgr` or Content Copy).

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Implementation Guidance"
>abstract="Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Fix the namespace definitions according to [JCR spec](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Follow steps mentioned [here](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.