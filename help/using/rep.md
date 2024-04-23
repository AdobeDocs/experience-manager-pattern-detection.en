---
title: REP
description: Pattern Detector code help page.
exl-id: e788deba-a301-404f-8e90-51f721409e69
---
# [!DNL REP] {#rep}

Replication Agent

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Replication Agent"
>abstract="REP identifies enabled replication agents. These are reported because of the potential for issues that should be addressed when upgrading to AEM as a Cloud Service. AEM as a Cloud Service uses Sling Content Distribution to distribute content from author to publish environments. This is done outside of the AEM runtime using the pipeline service of Adobe I/O Runtime on Adobe Developer. This is automatically configured in the provisioned AEM as a Cloud Service environment."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Notable Changes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Development Guidelines"

REP identifies enabled replication agents. These are reported because of the potential for issues that should be addressed when upgrading to AEM as a Cloud Service.

Subtypes are used to identify different types of information:

* `forward.replication`: Identify the enabled forward replication agents.
* `reverse.replication`: Identify the enabled reverse replication agents.
* `standard.replication.agent.modification`: Identify the enabled standard replication agents which are modified.
* `custom.replication.agent.detection`: Identify the enabled custom replication agents.

AEM as a Cloud Service uses [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) to distribute content from author to publish environments. This is done outside of the AEM runtime using the pipeline service of Adobe I/O Runtime on Adobe Developer. This is automatically configured in the provisioned AEM as a Cloud Service environment.

## Possible implications and risks {#implications-and-risks}

* The configuration of replication has changed with AEM as a Cloud Service. All current replication agents should be reviewed to see which are replaced by standard capability, which configurations must be moved to code, and which are not supported.
* Any use of replication agents in custom code or workflows should be reviewed while upgrading to AEM as a Cloud Service.
* Reverse replication is not initially supported in AEM as a Cloud Service.
* There is no need to configure a separate Dispatcher flush agent. This is automatically configured in the AEM as a Cloud Service environment.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to Review, refactor, and optimize custom functionality directly dependent on replication agents and make it compatible with AEM as a Cloud Service. Contact Adobe Support for help or clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replication - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* See the AEM as a Cloud Service [Development Guidelines](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) and release notes for [replication agents](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Review, refactor, and optimize functionality directly dependent on replication agents to perform business tasks.
* See how [replication](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) is affected by deployment in AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
