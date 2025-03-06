---
title: SCR
description: Pattern Detector code help page.
---
# SCR {#scr}

## Background {#background}

SIF identifies AEM Screens usage that is incompatible with AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possible solutions {#solutions}

Find the possible solutions for the different subtypes below:

* `screens.bundles.detected` - These bundles will be uninstalled during the upgrade.
* `screens.packages.detected` - These packages will be deleted during the upgrade.
* `screens.packages.dependency` - Remove any dependency on Screens from your custom packages.
* `screens.configs.detected` - Make sure you are not using any Screens config properties in your custom code.
* `screens.users.detected` - Make sure you are not using Screens service users in custom code.
* `screens.paths.detected` - Remove Screens paths after making sure that they are not being used in AEM.
* `screens.resource.type.detected` - Remove Screens resource type usage.
* `screens.usage` - Remove Screens APIs from your custom code.