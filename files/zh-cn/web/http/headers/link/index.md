---
title: Link
slug: Web/HTTP/Headers/Link
translation_of: Web/HTTP/Headers/Link
---
<p>{{HTTPSidebar}}</p>

<p>HTTP 实体报头 <strong><code>Link</code></strong> 提供了序列化 HTTP 头部链接的方法。它在语义上与 HTML 元素 {{HTMLElement("link")}} 相等。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">Link: &lt; <var>uri-reference</var> &gt;; <var>param1</var>=<var>value1</var>; <var>param2</var>="<var>value2</var>"</pre>

<dl>
 <dt><code>&lt;uri-reference&gt;</code></dt>
 <dd>URI reference 必须要用 <code>&lt;</code> 和 <code>&gt;</code>来关闭。</dd>
</dl>

<h3 id="参数">参数</h3>

<p>link 头部包含以 <code>;</code> 分隔的参数，这些参数与 HTML 元素 {{HTMLElement("link")}} 的属性一致。</p>

<h2 id="示例">示例</h2>

<p>URI 必须要用 <code>&lt;</code> 和 <code>&gt; 来关闭：</code></p>

<pre class="brush: http; example-good">Link: &lt;https://example.com&gt;; rel="preload"</pre>

<pre class="brush: http; example-bad">Link: https://bad.example; rel="preload"</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li>{{HTTPStatus(103, "103 Early Hints")}}</li>
</ul>