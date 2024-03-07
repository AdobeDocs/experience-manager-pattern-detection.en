---
title: MI
description: Pattern Detector code help page
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
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
* `missing.maintenance.configuration`: Identify missing maintenance task configurations.

## Possible implications and risks {#implications-and-risks}

* `sling.job.max.parallel`
  * A value of -1 is substituted with the number of available processors. This might cause performance issues on AEM instance.
* `missing.maintenance.configuration`
  * Missing maintenance task configurations may cause loss of performance or instance corruption.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Implementation Guidance"
>abstract="Contact Customer Care for help."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* `sling.job.max.parallel`
  * It is advisable to set the value to 0.5 in order to avail half of the available processors.
* `missing.maintenance.configuration`
  * Revision Clean Up: Please refer to [Revision Clean Up](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). The important part regarding the configuration is here: [Revision Cleanup - Configure Tail and Full compaction](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
  * Lucene Binaries Cleanup: Please refer to [Operations Dashboard - Lucene Binaries Cleanup](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
  * Data Store Garbage Collection: Please refer to [Data Store Garbage Collection](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
  * Workflow Purge: Please refer to [Regular Purging of Workflow Instances](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html#regular-purging-of-workflow-instances).
  * AuditLog Maintenance Task: Please refer to [Audit Log Maintenance](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Reach out to our [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
