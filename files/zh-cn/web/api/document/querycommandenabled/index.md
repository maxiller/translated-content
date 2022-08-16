---
title: Document.queryCommandEnabled()
slug: Web/API/Document/queryCommandEnabled
---
<p>{{ApiRef("DOM")}}{{deprecated_header}}</p>

<div class="note">
<p>该方法在部分浏览器返回的结果是不可预料的。因此，建议使用 execCommand 的返回值直接判断，或通过其它方式嗅探，而非使用该方法。</p></div>

<p><code><strong>Document.queryCommandEnabled()</strong></code> 方法可查询浏览器中指定的编辑指令是否可用。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>var isEnabled</var> = document.queryCommandEnabled(<var>command</var>);
</pre>

<dl>
 <dt>
 <h3 id="参数">参数</h3>
 </dt>
 <dt><code>command</code></dt>
 <dd>待查询的是否可用的指令。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>返回 {{jsxref("Boolean")}} 值，<code>true</code> 表示指令可用，<code>false</code>表示指令不可用。</p>

<h2 id="备注">备注</h2>

<ul>
 <li>经过测试，在部分浏览器它永远返回 <code>false</code>，而 IE 浏览器即使对于同样支持的属性也可能有不同返回值；有时 IE 还会对不支持的属性抛出异常而不是返回 <code>false</code>。</li>
 <li>对于 <code>"cut"</code> 和 <code>"copy"</code> 指令，只有当用户启动的线程调用该方法时才返回 true。</li>
 <li><code>"paste"</code> 指令不仅当特性不可用时返回 <code>false</code> ，脚本权限不足时也一样。</li>
</ul>

<h2 id="示例">示例</h2>

<pre class="brush:js">var flg = document.queryCommandEnabled("SelectAll");

if(flg) {
  document.execCommand("SelectAll", false, null); // command is enabled, run it
}
</pre>

<h2 id="规范">规范</h2>

<p>此特性不属于任何规范，也不再有望被标准化。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<div>{{Compat}}</div>

<h2 id="参考资料">参考资料</h2>

<ul>
 <li>{{domxref("Document.execCommand()")}}</li>
 <li>{{domxref("Document.queryCommandSupported()")}}</li>
</ul>