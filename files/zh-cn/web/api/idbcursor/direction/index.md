---
title: IDBCursor.direction
slug: Web/API/IDBCursor/direction
---
<p>{{ APIRef("IDBCursor") }}</p>
<div>
 <p>{{domxref("IDBCursor")}} 的方向属性是一个 {{domxref("DOMString")}} ，表示游标遍历的方向， (比如可以通过 {{domxref("IDBObjectStore.openCursor")}} 设置). 查看下文中<a href="#取值">取值</a>章节获取可取值。</p>
</div>
<h2 id="语法">语法</h2>
<pre class="brush: js" style="font-size: 14px;">cursor.direction;</pre>
<h3 id="取值">取值</h3>
<p>用一个字符串 (defined by the <a href="https://dvcs.w3.org/hg/IndexedDB/raw-file/default/Overview.html#idl-def-IDBCursorDirection"><code>IDBCursorDirection</code> enum</a>) 表示游标的遍历方向。相关取值如下表所示：</p>
<table>
 <thead>
  <tr>
   <th scope="col">Value</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>next</code></td>
   <td>从数据源开始位置遍历</td>
  </tr>
  <tr>
   <td><code>nextunique</code></td>
   <td>
    <p> </p>
    <p>从数据源开始遍历；当取值有重复时，只获取一次。</p>
   </td>
  </tr>
  <tr>
   <td><code>prev</code></td>
   <td>
    <p>从数据源的最后位置位置开取值</p>
   </td>
  </tr>
  <tr>
   <td><code>prevunique</code></td>
   <td>从数据源的最后位置开始取值，只获取一次。<br>
     </td>
  </tr>
 </tbody>
</table>
<h2 id="例子">例子</h2>
<p>在这个简单的例子中，我们首先创建一个事物对象，返回一个对象仓库 (store), 然后使用邮编遍历整个数据仓库。在每次迭代中我们记录了游标的方向，例如 prev（倒序遍历）</p>
<pre class="language-html" style="padding: 1em 0px 1em 30px; font-size: 14px; color: rgb(77, 78, 83);"><code class="language-html" style="font-family: Consolas, Monaco, 'Andale Mono', monospace; direction: ltr;">prev</code></pre>
<div class="note">
 <p><strong>注意</strong>：我们不能改变游标的取值，因为这是个只读属性；应该在{{domxref("IDBObjectStore.openCursor")}}方法调用的第二个参数指定游标遍历的方向；</p>
</div>
<p>使用游标遍历数据时，可以不需要我们指定在特定字段选择数据；我们可以直接获取所有数据，同时在每次循环迭代过程当中，我们可以通过 cursor.value.foo 获取数据，如下是一个完整的游标遍历数据的例子； <a href="https://github.com/mdn/IDBcursor-example/">IDBCursor example</a> (<a href="http://mdn.github.io/IDBcursor-example/">view example live</a>.)</p>
<pre class="brush: js">function backwards() {
  list.innerHTML = '';
  var transaction = db.transaction(['rushAlbumList'], 'readonly');
  var objectStore = transaction.objectStore('rushAlbumList');

  objectStore.openCursor(null,'prev').onsuccess = function(event) {
    var cursor = event.target.result;
      if(cursor) {
        var listItem = document.createElement('li');
        listItem.innerHTML = '&lt;strong&gt;' + cursor.value.albumTitle + '&lt;/strong&gt;, ' + cursor.value.year;
        list.appendChild(listItem);

        console.log(cursor.direction);
        cursor.continue();
      } else {
        console.log('Entries displayed backwards.');
      }
  };
};</pre>
<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>
<div>
{{Compat("api.IDBCursor.direction")}}

<h2 id="sect1"> </h2>
<h2 id="参考资料">参考资料</h2>
<ul>
 <li><a href="/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB">Using IndexedDB</a></li>
 <li>Starting transactions: {{domxref("IDBDatabase")}}</li>
 <li>Using transactions: {{domxref("IDBTransaction")}}</li>
 <li>Setting a range of keys: {{domxref("IDBKeyRange")}}</li>
 <li>Retrieving and making changes to your data: {{domxref("IDBObjectStore")}}</li>
 <li>Using cursors: {{domxref("IDBCursor")}}</li>
 <li>Reference example: <a href="https://github.com/mdn/to-do-notifications/tree/gh-pages">To-do Notifications</a> (<a href="http://mdn.github.io/to-do-notifications/">view example live</a>.)</li>
</ul>