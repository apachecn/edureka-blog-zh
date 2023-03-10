# 如何实现 CSS 过渡:动画制作正确

> 原文：<https://www.edureka.co/blog/css-transition/>

网页中的动画可以吸引更多的用户。问问你自己——如果你看到一个有很多动画的网页，难道你不想探索更多吗？现在，有了 CSS 转场，你可以用一些很棒的动画让你的作品变得生动起来。而且，请注意，这些都需要做好。让我们按照以下顺序探索 CSS 过渡的世界:

*   [为什么要进行 CSS 转换？](#why)
*   [过渡属性](#transition)
*   [你需要说明什么？](#specify)
*   [过渡-计时-功能功能属性](#timing)
*   [过渡延迟特性](#delay)

## **为什么要进行 CSS 转换？**

让我们举一个例子。如果你要把一个元素的颜色从白色变成蓝色，这种变化几乎是瞬间的。为了获得更生动的效果，您可以让这种变化逐渐发生。这看起来也很吸引人。通过启用 CSS 转换，您可以自定义变化发生的方式。您可以定义元素如何按照加速度曲线以特定的时间间隔发生变化。

CSS 转换让你定义 HTML 元素的变化，特定的时间间隔，加速曲线的速度等等。你可以不使用 Flash 或者 [JavaScript](https://www.edureka.co/blog/javascript-classes/) 来完成所有这些。

为了更好地理解，您可以参考下图:

在上图中，HTML 元素会在一秒钟内从红色变成蓝色。当过渡发生时，您还会看到中间色。如果你不打算使用 CSS 过渡，你会注意到颜色从红色到蓝色的变化是即时的——你不会看到中间色。使用 CSS 转换，当 HTML 元素从旧状态转换到新状态时，您会注意到动画效果。

## **过渡属性**

你可以使用速记转换属性来控制 CSS 转换。使用这种简写方式不仅简单，而且还可以避免不同步的参数，这种不同步的参数在 CSS 中调试起来会非常令人沮丧。

transition-property 指定你想要的过渡效果的 CSS 属性。只有这些 CSS 属性是动态的。

**语法:**

```

transition: <property> <duration> <timing-function> <delay>;

```

![Animations with Transitions](img/4f0113ddeceb3c2fa0e6641f4416bd52.png)

作为初学者，你在使用速记时可能会遇到一些困难。如果您认为现在使用简写对您来说有点复杂，您可以单独指定转换属性。对于 HTML 元素，可以逐个指定过渡属性，如下例所示:

```

<!DOCTYPE html>
<html>
<head>
<style>
div {
width: 100px;
height: 100px;
background: lightblue;
transition-property: width;
transition-duration: 2s;
transition-timing-function: linear;
transition-delay: 1s;
}

div:hover {
width: 300px;
}
</style>
</head>
<body>

<p>Hover over the box </p>

<div></div>

</body>
</html>

```

在上面的例子中，我们已经分别指定了属性(过渡属性、过渡持续时间、过渡定时功能和过渡延迟)及其值。我们将很快了解这些转变特性。

## **你需要说明什么？**

创建 CSS 过渡主要需要指定两件事:想要添加效果的 CSS 属性，以及效果的持续时间。 你需要记住一点——当你没有指定持续时间的时候，转场会取默认值 **0** ，不会有任何效果。

让我们考虑一个例子:

下面的代码定义了持续五秒钟的宽度属性的过渡效果。

```
<!DOCTYPE html>
<html>
<head>
<style>
div{
width: 100px;
height: 100px;
background: blue;
transition: width 5s;
}
div:hover {
width: 600px;
}
</style>
</head>
<body>
<div></div>
<p>Move the cursor over the div element above, to see the transition effect.</p>
</body>
</html>

```

在上面的代码中，您会看到当您将光标悬停在蓝框上时，蓝框会逐渐增加宽度，持续五秒钟。您还会注意到，当您将光标从蓝色框中移开时，蓝色框会逐渐恢复到其原始大小(不是瞬间)。您还可以更改 width 和 time duration 的值，以查看此转换属性如何影响 HTML 元素。

您还可以为多个属性添加过渡效果。您可以通过使用逗号分隔属性来做到这一点。让我们考虑一个例子:

在下面的代码中，为宽度、高度和变换指定了过渡属性。

```
<!DOCTYPE html>
<html>
<head>
<style>
div {
padding:15px;
width: 150px;
height: 100px;
background: green;
transition: width 2s, height 2s, transform 2s;
}
div:hover {
width: 300px;
height: 200px;
transform: rotate(360deg);
}
</style>
</head>
<body>
<div><b>Hello World</b><p> (Hover Over Me)</p></div>
</body>
</html>

```

在上面的例子中，当你将鼠标悬停在绿色方框上时，你会看到它是如何移动的。

我们只指定了属性和持续时间。让我们用各种例子来看看其他参数。

## **过渡计时功能功能属性**

该属性定义了过渡效果的速度曲线。它可以取以下值:

*   **缓动值:**这是默认值，效果开始时慢，然后快，慢慢结束。
*   **线性值:**这种效果不会改变过渡的速度——它从开始到结束都保持速度一致。
*   **渐强值:**这个效果开始时很慢。
*   **缓出值:**这个效果有一个缓慢的结束。
*   **渐出值:**这个效果有慢开始也有慢结束。
*   **三次贝塞尔值(n，n，n，n):** 你可以在三次贝塞尔函数中指定自己的一组值。

下面的代码显示了线性、缓入、缓出和缓出值的过渡效果。

```

<!DOCTYPE html>
<html>
<head>
<style>
div {
width: 100px;
height: 100px;
background: pink;
transition: width 2s;
}

#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}

div:hover {
width: 300px;
}
</style>
</head>
<body>

<p>Hover over the div elements below </p>

<div id="div1">linear</div><br>
<div id="div2">ease</div><br>
<div id="div3">ease-in</div><br>
<div id="div4">ease-out</div><br>
<div id="div5">ease-in-out</div><br>

</body>
</html>

```

## **过渡延迟特性**

有时，您希望动画在一定时间后出现。“过渡延迟”属性允许您指定过渡效果的延迟。您可以指定以秒为单位的延迟。

我们举个例子看看过渡效果的延迟:

```

<!DOCTYPE html>
<html>
<head>
<style>
div {
width: 100px;
height: 100px;
background: yellow;
transition: width 3s;
transition-delay: 1s;
}

div:hover {
width: 300px;
}
</style>
</head>
<body>

<p>Hover over the div element below</p>

<div></div>

<p><b>Note:</b> You can observe that 1 second delay before the effect starts</p>

</body>
</html>

```

在上面的代码中，当您将光标悬停在黄色框上时，您会注意到(有一秒钟)没有任何效果。等待一秒钟后，您会注意到效果。

至此，我们结束了这篇 CSS 转换文章。您现在可以将动画添加到您的网页。试试这些例子。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“CSS 过渡”博客的评论部分提到它，我们会给你回复。