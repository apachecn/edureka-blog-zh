# 所有关于在 Tableau 中使用双轴图表的不同方法

> 原文：<https://www.edureka.co/blog/ways-to-use-dual-axes-charts-in-tableau/>

本文将向您介绍在 [Tableau](https://www.edureka.co/blog/tableau-tutorial/) 中使用双轴图表的各种方法。本文将涉及以下几点:

*   [如何构建传统用途的 Tableau 双轴图表](#HowtoBuildTableauDual-AxisChartsfortheirTraditionaluse)
*   [使用双轴图表让你的用户成为故事的一部分](#Usingadual-axischarttomakeyouruserpartofthestory)
*   [使用双轴改进线图的设计](#Usingadual-axistoimprovethedesignofalinegraph)

## **在 Tableau 中使用双轴图表的方法**

Tableau 中的双轴图表之所以如此命名，是因为它们有两个相互层叠的独立轴。通常情况下，它们会显示不同标记类型的组合。

例如，在这里您可以创建一个可视化效果，在一个轴上显示一个度量，在另一个轴上显示线条。这是 Tableau 中我最喜欢的图表之一，因为它可以添加一个新的轴，并且可以单独控制这些轴。这释放了一些额外的灵活性，创建了几个可用于改进您的分析、用户体验和设计的实际应用程序。这篇文章将向你展示如何在 Tableau 中构建双轴图表，以及使用它们的三种不同方式:

在继续这篇关于如何在 Tableau 中使用双轴图表的文章之前，请观看此视频，详细了解 Tableau 图表。

[https://www.youtube.com/embed/A-A6-UIqFsk](https://www.youtube.com/embed/A-A6-UIqFsk)

## **如何构建传统用途的 Tableau 双轴图表**

因此，我将使用 Tableau 提供的样本超市数据集。现在，让我们从制作一个传统的双轴组合图开始。你可能对它很熟悉，但我还会分享第二种方法，你可能不知道它能帮你节省一两次点击。第一张图表在一个轴上绘制了按年销售额，在另一个轴上绘制了按年利润率；这两项措施也应按照类别维度进行细分。

*   首先，让我们创建一个图表，我将按类别从每年的销售额开始。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/bebc43b7c6b2337a35032142bd0b8965.png) 接下来，让我们将第二个衡量标准(即利润率)放在 Rows 货架上。此时，你在两行上有两个单独的条形图。有两种方法可以将这两个独立的条形图转换为双轴条形图。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/b74a686e1b7cd6a49f2f44f57cfbd64d.png)

首先，也是大多数人学习的方式，是右键单击 Rows Shelf 上的第二个 measure pill，然后选择 Dual Axis。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/f819622d2d1db1a3363a6e7a603f7d5b.png)

第二种也是更有效的方法是悬停在第二行的轴上。

*   悬停时，轴的左上角会出现一个绿色的小三角形。
*   您可以在三角形上单击鼠标左键，并将其拖动到第一行左轴的对面。
*   当您将鼠标悬停在图表的右侧时，您会看到一条虚线，该虚线是在您松开鼠标左键时轴将要显示的位置。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/dfe60bc7cdbb05773aea570923424314.png)

在这两种情况下，最终都会得到一个双轴条形图。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/fbf20d66f547e9d338c024876543abb1.png)

传统上，双轴组合图会更好。所以，这就是我们要做的。现在，对于一个双轴组合图，我们需要一个标记类型的组合。当在行架和/或列架上有多个度量时，每个度量最终都有自己的标记架。这意味着您可以独立编辑测量的标记类型。

下面是我将利润率的标记类型从条形改为线形后的最终视图。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/3a7636ca6f31c31568b3166ee7658091.png)

当数据点之间随着时间的推移而存在关系时，或者如果它们由连续的维度/度量连接时，应严格使用线条。在 Tableau 的行架或列架上，离散字段按特定顺序处理。

因此，在本例中，销售额和利润率首先按类别维度分解，然后按年份(订单日期)维度分解。这是可行的，但是如果我们想先按年份(订单日期)再按类别来分解这两个度量标准呢？它看起来是这样的:

![chart-3 ways to use dual axes charts in tableau- Edureka](img/cf4fab765b3e31d30b71fd86bf3d02ec.png)

继续这篇关于如何在 Tableau 中使用双轴图表的文章

## **使用双轴图表让你的用户成为故事的一部分**

下图是翻拍自 money.cnn.com 的 CNN 金钱计算器。

给定的 viz 以一条曲线为特征，显示了每个家庭的收入是如何按百分位数排列的。这是一个非常常见的“描述性”视图，用于描述高级统计数据。通过使用第二个轴来显示使用仪表板的个人在该曲线上的排名，可以获得真实值。这使得用户成为故事的一部分，是一种更吸引人的用户体验。

为了实现这一效果，我在 Tableau 中使用了一个参数，它是内置的，允许最终用户选择 2000 美元到 450000 美元之间的任何家庭收入选项。做出此选择后，圆会根据用户的选择移动到适当的位置。此外，该标签将更新为一个标题，告诉最终用户他们的家庭收入处于哪个百分点等级。

这是一个双轴组合图。左轴的曲线使用折线图的标记类型，圆是仅在右轴上显示圆供最终用户选择的第二个度量。只显示一个圆圈的诀窍是这个简单的公式，它计算用户的参数选择是否与 Y 轴上的家庭收入值相匹配。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/0360e52f222c6f66a1a7f08e33a4c8b8.png)

一旦你有了这样的计算，你就可以在左边的轴上画出曲线，在右边画出圆的尺寸。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/acedcf09373ba85d863de2fdb1eb5521.png)

要完成此视图，可以通过右键单击“圆”的轴并选择“同步轴”选项来同步轴。这确保了圆与相对轴上的直线完全对齐。最后，通过右键单击隐藏右边的轴，并取消选中显示标题选项。

继续这篇关于在 Tableau 中使用双轴图表的 3 种方法的文章

## **使用双轴改进线图的设计**

假设您有一个按月趋势显示销售额的折线图。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/d88f465620703518aaedccb91d4b3d5e.png)

现在，我将把 Sales 度量放在右轴上，同步这两个轴，并将第二个轴的标记类型更改为 Area。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/961ee338779333bc5993cb53d260c552.png)

在这一点上，我们有一个双轴组合图，其中每月的销售额分别是一个线形图和一个面积图。要完成视图，隐藏右轴，并将该区域的不透明度降低到 10%。

![chart-3 ways to use dual axes charts in tableau- Edureka](img/f578f279e647c25b945408b4f79b4a32.png)

一次只能将第二个轴用于一个目的。但是，如果您不是因为上面提到的前两个原因中的一个原因而使用它，这是第三个应用程序，可以用来增强您的传统线图。

这就把我们带到了这篇关于如何在 Tableau 中使用双轴图表的文章的结尾。

*如果你希望掌握 Tableau，Edureka 有一个关于 **[Tableau 培训](https://www.edureka.co/tableau-certification-training)** 的策划课程，该课程深入涵盖了数据可视化的各种概念，包括条件格式、脚本、链接图表、仪表板集成、Tableau 与 R 的集成等等。它提供 24*7 支持，在整个学习期间为您提供指导。新的批次即将开始。*

*有问题吗？请在评论区提到它，我们会尽快回复您。*