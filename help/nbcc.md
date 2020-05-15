---
title: NBCC
description: null
uuid: 0e920e8a-2cff-4d2d-8b3b-1e061c1a1be0
contentOwner: sarchiz
discoiquuid: a9f9a349-c287-4e1c-b1d4-4a59f6a782e7
---

# NBCC{#nbcc}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>NBCC</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>Non-Backwards Compatible Changes</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td>Some JCR nodes or bundles are changed in a non-compatible way, but customer might be not aware of that before upgrade.</td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li> The functionality that depends on component that uses non-backward compatible changes can be broken and might not resolve correctly<br /> </li>
     <li>Some features of customer application (and in some cases AEM functionalities) after upgrade might not work correctly</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>
    <ul>
     <li> Overlay or reference only Sling components that are backwards compatible<br /> </li>
     <li>Consider resources needed for adapting changes coming from /libs or bundles after AEM upgrades</li>
    </ul> </td>
  </tr>
 </tbody>
</table>

