---
title: AC
description: Pattern Detector code help page.
exl-id: 4c6ac075-5ba6-4511-97c6-a9b496d4677a
---
# AC {#ac}

## Background {#background}

AC identifies Assets bundle usage that is incompatible with AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possible solutions {#solutions}

Find the possible solutions for the different subtypes below:

* `asset.bundles.detected` - This bundle will be uninstalled during the upgrade.
* `asset.usage` - Remove any Asset Rating and Asset catalog component dependencies from custom code. Where applicable, change the code to use new API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected` - Overlays created on Assets Rating and Catalog components need to be removed.
* `asset.resource.type.detected` - Remove any usage of the Assets rating component resourcetype in your custom code.
* `asset.paths.detected` - Move any customer content present under these paths and remove these paths after making sure that they are not being used in AEM.
