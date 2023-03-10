# 如何用 CSS 实现悬停并举例

> 原文：<https://www.edureka.co/blog/hover-in-css/>

级联样式表(CSS)是使用 [HTML](https://www.edureka.co/blog/what-is-html/) 或 XML(包括 XHTML、SVG)格式设计的。它是一种样式表语言，主要用于通过一系列不同的格式化方法来描述元素。其中一种方法是悬停，在本文中，我们将通过以下方式理解 CSS 中的悬停:

*   [CSS 中的 Hover 是什么？](#what)
*   [Hover 用在哪里？](#where)
*   【Hover 是做什么的？
*   [兼容性](#compatibility)
*   它是如何工作的？
*   [悬停背景颜色变为“红色”](#background)
*   [在图像上创建悬停不透明度](#opacity)
*   [在图像上创建文本覆盖图](#overlay)

## **CSS 中的 Hover 是什么？**

CSS hover 是一个选择器组件，当鼠标指针悬停在不同的元素上时，它可以用来设置这些元素的样式。它们可以用在几乎所有的 HTML 元素上。CSS 中的悬停功能在网页设计中非常重要。

![Hover in CSS](img/12c7b9e7fc8dfd3699cf20ab77014a97.png)

在一个紧凑而有效的网页设计程序中，悬停组件可以根据用户偏好突出显示、编码和定制网页。

## **Hover 用在哪里？**

悬停功能可行性最常见的例子可以在 Flipkart 和亚马逊等主要购物网站上突出显示。当用户悬停在这些电子商务网站上的任何产品上时，该产品被编程为执行自动缩放悬停功能，以向客户提供他们所选产品的更好视图。通过这种编程，网页被设计成在单个网页设计中显示整个产品范围的紧凑视图以及感兴趣的产品的详细视图。

## 【Hover 是做什么的？

hover 是一个多功能的编程工具，通过它用户可以用无数的格式标准定制目标元素。悬停功能的一些操作诀窍包括:

*   更改背景/字体颜色
*   嵌入悬停时显示的隐藏文本
*   在图像上创建翻转效果
*   文本/图像的自动缩放
*   修改图像不透明度
*   文本嵌入
*   图像交换
*   Div。盘旋
*   多个其他 CSS 悬停格式化操作。

悬停效果基本上修改元素的属性值，以使得能够动画化对所陈述的文本/图像或相应元素的改变。在网页设计中嵌入 CSS 悬停元素可以将一个普通的网页转换成一个交互的、健壮的、功能强大的网页。这些网页设计是用户友好和全面的。悬停设计的网页包含更高的消费者吸引力，它们吸引潜在客户的注意。

## **CSS 中悬停的兼容性**

悬停功能兼容所有主要的网络浏览器。然而，在触摸设备上实现这一元素仍然是一项具有挑战性的任务。CSS 中的悬停在不支持悬停功能的设备上启用内容可访问性。已经观察到，在非支持设备上激活的悬停功能会卡在设备上。

因此，关键内容的重要显示因格式问题而受阻。一方面，CSS 程序中的悬停元素为网页提供了高效的个性化；相反，它在移动设备上的可操作性是高度休眠的。屈服于信息技术世界日益显著移动化的环境，悬停功能面临着随着技术进步而过时的风险。因此，制造一种可与触摸和移动设备一起工作的便携式嵌入式功能的需求是极其重要的。

## 【Hover 在 CSS 中是如何工作的？

活动伪类样式在 CSS 悬停格式中占主导地位，它覆盖该伪类后面的任何/所有后续链接。例如，在伪类“:link: visited，or: active”中，需要将:hover 规则放在:link 和:visited 之后，但在:active 之前，以获得适当的:hover 样式。LVHA-order: :link，:hover，:visited 和:active 被用作适当的:hover 格式样式的参考。

```
<html>
<head>
<style>
div {
background-color: green;
padding: 18px;
display: none;
}

span:hover + div {
display: block;
}
</style>
</head>
<body>

<span>Hover Test!</span>
<div>Hidden code shows on hover</div>

</body>
</html>

```

在上面的代码中，span 元素被修改为通过使用 span: hover + div 元素来合并 hover 和 div 元素。将显示在主登录网页上的 span 元素将显示文本“悬停测试！”进一步悬停在 span 元素上会显示 div 元素“悬停时显示隐藏的代码”。这种嵌入格式对文本和图像都有效。

## **悬停背景颜色变为“红色”**

```
<html>
<head>
<style>
p:hover, h1:hover, a:hover {
background-color: Red;
}
</style>
</head>
<body>
<h1>CSS:Hover Test Code</h1>

<div class="intro">
<h2 id="firstname">Hover Red</h2>
<p id="hometown">Hover Red</p>

<h2>Links:</h2>
<p>Hover Test Red:</p>
<a href="https://www.google.com">google.com</a>
<p>
<b>Note:</b>hello</p>
</div>
</body>

</html>

```

上面的代码定制了

、

# 和

## **在图像上创建悬停不透明度**

```
<html >
<head>
<style type="text/css">
.pic{
width:1900px;
height:1900px;
opacity: 1;
filter: alpha(opacity=100);
background: url(https://cdn.pixabay.com/photo/2013/07/13/11/29/orange-158258_1280.png) no-repeat;
}
.pic:hover
{
opacity: 0.2;
filter: alpha(opacity=30);
}
</style>
</head>
<body>
<div class="pic">
</div>
</body>
</html>

```

上面的 CSS 程序显示了悬停时图像不透明度的修改。图像的原始不透明度为**1**；然而，利用不透明度悬停过滤器相同已被修改为 0.2。这段代码显示，通过使用 hover 元素，可以修改图像和/或文本的不透明度。

## **在图像上创建文本覆盖图**

```
<html >
<head>
<style type="text/css">
.pic{
width:4000px;
height:2170px;
background: url(http://eatlogos.com/food_and_drinks/png/vector_orange_logo.png) no-repeat;
}
.text{
width:3400px;
height:2170px;
background:#FFF;
opacity:0;
}
.pic:hover .text
{
opacity:0.6;
text-align:justify;
color:#000000;
font-size:20px;
font-weight:700;
font-family:"Times New Roman", Times, serif;
padding:30px;
}
</style>
</head>
<body>
<div class="pic">
<div class="text">
Orange is a fibre rich fruit. The anti-oxidants present in an orange can help in digestion, make the skin-glow and act as an anti-aging element.
</div>
</div>
</body>
</html>

```

CSS hover 中的文本分层是将图像的描述性文本嵌入图像本身的有效工具。这个工具有助于提供一个紧凑的图像概览，而不占用有限的网页设计空间的休眠空间。在这段代码中，背景图像嵌入了一个描述性文本，当鼠标指针悬停在该文本上时会显示该文本。

这总结了 CSS 中 hover 的所有重要方面，并强调了它在 web 开发中的可用性。它可以给我们的网页带来许多特殊效果。我们总是可以尝试悬停选择器与其他 CSS 属性的不同组合，如动画、背景图像、超链接等，并探索其潜力，正如我们在一些示例中看到的那样。最后，CSS 是设计和转换网页的最强大的方法之一，因此对于 web 开发人员来说，获得这种技能以构建动态网页迫在眉睫。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“悬停在 CSS 中”博客的评论部分提到它，我们将会回复您。