---
title: document.width
slug: Web/API/Document/width
---
<div>{{ApiRef}} {{deprecated_header}}</div>
<div class="note">
 <p>从 Gecko 6.0 开始，<code>不再支持 document.width，请使用</code><code>document.body.clientWidth</code>来代替。查看{{domxref("element.clientWidth")}}.</p>
</div>
<h2 id="Summary">概述</h2>
<p>返回当前文档中的{{HTMLElement("body")}}元素的宽度，单位为像素.Internet Explorer 不支持该属性。</p>
<h2 id="Syntax">语法</h2>
<pre class="syntaxbox"><em>pixels</em> = document.width;
</pre>
<h2 id="Example">示例</h2>
<pre class="brush:js">function init() {
    alert("当前文档的宽度为 " + document.width + " 像素.");
}
</pre>
<h2 id="Alternatives">请使用下面的属性来替代该属性</h2>
<pre class="syntaxbox">document.body.clientWidth              /* &lt;body&gt;元素的宽度 */
document.documentElement.clientWidth   /* &lt;html&gt;元素的宽度 */
window.innerWidth                      /* window 的宽度 */
</pre>
<h2 id="Specification">规范</h2>

<p>HTML5</p>

<h2 id="See_also">相关链接</h2>
<ul>
 <li>{{domxref("document.height")}}</li>
</ul>