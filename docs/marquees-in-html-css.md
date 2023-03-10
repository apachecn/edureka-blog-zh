# 如何在 HTML 和 CSS 中实现样式选择

> 原文：<https://www.edureka.co/blog/marquees-in-html-css/>

字幕是创建滚动、跳跃或滑入文本和图像的标准方法。就 HTML 和 CSS 而言，这是一个非常重要的方面。让我们按照以下顺序开始 HTML 和 CSS 中的 Marquees 之旅:

*   什么是侯爵？
*   [HTML 字幕](#HTMLMarquees)
*   [CSS 字幕](#CSSMarquees)
*   [滚动文字](#ScrollingText)
*   [滑入文本](#Slide-InText)
*   [从左到右](#LefttoRight)
*   [垂直滚动](#ScrollVertically)
*   [弹跳文字](#BouncingText)
*   [在 CSS 中创建字幕的另一种方法](#AnotherwaytocreateMarqueeinCSS)
*   [HTML 字幕 vs CSS 字幕](#HTMLMarqueesvsCSSMarquees)

## 什么是侯爵？

Marquee 是一种特殊效果，用于在 HTML 网页中横向和纵向移动或滚动内容。内容可以是网页中的任何内容，如一些文本或图像。

可以使用 HTML 标签和 CSS 属性来设置字幕。

## **HTML 字幕**

HTML <字幕>标签用于创建和设置字幕样式。 使用 marquess 创建滚动文本的 HTML 语法是

```
<marquee attribute_name = "attribute_value" attribute_name_2 = "attribute_value_2" ..... >
		Text or Image to Scroll
</marquee>

```

```
<html>
    <body>
        <marquee>Scrolling Marquee</marquee>
    </body>
</html>

```

可以和<marquee>标签一起使用的属性值可能是:</marquee>

*   **宽度**–表示字幕的宽度。例如 20%、40%、50%等。宽度的默认值是 100%

```
<html>
    <body>
        <marquee width = "50%">Scrolling Marquee with 50% width</marquee>
    </body>
</html>

```

*   **高度**–表示字幕的高度。例如 20%、50%等。高度的默认值是内容的自然高度。

```
<html>
    <body>
        <marquee height = "50%">Scrolling Marquee with 50% height</marquee>
    </body>
</html>

```

*   **方向**–它表示我们希望字幕滚动的方向。它的值是向上、向下、向左或向右。方向的默认值是向左，即字幕从右边开始向左移动。

```
<html>
    <body>
        <marquee direction = "right">Marquee moving left to right</marquee>
    </body>
</html>

```

*   **行为**–表示内容的滚动类型。该属性的可能值是、滚动、滑动和交替。例如的值，如滚动、滑动和交替。

```
<html>
    <body>
        <marquee behavior = "alternate">Scrolling Marquee with alternate behavior</marquee>
    </body>
</html>

```

*   **scroll delay**–这表示每个字幕显示之间的延迟。以毫秒为单位分配的延迟量。该属性的默认值为 85。

```
<html>
	<body>
		<marquee scrolldelay = "200">Marquee with scrolldelay</marquee>
	</body>
</html>

```

*   **scrollamount**–这表示内容或字幕文本的速度。它的值可以是 10、20 等。该属性的默认值为 6。属性 scrolldelay 和 scrollamount 一起使用时，可以很好地控制字幕的速度和显示。

```
<html>
    <body>
        <marquee scrollamount = "200">Marquee with scrollamount </marquee>
    </body>
</html>

```

*   **bgcolor**–该属性设置字幕的背景颜色。颜色可以指定为颜色名称或颜色十六进制值。

```
<html>
    <body>
        <marquee bgcolor = "cyan">Marquee with bgcolor</marquee>
    </body>
</html>

```

*   **循环**–该属性指定一个字幕应该循环的次数。默认情况下，marquee 无限循环，因此它的默认值是无穷大。

```
<html>
    <body>
        <marquee loop = "2">Marquee with loop</marquee>
    </body>
</html>

```

*   **hspace**–该属性指定字幕左右的水平间距。它的值可以是 20%、40%等。

```
<html>
    <body>
        <marquee hspace = "20">Marquee with hspace</marquee>
    </body>
</html>

```

*   **vspace**–该属性指定字幕顶部和底部的垂直间距。它的值可以是 20%、40%等。

```
<html>
    <body>
        <marquee vspace = "20">Marquee with vspace</marquee>
    </body>
</html>

```

继续这篇关于在 HTML 和 CSS 中设置字幕样式的文章

## **CSS 字幕**

CSS 字幕是创建字幕的标准方式。通过提供更多滚动文本内容和图像的功能，它们正在取代 HTML 字幕。

CSS 中的字幕是使用 CSS animation 属性和@keyframes 来操作元素和创建动画而创建的。

此外，我们需要使用 translateX()和 translateY()来指定滚动内容的路径。使用这种方法的好处是它完全符合 CSS 标准。

## **滚动文字**

这里 translateX()用于指定动画开始和结束时的内容位置。在整个动画过程中，它一直在起点和终点之间移动。

```
<html>
<style>
.cssmarquee {
height: 50px;
overflow: hidden;
position: relative;
}
.cssmarquee h1 {
font-size: 2em;
color: turquoise;
position: absolute;
width: 100%;
height: 100%;
margin: 0;
line-height: 50px;
text-align: center;
transform:translateX(100%);
animation: cssmarquee 10s linear infinite;
}
@keyframes cssmarquee {
0% {
transform: translateX(100%);
}
100% {
transform: translateX(-100%);
}
}
</style>

<div class="cssmarquee">
<h1>Eurekaaa..Scrolling Text </h1>
</div>
<html>

```

## **滑入文本**

当可以通过将 translateX()值设置为零或任何正值并移除动画的无限设置来使内容滑入。这里我们也使用了动画的缓出，因为我们需要在文本最终停止之前减慢它的速度。

```
<html>
<style>
.cssmarquee {
height: 50px;
overflow: hidden;
position: relative;
}
.cssmarquee h1 {
position: absolute;
width: 100%;
height: 100%;
margin: 0;
line-height: 50px;
text-align: left;
animation: cssmarquee 5s ease-out;
}
@keyframes cssmarquee {
0% {
transform: translateX(200%);
}
100% {
transform: translateX(0%);
}
}
</style>

<div class="cssmarquee">
<h1>Eurekaaa..Slide-In Text </h1>
</div>
<html>

```

## **从左到右**

为了使文本内容以相反的方向滚动，即从左到右，我们应该反转 translateX()的值

```
<html>
<style>
.cssmarquee {
height: 50px;
overflow: hidden;
position: relative;
}
.cssmarquee h1 {
position: absolute;
width: 100%;
height: 100%;
color: turquoise;
margin: 0;
line-height: 50px;
text-align: center;
/* Starting position */
transform:translateX(-100%);
animation: cssmarquee 10s linear infinite;
}
@keyframes cssmarquee {
0% {
transform: translateX(-100%);
}
100% {
transform: translateX(100%);
}
}
</style>

<div class="cssmarquee">
<h1>Eurekaa....Left to Right... </h1>
</div>
</html>

```

## **垂直滚动**

为了使内容垂直滚动，我们需要使用 translateY()而不是我们在前面的例子中使用的 translateX()..

```
<style>
.cssmarquee {
height: 200px;
overflow: hidden;
position: relative;
}
.cssmarquee h1 {
position: absolute;
color: turquoise;
width: 100%;
height: 100%;
margin: 0;
line-height: 50px;
text-align: center;
transform: translateY(-100%);
animation: cssmarquee 10s linear infinite;
}
@keyframes cssmarquee {
0% {
transform: translateY(-100%);
}
100% {
transform: translateY(100%);
}
}
</style>

<div class="cssmarquee">
<h1>Eurekaa..Scrolling down... </h1>
</div>

```

## **弹跳文字**

这用于使内容像弹跳球一样来回移动。为了渲染内容中的反弹性质，我们需要在动画属性的末尾添加替换。稍后我们还可以修改 translateX()的值，这样内容就不会跳出页面。

```
<html>
<style>
.cssmarquee {
height: 50px;
overflow: hidden;
position: relative;
}
.cssmarquee h1 {
position: absolute;
color: turquoise;
width: 100%;
height: 100%;
margin: 0;
line-height: 50px;
text-align: left;
animation: cssmarquee 2s linear infinite alternate;
}
@keyframes cssmarquee {
0% {
transform: translateX(70%);
}
100% {
transform: translateX(0%);
}
}
</style>

<div class="cssmarquee">
<h1>Eurekaa...Bouncing text... </h1>
</div>
<html>

```

## **在 CSS 中创建字幕的另一种方法**

marquee-style 属性是在 CSS 中设置字幕样式的另一种方式。它提供了在内容中滚动、弹跳或滑动的能力。然而，这种方法并没有被广泛使用，建议使用早期的方法。

可以与 CSS 字幕一起使用的可能参数有:

*   **scroll:** 这表示内容应该从元素的一端滚动到另一端。一旦它到达另一边，内容消失，然后再次开始滚动。这是字幕的默认值。

*   **slide:** 这使得内容从元素的一端开始滑动，并继续滑动，直到到达另一端，所有的内容都显示出来。

*   **交替:**这使得内容从元素的一端滚动到另一端，然后使其来回反弹。

*   **initial:** 设置属性的默认值。

*   **inherit:** 设置从父元素继承的值。

*   **无**:不移动内容。

虽然所有浏览器都支持字幕，但它们是一些基于 webkit 的旧浏览器，可能不支持此属性。因此，需要添加前缀 webkit 来解释这些旧浏览器中的侯爵。例如 webkit-marquee-style。

继续这篇关于在 HTML 和 CSS 中设置字幕样式的文章

## **HTML 字幕 vs CSS 字幕**

*   HTML 字幕是使用<marquee>标签定义的。这种方法为我们提供了一种快速的方法来创建字幕，并轻松地将它们添加到我们的网页中。标签有一些特殊的属性，可以创建滚动的文本和图像。这种用 html 编码的风格使得代码易于阅读，并且可以在很短的时间内创建字幕。</marquee>

*   使用 HTML marquee 或<marquee>标签的问题是它不完全符合官方 HTML 标准。因为<marquee>标签不是 HTML 规范的一部分，所以如果我们想要创建完全兼容的 HTML 网页，我们应该使用 CSS 字幕而不是 HTML 字幕。</marquee></marquee>

*   CSS 字幕符合官方的 CSS 规范。它内部使用 CSS 动画，也包括在 CSS 规范中，因此，它允许我们使用字幕创建完全兼容的网页。

*   此外，CSS 字幕更强大，并提供了更多的高级功能来创建和设计我们的字幕。然而，这些类型的字幕的缺点是它们需要相对较长的编码时间，并且对于初学者来说很复杂。

**举例:**

**HTML 字幕滚动**

```
<marquee behavior="scroll" direction="left">
    <h1>HTML text scrolling...</h1>
</marquee>

```

**CSS 滚动字幕**

```
<html>
    <style>
.cssmarquee {
 height: 50px;  
 overflow: hidden;
 position: relative;
}
.cssmarquee h1 {
 font-size: 2em;
 color: turquoise;
 position: absolute;
 width: 100%;
 height: 100%;
 margin: 0;
 line-height: 50px;
 text-align: center;    
 transform:translateX(100%);
 animation: cssmarquee 10s linear infinite;
}

@keyframes cssmarquee {
 0%   { 
 transform: translateX(100%);       
 }
 100% { 

 transform: translateX(-100%); 
 }
}
    </style>

    <div class="cssmarquee">
        <h1>CSS..Text Scrolling </h1>
    </div>
</html>

```

从上面的例子中我们可以清楚地看到，两个例子展示了相似的结果。然而，用 CSS 创建滚动文本稍微复杂一些，需要更多的代码。另一方面，使用 CSS marquees 的好处是，它为我们提供了更多的功能来设计我们的滚动内容，并使我们的浏览器完全适应各种浏览器。

这总结了 HTML 和 CSS 中关于字幕的所有内容。它提供了一个很好的方式来设计我们内容中的动画，无论是文本还是任何图像。我们应该利用它提供的所有选项，创建不同的字幕行为。对于 web 开发人员来说，详细了解动画和字幕非常重要。这有助于创建动态内容网页。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“HTML 中的 Marquees”博客的评论部分提到它，我们会给你回复。