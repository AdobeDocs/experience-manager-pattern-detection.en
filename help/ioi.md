---
title: IOI
seo-title: IOI
description: null
seo-description: null
uuid: d6c53c0d-c493-41f3-9345-76fc06266118
contentOwner: sarchiz
discoiquuid: 2d40b93e-e814-4129-b213-af692014b4f5
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# IOI{#ioi}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>IOI</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>Internal Oak Import</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td><p>The customer uses internal Oak packages importing them via OSGi. They are in majority exported without any particular version and they are intended to be consumed mostly by other Oak bundles or low level AEM services.</p> <p>Some of them are used by <code>com.adobe.granite.repository</code> which sets up a repository for AEM during startup.</p> <p>The same example is for <code>com.adobe.granite.maintenance.oak</code> Adobe bundle which wraps and provides Oak maintenance tasks</p> </td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li> In a future versions internal exports might be removed causing broken dependencies and inactive bundles depending directly on Oak<br /> </li>
     <li>API in internal exports might change</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>
    <ul>
     <li> Use Sling Resource/JCR API where possible (this is an API)<br /> </li>
     <li>Avoid depending on internal packages that might be implementation-related (they are not part of any public API or SPI)</li>
    </ul> </td>
  </tr>
 </tbody>
</table>

