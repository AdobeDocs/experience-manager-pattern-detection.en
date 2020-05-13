---
title: DADS
seo-title: DADS
description: null
seo-description: null
uuid: 17482f78-3d64-4bde-a0fc-4726cb0ddcdd
contentOwner: sarchiz
discoiquuid: 044ba956-d370-41e7-99db-21204836c427
noindex: true
nosnippets: true
index: y
internal: n
snippet: y
---

# DADS{#dads}

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td> 
   <td>DADS</td> 
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td> 
   <td>Duplicated Active Data Stores</td> 
  </tr>
  <tr>
   <td><strong>Background</strong></td> 
   <td>For some repositories FileDataStore vs S3DataStore might be activated at<br /> the same time (both configs might exist) which then after/during <br /> upgrade this might cause a serious problem.</td> 
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td> 
   <td>The AEM upgrade leads to errors (not related and it is easy to debug <strong>after</strong> the fact)</td> 
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td> 
   <td>Remove the outdated configuration that might be still presrnt in OSGi config console or under Felix launchpad directory</td> 
  </tr>
 </tbody>
</table>

