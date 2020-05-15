---
title: ECU
seo-title: ECU
description: null
seo-description: null
uuid: c4eb958c-08f6-4e1d-a6b0-3aad4c9319bf
contentOwner: sarchiz
discoiquuid: 4033b736-0640-416a-920f-888c3f41d70b
noindex: true
nosnippets: true
index: n
internal: n
snippet: y
---

# ECU{#ecu}

<table>
<tbody>
<tr>
<td><strong>Pattern code</strong></td>
<td>ECU</td>
</tr>
<tr>
<td><strong>Pattern name</strong></td>
<td>Extraneous Content Usage</td>
</tr>
<tr>
<td><strong>Background</strong></td>
<td><p><strong>Extraneous Content Usage</strong> refers to the pattern where different content areas are used crossing safe boundaries.<br></br>
Content Area Usages</p>
<p>When it comes to <strong>usages</strong> there are many kinds of them:</p>
<p><strong>Reference</strong></p>
<p>It allows to declare any content with <code>sling:resourceType</code> which value will be resolved as path that will be used for rendering the content that references it.</p>
<p><strong>Override</strong></p>
<p>It allows to declare any rendering code (to be used via reference) with <code>sling:resourceSuperType</code> which value will be resolved as path that will be used for rendering the content that references it.</p>
<p><strong>Overlay</strong></p>
<p>The Sling overlay is defined via JCR hierarchy when search paths like <strong>/libs</strong> and <strong>/apps</strong> are configured by default in such way that changes from <strong>/libs</strong> are shadowed by <strong>/apps</strong>.</p>
<p>This means that in example JCR node:</p>
<p><strong>/libs/</strong>aem/component/pageTemplate is shadowed by Sling if <strong>/apps/</strong>aem/component/pageTemplate exist so properties defined in node: <strong>/apps/</strong>aem/component/pageTemplate are taken into account and <strong>/libs/</strong>aem/component/pageTemplate is used as fallback.</p>
<p>This is crucial especially if pageTemplate node is a component and any other component or page references: aem/component/pageTemplate as <code>sling:resourceType</code> or <code>sling:superResourceType</code></p>
<p><strong>Safe boundaries</strong></p>
<p>The boundaries of content are indicated by mixin types. They are defined as follows:</p>
<p><code>/**</code><br></br>
* Defines a node as internal, so that it shouldn't be used as resourceType<br></br>
* nowhere outside the parent path area. It has the same limitations as:<br></br>
* granite:Final but it is even more restrictive for<br></br>
* sling:resourceType.<br></br>
*/<br></br>
 <code>[granite:InternalArea] mixin</code></p>
<p><code>/**</code><br></br>
* Defines a node as final, so that it cannot be overlaid or inherited by<br></br>
* sling:resourceSuperType.<br></br>
*/<br></br>
 <code>[granite:FinalArea] mixin</code></p>
<p><code>/**</code><br></br>
* Defines a node as abstract, so that it can only be overlaid or inherited by<br></br>
* sling:resourceSuperType but it should not or cannot be used<br></br>
* directly by sling:resourceType.<br></br>
*/<br></br>
 <code>[granite:AbstractArea] mixin</code></p>
<p><code>/**</code><br></br>
* Defines a node as public, so that it can be overlaid, inherited or used<br></br>
* The node can be used in both:<br></br>
* <br></br>
* sling:resourceSuperType or<br></br>
* sling:resourceType<br></br>
* <br></br>
*/<br></br>
 <code>[granite:PublicArea] mixin</code></p>
</td>
</tr>
<tr><td><strong>Possible implications and risks</strong></td>
<td>
<ul>
<li>Security updates are not effective<br></br>
</li>
<li>The functionality that depends on original component can be broken with shadowed functionality<br></br>
</li>
<li>The AEM upgrade leads to errors and page rendering problems (all or for selective content)</li>
</ul>
</td>
</tr>
<tr>
<td><strong>Possible solutions</strong></td>
<td>
<ul>
<li>Overlay only content that you&#39;re really changing.<br></br>
</li>
<li>Consider adapting changes coming from /libs after AEM upgrades, ServicePack or CumulativeFixPack installations<br></br>
</li>
<li>Avoid overlay as much as possible for restricted content (internal/final) and try to reduce the amount of overlayed content in general due to security problems that might be not effective automatically even after installation of the newest CumulativeFixPack<br></br>
</li>
</ul>
</td>
</tr>
</tbody>
</table>
