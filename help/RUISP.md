---
title: RUISP
seo-title: RUISP
description: null
seo-description: null
uuid: 6c1dc379-5613-475f-97fd-25feee89d4c2
contentOwner: sarchiz
discoiquuid: 35183b83-76c2-404b-b80f-8ec1d8c281aa
noindex: true
nosnippets: true
index: y
internal: n
snippet: y
---

# RUISP{#ruisp}

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td> 
   <td>RUISP</td> 
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td> 
   <td>Resources Under Invalid Search Path</td> 
  </tr>
  <tr>
   <td><strong>Background</strong></td> 
   <td>Components defined under a Sling search path that is no longer present might not be available at all or might be available under a different resource type ID.<br /> </td> 
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td> 
   <td>Missing functionality of affected components (not available for other components)</td> 
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td> 
   <td>Migrate and move components from <span class="code">/apps/foundation/components/primary</span> to <span class="code">/apps</span></td> 
  </tr>
 </tbody>
</table>

