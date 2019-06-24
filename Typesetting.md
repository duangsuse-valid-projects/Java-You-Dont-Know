# Standard HTML5 inline tag tests

## Development: Markdown Inline Typesetting tests 内联排版测试

### Standard HTML 4

#### 表格

##### 无序表

<ul>
  <li>列表项</li>
</ul>

##### 有序表

<ol>
  <li>列表项</li>
</ol>

##### Table & `<style>`

<style>
.outline table, .outline th, .outline td {
  border: 1px solid black;
}
</style>

<table class="outline" summary="summary" cellspacing="0" cellpanding="0">
  <caption>caption</caption>
  <thead></thead>
    <tr>
      <td>A</td>
      <td>B</td>
    </tr>
  <tbody>
    <tr>
      <td>1</td>
      <td>2</td>
    </tr>
  </tbody>
</table>

##### Abbreviation (replaces `<acronym>`)

<abbr title="title">inner html</abbr>

#### 文字风格

<p id="typesetting-text">
  <h6>Header 7</h6>
  <kbd>Enter</kbd> Key
  <br><i>Italic</i> text
  <br><var>Variable</var> text <br>f(<var>x</var>) = <var>x</var><sup>2</sup>
  <br><b>Bold</b> text
  <br><strong>Strong</strong> text
  <br><em>Emphasized</em> text
  <br><small>Small</small> text
  <br><big>Big</big> text, not supported in HTML5
  <br><code>Computer code</code>
  <br><samp>Sample output</samp>
  <br><bdo dir="rtl">你好世界</bdo> bdo rtl
  <br><bdi>إيان</bdi> Bi directional (HTML 5)
  <br><mark>Mark</mark>up (H5)
  <br><del>Del eted</del>
  <br><ins>Ins</ins>erted
  <br><u>u</u>nderlined
  <br><s>ThreadDeath</s> &lt;/s&gt;
  <br>天依色 <span style="color:#66ccff">0w0</span>
  <br>To write good Java IO code, try java.<wbr>io.<wbr>InputStream interface. &lt;wbr&gt;
</p>

<template>
  <h2>Flower</h2>
  <img src="">
</template>

<blockquote cite="https://www.w3schools.com/tags/tag_blockquote.asp">
  <p>Long blockquote</p>
  <footer>—— duangsuse</footer>
</blockquote>

<pre>
Text in a pre element
is displayed in a fixed-width
font, and it preserves
both      spaces and
line breaks
</pre>

<q>quotation</q>

<center>cvalign, <del>HTML 5</del></center>

<cite id="mrII">The Book 《Metaprogramming Ruby II》</cite> `<cite>`

<p>dfn <dfn id="html-def" title="HyperText Markup Language">HTML</dfn> is the standard markup language for creating web pages.</p>

<p>Learn <a href="#html-def">HTML</a> now.</p>

#### Rich media

<picture>
  <source media="(min-width: 650px)" srcset="resources/images/docs.oracle.com.javase.8.docs.table.png">
  <source media="(min-width: 465px)" srcset="resources/images/javayoudontknow.png">
  <img src="resources/images/javaversions.png" alt="Javas" style="width:auto;">
</picture>

<video controls="">
  <source src="http://mdui-aliyun.cdn.w3cbus.com/docs/assets/docs/video/demo_mp4.mp4" type="video/mp4">
  <param name="autoplay" value="true">
</video>
<br>
<img src="resources/images/javayoudontknow.png" width="512" height="256" alt="Java you dont know" usemap="#jdnmap">

<map name="jdnmap">
  <area shape="rect" coords="357,78,455,140" href="#mrII" alt="Funny">
  <area shape="circle" coords="32,20,124" href="#typesetting-text" alt="Jawa">
</map>

<figure>
  <img src="resources/images/javaversions.png" alt="javaversions" style="width:100%">
  <figcaption>Fig.1 - Java Versions.</figcaption>
</figure>

#### HTML Widgets

See [HtmlWidgets.md](HtmlWidgets.md). 😘
