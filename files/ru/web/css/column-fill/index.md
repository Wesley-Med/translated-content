---
title: column-fill
slug: Web/CSS/column-fill
translation_of: Web/CSS/column-fill
---
<div>{{CSSRef("CSS Multi-columns")}}</div>

<p>Свойство <code>column-fill </code>применяется к родительскому элементу, разбитому на столбцы и указывает как содержимое располагается внутри столбца (column). Если значение свойства <code>column-fill</code> установлено как balanced, то содержимое во всех столбцах будет иметь одинаковую высоту. В случае использования значения <code>auto</code>, содержимое занимает столько пространства сколько ему потребуется.</p>

<p>{{cssinfo}}</p>

<h2 id="Синтаксис">Синтаксис</h2>

<pre class="brush: css">column-fill: auto;
column-fill: balance;

/* Значения по умолчанию */
column-fill: inherit;
column-fill: initial;
column-fill: unset;
</pre>

<h3 id="Значения">Значения</h3>

<dl>
 <dt><code>auto</code></dt>
 <dd>Высота столбцов не контролируется.</dd>
 <dt><code>balance</code></dt>
 <dd>Разделяет содержимое на равные по высоте столбцы.</dd>
</dl>

<h3 id="Возможные_значения">Возможные значения</h3>

{{csssyntax}}

<h2 id="Примеры">Примеры</h2>

<pre class="brush:css; highlight=[4]">.content-box {
  column-count: 4;
  column-rule: 1px solid black;
  column-fill: balance;
  height: 200px;
}
</pre>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Поддержка_браузерами">Поддержка браузерами</h2>

<p>{{Compat}}</p>