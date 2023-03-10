# 引导颜色是如何实现的？

> 原文：<https://www.edureka.co/blog/bootstrap-color/>

[Bootstrap](https://getbootstrap.com/) 是一个基于前端框架的 web 开发平台。它用于使用 [、HTML](https://www.edureka.co/blog/what-is-html/) 和 [CSS](https://www.edureka.co/blog/what-is-css/) 创建卓越的响应式设计。这些模板用于表单、表格、按钮、排版、模型、表格、导航、传送带和图像。自举色用于使你的背景和文字看起来很有美感。在这篇博客中，你将学习:

*   [文字自举颜色](#text)
*   [背景引导颜色](#background)

## **文本自举颜色**

文本引导颜色用于通过颜色解释含义。在 Bootstrap 中，有多种颜色来解释表达文本的意义。文本颜色的类别有:

| **类** | **描述** |
| 。文本静音 | 用浅灰色表示文本颜色。用于使文本静音。 |
| 。文本-主要 | 用蓝色表示文本颜色。用来表示一篇文章的重要性 |
| 。文本-成功 | 用绿色表示文本颜色。用来表示成功 |
| 。文本信息 | 用浅蓝色表示文本颜色。用来表示一些信息 |
| 。文本警告 | 用黄色表示文本颜色。用于表示警告 |
| 。文本-危险 | 用红色表示文本颜色。用来表示危险 |
| 。文本-次要 | 用灰色表示文本颜色。用于指示次要文本 |
| 。文本-白色 | 以白色表示文本颜色 |
| 。文本-深色 | 用深灰色表示文本颜色 |
| 。正文-正文 | 用黑色表示文本颜色。这是默认的文本颜色 |
| 。文本灯 | 在白色背景上用浅灰色表示文本颜色 |

现在我们已经了解了不同类型的引导颜色类及其含义，让我们来执行它们。

**举例:**

```
<body>
<div class="container">
<h2> Contextual Colors </h2>
<p> Use the contextual classes to provide "meaning through colors”: </p>
<p class = "text-muted"> This text is muted. </p>
<p class = "text-primary" > This text is important. </p>
<p class = "text-success"> This text indicates success. </p>
<p class = "text-info"> This text represents some information. </p>
<p class = "text-warning"> This text represents a warning. </p>
<p class = "text-danger"> This text represents danger. </p>
<p class = "text-secondary"> Secondary text. </p>
<p class = "text-dark"> This text is dark grey. </p>
<p class = "text-body"> Default body color (often black). </p>
<p class = "text-light" > This text is light grey (on white background). </p>
<p class = "text-white"> This text is white (on white background). </p>
</div>
</body>
```

**输出:**

![output - bootstrap color - edureka](img/1bcc8963eb1c0dfed9b096d213874ac6.png)

除此之外，您还可以添加 50%的不透明度使用。文本-黑色-50 "或"。text-white-50 "类。

**例如**:

```
<body>
<div class = "container">
<p> Add 50% opacity for black or white text with the .text-black-50 or .text-white-50 classes: </p>
<p class = "text-black-50"> Black text with 50% opacity on white background </p>
<p class = "text-white-50 bg-dark"> White text with 50% opacity on black background </p>
</div>
</body>
```

**输出:**

![](img/b56e012e3683489d0d129d466635bf0a.png)

## **背景颜色**

可以使用的背景色类别有:

| **类** | **描述** |
| 。血糖-主要 | 用蓝色墨水突出显示重要文本 |
| 。BG-成功 | 用绿色突出显示成功文本 |
| 。血糖信息 | 用浅蓝色突出显示信息 |
| 。血糖-警告 | 用黄色突出显示警告文本 |
| 。背景-红色 | 用红色突出显示危险文本 |
| 。血糖-中学 | 以灰色突出显示次要文本 |
| 。背景-黑暗 | 用灰色突出显示文本 |
| 。烧烤灯 | 用浅灰色突出显示文本 |

**举例:**

```
<body>
<div class="container">
<p> Use the contextual background classes to provide " meaning through colors". </p>
<p> Note that you can also add a .text - * class if you want a different text color: </p>
<p class = "bg-primary text-white"> This text is important. </p>
<p class = "bg-success text-white"> This text indicates success. </p>
<p class = "bg-info text-white"> This text represents some information. </p>
<p class = "bg-warning text-white"> This text represents a warning. </p>
<p class = "bg-danger text-white"> This text represents danger. </p>
<p class = "bg-secondary text-white"> Secondary background color. </p>
<p class = "bg-dark text-white"> Dark grey background color. </p>
<p class = "bg-light text-dark"> Light grey background color. </p>
</div>
</body>
```

**输出:**

![Output - Bootstrap color - edureka](img/022fa8660d3ee0ea020476eeabbb0161.png)

就这样，我们来到了这篇文章的结尾。我希望你明白自举色是如何被用于造型的。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“Bootstrap Color”博客的评论部分提到它，我们将会回复您。