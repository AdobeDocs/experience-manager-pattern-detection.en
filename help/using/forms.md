---
title: FORM
description: Pattern Detector code help page.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
---
# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="FORMS code identifies potential issues related to migrating from AEM (Adobe Experience Manager) Forms to AEM Forms as a Cloud Service. Review possible implications and risks associated and address these issues before migrating to Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Possible implications and risks"

`FORMS`  Identifies potential issues related to migrating from [!DNL Adobe Experience Manager Forms] to [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Address these issues before migrating to [!DNL Cloud Service].

The following subtypes help you identify the different types of issues:

* `modified.feature`: These features, assets, or APIs were updated or modified for Cloud Service. Before migrating to the Cloud Service, run the migration utility to make these features and assets compatible with the Cloud Service.  
* `unavailable.feature`: Your environment has features and assets that are not available or removed from Cloud Service. Do not migrate such features or assets to a Cloud Service environment.
* `unsupported.feature`: Your environment uses some features yet unsupported on Cloud Service. Do not migrate such features or assets to a Cloud Service environment. Look for monthly release notes for information on availability of the features.
* `unsupported.api`: Your environment has some APIs yet unsupported on the Cloud Service. Before migrating to the Cloud Service, disable, replace, or remove these APIs from your code. Look for monthly release notes for information on availability of the features.

See the [Possible implications and risks](#implications-and-risks) and [Possible solutions](#solutions) sections for information about replacements and other actions required to make some features and APIs compatible with the Cloud Service

## Possible implications and risks {#implications-and-risks}

Address the following issues, before migrating to [!DNL Adobe Experience Manager Forms as a Cloud Service]. When the below-listed implications and risks are not addressed, some features do not function as expected in the Cloud Service environment.

* The code editor functionality of the rule editor feature is not available. (CODE_EDITOR)

* Email support (SMTP port) is disabled by default. (EMAIL_SERVICE_CONFIGURATION)

* The **[!UICONTROL Email PDF]** Submit Action is not available. (EMAIL_PDF_SUBMIT_ACTION)

* XFA-based Adaptive Forms are not supported yet. (XFA_BASED_FORM, XDP_BASED_FORM)

* A Submit Action is invoked immediately on form submission instead of waiting for all signers to complete the signing. So, the Adobe Sign agreement PDF sent to signers is not available for Submit Actions to use or process. (FORM_SIGN_INTEGRATION)  

* The Signature step is not available. (SIGNATURE_STEP)

* The Verify step is not available. (VERIFY_STEP)

* The **[!UICONTROL Submit to Forms Workflow]** Submit Action is not available. On AEM 6.5 Forms and previous versions, the Submit Action was used to submit Adaptive Form data to legacy AEM Forms on JEE Workflows and LiveCycle Workflows. (LC_WORKFLOW_SUBMISSION)

* The Interactive Communications capability is not available. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* Metadata accordion is not available. (METADATA_ACCORDION_FORM_CONTAINER)

* The CAPTCHA component now uses the Google reCAPTCHA service to validate CAPTCHA, by default. The option to use Adobe Experience Manager to validate CAPTCHA is deprecated. (FORMS_CAPTCHA)

* [!DNL AEM Forms] app is not available for [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Document services](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) steps are not available in AEM Workflows. (WORKFLOW_DOCSERVICES)

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Implementation Guidance"
>abstract="Information exposed via FORMS code can provide guidance about replacements and other actions required to make some features and APIs compatible with the Cloud Service. Contact Adobe Support for help or clarifications."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Use a migration utility to convert all rule scripts in your environment to reusable functions. You can use the reusable functions with Visual Rule Editor to continue obtaining results obtained with rule scripts. (CODE_EDITOR)

* Contact the support team so you can have email functionality enabled (open SMTP Port) for your environment. Only outgoing HTTP and HTTPS connections are enabled by default. (EMAIL_SERVICE_CONFIGURATION, Email step)

* Use **[!UICONTROL Email]** Submit Action instead of **[!UICONTROL Email PDF]**. The **[!UICONTROL Email]** Submit Action provide options to send attachments and attach Document of Record (DoR) with email. (EMAIL_PDF_SUBMIT_ACTION)

* Submitted data contains Adobe Sign Agreement ID. You can use the Sign Agreement ID to retrieve a Sign Agreement PDF, if necessary. (FORM_SIGN_INTEGRATION)

* Remove the Signature step from an existing Adaptive Form. Configure your Adaptive Form to use an [in-browser signing experience](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). It displays Adobe Sign agreement to sign the agreement within the browser on submission of an Adaptive Form. In-browser signing experience helps provide a faster signing experience and saves time for the signer. (SIGNATURE_STEP)

* Remove the verification step from your existing Adaptive Forms before moving such forms to a [!DNL Cloud Service] environment. (VERIFY_STEP)

* Edit your existing adaptive forms so you can use [Submit to REST endpoint](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Send email](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Submit using Form Data Model](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model), and [Invoke an AEM Workflow](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Submit Actions.

* You can develop an AEM Workflow and edit your existing adaptive forms to use [AEM Workflow](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Submit Action to send data to an AEM Workflow instead of using the **[!UICONTROL Submit to Forms Workflow]** Submit Action. You can develop a custom Submit Action to send data, attachments, or Document of Record (DoR) to a LiveCycle process instead of using the [!UICONTROL Submit to Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Look for monthly release notes for information on availability of the Interactive Communications feature. Do not migrate your Interactive Communications, Letters, and related Dictionaries to a Cloud Service environment until the feature is not available. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* There is no replacement for metadata accordion. Remove it from your forms before migrating them to Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use the Google reCAPTCHA instead of the CAPTCHA service provided by Adobe Experience Manager. (FORMS_CAPTCHA)

* Do not migrate to a AEM Workflow model that uses a document services Workflow step. Also, do not migrate or update Adaptive Forms that send user data to a Workflow Model that uses document services Workflow steps or change the **`Submit Action`** to a [supported one](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) before migrating the form. (WORKFLOW_DOCSERVICES)

* Adaptive Forms offer a responsive design. These forms change the appearance, design, and interactivity based on the underlying device. You can continue using Adaptive Forms on a mobile device. Look for monthly release notes for information on the availability of the [!DNL AEM Forms] app. (AEM_FORMS_APP)

* Support for XFA-based Adaptive Forms is not available out of the box. If you intend to use XFA-based Adaptive Forms, contact Adobe Support with details of your use case and specific requirements.(XFA_BASED_FORM, XDP_BASED_FORM)

Contact [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) if you need clarifications or concerns addressed.
