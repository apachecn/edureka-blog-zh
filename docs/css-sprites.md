# 如何实现 CSS 精灵来增强网页

> 原文：<https://www.edureka.co/blog/css-sprites/>

精灵的概念已经存在一段时间了。这是游戏行业中最常用的技术之一，用于加速在屏幕上显示动画的过程。在本文中，我们将按照以下顺序，特别关注这种技术如何帮助我们在 CSS 精灵的帮助下改善用户在网页上的体验:

*   什么是雪碧？
*   什么是 CSS Sprite–快速概述？
*   它如何帮助 Web 开发的例子？
*   [使用 CSS 精灵的优势](#advantage)
*   开发人员在使用 CSS 精灵时需要做什么？
*   [如何创建 CSS Sprite 工作表？](#create)
*   如何使用 CSS 精灵？
*   [使用 CSS 精灵的公司](#companies)

## 什么是雪碧？

精灵是一个单独的图像，是游戏中更大场景的一部分。多个精灵然后被组合成一个大图像，称为精灵表。一旦一个精灵被加载到内存中，不同的精灵会被快速连续的渲染以产生动画的效果。这是为几十到几百个不同的精灵同时完成的，以生成游戏中的一个场景。

![CSS Sprites](img/78a982ec1cab049ac298ff908b8bfb7e.png)

基本思想是，与加载多个图像并显示它们相比，加载一个图像并在任何需要的地方显示它的一部分要快得多。

## 什么是 CSS Sprite:快速概述？

CSS sprite 是 web 开发人员经常使用的一种优化网页性能的技术。在这种技术中，通常尺寸相同的多个较小图像被组合成一个大图像，称为 **子画面** 或 **图块集** 。然后，这个 sprite 工作表用于在我们需要的任何地方显示单个元素。

通常，像徽标、导航箭头、按钮这样的元素都包含在 sprite 工作表中，因为它们几乎具有相同的尺寸，并且经常在网页中使用。

## 它如何帮助 Web 开发的例子？

通常，在设计网页时，图像是作为单独的文件存储和使用的。因此，当用户打开一个网页时，浏览器必须对每个文件发出 HTTP 请求，分别下载并显示它们。这导致更高的页面加载时间，因为一个特定的网页可能有大量的小图像，如按钮，图标，标志。

![How Sprites Helps](img/0066633eb06f19e4de8f346dd38d13eb.png)

CSS 精灵帮助开发者将这些常用的小图片合并成一个大图片。然后，浏览器只需下载一个文件，该文件用于通过偏移图像来显示所需的部分。

## **使用 CSS 精灵的优势**

与普通图像相比，使用 CSS 精灵有两个主要优点:

*   **更快的页面加载:**缩短页面加载时间，因为网页中使用的图像会在页面下载后立即出现。

*   **更高的吞吐量和更低的资源使用率:**这种技术不仅通过加快页面加载速度来改善最终用户体验，而且还通过减少 HTTP 请求数量来减少网络拥塞。

## 开发人员在使用 CSS 精灵时需要做什么？

当处理单个图像时，开发人员可以简单地使用 HTML 标签并在需要时在 CSS 中对其进行样式化。但是当使用 CSS 精灵时，开发人员需要做两件具体的事情:

*   **创建精灵表**

在开发网页时，如果开发者决定使用 CSS sprites，他/她必须首先通过合并所有想要的元素(如按钮、徽标等)来创建 sprite 表。呈网格状。这可以使用任何图像编辑程序来完成，如 Photoshop 或 Gimp。还有许多在线工具可以帮助你制作精灵表。本文稍后将讨论这些工具。

*   **使用 *CSS 背景位置*属性**访问精灵的特定元素

一旦 sprite 工作表准备好了，开发者就必须使用 CSS 属性来访问工作表的不同部分。

*   **宽度:**精灵的宽度
*   **高度:**精灵的高度
*   **背景:**参考雪碧单
*   **背景-位置:**偏移值(以像素为单位)以仅访问 sprite 工作表的所需部分

## **如何创建 CSS Sprite 工作表？**

您可以使用任何图像编辑软件将较小的图像排列成网格，但下面讨论两种更简单的方法:

**1。在线精灵表单创建工具**

链接:[toptal.com/developers/css/sprite-generator/](https://www.toptal.com/developers/css/sprite-generator/)

![Online sprite sheet creation tool](img/719bc3e5b6d248747ef7b347adc46e5e.png)

这个工具不仅可以免费使用，还提供了引用 sprite 工作表时可以使用的 CSS 代码。此外，您可以调整不同的属性，如元素之间的填充和更改它们的对齐方式。

### **2。用精灵**生成精灵表

如果你正在使用 Grunt，Node 或 Gulp，你可以安装一个叫做 Sprity 的软件包，它将帮助你创建一个 sprite 工作表，格式多样，如 PNG，JPG 等。

首先，您需要使用以下命令安装 Sprity:

```
npm install sprity -g

```

然后，要生成 sprite 工作表，请使用以下命令:

```
sprity ./output-directory/ ./input-directory/*.png

```

## 如何使用 CSS 精灵？

在这个例子中，我们将使用下面的精灵表:

![work with Sprites](img/5c9f3fc281752d6f2fc5413809c28362.png)

正如你在上面的图片中看到的，六个图标(Instagram、Twitter 和脸书)被排列成网格状。在第一行中，我们有一个正常状态，在第二行中，我们有他们的悬停状态(当我们将鼠标光标悬停在他们身上时出现的图像)。

如果你用我们上面讨论的工具制作了 sprite sheet，那么你已经知道 CSS 中需要的偏移量，但是如果你用了其他的工具或者你只是得到了一些 sprite sheet，那么不要担心，我们将讨论一种方法来帮助你得到所需元素的偏移量。

现在让我们来看一个非常简单的方法，通过使用 MS Paint 来为六个图标中的每一个获得所需的偏移量。对于精灵来说，这可能不是一个理想的解决方案，但是因为它具有提供鼠标光标坐标的特性，所以它可以用来获得所需的 X 和 Y 坐标。

首先，打开 sprite 工作表图像(包含所有较小图像的网格),将鼠标光标放在要抓取的 sprite 的左上角。

![grid](img/952fc177d85a4afe4cc24c6f24bf8538.png)

一旦获得了 sprite 左上角的坐标(左上角的 Instagram 图像)，就可以使用 CSS 代码在任何需要的地方显示这个特定的 sprite:

`background: url('img_sprites.png');` `background-position:0 0;` `width: 125px;`

我们使用的宽度和高度为 125 像素，因为我们的图标就是这个尺寸。为了获取同一行中的下一张图片(Twitter ),我们使用以下代码:

`background: url('img_sprites.png');` `background-position:-128px 0px;` `width: 125px;`

请注意上面代码片段中的背景位置属性。(-128px，0)意味着我们将 sprite 工作表在 Y 轴上向左偏移 128 像素(考虑元素之间的填充)和 0 像素。如果我们要访问 twitter 悬停图标，那么我们的背景位置属性将是:

`background-position:-128px -128px;`

这样，我们现在可以使用 CSS 访问 sprite 工作表的每个组件。让我们通过一个完整的 HTML 和 CSS 代码来了解如何做到这一点。

**第一步:**编写所需的 HTML 代码

在下面的代码中，我们简单地添加了三个链接。此外，我们将把 HTML 与样式表(screen.css)链接起来。

` <span class="instagram icon"><a href="#">Instagram</a></span>`

` <span class="twitter icon"><a href="#">Twitter</a></span>`

` <span class="facebook icon"><a href="#">Facebook</a></span>`

**第二步:**编写必要的 CSS。首先，我们将设计共享图标类的样式。在这里，你可以看到我们引用了我们创建的 sprite 表。

`/* Shared icon Class */`

`span.icon a:link,`

`span.icon a:visited {`

`  display: block;`

`  text-indent: -9999px;`

`  background-image: url(./img_sprites.png);`

`  background-repeat: no-repeat;`

`}`

步骤 3:使用偏移量从 sprite 工作表中获取单独的图标。

`/* Instagram Icon */`

`span.instagram a:link,`

`span.instagram a:visited {`

`  width: 125px;`

`  height: 125px;`

`  background-position: 0 0;`

`}`

`/* Twitter Icon */`

`span.twitter a:link,`

`span.twitter a:visited {`

`  width: 125px;`

`  height: 125px;`

`  background-position: -128px 0;`

`}`

`/* Facebook Icon */`

`span.facebook a:link,`

`span.facebook a:visited {`

`  width: 125px;`

`  height: 125px;`

`  background-position: -257px 0;`

`}`

**步骤 4:** 使用偏移量从 sprite 工作表中获取悬停图标。

`span.instagram a:hover {background-position: 0 -128px;}`

`span.twitter a:hover {background-position: -128px -128px;}`

`span.facebook a:hover {background-position: -255px -128px;}`

## **使用 CSS 精灵的公司**

业内很多大牌都用 CSS Sprites 来提高自己网站的响应性。谷歌、脸书、亚马逊等公司广泛使用这种方法，因为这有助于他们减少特定用户每次会话的 HTTP 请求数量。当我们考虑到这些公司在任何给定时刻都为数百万客户提供服务时，这是一个巨大的优势。

现在你已经掌握了什么是 CSS 精灵以及如何使用它们，你离学习 CSS 又近了一步。像 sprites 这样的概念是当今时代的游戏规则改变者，因为对于开发者来说，从网页中提取每一点性能变得极其重要。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“HTML 图片”博客的评论部分提到它，我们会给你回复。