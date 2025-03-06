---
title: SIF
description: Pattern Detector code help page.
---
# SIF {#sif}

## Background {#background}

SIF identifies Social usage that is incompatible with AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possible solutions {#solutions}

Find the possible solutions for the different subtypes below:

* `social.bundles.detected` - These bundles will be uninstalled during upgrade
* `social.packages.detected` - These packages  will be deleted during upgrade
* `social.packages.dependency` - Please remove social's package dependency from custom packages
* `social.nodes.detected` - Update custom code to not create social nodes
* `social.configs.detected` - Do not use social config properties in custom code
* `social.users.detected` - Do not use social users in custom code
* `social.overlays.detected` - Remove social overlays usage
* `social.paths.detected` - Remove social paths after making sure that these paths are not being used in AEM
* `social.resource.type.detected` - Remove social resource type usage
* `social.usage` - Remove social APIs from custom code.