# <ruby><span style="color:brown">Java</span> You-Dont-Know<rt>你不知道的 Java</rt></ruby> [![badge-handwrote](https://img.shields.io/badge/handwrote-knowledge_base-blueviolet.svg?style=flat-square)](https://en.wikipedia.org/wiki/Knowledge_base) ![badge-javaversion](https://img.shields.io/badge/java-≤1.8-brown.svg?style=flat-square)

<div align="center">
  <img alt="Java You Dont Know" src="resources/images/javayoudontknow.png" />
</div>

你不知道的 Java：那些原理不为人知却总是被使用的“黑科技” — 截至 [Java] 语言版本 [1.8]

> 我的语言 Java 今年 23 岁，完美的程序设计材料，完美的 <ruby>OOP<rt>面向对象编程</rt></ruby>语言，但在我手里却是个超辣鸡的[干物] lang。经常看到看不懂的语法、重复的代码、假装会用的泛型，不断 <kbd>Ctrl</kbd> - <kbd>C</kbd>; <kbd>Ctrl</kbd> - <kbd>V</kbd> 抄改别人的代码，可是莫名其妙地无法停下来啊！！！<br>
然而 Java 在这里的一切她生活中的秘密，作为主人的我并不知道，<ruby>推<rt><del>zhōng</del></rt>倒<rt><del>chū</del></rt></ruby>了居住在同一栋楼的天然少女 [C++]，以及无意间来到我家的冷酷少女 [Haskell] 后，我会发现 Java 的真实面目吗？<a href="#notes-intro[0]"><sup>[0]</sup></a>

Java 是什么？Java 是领先全球的[计算机程序设计]技术之一。

Java 是一门[程序设计语言]，它更是一个[软件开发]平台，根据平台的组成部分、主要业务领域区分，Java 技术体系可以被分为 __4__ 个子体系：

[计算机程序设计]: https://en.wikipedia.org/wiki/Computer_programming
[程序设计语言]: https://en.wikipedia.org/wiki/Programming_language_theory
[软件开发]: https://en.wikipedia.org/wiki/Software_engineering

+ __Java Card__：支持一些小程序（[Applets]）在诸如[智能卡]等 __小内存设备__ 上的平台
+ __Java ME__（Micro Edition，J2ME）：支持 Java 运行在智能手机、<abbr title="Personal Digital Assistant">PDA</abbr> 等设备上的技术，对 JavaSE 的 API __有所精简__，并且加入了针对嵌入式通讯设备的 API 支持
+ __Java SE__（Standard Edition，J2SE）：支持面向桌面工作站（和个人电脑、平板等）上如桌面窗口应用程序开发的 Java，提供了完整的 Java 核心 API（比如 [Collections 框架]）以及开发使用的辅助框架（比如 [javax.swing], [java.awt]）
+ __Java EE__（Enterprise Edition，J2EE）：支持使用了多层架构的企业级应用程序（比如 [ERP] 和 [CRM]<a href="#notes-intro[1]"><sup>[1]</sup></a>），以开发各类对应用程序健壮性、安全性、可测试性、可部署性、性能、并发支持性和软件工程理论有较强要求的应用程序（比如生产级别的 <abbr title="client/server">C/S</abbr> 架构服务器程序）
<br>著名的 Java EE 技术例如 [Java Bean] (组合<ruby>可序列化<rt><code>@java.io.Serializable</code></rt><abbr title="java.lang.Object">对象</abbr></ruby>, <ruby>实例<rt>instance</rt></ruby>比如 EJB); [Web servlet] 架构; [JNDI] 服务访问接口架构

[ERP]: https://en.wikipedia.org/wiki/Enterprise_resource_planning
[CRM]: https://en.wikipedia.org/wiki/Customer_relationship_management

[Java]: https://www.oracle.com/java/
[1.8]: https://docs.oracle.com/javase/specs/jls/se8/html/index.html
[干物]: https://zh.moegirl.org/%E5%B9%B2%E7%89%A9%E5%A5%B3#

[C++]: https://en.wikipedia.org/wiki/C%2B%2B
[Haskell]: https://www.haskell.org/

[智能卡]: https://en.wikipedia.org/wiki/Smart_card
[Applets]: https://en.wikipedia.org/wiki/Java_applet

