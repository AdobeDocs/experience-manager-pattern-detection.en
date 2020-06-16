---
title: LUI
description: Pattern Detector code help page
---

# LUI {#lui}

Legacy User Interface

## Background {#background}

`LUI` identifies the use of deprecated user interface elements that are not recommended or not supported by AEM as a Cloud Service.

Subtypes are used to identify the different types of user interface elements that should or must be upgraded:

* `legacy.dialog.classic`: Classic UI dialogs based on ExtJS, must be changed to Coral.
* `legacy.dialog.coral2`: Coral 2 dialogs, should be updated to use Coral 3.
* `logacy.custom.component`: Components that inherit from `foundation/components`, should be updated to use Custom Components.
* `legacy.static.template`: Static Templates, should be upgraded to Editable Templates.

## Possible implications and risks {#implications-and-risks}

* The Classic UI is no longer available in AEM as a Cloud Service. The standard interface for authoring is the Touch-enabled UI.
* Relying on legacy custom components may increase maintenance costs over time.

## Possible solutions {#solutions}

* Utilize [AEM Modernization Tools suite](https://opensource.adobe.com/aem-modernize-tools/) to reduce the effort needed to modernize your AEM Sites implementations. These tools include conversion of:
  * Classic (ExtJS) Dialogs to Coral Dialogs
  * Foundation Components to Core Components
  * Static Templates and Column Control to Editable Templates & Responsive Grid
  * Designs & Design Dialogs to Editable Template Policies
* Review your project's custom components library and transition, if possible, to the set of standardized [Core Components](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html) to accelerate the development time and reduce the maintenance cost of your applications.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
