---
title: MI
description: Pattern Detector code help page.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
---
# MI {#mi}

Misconfiguration Issue

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Misconfiguration Issue"
>abstract="MI identifies configuration issues on AEM instance"

`MI` (Misconfiguration Issue) Identifies configuration issues on AEM instance.

Subtypes are used to identify the different types of information, such as:

* `sling.job.max.parallel`: Identify the sling jobs where max parallel configuration is set to -1.
* `missing.maintenance.configuration`: Identify missing Maintenance Task configurations.

## Possible implications and risks {#implications-and-risks}

* `sling.job.max.parallel`
  * A value of -1 is substituted with the number of available processors. As such, it might cause performance issues on an AEM instance.
* `missing.maintenance.configuration`
  * Missing Maintenance Task configurations may cause loss of performance or instance corruption.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementation Guidance"
>abstract="Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* `sling.job.max.parallel`
  * Adobe recommends setting the value to 0.5 to take advantage of half of the available processors.
* `missing.maintenance.configuration`
  * Revision Clean Up: See [Revision Clean Up](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). The important part regarding the configuration is here: [Revision Cleanup - Configure Tail and Full compaction](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
  * Lucene Binaries Cleanup: See [Operations Dashboard - Lucene Binaries Cleanup](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
  * Data Store Garbage Collection: See [Data Store Garbage Collection](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
  * Workflow Purge: See [Regular Purging of Workflow Instances](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
  * AuditLog Maintenance Task: See [Audit Log Maintenance](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Contact the [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to address concerns.
