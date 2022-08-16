---
title: GlobalEventHandlers.onpointerenter
slug: Web/API/Element/pointerenter_event
---
<div>HTML DOM</div>

<div>pointerenter 事件的 GlobalEventHandlers（全局事件处理函数）</div>

<pre class="brush: js">var <var>enterHandler</var> = <var>targetElement</var>.onpointerenter;
</pre>

<h3 id="返回值">返回值</h3>

<dl>
 <dt><code>enterHandler</code></dt>
 <dd><code>targetElement</code>的 pointerenter 事件处理函数。</dd>
</dl>

<h2 id="例子">例子</h2>

<p>这个例子展示了使用 onpointerenter 来设置元素 pointerenter 事件处理函数的两种方式<em>。</em></p>

<pre class="brush: js">&lt;html&gt;
&lt;script&gt;
function enterHandler(ev) {
 // 处理 pointerenter 事件
}
function init() {
 var el=document.getElementById("target1");
 el.onpointerenter = enterHandler;
}
&lt;/script&gt;
&lt;body onload="init();"&gt;
&lt;div id="target1"&gt; 点我 ... &lt;/div&gt;
&lt;div id="target2" onpointerenter="enterHandler(event)"&gt; 点我 ... &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{ event("pointerenter") }}</li>
</ul>