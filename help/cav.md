---
title: CAV
seo-title: CAV
description: null
seo-description: null
uuid: 2b143dd5-c565-4f8e-a9aa-fbed3319c555
discoiquuid: 74d1a471-e134-489f-a526-5c98755568b4
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# CAV{#cav}

<table>
 <tbody>
  <tr>
   <td><strong>Pattern code</strong></td>
   <td>CAV</td>
  </tr>
  <tr>
   <td><strong>Pattern name</strong></td>
   <td>Content Area Violation</td>
  </tr>
  <tr>
   <td><strong>Background</strong></td>
   <td><p><strong>Content Area Violation</strong> refers to the pattern where different content areas are used crossing safe boundaries.</p> <h2>Content Area Usages</h2> <p>When it comes to <strong>usages</strong> there are many kinds of them:</p> <h3><strong>Reference (usage, inclusion)</strong></h3> <p>It allows to declare any content with <span class="code">sling:resourceType</span> which value will be resolved as path that will be used for rendering the content that references it.</p> <h3><strong>Override</strong></h3> <p>It allows to declare any rendering code (to be used via reference) with <span class="code">sling:resourceSuperType</span> which value will be resolved as path that will be used for rendering the content that references it.</p> <h3><strong>Overlay</strong></h3> <p>The Sling overlay is defined via JCR hierarchy when search paths like <strong>/libs</strong> and <strong>/apps</strong> are configured by default in such way that changes from <strong>/libs</strong> are shadowed by <strong>/apps</strong>.</p> <p>This means that in example JCR node:</p> <p><strong>/libs/</strong>aem/component/pageTemplate is shadowed by Sling if <strong>/apps/</strong>aem/component/pageTemplate exist so properties defined in node: <strong>/apps/</strong>aem/component/pageTemplate are taken into account and <strong>/libs/</strong>aem/component/pageTemplate is used as fallback.</p> <p>This is crucial especially if pageTemplate node is a component and any other component or page references: aem/component/pageTemplate as <span class="code">sling:resourceType</span> or <span class="code">sling:superResourceType</span></p> <h2><strong>Safe boundaries</strong></h2> <p>The boundaries of content are indicated by mixin types. They are defined as follows:</p> <pre><code class="code">/**
* Defines a node as internal, so that it shouldn't be
* used as resourceType nowhere outside the parent path area.
* It has the same limitations as: granite:Final but
* it is even more restrictive for sling:resourceType.
*/

[granite:InternalArea] mixin</code> </pre> <pre><code class="code">/**
* Defines a node as final, so that it cannot be overlaid
* or inherited by sling:resourceSuperType.
*/

[granite:FinalArea] mixin</code> </pre> <pre><code class="code">/**
* Defines a node as abstract, so that it can only be
* <span class="code">overlaid or inherited by </span>sling:resourceSuperType but it
* should not or cannot be used directly by sling:resourceType.
*/

[granite:AbstractArea] mixin</code> </pre> <pre><code class="code">/**
* Defines a node as public, so that it can be overlaid,
* inherited or used. The node can be used in both:
*
* sling:resourceSuperType or
* sling:resourceType
*
*/

[granite:PublicArea] mixin</code> </pre> </td>
  </tr>
  <tr>
   <td><strong>Possible implications and risks</strong></td>
   <td>
    <ul>
     <li>Security updates are not effective<br /><br /> </li>
     <li>The functionality that depends on original component can be broken with shadowed functionality<br /><br /> </li>
     <li>The AEM upgrade leads to errors and page rendering problems (all or for selective content)</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Possible solutions</strong></td>
   <td>
    <ul>
     <li>Overlay only content that you're really changing.<br /><br /> </li>
     <li>Consider adapting changes coming from /libs after AEM upgrades, ServicePack or CumulativeFixPack installations<br /><br /> </li>
     <li>Avoid overlay as much as possible for restricted content (internal/final) and try to reduce the amount of overlayed content in general due to security problems that might be not effective automatically even after installation of the newest CumulativeFixPack<br /><br /> </li>
    </ul> </td>
  </tr>
 </tbody>
</table>