[Collections 框架]: https://docs.oracle.com/javase/8/docs/technotes/guides/collections/reference.html
[java.awt]: https://docs.oracle.com/javase/8/docs/api/java/awt/package-summary.html
[javax.swing]: https://docs.oracle.com/javase/8/docs/api/javax/swing/package-summary.html
[Java Bean]: https://en.wikipedia.org/wiki/JavaBeans
[Web servlet]: https://en.wikipedia.org/wiki/Java_servlet
[JNDI]: https://en.wikipedia.org/wiki/Java_Naming_and_Directory_Interface

<div id="intro-javase8-stack" align="center">
  <details open>
  <summary><var>JavaSE 8 <a href="https://docs.oracle.com/javase/8/docs/#content">技术栈</a></var></summary>
  <img alt="JavaSE Tech Stack" src="resources/images/docs.oracle.com.javase.8.docs.table.png">
  </details>
</div>

Java 开发平台提供了以 Java 程序设计语言为核心的 __完整跨平台程序设计开发工具链__，并且，它被广泛地应用于桌面程序、服务器程序、移动终端、大型计算机等场合。

Sun 定义的 Java 技术体系包含以下项目：

<dl>
  <dt>Java 程序设计语言</dt>
    <dd><div id="intro-lang">
      Java 程序设计语言是 Java 开发平台的 <b>灵魂</b>
      <br>Java 是一门 <b>强类型、静态检查、显式类型</b> 的“低糖”语言，它支持<a href="https://en.wikipedia.org/wiki/Programming_paradigm">面向对象编程、面向对象多态、并发编程、事件驱动、反射元编程、泛型编程、Annotation 处理</a>，当然，也包含基本的<a href="https://en.wikipedia.org/wiki/Functional_programming">函数式编程</a>和<a href="https://en.wikipedia.org/wiki/Recursion_(computer_science)">递归</a>支持
      <br>Java 是使用<abbr title="garbage collection">自动内存管理</abbr>的程序设计语言，这意味着，你不需要考虑如何为这门语言的『值』分配内存空间。
      Java 的对象会在需要时被 <code>new</code> 创建，不可能被访问时自动丢弃。
      <br>Java 很大程度上类似 C++，但没有采用 C++ 的<abbr title="指针是计算机科学 PLT 里的一种数据类型概念。1964 年它被计算机科学家 Harold Lawson 首创；C99、Ada95、FreeBasic、C# 等语言都对指针概念的良好支持，用于进行内存单元对象的偏移取值等运算">『指针』</abbr>模型，只支持『<ruby>可空<rt>nullable</rt>』</ruby>引用和提供 <code>native</code> 方法来取代，并且移除了 C++ 里的<abbr title="operator overloading">操作符重载</abbr>和<a href="https://zh.wikipedia.org/wiki/%E7%BB%A7%E6%89%BF_(%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6)">多继承</a>，用 <code>interface</code> 接口规范定义取代。
      <br>自 <a href="https://www.oracle.com/technetwork/java/javase/archive-139210.html#top">Java 1.5</a> 以来，Java 引入了类型安全的 <code>enum</code>、值类型自动装箱拆箱、基于泛型擦除的泛型检查、不定长参数、foreach (<code>for (VarModifier TypedVarId: Expression)</code>) 等特性，Java 技术进入了新时代。
      <br><br>Sun Microsystems 这么描述 Java:
      <br><blockquote>Java 是个简单、面向对象、分布式、解释性、健壮、安全、与系统平台无关、可移植、高性能、多线程和动态灵活的编程语言</blockquote>
    <div id="intro-java-links">
      <br><a href="https://github.com/antlr/grammars-v4/blob/master/java8/Java8.g4#L877">Java 8 ANTLR Grammar</a>
      <br><a href="https://docs.oracle.com/javase/specs/jls/se8/html/index.html">Java 8 Language Spefification</a>
      <br><a href="https://docs.oracle.com/javase/specs/jvms/se8/html/index.html">Java 8 JVM Spefification</a>
    </div></div></dd>
  <dt>Class 文件格式<sub>（Java 字节码格式）</sub></dt>
    <dd><div id="intro-classfile-links">
      <a href="https://duckduckgo.com/?q=Javaassist&t=ffab&atb=v163-1&ia=web">JavaAssist Java bytecode engineering toolkit</a>
      <br><a href="http://asm.ow2.org/">ObjectWeb ASM bytecode manipulation and analysis framework</a>
      <br><a href="https://github.com/apache/commons-bcel">Apache Commons Bytecode Engineering Library</a>
    </div></dd>
  <dt>Java 虚拟机<sub>（在各种实际硬件和操作系统平台上的实现）</sub></dt>
    <dd><div id="intro-jvm-links">
      <a href="https://github.com/imkiva/KiVM">KiVM Java VM (spec version 8 and only Java 8 is supported) implementation in C++</a>
    </div></dd>
  <dt>Java 语言 API <sub>（<code>java.*</code> 标准库）</sub></dt>
  <dt>Java 外部 API <sub>（来自商业机构和开源社区的第三方 Java <abbr title="Class library">类库</abbr>）</sub></dt>
