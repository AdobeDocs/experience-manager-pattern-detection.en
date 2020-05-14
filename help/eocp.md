---
title: EOCP
seo-title: EOCP
description: null
seo-description: null
uuid: d5148d06-a4d8-4961-884c-fbdeb0bf6cfa
contentOwner: sarchiz
discoiquuid: 97309437-073a-4558-b94f-dad8f343b39d
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# EOCP{#eocp}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>EOCP</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>/etc Overwriting Custom Packages</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td>Custom packages that delivers changes to Adobe clientlibs or out of the box templates in /etc is anti-pattern. Hardly ever the clientlib modified partially can work properly after upgrade.</td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li>The customer code from client lib might be deleted or replaced for any CFP, SP or major AEM upgrade.<br /> </li>
     <li>In some cases the new client libs with customer client libs changes might not work at all</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>
    <ul>
     <li>Copy templates into a separate structure<br /> </li>
     <li>Extension Points</li>
    </ul> </td>
  </tr>
 </tbody>
</table>

