---
title: Selection.extend()
slug: Web/API/Selection/extend
---
<div>
<div>
<div>{{ ApiRef("DOM") }}{{SeeCompatTable}}</div>
</div>
</div>

<p> <strong><code>Selection.extend()</code></strong> 方法移动选中区的焦点到指定的点。选中区的锚点不会移动。选中区将从锚点开始到新的焦点，不管方向。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><em>sel</em>.extend(<em>node</em>, <em>offset</em>)
</pre>

<h3 id="Parameters">参数</h3>

<dl>
 <dt><em>node</em></dt>
 <dd>焦点会被移至此节点内。</dd>
 <dt><em>offset</em> {{optional_inline}}</dt>
 <dd>焦点会被移至 <code>node</code> 内的偏移位置。如果没有指定，使用 <code>0</code> 作为默认值。</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

{{Compat("api.Selection.extend")}}

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{domxref("Selection")}}, 此方法所属接口。</li>
</ul>