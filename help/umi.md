---
title: UMI
description: Pattern Detector code help page
feature: Developer Tools
role: Developer
---

# UMI {#umi}

Upgrade Misconfiguration Issue

## Background {#background}

`UMI` identifies modifications to certain OSGi configurations that will cause issues when upgrading, including a failed upgrade or reduced functionality.

The following configurations are checked for modification:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Possible implications and risks {#implications-and-risks}

* Changing or removing configurations may cause below issues:
  * Upgrade may get stuck (for example `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` was missing but present in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
  * Authorization issues may come after upgrade (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
  * Certain functionality may not work as expected. For example changing `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` may result in some JSP files not being compiled, which ultimately will result in loss of functionality.

## Possible solutions {#solutions}

* Do not change or remove the four configurations mentioned above.
* If configurations have been changed, they should be restored to their expected values. These values are indicated in the `UMI` messages.
* Please reach out to our [AEM Support Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) to get clarifications or to address concerns.
