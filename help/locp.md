---
title: LOCP
description: Pattern Detector code help page
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
---
# LOCP {#locp}

/libs Overwriting Custom Packages

## Background {#background}

`LOCP` identifies the detection of a custom package that delivers content to `/libs`, which is an anti-pattern (except in the case ACLs).

## Possible implications and risks {#implications-and-risks}

* The customer code might be deleted or replaced for any CFP, SP or major AEM upgrade.
* In some cases the new content might not be installed properly.

## Possible solutions {#solutions}

* Customer packages should deploy content to `/apps` instead of `/libs`.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
