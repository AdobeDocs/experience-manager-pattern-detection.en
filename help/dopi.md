---
title: DOPI
description: null
uuid: 66a16462-11a2-483e-a5a0-b3405fa8fc20
contentOwner: sarchiz
discoiquuid: 12a82fbd-39ec-4690-aa34-bb3a53e89a03
---

# DOPI{#dopi}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>DOPI</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td><strong>D</strong>eprecated "<strong>O</strong>rdered" <strong>P</strong>roperty <strong>I</strong>ndex</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td><p>Ordered property index definitions (primaryType=oak:QueryIndexDefinition AND type="ordered") have been deprecated since 6.1 and were removed in 6.2.</p> <p>If such indices are used they need to be migrated to a supported (Lucene based) definition (by either modifying an existing definition OR by adding a new one) to address the queries that required that index.</p> </td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li>No response from some queries</li>
     <li>Customer functionality might work incorrectly</li>
     <li>Traversal warnings or even errors and a significant performance penalties as the indices cannot be used anymore<br /><br /> </li>
    </ul> </td>
  </tr>
 </tbody>
</table>

