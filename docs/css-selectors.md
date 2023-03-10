# 关于 CSS 选择器你需要知道的一切

> 原文：<https://www.edureka.co/blog/css-selectors/>

这篇文章提出了一个有趣而重要的主题，称为 [CSS](https://www.edureka.co/blog/what-is-css/) 选择器，并通过一个支持性的实践演示来跟进。本文将涉及以下几点:

*   [样式化 HTML 元素](#StylingHTMLElements)
*   [CSS 选择器](#CSSSelectors)
*   [CSS Id 选择器](#CSSIdSelector)
*   [CSS 类选择器](#CSSClassSelector)
*   [CSS 通用选择器](#CSSUniversalSelector)
*   [CSS 组选择器](#CSSGroupSelectors)

那么让我们开始吧，

## **样式化 HTML 元素**

在讨论 CSS 选择器之前，让我们先了解一下什么是 CSS。如果 HTML 被认为是一个骨架，那么 CSS(层叠样式表)就像肌肉和皮肤。大脑是 JavaScript。所以，对于一个网页来说，CSS 样式本质上就是布局和设计。从图像和文本的位置到字体大小和背景颜色，CSS 控制了 HTML 元素在浏览器中的外观。

如果你很好地掌握了 CSS 选择器是什么，你就能更好地理解 CSS。这些选择器允许您将特定的 HTML 元素作为目标，以便对它们应用正确的样式。

![Sample - CSS Selectors - Edureka](img/a4161b616de5506bb3b9709d7298a548.png)让我们了解一下我们如何选择 HTML 元素，

## **如何选择元素？**

比方说，你希望某个标题的风格不同于网页中的其他内容。现在，使用 CSS 选择器，您可以针对 HTML 元素设置不同的样式。CSS 选择器有助于定义应用一组 CSS 规则的元素。有各种类型的 CSS 选择器可以让您精确地选择想要样式化的元素。您可以给整个 web 页面一个通用的样式，然后按照自己的方式设计页面的其他元素。

选择器是 CSS 规则的一部分，这些选择器就在 CSS 块声明之前。为了更好的理解，可以参考下图。

用 CSS 选择器继续文章

## **CSS 选择器**

这个选择器允许你通过名称选择一个 HTML 元素。

考虑下面的代码:

```
<!DOCTYPE html>
<html>
<head>
<style>
p{
text-align: center;
color: magenta;
}
</style>
</head>
<body>
<p>This style will be applied on every paragraph.</p>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
</html>
```

这段代码将给出以下输出:

**该样式将应用于每一个段落**

**第 1 段**

**第二段**

在上面的代码中，HTML 元素已经居中对齐，颜色为“洋红色”。

用 CSS 选择器继续文章

## **CSS Id 选择器**

通过选择 HTML 元素的 id 属性，您可以选择特定的元素。由于 id 对于页面来说是唯一的，所以可以使用 id 属性来选择正确的元素。

您可以使用“#”后跟该元素的 id 来选择 HTML 元素。例如，“#firstname”选择 id 为“firstname”的元素。

考虑以下代码:

```
<!DOCTYPE html>
<html>
<head>
<style>
#para1{
text-align: center;
color: orange;
}
</style>
</head>
<body>
<p id="para1">Hello World</p>
<p>This paragraph will not be affected.</p>
</body>
</html>
```

上述代码的输出为:

**你好世界**

这一段不会受到影响。

正如您在上面的输出中看到的，通过包含 id="para1 ",我们能够将该元素的颜色更改为橙色。没有这个的其他元素保持不变。

用 CSS 选择器继续文章

## **CSS 类选择器**

使用类选择器，你可以选择具有特定类属性的 HTML 元素。您可以使用句点(句号符号)后跟类名来定义选择器。例如，。intro 选择类为“intro”的元素。需要记住的一点是，类名不能以数字开头。

考虑以下代码:

```
<!DOCTYPE html>
<html>
<head>
<style>
.center {
text-align: center;
color: pink;
}
</style>
</head>
<body>
<h2 class="center">This heading is pink and center-aligned.</h1>
<p class="center">This paragraph is pink and center-aligned.</p>
</body>
</html>
```

上述代码的输出是:

这个标题是粉红色的，居中对齐。

这个段落是粉红色的，居中对齐。

你可以为一个特定的元素使用 CSS 类选择器。如果您只想设计一个特定元素的样式，那么您可以使用元素名称和类选择器。

例如，考虑下面的代码:

```
<!DOCTYPE html>
<html>
<head>
<style>
p.center {
text-align: center;
color: pink;
}
</style>
</head>
<body>
<h2 class="center">This heading is not affected</h1>
<p class="center">This paragraph is pink and center-aligned.</p>
</body>
</html>
```

上述代码的输出是:

**该航向不受影响**

这个段落是粉红色的，居中对齐。

正如您在输出中看到的，标题 h2 不受样式的影响。因为我们已经指定了“p.center ”,所以只有段落受到样式的影响。

继续这篇 CSS 选择器的文章，

**CSS 通用选择器**

这种类型的选择器可以被认为是一个通配符，用于选择页面中的所有元素。它选择页面上的所有元素，并由“*”指定。

例如，考虑下面的代码:

```
<!DOCTYPE html>
<html>
<head>
<style>
*{
color: darkgreen;
font-size: 30px;
}
</style>
</head>
<body>
<h1>This is the heading</h2>
<p>This style will be applied to every paragraph.</p>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
</html>
```

上述代码的输出是:

**这是标题**

这种风格将应用于每一个段落。

第 1 段

第二段

正如您在输出中看到的，在“*”下定义的任何内容都被应用于指定的每个 HTML 元素。

继续这篇 CSS 选择器的文章，

## **CSS 组选择器**

这种选择器用于选择具有相同样式定义的元素。组选择器的主要目的是最小化所使用的代码。您可以使用逗号来分隔分组中的选择器。

让我们看看组选择器是如何最小化代码使用的。

下面的代码片段不包含任何组选择器:

```
h1 {
text-align: center;
color: blue;
}
h2{
text-align: center;
color: blue;
}
p{
text-align: center;
color: blue;
}
```

上面的代码片段对元素 h1、h2 和 p 应用了相同的样式定义。您可以使用逗号将它们分组，如下面的代码片段所示:

```
h1,h2,p
{
text-align: center;
color: blue;
}
```

如你所见，编写的代码量显著减少。您不必编写多余的代码来为不同的 HTML 元素应用相同的样式定义。

让我们用一个例子来看看如何实现 CSS 组选择器:

```
<!DOCTYPE html>
<html>
<head>
<style>
h1, h2, p {
text-align: center;
color: cyan;
}
</style>
</head>
<body>
<h1>Hello World</h1>
<h2>This is a test (smaller font)</h2>
<p>This is a paragraph.</p>
</body>
</html>
```

上述代码的输出是:

**你好世界**

**这是一个测试(较小的字体)**

**这是一段。**

正如您在输出中看到的，使用组选择器定义的所有元素都有相同的样式定义——它们居中对齐，字体颜色为青色。

这就把我们带到了本文的结尾。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在文章的评论部分提到它，我们会给你回复。