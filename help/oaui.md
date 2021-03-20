---
title: OAUI
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# OAUI {#oaui}

OAuth Users Instance

## Background {#background}

`OAUI` identifies the pattern where there is at least one OAuth-related configured user that requires correct migration.

OAuth is configured for users when there is a subnode named `oauth` directly under a `rep:AuthorizableId` node in the form of `/home/user-path/user-node/oauth`.

An example is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possible implications and risks {#implications-and-risks}

* External users configured with OAuth won't be able to login on author/publish instances until they are reconfigured with the below procedure.

## Possible solutions {#solutions}

* Contact your Adobe representative to discuss options for user migration.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
