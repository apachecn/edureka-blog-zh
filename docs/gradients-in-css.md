# 你所需要知道的关于 CSS 中的渐变

> 原文：<https://www.edureka.co/blog/gradients-in-css/>

颜色渐变指定位置相关颜色的范围，通常用于填充区域。这是美化和给你的内容添加主题的一个非常重要的方面。让我们按照以下顺序理解如何在 [CSS](https://www.edureka.co/blog/backgroung-image-in-css/) 中实现渐变:

*   [CSS 中的渐变是什么？](#what)
*   [CSS 中的渐变类型](#types)
*   [线性渐变](#linear)
*   [径向梯度](#radial)

## **CSS 中的渐变是什么？**

如果我们想设计网页风格，那么 CSS 有能力做到。它广泛应用于网站开发中，将一个简单静态的网页转换成一种全新的形式。它为我们提供了各种可供探索的特性。

在这篇文章中，我们将看看 CSS 中的渐变。CSS 中的渐变允许我们在属性中指定的两种或多种颜色的组合之间呈现平滑的过渡。渐变是借助浏览器创建的图像。因此，这也为在网页中设置背景提供了另一种方式。

## **CSS 中的渐变类型**

*   **线性渐变:** 由它们的方向定义，即上、下、左、右等。

*   **径向渐变:** 由中心位置定义

*   **重复线性渐变:** 以重复方式执行的线性渐变

*   **重复径向渐变:** 以重复方式执行的径向渐变

**注意:** 所有浏览器都支持 CSS 渐变语法。但是，有一些较旧的浏览器不支持它们，如旧的 Mozilla 或 Safari 浏览器(直到版本 8.0)。因此，需要添加前缀“-webkit-”或“-moz-”(取决于浏览器)以使浏览器解释渐变属性语法。

## **CSS 中的线性渐变**

线性渐变可能是 CSS 中使用最广泛的渐变之一，在设计网页时常见。它需要至少两种颜色来形成渐变。这些颜色以线性格式排列(例如从上到下或从左到右)，然后以平滑过渡的方式呈现。

有很多方法可以让我们产生渐变效果，我们将会详细探讨。

CSS 的**linear-gradient()**属性用于创建线性渐变，然后设置为背景图片。

该属性的可能值为:

*   **侧面或方向:**表示渐变应该渲染的方向。

*   **颜色列表:** 这是由两种或两种以上颜色组成的颜色列表，颜色之间用逗号隔开。这些颜色用于渲染平滑过渡。该参数接受所有类型的颜色语法，即名称、十六进制、RGB 或 HSL。

**语法:**

```
background-image: linear-gradient(<side or direction>, < color_list > ...);
```

**举例:**

```
<html>
<head>
<style>
.gradient {
height: 300px;
background- image: linear-gradient(to bottom, green, blue);
}
</style>
</head>
<body>
<div class="gradient"/>
</body>
</html>

```

**输出:**

![linear gradient](img/00bf5fdfc26203a352723b2a793b6900.png)

**线性渐变的类型**

现在让我们探索各种类型的线性渐变:

*   **从上到下–线性渐变:** 这是渐变图案的默认形式。它从一种颜色开始，然后过渡到另一种颜色。

例如，在这里我们可以看到，颜色从蓝色开始，然后向蓝绿色过渡。

```

<html>
<head>
<style>
.gradient {
height: 300px;
background-image: linear-gradient(blue, turquoise);
}
</style>
</head>
<body>

<div class="gradient"></div>

</body>
</html>

```

**输出:**

![top-bottom](img/22832641401e7ecfe1fca98887024cc2.png)请注意，这里我们没有指定方向；CSS 将其解释为默认，即**从上到下。**

*   **从左到右–线性渐变:** 我们也可以通过在方向属性中指定“到右”值来改变渐变从左到右的方向。类似地，这也可以通过指定“向左”来从右向左反转。

在这里，过渡从左侧开始，以蓝色开始，然后以蓝绿色平滑地向右移动。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: linear-gradient(to right, blue, turquoise);
}
</style>
</head>
<body>
<div class="gradient"/>
</body>
</html>

```

**输出:**

![left-right](img/7c5809242f7432452d028bfa676235b6.png)

*   **对角线-线性渐变:** 渐变也可以通过调整方向并在参数值中指定水平和垂直位置来进行对角线遍历。

例如:向左上方、向左下方、向右上方、向右下方等。

这里，颜色从紫色开始，从左侧开始，沿对角线向上移动到橙色。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: linear-gradient(to top left, purple, orange);
}
</style>
</head>
<body>
<div class="gradient"/>
</body>
</html>

```

**输出:**

![diagonal](img/2f0433cc5446f0c34c9f5057c8896512.png)

*   **角度-线性渐变** :渐变的方向也可以通过指定角度(以度为单位)来控制。这允许我们通过定制过渡而不是提供正常方向，以更精确和更有组织的方式创建模式。

这里的渐变从红色开始，以蓝色移动 45 度。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: linear-gradient(45deg, red, blue);
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![angles](img/c6568bbca89360d9f36746a342932859.png)**

*   **在渐变中使用多种颜色:** 正如我们在定义线性渐变时看到的，我们可以拥有任意多的逗号分隔的颜色。这些多种颜色可用于形成多彩的渐变。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image:linear-gradient(to left, blue, green, red, yellow, orange );
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![multiple-gradients-in-css](img/82b1d0fc5f2a5f49211c3d5a53e3006d.png)**

我们也可以通过陈述颜色的起始点来定义我们想要多少特定的颜色。这些点被称为颜色停止点，因为它们声明了前一个颜色的停止点。

**例如:**如果我们想要一个渐变，其中蓝色应该是最大的，而绿色只在开始的大约 20%，那么我们可以让颜色停止在 20%，蓝色可以从那个点继续。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image:linear-gradient(to right, green, blue 20%);
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![multiple-2](img/95c63d84b5564efc4507ac277eaef7f1.png)**

*   **线性渐变中的透明度:**在 CSS 渐变中创建渐变效果的一个很好的方法就是使用透明度。在定义颜色时，可以使用 rgba()将其添加到渐变中。rgba()接受四个参数，即红色、蓝色、绿色代码和一个表示透明度的附加数字参数(范围从 0 到 1)。值 0 表示完全透明，而值 1 表示不透明。

这里有一个例子，显示了从上到下的线性渐变，并逐渐从透明变为蓝色。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: linear-gradient(to bottom, rgba(0,0,255,0), rgba(0,0,255,1));
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![transparency-gradients-in-css](img/7f9831be0da46a22fd9f9b8d9ec94c76.png)**

让我们看看另一种使用透明度创建线性渐变和使用色标创建多种颜色的方法。

```
body {
background-color:#001;
background-image: linear-gradient(white 15%, transparent 16%),
linear-gradient(white 15%, transparent 16%);
background-size: 60px 60px;
background-position: 0 0, 30px 30px;
}
```

**输出:![transparency-2](img/82ac408adca256b9bd6d7f8b306bfa0d.png)**

*   **重复线性梯度**

这是一个线性梯度，在每个周期重复。这种渐变的重复方式让 in 更有吸引力。

让我们修改上面看到的代码，看看重复线性渐变的区别

```
body {
background-color:#001;
background-image: repeating-linear-gradient(white 15%, transparent 16%),
repeating-linear-gradient(white 15%, transparent 16%);
background-size: 60px 60px;
background-position: 0 0, 30px 30px;
}
```

**输出:![repeating-linear-css](img/ad20ddb1373216de7a4c1810a69b773c.png)**

## **径向梯度**

CSS 中的径向梯度是那些从中心出现的梯度。它还需要至少两种颜色，并且从中心到边缘发生过渡。这些颜色以线性格式排列(例如，从上到下或从左到右)，然后以平滑过渡呈现。因为梯度本质上是径向的，所以它产生的形状大部分是圆形，如圆形或椭圆形。

CSS 的**radial-gradient()**属性用于创建径向渐变，然后设置为背景图片。

语法:

```
background-image: radial-gradient(<shape and size>, starting color, …. , ending color);

```

**形状** :该参数决定了从一种颜色向外过渡到另一种颜色时形成的圆形渐变的形状。例如圆形或椭圆形。

**大小** :定义渐变的大小，确定渐变的结束形状——基于形状的中心。它具有以下可能的值。

*   **-最近的角**-渐变在最靠近形状中心的角结束。
*   **最远角**–这与最近角正好相反，即渐变在离形状中心最远的角结束。
*   **-最近侧**-渐变终止于最靠近形状中心的一侧。
*   **最远侧**–这与最近侧完全相反，即渐变从形状的中心结束到最远侧。

形状的默认参数值是椭圆，大小是最远角，位置是中心。

让我们看一个径向梯度的例子:

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: radial-gradient(blue, red);
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![radial-gradients-in-css](img/1becdf17012ca88871afa1ec41b99083.png)**

*   **圆形-放射状渐变:** 这种渐变是一个圆形，只渐变到另一种颜色

现在，既然我们已经为尺寸指定了一个值，它将淡出到形状的。

```
<html>
<head>
<style>
.gradient {
height: 300px;
background-image: radial-gradient( circle closest-side, cyan, orange);
}
}
</style>
</head>
<body>
<div class="gradient"></div>
</body>
</html>

```

**输出:![circle-gradient](img/1d57d05f691e3eec6f134a472bfea425.png)**

*   **重复径向梯度**

这是一个径向梯度，在每个周期重复。这种梯度的重复产生了诱人的图案。

```
body {
background-color:#001;
background-image: repeating-radial-gradient(white 15%, transparent 16%),
repeating-radial-gradient(white 15%, transparent 16%);
background-size: 60px 60px;
background-position: 0 0, 30px 30px;
}
```

**输出:![repeating-radial-css](img/e26f2cc77c9d93d056988360c37764de.png)**

至此，我们结束了这篇 CSS 渐变文章。我希望你现在已经了解了我们如何在 CSS 中实现不同类型的渐变。

*既然你已经了解了 CSS 中的渐变，那就去看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

有问题要问我们吗？请在“CSS 中的渐变”的评论部分提到它，我们会给你回复。