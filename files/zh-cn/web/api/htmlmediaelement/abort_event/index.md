---
title: 'HTMLMediaElement: abort event'
slug: Web/API/HTMLMediaElement/abort_event
---
<div>{{APIRef}}</div>

<p>资源没有被完全加载时就会触发 <strong><code>abort</code></strong> 事件，但错误不会触发该事件。</p>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row">Bubbles</th>
   <td>No</td>
  </tr>
  <tr>
   <th scope="row">Cancelable</th>
   <td>No</td>
  </tr>
  <tr>
   <th scope="row">Interface</th>
   <td>{{domxref("Event")}}</td>
  </tr>
  <tr>
   <th scope="row">Event handler property</th>
   <td>{{domxref("GlobalEventHandlers/onabort", "onabort")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="示例">示例</h2>

<pre class="brush: js">const video = document.querySelector('video');
const videoSrc = 'https://path/to/video.webm';

video.addEventListener('abort', () =&gt; {
  console.log(`Abort loading: ${videoSrc}`);
});

const source = document.createElement('source');
source.setAttribute('src', videoSrc);
source.setAttribute('type', 'video/webm');

video.appendChild(source);</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.HTMLMediaElement.abort_event")}}</p>

<h2 id="参阅">参阅</h2>

<ul>
 <li>{{domxref("HTMLAudioElement")}}</li>
 <li>{{domxref("HTMLVideoElement")}}</li>
 <li>{{HTMLElement("audio")}}</li>
 <li>{{HTMLElement("video")}}</li>
</ul>