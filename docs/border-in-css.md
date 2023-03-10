# 如何在 CSS 中实现不同的边框？

> 原文：<https://www.edureka.co/blog/border-in-css/>

HTML 页面中使用边框来划分和突出显示内容。当一个页面上有大量的信息，而你希望把用户的注意力吸引到特定的部分，那么就在内容周围使用边框。在这篇关于 CSS 中的边界的文章中，我将讨论以下主题:

*   [何时使用边框](#useborder)
*   [CSS 中的边框](#cssborders)
*   [CSS 边框的属性](#attributes)
*   [边框属性的默认值](#defaultvalues)
*   [用速记法定义边框](#shorthand)
*   [在 CSS 中设计边框时要记住的几点](#designborders)

## **何时使用边框**

标准做法是使用 CSS border 标记来定义 HTML 页面中的边框，用于:

*   围绕重要标题
*   突出显示附言或重要注释
*   附上图片、插图、人物语录、视频
*   引起对定价、时间表或此类重要信息的注意

在开始学习 CSS 边框之前，你可能需要阅读一下 [CSS 基础知识](https://www.edureka.co/blog/what-is-css/) 。

欲了解全面的 CSS 教程，请访问 [Edureka CSS 初学者教程](https://www.youtube.com/watch?v=3_9znKVNe5g) 。你将得到一个很好的关于 CSS 如何被用来增强 HTML 网页设计的提示。

## **CSS 中的边框**

CSS 边框可以分配到 HTML 页面的不同部分，无论是包含标题还是段落。先说个例子。这里我们定义了标题周围的一个边框和段落文本周围的另一个边框。

```

<!DOCTYPE html>
<html>
<head>
<style>
body {
background-color: lightblue;
}

h1 {
text-align: center;
border-style: solid;
}

p {
font-family: verdana;
font-size: 20px;
border-style: dotted;
}

</style>
</head>
<body>

<h1>My First Border in the heading</h1>
<p>Border around the paragraph too!</p>

</body>
</html>

```

![Borders in CSS](img/bf7804c0728e030eaf7a622b94f862ab.png)

## **CSS 边框的属性**

CSS 边框有 3 个主要属性

*   **样式:样式属性定义了边框的图案。**
*   **颜色:**颜色可以是 CSS 颜色定义的集合中的任意一种。
*   **宽度:**宽度用于改变边框的粗细，使其更加突出。

在上面的例子中，我们看到只定义了一个 border 属性，那就是它的样式。其他属性在未定义时采用默认值。还有一个属性叫做半径，不太常用。它用于使边框的边缘变圆。

*   ***边框式*** **属性**

| **风格** | **描述** |
| 边框样式:实心 | ![a solid border](img/1355ac9a206f9edb406a2705c4d695fc.png) |
| 边框样式:双 | ![a solid border](img/26282d74f617aff9a61ef92176fec2ab.png) |
| 边框样式:凹槽 | ![groove borders in css](img/6a093cfb1292e436b031157e4b112407.png) |
| 边框样式:山脊 | ![ridge ](img/3325a278a84102dfa07eff599ccc2070.png) |
| 边框样式:嵌入 | ![inset border in css](img/aec8a194d7374f3dfdf5088202dd2ef9.png) |
| 边框样式:开头 | ![outset border in css](img/47c243109113ca5a706180c924badd66.png) |
| 边框样式:无 | ![no border](img/f024cfe95c856a040699c84066d724fb.png) |
| 边框样式:隐藏 | ![hidden border](img/eab197ec41cea02bdae2ea2722a213ce.png) |
| 边框样式:虚线 | ![dotted borders in css](img/dcaada4504c52a1ca63a72d56fec201f.png) |
| 边框样式:虚线 | ![dashed border](img/78d6cbf2f6606304d5a8d2492b6c7e72.png) |

你会注意到有一个“无边框”和“隐藏边框”选项。一个开发者可以简单地避免定义一个边框，为什么要明确地定义为“隐藏边框”？这样做是为了空间使用和与页面中的其他元素对齐。

边框样式也可以在一个元素中混合。为此，可以用不同的样式分别定义 4 个单独的边界边。这可以通过两种方式实现。要么在一个标签中定义所有 4 个边。在这种情况下，计数从顶行开始，然后顺时针移动。或者，4 条边界线中的每一条也可以在单独的标签中定义。下一个示例显示了这两种情况。

| **风格** | **描述** |
| **border-style: dotted dashed solid double**border-top-style:点线；border-right-style:虚线；border-bottom-style:实心；border-left-style:double； | ![mixed ](img/3872a27d7db247d75f8f1bee44308375.png) |

*   ***边框颜色*** **属性**

可以通过多种方式设置边框的颜色属性。这类似于为其他元素设置颜色。可以通过以下方法之一设置颜色:

*   **名称**–指定颜色名称，如“蓝色”。你也可以尝试一些花哨的颜色选项，如“BlanchedAlmond”！
*   **十六进制**–指定一个十六进制值，如“# ff 0000”
*   **RGB**–设置 RGB 代码。例如，rgb(255，255，0)表示黄色。
*   **设置**——如“透明”或“不透明”

*   ***边框宽度*** **属性:**

顾名思义，width 属性定义了 4 个边框的宽度。如果定义了一个值，则该值适用于所有边，否则也可以设置单独的宽度值。

宽度可以用任何标准单位指定，如像素(' px ')、磅(' pt ')或厘米(' cm ')。您还可以使用预定义的值“厚”、“薄”和“中”来指定宽度。

| **风格** | **描述** |
| **边框宽度:10px** | ![10px-borders-in css](img/7454d55fdb21181280e284602380f61a.png) |
| **边框宽度:0.1cm** | ![0.1cm](img/f2d2744bf8f6f3ca0f01da5742ffde0b.png) |
| **边框宽度:中等** | ![medium-width](img/8e585a709378668063e8f0da53ce1f8c.png) |

*   **属性**

定义半径的目的是为边界获得圆角。半径因子定义了圆度的范围。该值越大，拐角越弯曲。作为标准做法，半径值保持在边框宽度的 1-3 倍之间。

以下代码将生成:

边框宽度:10px 边框-半径:30px

![round](img/6eb5425f93ee26c452c31f4355e4d05d.png)

## **边框属性的默认值**

*   唯一的强制属性是 **风格** 。如果缺少样式，边框将不会出现。

*   如果未指定颜色，则底层元素的颜色将被视为默认值。例如，如果一个段落的文本颜色被定义为“蓝色”，那么默认的边框颜色也将是蓝色。如果元素没有颜色定义，则默认颜色为“黑色”。

*   宽度的默认值为“中等”。

## **用速记法定义边框**

一些开发人员喜欢在一个简洁的单行标签中定义边框属性。这种简写格式有助于最大限度地减少代码行，专业开发人员更喜欢这种格式。当边界定义简单且相当标准化时，建议使用简写格式。但是，如果您需要以不同的样式突出显示边框的每一侧，那么您需要坚持定义单个标签的格式。

使用了以下代码:

边框样式:虚线；边框颜色:绿色；边框宽度:5px 边框:虚线绿色 5px

![green borders in css](img/58c72ab907a76c0a411a4b5880420b38.png)

## **在 CSS 中设计边框时要记住的几点**

*   不要在一个页面上使用太多的边框，这会分散注意力，让用户难以集中注意力。

*   保持边框样式和颜色的一致性很重要。为了统一，页面中同一层级的元素必须具有相似的边框样式和宽度。例如，如果 *段落* 被定义为实线边框和 5px 宽度，那么在网站设计期间，在其他 *段落* 元素中保持这种格式。

*   坚持一种风格的标签定义。一些开发人员习惯于将所有值赋给单个 ***边框*** 标签的快捷方式定义。还有一些人喜欢明确列出宽度、颜色和样式的所有标签。惯例是，当页面需要复杂的边框装饰时，单独的标签会单独列出。这有助于调试这种定制的边界定义。对于正常情况，只需要一个快捷的定义就可以了。

希望你在 CSS borders 上找到了你要找的信息，至此，我们结束了这篇 CSS Borders 文章。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在“CSS 中的边界”博客的评论部分提到它，我们会给你回复。