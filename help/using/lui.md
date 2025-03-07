---
title: LUI
description: Pattern Detector code help page.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
---
# LUI {#lui}

Legacy User Interface

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Legacy User Interface"
>abstract="LUI identifies the use of deprecated User Interface elements. These elements that are not recommended or not supported in later versions of AEM and in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Notable Changes - AEM as a Cloud Service"

`LUI`  Identifies the use of deprecated User Interface elements. These elements are not recommended or not supported in later versions of AEM and in AEM as a Cloud Service.

Subtypes are used to identify the different types of user interface elements that should or must be upgraded:

* `legacy.dialog.classic`: Classic UI dialog boxes based on ExtJS must be changed to Coral.
  * This subtype is detected when the dialog box name is `dialog` or `design_dialog` and when
  the `jcr:primaryType` property value or the `xtype` property value is `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` dialog boxes should be updated to use `Coral 3`.
  * This subtype is detected when the dialog box and its child content node names are
    * `cq:dialog/content`,
    * `cq:design_dialog/content`, 
    * `cq:dialog.coral2/content`,
    * or `cq:design_dialog.coral2/content`
  and the `sling:resourceType` property value does not contain `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: Components that inherit from `foundation/components` should be updated to use Core Components.
  * This subtype is detected when the `jcr:primaryType` property value is `cq:Component` and the
  `sling:resourceSuperType` property value contains "foundation / components." Or, any of the
  `sling:resourceSuperType` property values of the chain of supertype components contain
  "foundation / components."
* `legacy.static.template`: Static Templates should be upgraded to Editable Templates.
  * This subtype is detected when the `jcr:primaryType` property value is `cq:Template`.
* `content.fragment.template`: Content Fragment Templates should create fragment models to replace the Fragment Templates.
  * Content fragment templates can be found at the following locations : 
    * Out of the box content fragment templates are stored in `/libs/settings/dam/cfm/templates`
    * They can be overlaid in  `/apps/settings/dam/cfm/templates`  or  `/conf/.../settings/dam/cfm/templates`(... = global or "tenant")
* `translation.dictionary`: `I18n` dictionary that is present under `/apps`.
    * `/apps` is immutable at runtime and translator.html would no longer be available in AEM as a cloud service.
  
## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementation Guidance"
>abstract="The Classic UI is no longer available in AEM as a Cloud Service and the standard interface for authoring is the Touch-enabled UI. Best Practice is to move all unsupported interfaces and linked customizations should be refactored to newer features and capabilities that are compatible with AEM as a Cloud Service. Customers can use the existing AEM Modernization Suite to help reduce the effort needed to modernize the AEM Sites implementations."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM Modernization Tools"

* The Classic UI is no longer available in AEM as a Cloud Service. The standard interface for authoring is the Touch-enabled UI.
* Relying on legacy custom components may increase maintenance costs over time.
* Content Fragment Templates superseded Content Fragment models in AEM 6.3. Migrating Content Fragments that are based on legacy templates to AEM as a Cloud Service retain these fragments as functional, but it is not possible to create fragments based on the legacy template. It is also not possible to deliver these fragments using AEM GraphQL, which requires Content Fragment models as schemas.
* /apps is immutable at runtime and translator.html would no longer be available in AEM as a cloud service. Thus, `I18n` dictionaries must come from Git by way of the CI / CD pipeline.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools and Resources"
>abstract="With the help of AEM Modernization Suite, Customers can convert Classic(ExtJS) Dialogs to Coral Dialogs. The intent is to help customers move from the unsupported or legacy features to the robust, modern AEM offerings. These tools are configurable, configuration-aware, and extensible. Also, explore replacement of custom components with the set of standardized Core Components to accelerate the development time and reduce the maintenance cost of your applications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Component Convertor"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction" text="Core Components"

* To reduce the effort needed to modernize your AEM Sites implementations, use the [AEM Modernization Tools suite](https://opensource.adobe.com/aem-modernize-tools/). These tools include conversion of:
  * Classic (ExtJS) Dialogs to Coral Dialogs
  * Foundation Components to Core Components
  * Static Templates and Column Control to Editable Templates and Responsive Grid
  * Designs and Design Dialogs to Editable Template Policies
* Review your project's custom components library and transition, if possible, to the set of standardized [Core Components](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction) to accelerate the development time and reduce the maintenance cost of your applications.
* Create Content Fragment models with equivalent capabilities to the legacy templates and use those models for Content Fragment creation in the future. See [Content Fragment Models](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) for more details.
* `I18n` dictionaries must come from Git via the CI / CD pipeline. [Documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
