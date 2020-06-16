---
title: DGV
description: Pattern Detector code help page
---

# DGV {#dgv}

Developer Guideline Violation

## Background {#background}

`DGV` identifies violations of selected [development guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/development-guidelines.html) for AEM as a Cloud Service. Although these violations might not be a problem in other application contexts, including with previous versions of AEM, they are issues when used with AEM as a Cloud Service.

Subtypes are used to identify the different types of detected violations:

* `maintenance.task.configuration`: The configuration of a certain periodic maintenance activity.
* `unsupported.scheduler`: The use of the Sling Commons Scheduler API for a scheduled task.

## Possible implications and risks {#implications-and-risks}

* `maintenance.task.configuration`
  * Some maintenance tasks that previously required explicit configuration are now automatically configured and managed within AEM as a Cloud Service.
  * Maintenance task configuration in AEM as a Cloud Service must be moved into source control.

* `unsupported.scheduler`
  * Applications dependent on background tasks using [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) might not work as expected because execution cannot be guaranteed in AEM as a Cloud Service.
  * AEM as a Cloud Service development guidelines for [background tasks and long running jobs](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggest that the code executed as a scheduled task must assume that the instance it is running on, can be brought down at any time. Therefore, the code must be resilient and resumable.

## Possible solutions {#solutions}

* `maintenance.task.configuration`
  * Review AEM as a Cloud Service [Maintenance Task](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/operations/maintenance.html) documentation.
  * Ensure that [Maintenance Task Configuration](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) is in source control.

* `unsupported.scheduler`
  * Replace the use of [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) with [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), which have an at-least-once execution guarantee.
  * Long running jobs should be avoided if possible.

* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
