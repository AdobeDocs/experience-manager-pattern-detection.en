---
title: WRF
description: Pattern Detector code help page.
---
# WRF {#wrf}

## Background {#background}

WRF identifies we-retail usage that is incompatible with AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possible solutions {#solutions}

Find the possible solutions for the different subtypes below:

* `weretail.bundles.detected` - These bundles will be uninstalled during upgrade
* `weretail.packages.detected` - These packages  will be deleted during upgrade
* `weretail.configs.detected` - Do not use We.Retail config properties in your custom code
* `weretail.packages.dependency` - Remove the dependency of any custom package on We.Retail
* `weretail.paths.detected` - These We.Retail paths can be deleted after making sure that you are not using social
* `weretail.resource.type.detected` - Remove We.Retail resource type usage
* `weretail.usage` - Remove We.Retail APIs from your custom code.