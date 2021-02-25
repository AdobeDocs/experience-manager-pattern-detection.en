---
title: FORM
description: Pattern Detector code help page
---

# FORM {#form}

Adobe Experience Manager Forms

## Background {#background}

`FORM` identifies potential issues related to migrating from Adobe Experience Manager Forms to Adobe Experience Manager Forms as a Cloud Service. Address these issues before migrating to Cloud Service.

The following subtypes help you identify the different types of issues:

* `modified.feature`: These features, assets, or APIs were updated or modified for Cloud Service. Before migrating to the Cloud Service, run the migration utility to make these features and assets compatible with the Cloud Service.  
* `unavailable.feature`: Your environment has features and assets that are not available or removed from Cloud Service. Do not migrate such features or assets to a Cloud Service environment.
* `unsupported.feature`: Your environment uses some features yet unsupported on Cloud Service. Do not migrate such features or assets to a Cloud Service environment. Keep an eye on monthly release notes for the availability of the features.
* `unsupported.api`: Your environment has some APIs yet unsupported on the Cloud Service. Before migrating to the Cloud Service, disable, replace, or remove these APIs from your code. Keep an eye on monthly release notes for the availability of the features.

See the [Possible implications and risks](#implications-and-risks) and [Possible solutions](#solutions) sections for information about replacements and other actions required to make some features and APIs compatible with the Cloud Service

## Possible implications and risks {#implications-and-risks}

Address the following issues, before migrating to Adobe Experience Manager Forms as a Cloud Service. When the below-listed implications and risks are not addressed, some features do not function as expected in the Cloud Service environment.

* The code editor functionality of the rule editor feature is not available. (CODE_EDITOR)

* Email support (SMTP port) is disabled, by default. (EMAIL_SERVICE_CONFIGURATION)

* The **[!UICONTROL Email PDF]** submit action is not available.(EMAIL_PDF_SUBMIT_ACTION)

* XDP-based adaptive forms are not yet supported. (XDP_BASED_FORM)

* A submit action is invoked immediately on form submission instead of waiting for all signers to complete the signing. So, The adaptive form signature document (Adobe Sign agreement PDF sent to signers) is not available for submit actions to use or process. (FORM_SIGN_INTEGRATION)  

* The Signature step is not available. (SIGNATURE_STEP)

* The Verify step is not available. (VERIFY_STEP)

* The Forms Portal feature and **[!UICONTROL Forms Portal submit action]** are not available. You cannot use Forms Portal to list forms, save drafts, or show submitted forms. You cannot send (use **[!UICONTROL Forms Portal submit action]** ) data submitted to an adaptive form to a Forms Portal. [!UICONTROL Save as draft] and [!UICONTROL Auto Save] an adaptive form features are not supported at present. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* The **[!UICONTROL Submit to Forms workflow]** submit action is not available. On AEM 6.5 Forms and previous versions, the submit action was used to submit adaptive form data to legacy AEM Forms on JEE Workflows and LiveCycle Workflows. (LC_WORKFLOW_SUBMISSION)

* The Interactive Communications capability is not available.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Save as draft]** and **[!UICONTROL Auto Save]** an adaptive form features are not supported at present. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Metadata accordion is not available. (METADATA_ACCORDION_FORM_CONTAINER)

* The CAPTCHA component now uses the Google reCAPTCHA service to validate CAPTCHA, by default. The option to use Adobe Experience Manager to validate CAPTCHA is not available. (FORMS_CAPTCHA)

## Possible solutions {#solutions}

* Use migration utility to convert all rule scripts on your environment to reusable functions. You can use the reusable functions with Visual Rule editor to continue obtaining results obtained with rule scripts. (CODE_EDITOR)

* Contact the support team to enable email (open SMTP Port) functionality for your environment. Only outgoing HTTP and HTTPS connections are enabled, by default. (EMAIL_SERVICE_CONFIGURATION)

* Use **[!UICONTROL Email]** submit action instead of **[!UICONTROL Email PDF]**. The **[!UICONTROL Email]** submit action provide options to send attachments and attach Document of Record (DoR) with email. (EMAIL_PDF_SUBMIT_ACTION)

* Do not migrate XDP based adaptive forms to a Cloud Service environment. Keep an eye on monthly release notes for the availability of the features. (XDP_BASED_FORM)

* Submitted data contain Sign Agreement ID. You can use the Sign Agreement ID to retrieve a Sign Agreement PDF, if required.  (FORM_SIGN_INTEGRATION)

* Replace the Signature step in your adaptive forms with the option to Sign an adaptive form post submission, in the same window. It helps you continue providing an [in-browser signing experience](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). (SIGNATURE_STEP)

* Remove the verify step from your existing adaptive forms before moving such forms to a Cloud Service environment. (VERIFY_STEP)

* There is no alternative to **[!UICONTROL Forms Portal submit action]**. You can use this submit action once the Forms Portal feature is released for the Cloud Service. Keep an eye on monthly release notes for the availability of the features. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* There is no alternative submit action to **[!UICONTROL Submit to Forms workflow]** submit actions. You can develop a custom submit action to send data, attachments, or Document of Record (DoR) to a LiveCycle process. (LC_WORKFLOW_SUBMISSION)

* Do not migrate your Interactive Communications, Letters, and related Dictionaries to a Cloud Service environment. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Disable the **[!UICONTROL Save as draft]** and **[!UICONTROL Enable Auto Save]** option in your adaptive forms before migrating them to Cloud Service. You can enable these options once the Forms Portal feature is released for the Cloud Service. Keep an eye on monthly release notes for the availability of the features. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* There is no replacement for metadata accordion. Remove it from your forms before migrating them to Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use the Google reCaptcha instead of the CAPTCHA service provided by Adobe Experience Manager. (FORMS_CAPTCHA)

Reach out to [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
