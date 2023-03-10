# 如何最好地使用 HTML 属性？

> 原文：<https://www.edureka.co/blog/html-attributes/>

属性定义了一个 HTML 元素的特征，这个元素被放在元素的开始标签中。在这篇文章中，我们将探索 HTML 属性。本文将讨论以下几点，

*   [HTML 属性](#HTMLAttributes)
*   [对齐属性样本代码](#SampleCodeForAlignmentAttribute)
*   [属性](#IdAttribute)
*   [标题属性](#TitleAttribute)
*   [类属性](#ClassAttribute)
*   [样式属性](#StyleAttribute)

让我们从这篇文章开始吧

## **HTML 属性**

在 HTML 中我们使用标题标签< h1 >、< h2 > be it 段落标签< p >等标签。这些是最简单形式的标签。这些标签也可以有属性。这些属性只不过是额外的信息。

属性定义了一个 HTML 元素的特征，这个元素被放在元素的开始标签中。一个属性中有两个部分

**名称**

是用户想要设置的属性。

举例:< p >是表示对齐的属性，可以用来对页面上的 段落进行 fro 对齐。

**值**

这是要设置的属性，它将始终在引号中。

示例:对于< p >属性，将有三种可能性来对齐文本，即 左对齐、居中对齐和右对齐。

注意:属性名和值是区分大小写的。万维网在 HTML 4 推荐中推荐小写属性和属性值。

继续这篇关于 HTML 属性的文章，

## **对齐属性样本代码**

校准属性示例:

```
</p>
<!DOCTYPE html>
<html>
<head>
<title> Align Attribute Example</title>
</head>
<body>
<p align="left">This is left aligned</p>
<p align="center">This is center aligned</p>
<p align="right">This is right aligned</p>
</body>
</html>
<p style="text-align: justify;">
```

这将显示以下结果:

![Output -HTML Attributes - Edureka](img/b7cc1bb31bf53bcde8f85d9cf50a3f41.png)

基本上有四个核心属性可以用于大多数 HTML 元素。他们是:

*   Id
*   Title
*   类
*   风格

继续这篇关于 HTML 属性的文章，

## **Id 属性**

id 属性用于标识 HTML 页面中的任何元素。该属性的重要性为:

如果 id 属性作为标识符被携带，则可以识别该元素及其内容。 样式表中出现了两个同名的元素，用户可以使用这个属性来区分这些元素

**例子**

< p id="intro" >此段落是页面的介绍< /p >

< p id="summary" >这一段是页面的摘要< /p >

继续这篇关于 HTML 属性的文章，

## **标题属性**

顾名思义，它给出了关于元素标题的额外信息。语法类似于 id 属性。

当光标在它上面时，或者当元素正在加载时，它通常显示为工具提示。这个属性动作依赖于元素。

**例子**

```
</p>
<!DOCTYPE html>
<html>
<head>
<title> title attribute </title>
</head>
<body>
<h3 title="i give extra bit of information about the heading">Move the cursor upon this text</h3>
</body>
</html>
<p style="text-align: justify;">
```

以下内容的输出将是:

![Output -HTML Attributes - Edureka](img/a17db5df49861d6d0400aacd67d29410.png)

继续这篇关于 HTML 属性的文章，

## **类属性**

class 属性用于关联一个元素和一个 CSS 样式表。顾名思义，它指定了元素的类。在 CSS 中，伪类被用来添加特殊效果。

主要是和 CSS 挂钩。

**例子**

```
class=”classname1 classname2 classname3”
```

继续这篇关于 HTML 属性的文章，

## **样式属性**

样式属性主要与 CSS 相关联，我们可以在其中应用元素的规范。比如颜色编码和字体。

**例子**

```
</p>
<!DOCTYPE html>
<html>
<head>
<title>Style attribute </title>
</head>
<body>
<p style="font-family:calibri; color:#00FF00;">Style is done to this text.</p>
</body>
</html>
<p style="text-align: justify;">
```

以下内容的输出将是:

这就把我们带到了这篇关于 HTML 属性的文章的结尾

*既然你知道了什么是 HTML，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这篇文章的评论部分提到它，我们会给你回复。*