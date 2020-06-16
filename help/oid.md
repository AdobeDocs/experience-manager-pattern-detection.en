---
title: OID
description: Pattern Detector code help page
---

# OID {#oid}

Oak Index Definition

## Background {#background}

`OID` identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. It also identifies modifications that have been made to standard Oak index definitions. The message for each `OID` finding will identify the index and provide additional information.

Subtypes are used to identify the different types of information:

* `custom.index.violation`: A custom Oak index incompatibility with AEM as a Cloud Service.
* `standard.index.modification`: A modification to a standard Oak index.

## Possible implications and risks {#implications-and-risks}

* Oak definitions are immutable, should be packaged with the customer project code, and should only be deployed using Cloud Manager.
* All Oak index definitions should follow the naming convention and other rules for Oak indexes in AEM as Cloud Service. Those that do not may cause undesired behavior.

## Possible solutions {#solutions}

* Resolve the index rule violations identified in the message.
* Follow AEM as a Cloud Service [packaging guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) to deploy new or custom Oak index definitions.
* Customized AEM standard indexes and new custom Oak index definitions should follow the [content indexing guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) for AEM as Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
