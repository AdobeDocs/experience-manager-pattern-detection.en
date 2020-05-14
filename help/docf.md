---
title: DOCF
seo-title: DOCF
description: null
seo-description: null
uuid: f8f108dd-f2d2-4837-ab3b-67a3ed16e507
contentOwner: sarchiz
discoiquuid: 3848f502-c03e-4f07-83cf-246c949f111a
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# DOCF{#docf}

<table border="1" cellpadding="1" cellspacing="0" width="100%">
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>DOCF</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>Duplicated OSGi Config Format</td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li> The AEM upgrade leads to errors (not related and it is easy to debug after the fact)<br /> </li>
     <li>Changed applied to one file are not visible due to 2nd outdated file being present (shadowing updated versions) - a lot of time might be wasted debugging the not effective configuration state</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>Remove one of the configuration file that is outdated and migrated if needed to a newer format version</td>
  </tr>
 </tbody>
</table>

