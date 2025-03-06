---
title: SPI
description: Pattern Detector code help page.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
---
# SPI {#spi}

## Background {#background}

SIF identifies Search and Promote usage that is incompatible with AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possible solutions {#solutions}

Find the possible solutions for the different subtypes below:

* `searchpromote.bundles.detected` - These bundles will be uninstalled during the upgrade
* `earchpromote.packages.detected` - These packages  will be deleted during the upgrade
* `searchpromote.packages.dependency` - Remove any Search and Promote dependency your custom packages might have
* `searchpromote.usage` - Remove Search and Promote APIs from your custom code
* `searchpromote.users.detected` - Do not use Search and Promote service users in custom code
* `searchpromote.configs.detected` - Do not use Search and Promote config properties in your custom code.
