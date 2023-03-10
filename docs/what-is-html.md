# 什么是 HTML？构建网页的一站式解决方案

> 原文：<https://www.edureka.co/blog/what-is-html/>

HTML 是网络上开发网页最广泛使用的语言之一。它有助于你深入[网络开发的世界](https://www.edureka.co/masters-program/full-stack-developer-training)并提高你的技能。那么，让我们按以下顺序进入**什么是 HTML** 和 HTML 的基础是什么的细节:

*   [HTML 的起源](#htmlorigin)
*   [什么是 HTML？](#whatishtml)
*   [HTML 结构](#htmlstructure)
*   HTML 是如何工作的？
*   [HTML 基础](#htmlfundamentals)

## **HTML 的起源**

超文本标记语言(HTML)的历史是一个奇怪而有趣的故事。HTML 背后的人，蒂姆·伯纳斯·李正在组装他的第一个基本的网络浏览和创作系统，并创造了一个快速的小超文本语言，将服务于他的目的。

但是问题在于语言的简单性。HTML 是基于文本的 T2，任何人都可以使用任何编辑器或文字处理器为网络创建或转换文档。开发人员开始在他们的浏览器中实现新功能，并开始发布 HTML 的高级版本。

**HTML 初学者教程| Edureka**



[//www.youtube.com/embed/88PXJAA6szs?rel=0&showinfo=0](//www.youtube.com/embed/88PXJAA6szs?rel=0&showinfo=0)

## **什么是 HTML？**

标记语言是一种用于将布局和格式约定应用于文本文档的计算机语言。标记语言使文本更加**互动**和**动态**。它可以把文本变成图像、表格、链接等。

![](img/638388668cb2044429e204b3a5f1b754.png)

HTML 代表**超文本标记语言**，它是创建网页和网络应用程序的标准标记语言。它用于使用标记来描述网页的结构。

## **HTML 结构**

HTML 标签主要有两种类型:  **块级** 和  **行内标签**。

1.  **块级**元素占据了全部可用空间，并且总是在文档中开始新的一行。块标签的例子包括**标题**和**段落。**

2.  **Inline** 元素只占用它们需要的空间，并且不会在页面上另起一行。它们通常用于格式化**块级**元素的内部内容。内联标签的一些例子包括**链接**和强调**字符串**。

![HTML Structure - What is HTML - edureka](img/259dc1a26864846bd4e2c1029340ef7f.png)

HTML 文档需要的三个块级标签是、和。

1.  **<HTML></HTML>**标签是封装每个 **HTML** 页面的最高层元素。
2.  **<head></head>**标签保存元信息，例如页面的**标题**和**字符集**。
3.  最后，**<body></body>**标签包围了页面上出现的所有**内容**。

## HTML 是如何工作的？

HTML 文档以**结尾。html** 或者**。htm** 扩展名。您可以使用任何网络浏览器查看它。浏览器读取 HTML 文件并呈现内容供用户查看。

![](img/87c0ec4dbcdcb9d4f856708b9595ddfe.png)

每个 HTML 页面由一组标记或元素组成，这些标记或元素被称为网页的构建块。它们创建了一个层次结构，将内容分为章节、段落、标题和其他内容块。

让我们举一个**的例子**，看看 HTML 中的元素是如何构造的:

```

<div>
<h1>The Main Heading</h1>
<h2>Subheading</h2>
<p>Paragraph</p>
<img src="/" alt="Image">
<p>Second Paragraph with <a href="https://example.com">hyperlink</a></p>
</div>

```

现在让我们继续讨论什么是 HTML？文章，并深入了解 HTML 中基本标签的细节。

## **HTML 基础**

要用 HTML 创建一个网页，你需要了解一些基本的元素，比如:

![HTML Elements- what is HTML -edureka](img/656cab2f426fbfe84e5f7cf458e7a52e.png)

### **标题**

HTML 标题是用 **< h1 >** 到 **< h6 >** 标签定义的。

**< h1 >** 定义了**最** **重要**的标题。鉴于， **< h6 >** 定义了**最不重要的**标题:

```

<h1>First Heading</h1>
<h2>Second Headng</h2>
<h3>Third Heading</h3>
<h4>Fourth Heading</h4>
<h5>Fifth Heading</h5>
<h6>Sixth Heading</h6>

```

### **段落**

HTML 段落是用 **< p >** 标签定义的。你可以用这个标签添加任意多的**段落**。

```

<p>First Paragraph</p>
<p>Second Paragraph.</p>

```

### **链接**

HTML 链接就是**超链接**。您可以点击链接并重定向到另一个文档或网页。链接被定义为带有**<>**标签:

```

<a href="www.edureka.co">Add Link</a>

```

### **图像**

你的网页需要用简单的方式美化或描绘复杂的概念。HTML 图片是用 **< img >** 标签定义的。

源文件 **(src)** 、可选文本 **(alt)** 、宽度和高度作为属性提供:

```

<img src="image.jpg" alt="Edureka" style="width:120px;height:150px"

```

### **按钮**

元素的作用是:创建一个 HTML 按钮。开始和结束标记之间的所有文本在按钮上都显示为文本。它定义了一个可点击的按钮。在一个 **<按钮>** 元素里面你可以添加文本或者图片:

```

<button>Click here</button>

```

### **列表**

HTML 提供了三种指定信息列表的方法。所有列表必须包含一个或多个列表元素。

1.  **< ul >** : **无序**列表使用普通项目符号对项目进行排序。

2.  **< ol >** : **有序**列表使用不同的数字方案来列出你的物品。

3.  **< dl >** :一个**定义**列表按照它们在字典中的排列方式来排列你的条目。

**无序列表**

这个列表是通过使用 HTML **< ul >** 标签创建的:

```

<ul>
<li>Python</li>
<li>Java</li>
<li>DevOps</li>
<li>Cloud Computing</li>
</ol>
</ul>

```

**有序列表**

这个列表是通过使用 **< ol >** 标签创建的:

```

<ol>
<li>Python</li>
<li>Java</li>
<li>DevOps</li>
<li>Cloud Computing</li>
</ol>

```

**定义列表**

定义列表是展示术语表、术语列表或其他名称/值列表的理想方式。使用 **< dl >、< dt >和< dd >** 标签创建:

```

<dl>
<dt><b>HTML</b></dt>
<dd>This stands for Hyper Text Markup Language</dd>
<dt><b>HTTP</b></dt>
<dd>This stands for Hyper Text Transfer Protocol</dd>
</dl>

```

### **表格**

一个 HTML 表格用一个 **<表格>** 标签定义。

*   用标签定义行。
*   标题由标签定义
*   表格单元格用标签定义。

```

<table>
<tr>
<th>Firstname</th>
<th>Lastname</th>
<th>Age</th>
</tr>
<tr>
<td>Jill</td>
<td>Smith</td>
<td>50</td>
</tr>
<tr>
<td>Eve</td>
<td>Jackson</td>
<td>94</td>
</tr>
</table>

```

现在你知道了基本原理，让我们来看看完整的**代码**来创建一个基本的 **HTML 网页**。

### **Example.html**

```

<html>
<head>
<title>What is HTML?</title>
</head>
<body BGCOLOR="black">
<h1><font color="white">Welcome to Edureka!</font></h1>
<p><font color="white">Learn about HTML <a href="www.edureka.co">here</a></font></p>

<center><img src="image.jpg" alt="Edureka" style="width:640px;height:360px"></center>
<ul><font color="white">
<li>Full Stack</li>
<li>Java</li>
<li>Python</li>
<li>Cloud Computing</li>
</ul></font>
</body>
</body>
<button>Click here</button>

</body>
</html>

```

这将创建一个基本网页作为**输出**:

![output-what is html - edureka](img/38afdde06ca39b9ee940f805dfbe9918.png)

*既然你知道了什么是 HTML，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“什么是 HTML？”的评论部分提及。我们会回复你的。*