---
title: Screen
slug: Web/API/Screen
---
<div>{{APIRef("CSSOM View")}}</div>

<p><code>Screen</code> 接口表示一个屏幕窗口，往往指的是当前正在被渲染的 window 对象，可以使用 <code>window.screen</code> 获取它。</p>

<p>请注意：由浏览器决定提供屏幕对象，此对象一般通过当前浏览器窗口活动状态动态检测来得到。</p>

<h2 id="Example">属性</h2>

<dl>
 <dt>{{domxref("Screen.availTop")}}</dt>
 <dd>Specifies the y-coordinate of the first pixel that is not allocated to permanent or semipermanent user interface features.</dd>
 <dt>{{domxref("Screen.availLeft")}}</dt>
 <dd>返回屏幕左边边界的第一个像素点</dd>
 <dt>{{domxref("Screen.availHeight")}}</dt>
 <dd>Specifies the height of the screen, in pixels, minus permanent or semipermanent user interface features displayed by the operating system, such as the Taskbar on Windows.</dd>
 <dt>{{domxref("Screen.availWidth")}}</dt>
 <dd>返回窗口中水平方向可用空间的像素值。</dd>
 <dt>{{domxref("Screen.colorDepth")}}</dt>
 <dd>返回屏幕的色彩深度。</dd>
 <dt>{{domxref("Screen.height")}}</dt>
 <dd>以像素为单位返回屏幕的高度。</dd>
 <dt>{{domxref("Screen.left")}}</dt>
 <dd>返回从最左边界到当前屏幕的像素值。</dd>
 <dt>{{domxref("Screen.orientation")}}</dt>
 <dd>返回当前屏幕的转向。</dd>
 <dt>{{domxref("Screen.pixelDepth")}}</dt>
 <dd>获取屏幕的像素点</dd>
 <dt>{{domxref("Screen.top")}}</dt>
 <dd>返回最上边界到当前屏幕的像素值。</dd>
 <dt>{{domxref("Screen.width")}}</dt>
 <dd>返回屏幕的宽度。</dd>
 <dt>{{domxref("Screen.mozEnabled")}}</dt>
 <dd>布尔值。如果设置为 false 将关闭设备的屏幕。</dd>
 <dt>{{domxref("Screen.mozBrightness")}}</dt>
 <dd>控制设备屏幕的亮度。期望参数是 0-1.0 之间的浮点数。</dd>
</dl>

<h3 id="Events_handler">Events handler</h3>

<dl>
 <dt>{{domxref("Screen.onorientationchange")}}</dt>
 <dd>对{{event("orientationchange")}} 事件的时间处理器。</dd>
</dl>

<h2 id="方法">方法</h2>

<dl>
 <dt>{{domxref("Screen.lockOrientation")}}</dt>
 <dd>锁定屏幕转向 (仅在全屏或者已安装的 APP 中生效)</dd>
 <dt>{{domxref("Screen.unlockOrientation")}}</dt>
 <dd>解锁屏幕转向 (仅在全屏或者已安装的 APP 中生效)</dd>
</dl>

<p>方法继承于 {{domxref("EventTarget")}}</p>

<p>{{page("/en-US/docs/Web/API/EventTarget","Methods")}}</p>

<h2 id="Example">示例</h2>

<pre class="brush:js">if (screen.pixelDepth &lt; 8) {
  // use low-color version of page
} else {
  // use regular, colorful page
}
</pre>

<h2 id="Specification">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>