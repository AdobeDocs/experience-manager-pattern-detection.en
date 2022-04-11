---
title: LUI
description: Pattern Detector code help page
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
---
# LUI {#lui}

Legacy User Interface

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Legacy User Interface"
>abstract="LUI identifies the use of deprecated user interface elements that are not recommended or not supported in later versions of AEM and in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Notable Changes - AEM as a Cloud Service"

`LUI` identifies the use of deprecated user interface elements that are not recommended or not supported in later versions of AEM and in AEM as a Cloud Service.

Subtypes are used to identify the different types of user interface elements that should or must be upgraded:

* `legacy.dialog.classic`: Classic UI dialogs based on ExtJS, must be changed to Coral.
  * This is detected when the dialog name is "dialog" or "design_dialog" and when
  the `jcr:primaryType` property value or the `xtype` property value is "cq:Dialog".
* `legacy.dialog.coral2`: Coral 2 dialogs, should be updated to use Coral 3.
  * This is detected when the dialog and its child content node names are "cq:dialog/content",
  "cq:design_dialog/content", "cq:dialog.coral2/content", or "cq:design_dialog.coral2/content"
  and the `sling:resourceType` property value does not contain
  "granite/ui/components/coral/foundation".
* `legacy.custom.component`: Components that inherit from `foundation/components`, should be updated to use Core Components.
  * This is detected when the `jcr:primaryType` property value is "cq:Component" and the
  `sling:resourceSuperType` property value contains "foundation/components" or any of the
  `sling:resourceSuperType` property values of the chain of supertype components contain
  "foundation/components".
* `legacy.static.template`: Static Templates, should be upgraded to Editable Templates.
  * This is detected when the `jcr:primaryType` property value is "cq:Template".
* `content.fragment.template`: Content Fragment Templates, should create fragment models to replace the fragment templates.
  * Content fragment templates can be found at the following locations : 
    * Out of the box content fragment templates are stored in `/libs/settings/dam/cfm/templates`
    * They can be overlaid in  `/apps/settings/dam/cfm/templates`  or  `/conf/.../settings/dam/cfm/templates`(... = global or "tenant")
  
## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Implementation Guidance"
>abstract="The Classic UI is no longer available in AEM as a Cloud Service and the standard interface for authoring is the Touch-enabled UI. Best Practice is to move all unsupported interfaces and linked cutomizations should be refactored to newer features/capabilities which are compatible with AEM as a Cloud Service. Customers can leverage existing AEM Modernization Suite to help reduce the effort needed to modernize the AEM Sites implementations."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM Modernization Tools"

* The Classic UI is no longer available in AEM as a Cloud Service. The standard interface for authoring is the Touch-enabled UI.
* Relying on legacy custom components may increase maintenance costs over time.
* Content fragment templates were superseded by content fragment models in AEM 6.3. Migrating content fragments that are based on legacy templates to AEM as a Cloud Service will retain these fragments as functional, but it will not be possible to create new fragments based on the legacy template. It will also not be possible to deliver these fragments using AEM GraphQL, which requires content fragment models as schemas.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Tools & Resources"
>abstract="With the help of AEM Modernization Suite, Customers can convert Classic(ExtJS) Dialogs to Coral Dialogs. The intent is to help customers move from the unsupported or legacy features to the robust, modern AEM offerings. These tools are condfigurable, configuration-aware and extensible. Also, explore replacement of custom components with the set of standardized Core Components to accelerate the development time and reduce the maintenance cost of your applications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Component Convertor"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Core Components"

* Utilize [AEM Modernization Tools suite](https://opensource.adobe.com/aem-modernize-tools/) to reduce the effort needed to modernize your AEM Sites implementations. These tools include conversion of:
  * Classic (ExtJS) Dialogs to Coral Dialogs
  * Foundation Components to Core Components
  * Static Templates and Column Control to Editable Templates & Responsive Grid
  * Designs & Design Dialogs to Editable Template Policies
* Review your project's custom components library and transition, if possible, to the set of standardized [Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) to accelerate the development time and reduce the maintenance cost of your applications.
* It is recommended to create content fragment models with equivalent capabilities to the legacy templates and use those models for content fragment creation moving forward.Refer to [Content Fragment Models](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=en) for more details.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
