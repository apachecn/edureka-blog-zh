# HTML DOM:如何使用文档对象模型

> 原文：<https://www.edureka.co/blog/html-dom>

一个文档对象代表显示在该窗口中的 [HTML](https://www.edureka.co/blog/what-is-html/) 文档。文档对象具有各种属性，这些属性引用允许访问和修改文档内容的其他对象。在本文中，我们将了解 HTML DOM。

*   [HTML DOM 概念](#concept)
*   [什么是 HTML DOM](#what-is)
*   [HTML DOM 不是什么](#what-is-not)
*   [DOM 从何而来](#where)
*   [HTML DOM 的属性](#properties)
*   [寻找 HTML 元素](#finding)

## **HTML DOM 概念**

访问和修改文档内容的方式称为[文档对象模型](https://www.edureka.co/blog/dom-in-javascript/)，或 DOM。对象按层次结构组织。这种层次结构适用于 Web 文档中对象的组织。

*   窗口对象——层次结构的顶层。它是对象层次结构的最高级元素。
*   文档对象——加载到窗口中的每个 HTML 文档都成为一个文档对象。文档包含页面的内容。
*   表单对象——

    <form>…</form>

    标签中的所有内容设置表单对象。
*   表单控件元素——表单对象包含为该对象定义的所有元素，如文本字段、按钮、单选按钮和复选框。

## **什么是 HTML DOM**

文档对象模型是用于文档的编程 API。对象模型本身非常类似于它所建模的文档的结构。例如，考虑这个取自 HTML 文档的表:

```
      <TABLE>
      <ROWS> 
      <TR> 
      <TD>Shady Grove</TD>
      <TD>Aeolian</TD> 
      </TR> 
      <TR>
      <TD>Over the River, Charlie</TD>
      <TD>Dorian</TD> 
      </TR> 
      </ROWS>
      </TABLE>
```

## **HTML DOM 不是什么**

本节旨在通过将文档对象模型与其他看似相似的系统区分开来，更准确地理解文档对象模型。

尽管文档对象模型受到动态 HTML 的强烈影响，但在第 1 级中，它并没有实现所有的动态 HTML。特别是，事件尚未定义。级别 1 旨在通过提供文档本身的健壮、灵活的模型，为这种功能打下坚实的基础。

文档对象模型不是二进制规范。用同一种语言编写的文档对象模型程序将是跨平台源代码兼容的，但是文档对象模型没有定义任何形式的二进制互操作性。

文档对象模型不是一种将对象持久化为 XML 或 HTML 的方式。文档对象模型不是指定如何在 XML 中表示对象，而是指定如何将 XML 和 HTML 文档表示为对象，以便它们可以在面向对象的程序中使用。

![HTML DOM is NOT](img/56f4f04a71898e7b558d265d2cbf4b83.png)

文档对象模型不是一组数据结构，它是一个指定接口的对象模型。虽然本文档包含显示父/子关系的图表，但这些是由编程接口定义的逻辑关系，而不是任何特定内部数据结构的表示。

文档对象模型没有定义 XML 或 HTML 的“真正的内部语义”。这些语言的语义是由语言本身定义的。

文档对象模型是一个设计用来尊重这些语义的编程模型。文档对象模型对您编写 XML 和 HTML 文档的方式没有任何影响；任何可以用这些语言编写的文档都可以用文档对象模型来表示。

尽管名为文档对象模型，但它并不是组件对象模型(COM)的竞争对手。像 CORBA 一样，COM 是一种独立于语言的指定接口和对象的方式；文档对象模型是一组为管理 HTML 和 XML 文档而设计的接口和对象。DOM 可以使用像 COM 或 CORBA 这样的独立于语言的系统来实现；它也可以使用特定于语言的绑定来实现，如本文中指定的 Java 或 ECMAScript 绑定。

## **文档对象模型从何而来**

文档对象模型起源于一种规范，允许 JavaScript 脚本和 Java 程序在 web 浏览器之间移植。动态 HTML 是文档对象模型的直接祖先，它最初主要是根据浏览器来考虑的。

![working of HTML](img/7a3aa46e9d1eb3cb474993818cd47d3b.png)

然而，当文档对象模型工作组形成时，其他领域的供应商也加入了进来，包括 HTML 或 XML 编辑器和文档存储库。在开发 XML 之前，这些供应商中有几家已经使用过 SGML 因此，文档对象模型受到了 SGML Groves 和 HyTime 标准的影响。其中一些供应商还开发了他们自己的文档对象模型，以便为 SGML/XML 编辑器或文档存储库提供编程 API，这些对象模型也影响了文档对象模型。

## **HTML DOM 的属性**

让我们看看文档对象可以访问和修改的文档对象的属性。

![DOM-Graph](img/eaac8a6834462ec0696783a925add781.png)

1.  **窗口对象:**窗口对象总是在层次结构的顶端。
2.  **文档对象:**当一个 HTML 文档被加载到一个窗口中时，它就变成了一个文档对象。
3.  **表单对象:**由 ***表单*** 标签表示。
4.  **链接对象:**用 ***链接*** 标签表示。
5.  **锚对象:**用 ***a href*** 标签表示。
6.  **表单控件元素:**表单可以有很多控件元素，如文本字段、按钮、单选按钮、复选框等。

**方法**文档对象的**:**

1.  **write("string"):** 在文档上写入给定的字符串。
2.  **getElementById():** 返回具有给定 Id 值的元素。
3.  **getElementsByName():** 返回具有给定名称值的所有元素。
4.  **getElementsByTagName():** 返回具有给定标记名的所有元素。
5.  **getElementsByClassName():**返回具有给定类名的所有元素。

## **寻找 HTML 元素**

当你想用 JavaScript 访问 HTML 元素时，你必须先找到元素。

有几种方法可以做到这一点:

*   通过 id 查找 HTML 元素
*   通过标记名查找 HTML 元素
*   通过类名查找 HTML 元素

**通过 Id 找到 HTML 元素**

在 DOM 中查找 HTML 元素最简单的方法是使用元素 id。

### 例子

![HTML DOM- Output-1](img/d0bfd2393f2a8b648937fa07ccd7f770.png)

**通过标签名寻找 HTML 元素**

此示例查找 id="main "的元素，然后查找" main "中的所有

元素:

![HTML DOM- Output-2](img/51bcb3b88e88a2429e4377bee05ff80d.png)

至此，我们结束了这篇 HTML DOM 文章。我希望您理解了 HTML DOM 的各个方面，文档对象模型。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“HTML 图片”博客的评论部分提到它，我们会给你回复。