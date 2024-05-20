---
title: OID
description: Pattern Detector code help page.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
---
# OID {#oid}

Oak Index Definition

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak Index Definition"
>abstract="OID identifies issues related to Oak index definitions. It identifies modifications that have been made to standard Oak index definitions. It also identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. The message for each OID finding identifies the index and provide additional information."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Content Indexing Guidelines"

`OID`  Identifies issues related to Oak index definitions. It identifies modifications that have been made to standard Oak index definitions. It also identifies custom Oak index definitions that are incompatible with AEM as a Cloud Service. The message for each `OID` finding identifies the index and provide additional information.

Subtypes are used to identify the different types of information:

* `index.rule.violation`: A custom Oak index incompatibility with AEM as a Cloud Service
* `standard.index.modification`: A modification to a standard Oak index.

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to review all custom indexes and restructure per the content indexing guidelines. Use the Index Converter to migrate existing Custom Oak Index Definitions to AEM as a Cloud Service compatible Custom Oak Index Definition"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Packaging Guidelines"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Index Converter"

* Modifications to standard Oak index definitions may be lost during an AEM upgrade.
* Oak definitions are immutable, should be packaged with the customer project code, and should only be deployed using Cloud Manager.
* All Oak index definitions should follow the naming convention and other rules for Oak indexes in AEM as a Cloud Service. Otherwise, it can cause undesired behavior.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Tools and Resources"
>abstract="Review WKND-legacy project to understand how OID violations can be resolved in your Project. Also, review the OID Violation Example on GitHub. It can help you understand how legacy indexes can be converted using the Index Converter tool and made compatible with AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-Legacy Project"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="OID Violation Example - GitHub"

* Resolve the index rule violations identified in the message.
* To deploy new or custom Oak index definitions, follow AEM as a Cloud Service [packaging guidelines](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* Customized AEM standard indexes and new custom Oak index definitions should follow the [content indexing guidelines](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) for AEM as a Cloud Service.
* Review [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) project and understand how [OID violations](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) can be corrected and made compatible with AEM as a Cloud Service.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
* Use the [Index Converter](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) to migrate existing Custom Oak index definitions to AEM as a Cloud Service compatible Custom Oak index definitions.
