---
title: CTEM
description: Pattern Detector code help page.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
---
# CTEM {#ctem}

Custom Template

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Custom Template"
>abstract="CTEM identifies custom components which have been installed on AEM. This information is provided for the purposes of best practices assessment"

CTEM identifies custom templates which have been installed on AEM. This information is provided for the purposes of best practices assessment.

Templates are identified by a primary type value of `cq:Template`. A subtype is used with this code to identify the category of template:

* `custom.editable.template`: The path of the template does not start with "/apps".
* `custom.static.template`: The path of the template starts with "/apps".

## Possible implications and risks {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Implementation Guidance"
>abstract="Best Practice is to move all static templates to editable templates. Customers can use existing AEM Modernization Tools to migrate Static Templates to Editable Templates."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Editable Templates"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM Modernization Tools"

* Best Practice is to move all static templates to editable templates.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Tools & Resources"
>abstract="With the help of AEM Modernization Suite, Customers can manipulate the structure of a page from a Static definition, to an Editable Template. The intent is to help customers move from the limited capabilities of the legacy features to the robust, modern AEM offerings. These tools are configurable, configuration-aware, and extensible. Contact Adobe Support for help or clarifications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Page Structure Converter"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud Support"

* Use the [AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/) to migration Static Templates to Editable Templates.
* Find more information about Editable Templates at [Templates](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
