---
title: WRK
description: Pattern Detector code help page
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
---
# WRK {#wrk}

Workflow

## Background {#background}

`WRK` identifies a finding related to a workflow model or launcher. These are reported because custom asset workflow models must be migrated when upgrading to AEM as a Cloud Service.

A subtype is used to identify the type of workflow issue currently detected.

* `custom.asset.workflow`: Detection of a custom asset workflow model or launcher.

## Possible implications and risks {#implications-and-risks}

* Asset processing has traditionally been performed with asset workflows executing on the AEM Author instance. With AEM as a Cloud Service, asset processing is now performed by asset microservices. (Please see the [asset microservices overview](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) for more information.
* Standard asset workflows are automatically supported my asset microservices.
* Customizations to asset workflows require migration in order to work with AEM as a Cloud Service.

## Possible solutions {#solutions}

* If a custom asset workflow model or launcher is identified, plan to run the [Asset Workflow Migration Tool](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Review the [Getting started using asset microservices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) for more information.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
