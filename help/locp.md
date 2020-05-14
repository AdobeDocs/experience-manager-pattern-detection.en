---
title: LOCP
seo-title: LOCP
description: null
seo-description: null
uuid: 396fed3e-9938-4cd1-983c-68baba52c2f8
contentOwner: sarchiz
discoiquuid: ffeb6d3f-da85-4fce-8128-9a733001616b
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# LOCP{#locp}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>LOCP</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>/libs Overwriting Custom Packages</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td>Custom packages that delivers content to /libs is anti-pattern (except ACLs). Customer should be able to deploy the same things under /apps.</td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li>The customer code might be deleted or replaced for any CFP, SP or major AEM upgrade.<br /> </li>
     <li>In some cases the new content might not be installed properly.</li>
    </ul> </td>
  </tr>
 </tbody>
</table>

