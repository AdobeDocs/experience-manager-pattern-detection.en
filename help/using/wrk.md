---
title: WRK
description: Pattern Detector code help page.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
---
# WRK {#wrk}

Workflow

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="WRK code identifies a finding related to a workflow model or launcher. These are reported because custom asset workflow models must be migrated when upgrading to AEM as a Cloud Service. With AEM as a Cloud Service, asset processing is now performed by asset microservices."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Asset Microservices"

`WRK` identifies a finding related to a workflow model or launcher. These are reported because custom asset workflow models must be migrated when upgrading to AEM as a Cloud Service.

A subtype is used to identify the type of workflow issue currently detected.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launcher.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Implementation Guidance"
>abstract="As standard asset workflows are automatically supported my asset microservices, Best Practice is to review all custom asset workflow model or launcher to see if they are needed once we transition to AEM as a Cloud Service. Customizations to asset workflows require migration in order to work with AEM as a Cloud Service with help of Asset Workflow Migration Tool"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Getting Started - Asset Microservices"

* Asset processing has traditionally been performed with asset workflows executing on the AEM Author instance. With AEM as a Cloud Service, asset processing is now performed by asset microservices. See the [asset microservices overview](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) for more information.
* Standard asset workflows are automatically supported my asset microservices.
* Customizations to asset workflows require migration in order to work with AEM as a Cloud Service.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Tools & Resources"
>abstract="Review & plan to run the Asset Workflow Migration Tool once a custom asset workflow model or launcher is identified. Reach out to Adobe Support for help & clarifications"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="Asset Workflow Migration Tool"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* If a custom asset workflow model or launcher is identified, plan to run the [Asset Workflow Migration Tool](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Review the [Getting started using asset microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) for more information.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
