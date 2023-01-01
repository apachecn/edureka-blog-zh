# 如何在 Tableau 中使用圆环图

> 原文：<https://www.edureka.co/blog/donut-chart-in-tableau/>

当我们让观众以最少的努力获得最大的洞察力时，就实现了伟大的 ***形象化*** 。这正是我们通过这篇关于 Tableau 中 ***圆环图的文章想要达到的目的。这里的主要目的是帮助你利用环形图作为 Tableau 中的一个工具，不仅用于参与，而且用于理解效率。***

让我们从回答以下问题开始:

*   [**什么是圆环图？**](#WhatisaDoughnutChart)

*   [**饼状图&甜甜圈图有什么区别？**](#differencebetweenthePieChartDoughnutChart)

*   [**甜甜圈图有什么好处？**](#benefits)

*   [**如何在 Tableau 中建立一个圆环图？**](#doughnutchartintableau)

*   [**甜甜圈图有哪些陷阱？**T3**T5**](#pitfalls)

## 什么是圆环图？

要理解什么是环形图，我们首先需要了解它的前身 ***饼状图*** 。

### **那么，什么是饼图呢？**

饼图是圆形的统计图或可视化，它被分成若干个切片来说明数字比例。在饼图中，每个切片的弧长与其代表的数量成比例。

![pie chart - doughnut chart in tableau - edureka](img/04112ec54489abb0ddda8751d4aec1ff.png)

### 但是饼状图有一个问题。

现在，饼状图经常受到批评，因为它将观众的注意力吸引到切片面积的比例上，并煽动他们相互比较以及与整个图表进行比较。这使得很难看出切片之间的差异，尤其是当您试图一起比较多个饼图时。

圆环图通过减少对该区域的使用在一定程度上解决了这个问题。

***圆环图本质上是一个中心区域被切掉的饼图。【T2***

在圆环图中，读者通常会关注弧线的长度，而不是比较各部分之间的比例。此外，圆环图比饼图更节省空间，因为里面的空白空间可以用来显示数据。

但是我们需要了解的是关于环形图，或者更确切地说是这两个图，是什么带来了差异。答案在于我们对它们的看法有多么不同。

[https://www.youtube.com/embed/Ia_Ou12QFJ4](https://www.youtube.com/embed/Ia_Ou12QFJ4)

## **饼状图&甜甜圈图有什么区别？**

你可能以前见过饼状图——大圆，切块，不能错过。圆环图本质上是一样的，除了它在中间有一个稍微小一点的圆形切口，将填满的饼图变成一个空心的圆环。让我们让你们都轻松一点。这是他们两个并排的照片。

看起来差别很小，但是移除 Timbit 后会发生一些重要的事情，这揭示了人类大脑和视觉感知的复杂性。

让我们明白这一点。

继续看上面的饼状图。注意你看它的方式——很可能，你的眼睛正好看向中心，并且(至少一开始)你看到了整个饼状图。

因为饼状图是填出来的，你是从整体来看的；你看到圆圈，根据它们的面积来判断棋子。

然后是这张环形图。因为甜甜圈图是镂空的，没有中心点吸引你的注意力。你的眼睛转到哪里去了？

如果像大多数人一样，你的眼睛环绕周线，根据每个棋子的长度来判断每个棋子。因此，您也可以将圈饼图视为本身已卷曲的堆叠条形图。

***那么，这有什么关系呢？***

为什么看东西是看面积还是看长度很重要？嗯，  我们的大脑处理这两种属性的方式不同——*，我们只擅长其中一种*。

人类特别擅长判断直线距离。你可以很容易地分辨出某物是更高、更宽、更长、更短；一维比较非常简单。

除非差异非常明显，否则区域划分并不容易。你可能需要一点时间来比较不同大小的物体。

我的观点是，当读者看到一个被细分成多个部分的圆圈时，他们会想要比较这些部分的大小，即使这不是你的目标。

当你看到饼状图时，比较大小是一种自动行为。

那么，圆环图提供了什么呢？

**了解我们在顶级城市的 Tableau 培训课程**

| 印度 | 美国 | 其他热门城市 |
| [班加罗尔的 Tableau 培训](https://www.edureka.co/tableau-certification-training-bangalore) | [达拉斯的 Tableau 球场](https://www.edureka.co/tableau-certification-training-dallas) | [华盛顿的 Tableau 课程](https://www.edureka.co/tableau-certification-training-washington) |
| [海德拉巴的 Tableau 培训](https://www.edureka.co/tableau-certification-training-hyderabad) | [夏洛特的 Tableau 课程](https://www.edureka.co/tableau-certification-training-charlotte) | [奥斯汀的 Tableau 课程](https://www.edureka.co/tableau-certification-training-austin) |
| [金奈的 Tableau 培训](https://www.edureka.co/tableau-certification-training-chennai) | [纽约的 Tableau 课程](https://www.edureka.co/tableau-certification-training-new-york-city) | [西雅图的 Tableau 课程](https://www.edureka.co/tableau-certification-training-seattle) |

甜甜圈图有什么好处？

两件事——***清晰度&空间效率*** 。

**透明度**

饼图实际上提供了三个独立的选项。你比较角度的比率，每个楔形或切片的面积比率，或者最后你可以使用外圆周的长度。圆环图只提供了后者，尽管它给了你一个内外边缘。

前面提到的饼状图的复杂性很少是一个好处。一个典型的观众将包含个人谁喜欢这三种方法中的每一种。这使得饼图失真比人们意识到的要普遍得多。

甜甜圈也会变形。只是更容易避免。只要边长保持一个固定的比率(没有倾斜的视图)，图表应该保持真实的数据。

**空间效率**

答案才是重点。正如上一节提到的，两个图表的中心吸引了观众的目光。所以用吧！圆环图中的空白区域非常适合用于总计、提升比较或趋势箭头。老实说，你应该能够完全符合这三个条件！

## **如何在 Tableau 中建立一个圆环图？**



<article>

本博客将详细介绍如何使用样本超市数据在 [***Tableau***](https://www.edureka.co/blog/what-is-tableau/) 中制作一个圆环图。要在 Tableau 中创建一个圆环图，我们首先需要知道我们想要分离和测量的维度，以定义比例。

因此，在这种情况下，可以使用“类别”作为维度，使用“销售额”作为度量。以下是在 Tableau 中创建圆环图的步骤:

1.连接到 Sample-Superstore 数据集:打开 Tableau 桌面并选择“Sample-Superstore”数据集

2.转到  **工作表 1** :

3.在**标记**的卡片中，选择图表类型为饼图

4.将“**类别**字段拖至“颜色”，将“销售”度量拖至“尺寸”&“标签”标志卡

5.现在，将**条记录**拖动到“行”架上

![Put the number of records on the row shelf - donut chart in tableau - edureka](img/1a135546d0a2c3c684ff81bf6829136f.png)

6.选择“行”架中的“**记录数”** 字段，并将默认汇总从“总和”更改为“最小值”

7.同样，从 measures 中拖动“Number of Records ”(记录数),并将其放在第一个“Number of Records ”(记录数)之后的“Rows ”(行)架上

8.对于“记录数”的第二个副本，也将默认聚合从“总和”更改为“最小值”

9.右键单击“**记录数量**字段的第二个副本，并选择“双轴”选项

![dual axis doughnut charts- doughnut chart in tableau - edureka](img/a6a302463608fda4ffb3905b7250292c.png)

10.在下一步中，选择“标记”卡中的“ **Min(记录数)(2)** ”，并删除以下内容: a .【颜色】中的“类别” b .【尺寸】和“标签”中的“销售”

11.再次选择“标记”卡中的“最小(记录数)(2)”，缩小饼图的尺寸，然后选择与背景颜色相同的饼图颜色(本例中为“白色”)

![single doughnut chart - doughnut chart in tableau - edureka](img/2336dcb0fe717e8c7c91fd49f17bbcdc.png)

12.最后一步，右键单击每个轴，并取消选择“**显示标题**

13.这就是环形图在 Tableau 中的样子。

![final doughnut chart - doughnut chart in tableau - edureka](img/23c71d0eb4800f4a9296df54dc28e74e.png)

**What are the pitfalls of a Donut Chart?**

当然，Tableau 中的甜甜圈图仍然有其缺点——虽然更容易阅读  ，但对于同一图表内的比较而言， ***仍然不是最棒的*** ，对于两个不同图表之间的比较而言更是糟糕透顶。

到 ***弥补*** 对于这种不足，我更喜欢在一个完整的仪表盘或一组图表中使用这些图表。但是那张单独的图表无法传达出具有可操作性或令人满意的深度信息。

</article>



所以，回到我最初的呼吁，视觉化是一门艺术。思考不是固定的规则。平衡、风格和创造力也应该是你的武器库的一部分。所以，继续画吧！

*如果你希望掌握 Tableau，Edureka 有一个关于 **[Tableau 认证](https://www.edureka.co/tableau-certification-training)** 的策划课程，该课程深入涵盖了数据可视化的各种概念，包括条件格式、脚本、链接图表、仪表板集成、Tableau 与 R 的集成等等。它提供 24*7 支持，在整个学习期间为您提供指导。新的批次即将开始。*

*有问题吗？请在评论区提到它，我们会尽快回复您。*