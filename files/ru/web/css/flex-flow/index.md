---
title: flex-flow
slug: Web/CSS/flex-flow
translation_of: Web/CSS/flex-flow
---
<div>{{ CSSRef}}</div>

<p><strong><code>flex-flow</code></strong> <a href="/en-US/docs/CSS" title="CSS">CSS</a> свойство, которое является сокращением для отдельных свойств <code>flex-direction</code> и <code>flex-wrap</code>.</p>

<pre class="brush:css no-line-numbers">/* flex-flow: &lt;'flex-direction'&gt; */
flex-flow: row;
flex-flow: row-reverse;
flex-flow: column;
flex-flow: column-reverse;

/* flex-flow: &lt;'flex-wrap'&gt; */
flex-flow: nowrap;
flex-flow: wrap;
flex-flow: wrap-reverse;

/* flex-flow: &lt;'flex-direction'&gt; and &lt;'flex-wrap'&gt; */
flex-flow: row nowrap;
flex-flow: column wrap;
flex-flow: column-reverse wrap-reverse;

/* Global values */
flex-flow: inherit;
flex-flow: initial;
flex-flow: unset;
</pre>

<p>{{cssinfo}}</p>

<p>Больше информации и свойств описано в <a href="/en-US/docs/CSS/Using_CSS_flexible_boxes" title="/en-US/docs/CSS/Using_CSS_flexible_boxes">Using CSS flexible boxes</a>.</p>

<h2 id="Синтаксис">Синтаксис</h2>

<h3 id="Значения">Значения</h3>

<p>Смотрите <a href="/en-US/docs/CSS/flex-direction" title="en-US/docs/CSS/flex-direction"><code>flex-direction</code></a> и <a href="/en-US/docs/CSS/flex-wrap" title="flex-wrap"><code>flex-wrap</code></a>.</p>

<h3 id="Формальный_синтаксис">Формальный синтаксис</h3>

{{csssyntax}}

<h2 id="Примеры">Примеры</h2>

<pre class="brush:css">element {
  /* Main-axis is the block direction with reversed main-start and main-end. Flex items are laid out in multiple lines */
  flex-flow: column-reverse wrap;
}
</pre>

<h2 id="Specifications">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость_с_браузерами">Совместимость с браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li><a href="/en-US/docs/CSS/Using_CSS_flexible_boxes" title="/en-US/docs/CSS/Using_CSS_flexible_boxes">Using CSS flexible boxes</a></li>
</ul>