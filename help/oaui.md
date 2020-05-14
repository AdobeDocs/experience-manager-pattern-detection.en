---
title: OAUI
seo-title: OAUI
description: null
seo-description: null
uuid: a33ac39c-8668-4526-8a5a-030d5302a616
discoiquuid: 74c31255-ee10-4804-8f65-c472cef3442c
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# OAUI{#oaui}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>OAUI</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>OAuth Users Instance<br /><br /> </td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td><p><strong>OAuth Users Instance</strong> refers to the pattern where there is at least one OAuth-related configured user.</p> <p>OAuth is configured for users when there is a subnode called exactly: <strong>oauth</strong> directly under node rep:AuthorizableId</p> <p><strong>/home/</strong>user-path/user-node<strong>/oauth</strong></p> <p>Example:</p> <p><strong>/home/users/</strong>ims/0001/R80w6XaUCBq3jHE47xDN<strong>/oauth</strong></p> </td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li>External users configured with OAuth won't be able to login on author/publish instances until they are reconfigured with the below procedure</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>
    <ul>
     <li>Use a procedure delivered by Adobe by using oak run with the attached groovy script.</li>
     <li>Please test the procedure on your development, test and staging instances first.</li>
     <li>Use our guidelines in (link to OAuth users migration procedure page)</li>
    </ul> </td>
  </tr>
 </tbody>
</table>

