---
title: MI
description: Pattern Detector code help page

---
# MI {#mi}

Misconfiguration Issue

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Misconfiguration Issue"
>abstract="MI identifies configuration issues on AEM instance"

`MI`  Misconfiguration Issue identifies configuration issues on AEM instance.

Subtypes are used to identify the different types of information, such as:

* `sling.job.max.parallel`: Identify the sling jobs where max parallel configuration is set to -1.

## Possible implications and risks {#implications-and-risks}

* `sling.job.max.parallel`
  * A value of -1 is substituted with the number of available processors. This might cause performance issues on AEM instance.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementation Guidance"
>abstract="Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* `sling.job.max.parallel`
    * It is advisable to set the value to 0.5 in order to avail half of the available processors.
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.