---
title: CTEM
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# CTEM {#ctem}

Custom Template

## Background {#background}

`CTEM` identifies custom templates which have been installed on AEM. This information is provided for the purposes of best practices assessment.

Templates are identified by a primary type value of "cq:Template". A subtype is used with this code to identify the category of template:

* `custom.editable.template`: The path of the template does not start with "/apps".
* `custom.static.template`: The path of the template starts with "/apps".

## Possible implications and risks {#implications-and-risks}

* Best Practice is to move all static templates to editable templates.

## Possible solutions {#solutions}

* Leverage the [AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/) to migration Static Templates to Editable Templates.
* Find more information about Editable Templates at [Templates](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
