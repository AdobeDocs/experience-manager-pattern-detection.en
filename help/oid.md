---
title: OID
description: Pattern Detector code help page
---

# OID {#oid}

Oak Index Definition

## Background {#background}

`OID` identifies issues related to Oak index definitions. It identifies modifications that have been made to standard Oak index definitions. It also identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. The message for each `OID` finding will identify the index and provide additional information.

Subtypes are used to identify the different types of information:

* `custom.index.violation`: A custom Oak index incompatibility with AEM as a Cloud Service.
* `standard.index.modification`: A modification to a standard Oak index.

## Possible implications and risks {#implications-and-risks}

* Modifications to standard Oak index definitions may be lost during an AEM upgrade.
* Oak definitions are immutable, should be packaged with the customer project code, and should only be deployed using Cloud Manager.
* All Oak index definitions should follow the naming convention and other rules for Oak indexes in AEM as Cloud Service. Those that do not may cause undesired behavior.

## Possible solutions {#solutions}

* Resolve the index rule violations identified in the message.
* Follow AEM as a Cloud Service [packaging guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) to deploy new or custom Oak index definitions.
* Customized AEM standard indexes and new custom Oak index definitions should follow the [content indexing guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) for AEM as Cloud Service.
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) project and understand how [OID violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) can be corrected and made compatible with AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
