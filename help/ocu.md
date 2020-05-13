---
title: OCU
seo-title: OCU
description: null
seo-description: null
uuid: 4ea1b9ad-5161-4d08-83b9-fb42b9df9dfa
contentOwner: sarchiz
discoiquuid: 8338635d-7c98-4635-b64f-5fc98e500f51
noindex: true
nosnippets: true
index: y
internal: n
snippet: y
---

# OCU{#ocu}

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td> 
   <td>OCU</td> 
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td> 
   <td>Outdated Code Usage</td> 
  </tr>
  <tr>
   <td><strong>Background</strong></td> 
   <td><p>Some JCR nodes like Sling or AEM components or API OSGi exports are changed or removed in a non-compatible way, but customer might be not aware of that before upgrade. They might be upgraded to a non-compatible version or can be not available at all.</p> <p>As the old versions are not installed by default, the customer application might not work correctly.</p> </td> 
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td> 
   <td>
    <ul> 
     <li> The functionality that depends on component that uses deprecated components or APIs can be broken and might not resolve correctly after upgrade<br /> </li> 
     <li>Some features of customer application (and in some cases AEM functionalities) after upgrade might not work correctly or might not be active</li> 
    </ul> </td> 
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td> 
   <td>
    <ul> 
     <li> Short-term: Installation of compatibility package might help<br /> </li> 
     <li>Long-term: adapting customer code for the newest version of AEM components or APIs</li> 
    </ul> </td> 
  </tr>
 </tbody>
</table>