</dl>

<div id="jdk,jre">
<b>我们把 Java 程序设计语言的基础工具、Java 虚拟机、Java API 这三部分统称为 <abbr title="Java Development Kit">JDK</abbr>，它是进行 Java 软件开发的最小支持环境

我们也把 Java 虚拟机、JavaSE API <sub>(所有 Java API 的子集)</sub> 这两部分统称为 <abbr title="Java Runtime Environment">JRE</abbr>，它是支持 Java 程序运行的基础环境</b>
</div>

<div id="intro-java-version-history" align="center">
  <details open>
  <summary><var>Java 版本历史</var> <a href="https://en.wikipedia.org/wiki/Java_version_history">详情</a></summary>
  <img alt="Java Version History" src="resources/images/javaversions.png" />
  </details>
</div>

时至今日，Java 技术已经吸引了 __900 多万__ 名软件开发者，使用 Java 技术的设备多达 __几十亿__ 台，包含众多智能卡、机顶盒、导航系统、游戏机和其他设备。<a href="#notes-intro[2]"><sup>[2]</sup></a>

由 Google 主导开发而领先世界且与 Apple 的 iOS 二分天下的移动操作系统平台，Android，[Android 使用的软件开发技术](https://en.wikipedia.org/wiki/Android_(operating_system)#Software_stack)，就是 Java 技术的一个衍生品。

__1991 年__，由 James Gosling 领导的 "_Green_ Project" 项目启动，此计划的目的是开发一种能够在多种消费电子产品（比如游戏机、机顶盒、个人电脑等）上面运行的程序运行时和软件平台架构。这个架构就是 Java 的前身：Oak（橡树），它尝试扩展 C++，和早期的 Java 大同小异<a href="#notes-intro[3]"><sup>[3]</sup></a>

即便其前身 [Oak] 在市场上并不算成功，Java 的诞生正好赶上了那个无论软件需求量还是工程量都暴涨的网络时代 — 这个时代只接受同类软件中 __第一个__ 弄出来的！

[Oak]: https://en.wikipedia.org/wiki/Oak_(programming_language)

自从 1995 年的 Oak to Java，Java 在 _SunWorld_ 大会上发布第一个版本 1.0 以来，Java 因为其强大的通用性、安全性、稳定性、可移植性、开发效率闻名于世。

Java 的领导者 [James Gosling 博士]从一开始就敏锐地注意到了其他开发平台不安全、时常出现严重的资源内存泄漏、缓冲区溢出、悬垂指针、并发数据竞争，处理复杂繁琐，开发效率低下、必须给不同硬件平台发布不同类型的软件包的问题<a href="#notes-intro[4]"><sup>[4]</sup></a>，Java <abbr title="Java 1.0 发布的时候在 SunWorld 大会上">及时地提出了</abbr> __"Write Once, Run Anywhere"__ 这个口号。极高的开发效率和依此而生的极短开发时间，使 Java 成为网络时代的理想计算平台，从个人智能手机终端到网络服务器，Java 扮演着游戏主持者的角色，赋予了计算以新的复杂性可能。

<div id="intro-java-96">
<b>1996 年 1 月 23 日</b>，JDK 1.0 发布，Java 终于有了第一个正式版本的运行环境

JDK 1.0 提供了一个纯字节码解释器版本的实现 — _Sun Classic VM_

JDK 1.0 时期的 Java 技术包括 JVM、Applet、AWT 等

<b>同年 4 月</b>，10 个操作系统供应商声明将在其产品中嵌入 Java 技术

<b>同年 9 月</b>，已经有 8.3 万网页使用了 Java 技术制作。

<b>同年 5 月底</b>，Sun 公司于美国<abbr title="San Francisco">旧金山</abbr>举行了首届 JavaOne 大会，从此 JavaOne 大会成为世界 Java 开发者一年一度的技术盛会

Java 1.1 发布和 <a href="https://www.haskell.org/definition/">Haskell</a> <abbr title="Haskell 1.4">97</abbr> 正好是同一年
</div>

<br><sub>以上内容部分信息来自[《深入理解 Java 虚拟机》第二版]，可以在豆瓣试读
<br><a href="https://book.douban.com/people/RednaxelaFX/annotation/24722612/)">RednaxelaFX对《深入理解Java虚拟机（第2版）》的笔记(6)</a></sub>

[《深入理解 Java 虚拟机》第二版]: https://book.douban.com/subject/24722612/

[James Gosling 博士]: https://en.wikipedia.org/wiki/James_Gosling

<div id="notes-intro"><small>
  <p id="notes-intro[0]"><sup>[0]</sup>详见 B 站<a href="https://www.bilibili.com/bangumi/media/md2580">《干物妹！小埋》</a><del>《干雾妹小霾》</del></p>
  <p id="notes-intro[1]"><sup>[1]</sup><abbr title="Enterprise resource planning">ERP</abbr>, 企业资源管理<br><abbr title="Customer relationship management">CRM</abbr>, 客户资源管理</p>
  <p id="notes-intro[2]"><sup>[2]</sup>信息来自 <a href="https://www.java.com/zh_CN/about/">java.com/zh_CN/about</a></p>
  <p id="notes-intro[3]"><sup>[3]</sup>Oak 的 primitive number 包括 <code>unsigned</code> 无符号整数<small>（考虑一下它受到了 C++ 启发）</small>；Oak 不存在 <i>private</i> 访问（<code>private</code> 是 package-private）；Oak 早就有 <abbr title="Java 1.5 加入（JSR 201）"><code>enum</code></abbr> 和 <abbr title="Java 1.4 加入（JSR 41）"><code>assert</code></abbr> 了；Oak 的 <a href="https://en.wikipedia.org/wiki/Exception_handling#In_software">exceptions</a> 可以不检查(unchecked)；利用 <code>unprotect</code> 关键字异步异常（比如说系统的 SIGINT，<a href="https://docs.oracle.com/javase/8/docs/api/index.html?java/lang/ThreadDeath.html">ThreadDeath</a>）可以不处理、Oak 支持<a href="https://zh.wikipedia.org/wiki/%E5%A5%91%E7%BA%A6%E5%BC%8F%E8%AE%BE%E8%AE%A1">契约式编程</a>（比如，给子类继承的方法前置逻辑）</p>
  <p id="notes-intro[4]"><sup>[4]</sup>排除增强类型系统安全检查强度和动态检查、运行时异常外；使用<ruby>中间码<rt><a href="https://en.wikipedia.org/wiki/Intermediate_representation">intermediate language</a></rt></ruby>，这也是属于见仁见智的问题，实际上，使用平台无关（全平台兼容）的中间代码作为最终的『二进制』形式而不是直接翻译到机器代码，最开始也给 Java 程序的执行带来了一些问题（虽然现在 Java 的选择也显得越来越符合“时代潮流”了），但是，语言<abbr title="『发布』代码的形式，有时被称为『二进制文件』，一般认为是会被持久化在非易失性 (non-volatile) 存储器 (memory) 上的代码形式">“最终”</abbr>的代码形式只是一个选择是否合适、是否符合定位的问题，不存在优劣之分。</p>
</small></div>

## Contents 内容

+ Java 的泛型
  + Java 的类型、子类型和型变
  + Java 类型相关名词解释
    + Subtyping, Type Compatibility, First-class-citizen, Polymorphism
    + Raw Type, Generic Type, Generic Method <sub>(Parameterized Types)</sub>
    + Type Constructor, Type Parameter <sub><abbr title="programming language theory">(PLT)</abbr></sub>
    + [Type Ereasure](https://en.wikipedia.org/wiki/Type_erasure) <sub>(in Java)</sub>
    + Type Wildcard (`capture<…>` in Java)
  + Java 的<ruby>泛型通配符<rt>Type wildcard</rt></ruby>、<ruby><abbr title="producer">生产者</abbr><rt><code>&lt;? extends T&gt;</code></rt></ruby>和<ruby><abbr title="consumer">消费者</abbr><rt><code>&lt;? super T&gt;</code></rt></ruby>模式使用
  + 子类型、泛型类型型变、类型参数的子类型约束、类型安全
  + <ruby>Java 编译器<rt>javac</rt></ruby></ruby>怎么<ruby>知道<rt>infer</rt></ruby>我指定的<ruby>子类型<rt>subtyping</rt>限定<rt>constraint</rt></ruby><ruby>安不安全<rt>well behaved?</rt></ruby>
  + Kotlin 的泛型型变标记：<ruby>生产者<rt><code>out</code></rt>和消费者<rt><code>in</code></rt></ruby>、声明处型变
  + Kotlin 的类型投影、`*` 类型参数
  + Java 的泛型参数推导
+ `invokedynamic` 和 Lambda、Runtime Desugar 有啥关系 <sub>(Android)</sub>
  + Java 8 的 `->` lambda：<ruby>匿名<rt>anonymouse</rt>子类<rt>subclass</rt></ruby>的语法糖、Kotlin 的 <abbr title="Single Abstract Method">SAM</abbr> interface 自动实现
  + Effective `final` 局部变量问题、Ruby、Python、C# 里的等价物
  + Java 是怎么实现 Lambda 的、为什么要这么做、为什么需要 `invokedynamic` 支持

+ Inner `class` 和 [Qualified instance creation](https://docs.oracle.com/javase/specs/jls/se9/html/jls-15.html#jls-15.9)
+ 数组上声明的 `java.lang.Annotation`
+ 执行资源的抽象：Java 里的 `Thread`，Green threads、<abbr title="Light-weight process">LWP</abbr>s、Fibers，`volatile` 和 `synchronized` 同步
+ “不常见”语法
  + `@interface`
  + `assert`
  + Generic Parameter 的 `&`
  + `strictfp` 和 `transient`
  + `package-info.java`
  + <ruby>非<rt>non</rt></ruby> ASCII <ruby>标识符<rt>identifer</rt></ruby>
+ 和语言本身 / 工具集成的类

## Thanks 特别感谢

> 排名不分先后；这是一个<ruby>集合<rt>set</rt></ruby>；而且当然是<abbr title="理论上的集合本身与线性表的主要区别在于集合不关心元素顺序，有序集（sorted set）只是说在『集合遍历』操作时输出对象存在顺序">无序</abbr>的

+ [《深入理解 Java 虚拟机（第二版）》](https://duckduckgo.com/?q=%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3Java%E8%99%9A%E6%8B%9F%E6%9C%BA%EF%BC%88%E7%AC%AC2%E7%89%88%EF%BC%89&t=ffab&atb=v163-1&ia=web) 从上面获取了一些 Java 历史相关的信息~
+ [《Kotlin 极简教程》](https://segmentfault.com/a/1190000010306636) 从上面了整理了关于泛型的性质描述~
+ [W3Schools](https://www.w3schools.com/tags/tag_abbr.asp) 没有你们我不知道有这些标签可用~
+ [Hello, I am Conmajia.](https://www.cnblogs.com/conmajia/) `<ruby>` notation 的风格就是从这里来的~
+ [GitHub Pages](https://pages.github.com/) （当然也包括 [Jekyll] 项目啦）
+ [Markdown] Inline HTML 爽到（

[Jekyll]: https://jekyllrb.com/
[Markdown]: https://commonmark.org

## Recommended Links 推荐链接

+ [duangsuse::Echo](https://t.me/s/dsuse) duangsuse 的 Telegram 频道~
+ RednaxelaFX：[虚拟机随谈（一）：解释器，树遍历解释器，基于栈与基于寄存器，大杂烩](http://rednaxelafx.iteye.com/blog/492667)

## Motivation 写作动机

<abbr title="这句才是真话">写着玩玩呗</abbr>，而且有时候读书：每有会意便欣然忘食

明明是自己忘了吃饭，可是还埋怨书和代码使得自己会意了… __(￢_￢)__

于是带着报复社会的心态，决定给它写出来，而且简化一点尝试使它更容易读懂

— 既然一个人不吃饭… 那就大家都不吃！ __(￣‿￣)✧__

## Licence 许可证

> 此许可证应用到文中所有由 _duangsuse_ 编写的 __示例代码__

```plain
MIT License

Copyright (c) 2019 duangsuse's code

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Development: Setup Jekyll

```bash
pushd Java-You-Dont-Know

git checkout -b gh-pages

print>Gemfile \
  "source \'https://rubygems.org\'" \
  "\ngem \'github-pages\', group: :jekyll_plugins"

bundle install
bundle exec jekyll serve

git checkout master
popd
```
