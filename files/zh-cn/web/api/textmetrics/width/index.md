---
title: TextMetrics.width
slug: Web/API/TextMetrics/width
---
<div>{{APIRef("Canvas API")}}</div>

<p>只读的 <code><strong>TextMetrics</strong></code><strong><code>.width</code></strong> 属性，包含文本先前的宽度（行内盒子的宽度），使用 CSS 像素计算。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><var>readonly <em>metrics</em></var>.width;</pre>

<h2 id="示例">示例</h2>

<p>事先给定 {{HTMLElement("canvas")}} 元素：</p>

<pre class="brush: html">&lt;canvas id="canvas"&gt;&lt;/canvas&gt;
</pre>

<p>你可以使用下面的代码得到一个 {{domxref("TextMetrics")}} 对象：</p>

<pre class="brush: js; highlight:[5]">var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");

var text = ctx.measureText("foo"); // TextMetrics object
text.width; // 16;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.TextMetrics.width")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{domxref("TextMetrics")}}</li>
</ul>