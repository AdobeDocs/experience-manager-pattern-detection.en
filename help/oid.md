---
title: OID
description: Pattern Detector code help page
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
---
# OID {#oid}

Oak Index Definition

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak Index Definition"
>abstract="OID identifies issues related to Oak index definitions. It identifies modifications that have been made to standard Oak index definitions. It also identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. The message for each OID finding will identify the index and provide additional information."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="Content Indexing Guidelines"

`OID` identifies issues related to Oak index definitions. It identifies modifications that have been made to standard Oak index definitions. It also identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. The message for each `OID` finding will identify the index and provide additional information.

Subtypes are used to identify the different types of information:

* `index.rule.violation`: A custom Oak index incompatibility with AEM as a Cloud Service.
* `standard.index.modification`: A modification to a standard Oak index.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review all custom indexes and restrcutured per the content indexing guidelines. Leverage the Index Converter to migrate existing Custom Oak Index Definitions to AEM as a Cloud Service compatible Custom Oak Index Definition"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="Packaging Guidelines"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Index Converter"

* Modifications to standard Oak index definitions may be lost during an AEM upgrade.
* Oak definitions are immutable, should be packaged with the customer project code, and should only be deployed using Cloud Manager.
* All Oak index definitions should follow the naming convention and other rules for Oak indexes in AEM as Cloud Service. Those that do not may cause undesired behavior.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Tools & Resources"
>abstract="Review WKND-legacy project to understand how OID violations can be resolved in your Project. Also, Review OID Violation Example on Github to understand how legacy indexes can be converted using the Index Converter tool and made compatible with AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-Legacy Project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="OID Violation Example - Github"

* Resolve the index rule violations identified in the message.
* Follow AEM as a Cloud Service [packaging guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) to deploy new or custom Oak index definitions.
* Customized AEM standard indexes and new custom Oak index definitions should follow the [content indexing guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) for AEM as Cloud Service.
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) project and understand how [OID violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) can be corrected and made compatible with AEM as a Cloud Service.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
* Leverage the [Index Converter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) to migrate existing Custom Oak Index Definitions to AEM as a Cloud Service compatible Custom Oak Index Definitions.
