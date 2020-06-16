---
title: REP
description: Pattern Detector code help page
---

# REP {#rep}

Replication Agent

## Background {#background}

`REP` identifies enabled replication agents. These are reported because of the potential for issues that should be addressed when upgrading to AEM as a Cloud Service.

AEM as a Cloud Service uses [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) to distribute content from author to publish environments. This is done outside of the AEM runtime using the pipeline service of Adobe I/O. This is automatically configured in the provisioned AEM as a Cloud Service environment.

## Possible implications and risks {#implications-and-risks}

* The configuration of replication has changed with AEM as a Cloud Service. All current replication agents should be reviewed to see which are replaced by standard capability, which configurations must be moved to code, and which are not supported.
* Any use of replication agents in custom code or workflows should be reviewed while upgrading to AEM as a Cloud Service.
* Reverse replication is not initially supported in AEM as a Cloud Service.
* There is no need to configure a separate dispatcher flush agent. This is automatically configured in the AEM as a Cloud Service environment.

## Possible solutions {#solutions}

* See the AEM as a Cloud Service [Development Guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) and release notes for [replication agents](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Review, refactor, and optimize functionality directly dependent on replication agents to perform business tasks.
* See how [replication](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/deploying/overview.html#replication) is affected by deployment in AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
