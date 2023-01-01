# Python 中探索性数据分析的原因和方法

> 原文：<https://www.edureka.co/blog/exploratory-data-analysis-in-python/>

数据分析基本上是使用[统计和概率](https://www.edureka.co/blog/statistics-and-probability/)来计算数据集中的趋势。它帮助你从统计噪音中整理出“**真实的**趋势。什么是“**噪音**”？一大堆看起来根本没有任何意义的数据。以下是我们将要讨论的主题，作为 Python 中探索性数据分析的一部分:

*   [Python 中的探索性数据分析是什么？](#eda)
*   [对探索性数据分析的需求](#need)
*   [Python 中探索性数据分析的步骤有哪些？](#steps)
*   [EDA 中使用的工具](#tools)

## **Python 中什么是探索性数据分析？**

**Python**中的探索性数据分析(EDA)是数据分析过程的第一步，由**约翰·图基**于 20 世纪 70 年代开发。在统计学中，探索性数据分析是一种[分析数据集](https://www.edureka.co/blog/football-world-cup-best-xi-analysis-using-python/)以总结其主要特征的方法，通常采用可视化方法。从名字本身就可以知道，这是我们需要探索数据集的一个步骤。

**例如，**你计划去“ **X** 地点旅行。做决定前要做的事情:

*   你将在谷歌、Instagram、脸书和其他社交网站上探索该位置的所有地方、瀑布、徒步旅行、海滩和餐馆。

*   计算它是否在你的预算之内。

*   检查覆盖所有地方的时间。

*   旅行方式的类型。

同样，当你试图建立一个[机器学习模型](https://www.edureka.co/blog/logistic-regression-in-python/)时，你需要非常确定你的数据是否有意义。探索性[数据分析](https://www.edureka.co/blog/python-pandas-tutorial/)的主要目的是获得对你的数据的信心，在一定程度上你已经准备好使用机器学习算法。

## **需要进行探索性数据分析**

探索性的数据分析是你跳到机器学习或数据建模之前的关键一步。通过这样做，您可以了解所选特征是否足以建模，是否所有特征都是必需的，是否存在任何相关性，我们可以基于这些相关性返回到数据预处理步骤或继续建模。

一旦**探索性数据分析**完成并得出见解，其特征可用于监督和非监督机器学习建模。

在每个机器学习工作流程中，最后一步是向利益相关者报告或提供见解，作为一名[数据科学家](https://www.edureka.co/blog/data-scientist-salary/)你可以解释每一点代码，但你需要记住受众。通过完成**探索性数据分析**，您将获得许多图表、热图、频率分布、图表、相关矩阵以及假设，通过这些图表，任何个人都可以了解您的数据是关于什么的，以及您从探索您的数据集中获得了什么见解。

有句话叫“**一图抵千言**”。

我想为 data scientist 修改为"**一个图值一千行**"

在我们的**旅行示例**中，我们对选定的地方进行了所有的探索，在此基础上，我们将获得计划旅行的信心，甚至与我们的朋友分享我们对该地方的见解，以便他们也能加入。

## **Python 中探索性数据分析的步骤有哪些？**

进行探索性数据分析有许多步骤。我想讨论使用波士顿数据集的以下几个步骤，该数据集可以从**sk learn . datasets import load _ Boston**导入

*   数据描述

*   处理缺失数据

*   处理异常值

*   通过情节理解关系和新的见解

### **a)数据描述:**

我们需要了解不同种类的数据和数据的其他统计数据，然后才能继续其他步骤。一个好的方法是从 python 中的 **describe()** 函数开始。在 [Pandas](https://www.edureka.co/blog/python-pandas-tutorial/) 中，我们可以在数据帧上应用 describe()，这有助于生成描述性统计数据，这些数据汇总了数据集分布的集中趋势、分散性和形状，不包括 NaN 值。

结果的索引将包括计数、平均值、标准差、最小值、最大值以及下限、50%和上限。默认情况下，下百分位是 25，上百分位是 75。50%与中位数相同。

正在加载数据集:

```
import pandas as pd
from sklearn.datasets import load_boston

boston = load_boston()
x = boston.data
y = boston.target
columns = boston.feature_names
# creating dataframes
boston_df = pd.DataFrame(boston.data)
boston_df.columns = columns
boston_df.describe()

```

**![Dataset example](img/da3fc4725fe59acd56d7e29a280704c7.png)**

### **b)处理缺失数据:**

现实世界中的数据很少是干净和同质的。由于多种原因，数据可能在数据提取或收集过程中丢失。缺失值需要小心处理，因为它们会降低我们任何绩效矩阵的质量。它还会导致错误的预测或分类，并且还会对所使用的任何给定模型造成高偏差。有几种处理缺失值的方法。然而，应该做什么的选择在很大程度上取决于我们的数据和缺失值的性质。以下是一些技巧:

*   删除空值或缺失值

*   填充缺失值

*   用 ML 算法预测缺失值

### **删除空值或缺失值:**

这是处理缺失值的最快和最容易的步骤。不过一般不建议。这种方法降低了我们模型的质量，因为它减少了样本量，因为它通过删除任何变量缺失的所有其他观察值来工作。

![](img/9aef7ccb07b4387a6d82f72bd465d08f.png)

上面的代码表明我们的数据集中没有空值。

### **填充缺失值**:

这是处理缺失值的最常见方法。在此过程中，缺失值将被测试统计数据(如缺失值所属的特定特征的平均值、中值或众数)替换。假设我们在波士顿数据集中缺少年龄值。然后下面的代码会用 30 来填充缺少的值。

**![](img/2e4f83b3473f1c07ba8e355e59355339.png)**

### **用 ML 算法预测缺失值:**

这是迄今为止处理缺失数据的最好和最有效的方法之一。根据缺失数据的类别，可以使用回归或分类模型来预测缺失数据。

### **c)处理异常值:**

离群值是与人群分离或不同的东西。异常值可能是数据收集过程中出现错误的结果，也可能只是数据中出现偏差的迹象。检测和处理异常值的一些方法:

*   BoxPlot

*   [散点图](https://www.edureka.co/blog/python-matplotlib-tutorial/#Scatter)

*   z 分数

*   IQR(四分位数间距)

### **箱式打印:**

箱线图是一种通过四分位数以图形方式描绘数字数据组的方法。该方框从数据的 Q1 值延伸到第三季度的四分位值，中间有一条线(Q2)。触须从框的边缘延伸出来，以显示数据的范围。离群点是那些超过胡须末端的点。箱线图显示了位置和分布的稳健度量，并提供了关于对称性和异常值的信息。

```
import seaborn as sns
sns.boxplot(x=boston_df['DIS'])

```

**![](img/61cf14a69e9140b57e730225c1991124.png)**

### **散点图**:

散点图是一种数学图表，使用笛卡尔坐标来显示一组数据的两个变量的值。数据显示为点的集合，每个点的一个变量的值决定水平轴上的位置，另一个变量的值决定垂直轴上的位置。远离总体的点可以称为异常值。

```
import matplotlib.pyplot as plt
fig, ax = plt.subplots(figsize=(16,8))
ax.scatter(boston_df['INDUS'] , boston_df['TAX'])
ax.set_xlabel('proportion of non-retail business acre per town')
ax.set_ylabel('full-value property-tax per $10000')
plt.show()

```

![](img/c1cbefee33178cc497eed78510c64013.png)

### **Z 分数:**

Z 得分是标准偏差的有符号数，通过它，观察值或数据点的值高于正在观察或测量的平均值。在计算 Z 值时，我们会重新调整数据的比例并使其居中，同时寻找离零太远的数据点。这些离零太远的数据点将被视为异常值。在大多数情况下，使用阈值 3 或-3，即如果 Z 分值分别大于或小于 3 或-3，则该数据点将被识别为异常值。

![](img/17e5251d4f6c5c85637c7be27f6890a3.png)

我们可以从上面的代码中看到，形状发生了变化，这表明我们的数据集有一些异常值。

### **IQR:**

四分位数间距(IQR)是统计离差的一种度量，等于第 75 个和第 25 个百分位数之间的差值，或者上四分位数和下四分位数之间的差值。

**IQR = Q3**T2Q1。

![](img/dabe95681d43b9abc6c84eca8ee3743b.png)

一旦我们有 IQR 分数低于代码将删除我们的数据集中所有的离群值。

**![](img/808bd3db11472020005a6e2c84421dd6.png)**

### **通过情节理解关系和新见解:**

通过可视化数据集，我们可以获得数据中的许多关系。让我们来看一些技巧，以便了解其中的洞见。

*   柱状图

*   热图

### **直方图:**

直方图是快速评估概率分布的一个很好的工具，几乎任何观众都可以很容易地理解它。 [Python](https://www.edureka.co/blog/python-programming-language) 为构建和绘制[直方图](https://www.edureka.co/blog/python-matplotlib-tutorial/#Histogram)提供了一些不同的选项。

![](img/7db2e131ddc44710c1a459b1050a034a.png)

### **热图:**

热图程序显示了定量变量在 2 个分类因素的所有组合中的分布。如果这两个因素中有一个代表时间，那么这个变量的演变就可以很容易地用图来观察。渐变色标用于表示定量变量的值。两个随机变量之间的相关性是一个从-1 到 0 到+1 的数字，分别表示强的反比关系、无关系和强的正关系。

![](img/43050aff99bd7a8ae4a0006cee1a174c.png)

## **工具探索性数据分析**

有很多开源工具可以自动执行预测建模的步骤，如数据清理、数据可视化。其中一些也很受欢迎，如 Excel，Tableau，Qlikview，Weka 和许多除了编程之外的其他软件。

在编程上，我们可以用 Python，R，SAS 来完成 EDA。Python 中的一些重要包是:

*   熊猫

*   [Numpy](https://www.edureka.co/blog/python-numpy-tutorial/)

*   [Matplotlib](https://www.edureka.co/blog/python-matplotlib-tutorial/)

*   [Seaborn](https://www.edureka.co/blog/python-seaborn-tutorial/)

*   散景

![](img/94d48eeb717ff6d752991fc1be9fca01.png)

许多数据科学家将急于进入[机器学习](https://www.edureka.co/blog/introduction-to-machine-learning/)阶段，有些人要么完全跳过探索过程，要么做非常简单的工作。这是一个具有多种含义的错误，包括生成不准确的模型，生成准确的模型但基于错误的数据，在数据准备中没有创建正确类型的变量，以及由于仅在生成模型后才意识到数据可能有偏差，或有异常值，或有太多缺失值，或发现某些值不一致而导致资源使用效率低下。

在我们的**旅行示例**中，如果没有事先探索这个地方，您将在旅行中面临许多问题，如方向、成本、旅行，这些都可以通过 EDA 来减少，这同样适用于机器学习问题。要掌握你的技能，报名参加 Edureka 的[数据科学 Python](https://www.edureka.co/data-science-python-certification-course) 认证项目，开始你的学习。

*有什么问题吗？在“python 中的探索性数据分析”的评论部分提到它们，我们会尽快回复您。*