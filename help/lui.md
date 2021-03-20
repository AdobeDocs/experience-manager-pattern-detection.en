---
title: LUI
description: Pattern Detector code help page
---

# LUI {#lui}

Legacy User Interface

## Background {#background}

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

## Possible implications and risks {#implications-and-risks}

* The Classic UI is no longer available in AEM as a Cloud Service. The standard interface for authoring is the Touch-enabled UI.
* Relying on legacy custom components may increase maintenance costs over time.

## Possible solutions {#solutions}

* Utilize [AEM Modernization Tools suite](https://opensource.adobe.com/aem-modernize-tools/) to reduce the effort needed to modernize your AEM Sites implementations. These tools include conversion of:
  * Classic (ExtJS) Dialogs to Coral Dialogs
  * Foundation Components to Core Components
  * Static Templates and Column Control to Editable Templates & Responsive Grid
  * Designs & Design Dialogs to Editable Template Policies
* Review your project's custom components library and transition, if possible, to the set of standardized [Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html) to accelerate the development time and reduce the maintenance cost of your applications.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
