---
title: OSGICM
seo-title: OSGICM
description: null
seo-description: null
uuid: c72dc46a-27da-4a54-a17f-449acb672c7f
contentOwner: sarchiz
discoiquuid: 16cb96d7-7981-4df9-b1f5-07d2f20c167f
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# OSGICM{#osgicm}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>OSGICM<br /> </td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>OSGi Config Misconfiguration</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td>Customer changed or removed some OSGi configs that are essential after upgrade</td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>Sample content that is insecure on production can be installed automatically on next upgrade due to runmode setting</td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>Bring back the config and inform customers about a new strategy for paths generated for new users</td>
  </tr>
 </tbody>
</table>

