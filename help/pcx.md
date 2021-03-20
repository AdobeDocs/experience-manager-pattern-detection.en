---
title: PCX
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# PCX {#pcx}

Page Complexity

## Background {#background}

`PCX` identifies pages that contain a large number of nodes in their structure.

Subtypes are used to identify the different types of information:

* `page.complexity.medium`: A page contains a moderately high number of nodes that may affect rendering performance.
* `page.complexity.high`: A page contains a very high number of nodes that will likely affect rendering performance.

## Possible implications and risks {#implications-and-risks}

* A large number of nodes within a page may affect its rendering performance.

## Possible solutions {#solutions}

* Take steps to reduce the total number of nodes within a page, including:
  * Verify that there are no unnecessary containers.
  * Test whether the same layout can be achieved with fewer containers.
  * Simplify the page content.
  * Reduce the depth of the node structure.
  * Refactor any included Experience Fragments for simplicity.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
