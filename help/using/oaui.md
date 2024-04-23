---
title: OAUI
description: Pattern Detector code help page..
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
---
# OAUI {#oaui}

OAuth Users Instance

## Background {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance"
>abstract="OAUI code identifies the pattern where there is at least one OAuth-related configured user that requires correct migration. OAuth is configured for users when there is a subnode named oauth directly under a rep:AuthorizableId node in the form of /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Release Notes"

OAUI identifies the pattern where there is at least one OAuth-related configured user that requires correct migration.

OAuth is configured for users when there is a subnode named `oauth` directly under a `rep:AuthorizableId` node in the form of `/home/user-path/user-node/oauth`.

An example is: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possible implications and risks {#implications-and-risks}

* External users configured with OAuth are unable to log in on author/publish instances until they are reconfigured with the below procedure.

## Possible solutions {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Implementation Guidance"
>abstract="External users configured with OAuth are unable to log in on author/publish instances until they are reconfigured to be compatible with AEM as a Cloud Service. AEM as a Cloud Service offers IMS authentication support only for Author, Admin, and Dev users and SAML-based integration for the publish environments. Contact Adobe Support for help or clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="IMS Support - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="SAML Integration - Publish"

* Contact your Adobe representative if you must discuss options for user migration.
* Contact the [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) for clarifications or to have concerns addressed.
