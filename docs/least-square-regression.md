# 101 最小二乘回归法指南

> 原文：<https://www.edureka.co/blog/least-square-regression/>

随着[机器学习](https://www.edureka.co/blog/what-is-machine-learning/)和[人工智能](https://www.edureka.co/blog/artificial-intelligence-with-python/)在 IT 市场蓬勃发展，学习这些趋势技术的基本原理变得至关重要。这篇关于最小二乘回归方法的博客将帮助你理解回归分析背后的数学原理，以及如何使用 Python 实现它。

要获得人工智能和机器学习的深入知识，可以报名参加 Edureka 提供的全天候支持和终身访问的直播 [***机器学习工程师硕士项目***](https://www.edureka.co/masters-program/machine-learning-engineer-training) 。

以下是本博客将涉及的主题列表:

1.  [什么是最小二乘法？](#What%20Is%20the%20Least%20Squares%20Method)
2.  [最佳拟合线](#Line%20Of%20Best%20Fit)
3.  [计算最佳拟合线的步骤](#Steps%20to%20Compute%20the%20Line%20Of%20Best%20Fit)
4.  [最小二乘回归法举例](#The%20least-squares%20regression%20method%20with%20an%20example)
5.  [实现线性回归的简短 python 脚本](#A%20short%20python%20script%20to%20implement%20Linear%20Regression)

## **什么是最小二乘回归法？**

*最小二乘回归法是回归分析中常用的一种技术。这是一种数学方法，用于寻找代表自变量和因变量之间的关系的最佳拟合线。*

为了理解最小二乘回归方法，让我们熟悉一下用公式表示最佳拟合线所涉及的概念。

## **最佳拟合线是什么？**

绘制最佳拟合线来表示两个或更多变量之间的关系。更具体地说，最佳拟合线绘制在数据点的散点图上，以表示这些数据点之间的关系。

[回归分析](https://www.edureka.co/blog/linear-regression-in-python/)利用最小二乘法等数学方法来获得预测变量和目标变量之间的确定关系。最小二乘法是用来绘制最佳拟合线的最有效的方法之一。它基于这样一种思想，即所获得的误差的平方必须尽可能地最小化，因此被称为最小二乘法。

如果我们要绘制一条最佳拟合线来显示一家公司在一段时间内的销售情况，它看起来会像这样:

![Regression Analysis Example - Least Squares Regression Method - Edureka](img/a2288f5d924ea440cd7cc5590574bd8c.png)

注意线尽可能靠近所有分散的数据点。这就是理想的最佳拟合线的样子。

为了更好地理解整个过程，让我们看看如何使用最小二乘回归计算直线。

## **计算最佳拟合线的步骤**

为了开始构建最好地描述数据中变量之间关系的线，我们首先需要得到我们的基本权利。看看下面的等式:

![Regression line formula - Least Squares Regression Method - Edureka](img/7bfd2408577453eb1466aef18547159b.png)

当然，你以前遇到过这个等式。这是一个简单的等式，表示沿二维数据(即 x 轴和 y 轴)的直线。为了更好地理解这一点，让我们来分解这个等式:

*   y:因变量
*   m:直线的斜率
*   x:独立变量
*   c: y 轴截距

因此，我们的目标是计算斜率、y 轴截距的值，并代入等式中相应的“x”值，以导出因变量的值。

让我们看看如何做到这一点。

作为假设，让我们考虑有“n”个数据点。

**第一步:** *用下列公式计算斜率‘m’:*

**![Slope of a Line formula - Least Squares Regression Method - Edureka](img/f699fd62097bf9ad8ad2a34a2f361c15.png)**

**第二步:** *计算 y 轴截距(直线与 y 轴交点处的 y 值):*

**![Y-Intercept formula - Least Squares Regression Method - Edureka](img/2fa0e3114e17fe8073e69cf5c585f6f1.png)**

**第三步:** *代入最终方程中的值:*

![Regression line formula - Least Squares Regression Method - Edureka](img/44d1005c7c49d26f7a5ce2b611c7a875.png)

简单，不是吗？

现在让我们看一个例子，看看如何使用最小二乘回归方法来计算最佳拟合线。

## **最小二乘回归示例**

考虑一个例子。汤姆是一家零售店的老板，他发现不同 t 恤的价格与一周内他店里卖出的 t 恤数量之间的关系。

他将此列表如下所示:

![Regression Example - Least Squares Regression Method - Edureka](img/94441d687bde3becfe0172b9aa0d4c79.png)

让我们用最小二乘回归的概念来找出上述数据的最佳拟合线。

**步骤 1:** 使用以下公式计算斜率‘m ’:

![Slope of a Line formula - Least Squares Regression Method - Edureka](img/ccaa1659aa443bbfde5fde3678919a2b.png)

代入相应的值后，m 约为 1.518。

**步骤 2:** 计算 y 轴截距值

![Y-Intercept formula - Least Squares Regression Method - Edureka](img/0369c9004eed14f35e2a966cbb0cf579.png)

代入相应的值后，c = 0.305 左右。

第三步:代入最终等式中的值

![Regression line formula - Least Squares Regression Method - Edureka](img/282a13a37c909a0f7b714e4dffbd7a2c.png)

一旦您替换了这些值，它应该看起来像这样:

![Regression Analysis Calculation - Least Squares Regression Method - Edureka](img/78c90ff2ad6497fc8c9c2bada8b32b53.png)

让我们构建一个代表最佳拟合的 **y=mx + c** 线的图形:

![Regression Analysis Plot - Least Squares Regression Method - Edureka](img/4a566dd376f002aa5326896123c33856.png)

现在，汤姆可以使用上面的等式来估计他在零售店可以卖出多少件价格为 8 美元的 t 恤。

*y = 1.518 x 8 + 0.305 = 12.45* T 恤

这归结为 13 件 t 恤！这就是使用线性回归进行预测的简单程度。

现在让我们试着理解基于什么因素我们可以确认上面的线是最佳拟合的线。

最小二乘回归方法的工作原理是使误差的平方和尽可能小，因此被称为最小二乘。基本上，最佳拟合线和误差之间的距离必须尽可能地最小化。这是最小二乘回归方法背后的基本思想。

在实施最小二乘回归方法之前，需要记住以下几点:

*   这些数据必须没有异常值，因为它们可能会导致有偏见和错误的最佳拟合线。
*   可以反复绘制最佳拟合线，直到得到误差平方最小的线。
*   这种方法即使对于非线性数据也能很好地工作。
*   从技术上讲,“y”的实际值和“y”的预测值之间的差称为残差(表示误差)。

现在，让我们来看一个使用 Python 的线性回归的实际实现。

## **Python 中的最小二乘回归**

在本节中，我们将运行一个简单的演示来理解使用最小二乘回归方法进行回归分析的工作原理。一个简短的声明，我将用 Python 做这个演示，如果你不熟悉这种语言，你可以浏览下面的博客:

1.  [Python 教程——学习 Python 编程的完整指南](https://www.edureka.co/blog/python-tutorial/)
2.  [Python 编程语言——Python 基础入门](https://www.edureka.co/blog/python-programming-language)
3.  [Python 函数初学者指南](https://www.edureka.co/blog/python-functions)
4.  [用于数据科学的 Python](https://www.edureka.co/blog/learn-python-for-data-science/)

**问题陈述:**应用线性回归，建立一个研究个体头部大小和大脑重量之间关系的模型。

**数据集描述:**数据集包含以下变量:

*   **性别:**用二元变量表示的男性或女性
*   **年龄:**个人的年龄
*   cm^3:人的头部尺寸 cm^3 人的头部尺寸
*   **大脑重量克数:**个人大脑的重量克数

需要对这些变量进行分析，以建立一个研究个体头部大小和大脑重量之间关系的模型。

**逻辑:**实现线性回归，以建立研究自变量和因变量之间关系的模型。将使用最小二乘回归方法对模型进行评估，其中 RMSE 和 R 平方将作为模型评估参数。

我们开始吧！

**第一步:导入所需的库**

```

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

```

**第二步:导入数据集**

```

# Reading Data
data = pd.read_csv('C:UsersNeelTempDesktopheadbrain.csv')
print(data.shape)
(237, 4)
print(data.head())
   Gender  Age Range  Head Size(cm^3)  Brain Weight(grams)
0       1          1             4512                 1530
1       1          1             3738                 1297
2       1          1             4261                 1335
3       1          1             3777                 1282
4       1          1             4177                 1590

```

**第三步:将“X”指定为自变量，将“Y”指定为因变量**

```
# Coomputing X and Y
X = data['Head Size(cm^3)'].values
Y = data['Brain Weight(grams)'].values

```

接下来，为了计算斜率和 y 轴截距，我们首先需要计算“x”和“y”的平均值。这可以按如下所示完成:

```
# Mean X and Y
mean_x = np.mean(X)
mean_y = np.mean(Y)

# Total number of values
n = len(X)

```

**第四步:计算斜率和 y 轴截距的值**

```
# Using the formula to calculate 'm' and 'c'
numer = 0
denom = 0
for i in range(n):
numer += (X[i] - mean_x) * (Y[i] - mean_y)
denom += (X[i] - mean_x) ** 2
m = numer / denom
c = mean_y - (m * mean_x)

# Printing coefficients
print("Coefficients")
print(m, c)

Coefficients
0.26342933948939945 325.57342104944223

```

以上系数分别是我们的斜率和截距值。代入最终等式中的值，我们得到:

*大脑重量= 325.573421049 + 0.263429339489 *头部大小*

就这么简单，上面的等式代表了我们的线性模型。

现在让我们用图表来表示。

**第五步:绘制最佳拟合线**

```
# Plotting Values and Regression Line

max_x = np.max(X) + 100
min_x = np.min(X) - 100

# Calculating line values x and y
x = np.linspace(min_x, max_x, 1000)
y = c + m * x

# Ploting Line
plt.plot(x, y, color='#58b970', label='Regression Line')
# Ploting Scatter Points
plt.scatter(X, Y, c='#ef5423', label='Scatter Plot')

plt.xlabel('Head Size in cm3')
plt.ylabel('Brain Weight in grams')
plt.legend()
plt.show()

```

**![Regression Analysis Demo Plot - Least Squares Regression Method - Edureka](img/c8d373188279c48d6354523d3afc958f.png)**

**第六步:模型评估**

考虑到我们的数据集很小，建立的模型相当不错。是时候评估该模型了，看看它对最后阶段(即预测)有多好。为此，我们将使用均方根误差方法，该方法主要计算最小二乘误差，并对求和值求根。

从数学上讲，均方根误差只不过是所有误差之和除以数值总数的平方根。这是计算 RMSE 的公式:

![RMSE - Least Squares Regression Method - Edureka](img/584af924846a30860df8b4c75d21d239.png)

在上式中，yI是让我们看看如何使用 Python 来实现这一点。

```
# Calculating Root Mean Squares Error
rmse = 0
for i in range(n):
    y_pred = c + m * X[i]
    rmse += (Y[i] - y_pred) ** 2
rmse = np.sqrt(rmse/n)
print("RMSE")
print(rmse)
RMSE
72.1206213783709

```

另一个模型评估参数是称为 R 平方值的统计方法，用于测量数据与最佳拟合线的接近程度。

数学上，它可以计算为:

![R-sqaured derivation - Least Squares Regression Method - Edureka](img/d12a0ed4743f7fe1e79d90f50cfcf571.png)

![R-squared derivation 2 - Least Squares Regression Method - Edureka](img/0b0054ceb266448530944bf24e445d0d.png)

![R-squared Formula - Least Squares Regression Method - Edureka](img/2f605f3693f1e6c9b62c3839a28fb662.png)

其中，

*   SSt是平方和
*   SSr是残差平方和的总和

R 平方的值介于 0 和 1 之间。负值表示模型是弱的，并且由此做出的预测是错误的和有偏差的。在这种情况下，分析所有预测变量并寻找与输出高度相关的变量至关重要。这一步通常属于 EDA 或探索性数据分析。

我们不要忘乎所以。以下是如何在 Python 中实现 R 平方的计算:

```
# Calculating R2 Score
ss_tot = 0
ss_res = 0
for i in range(n):
    y_pred = c + m * X[i]
    ss_tot += (Y[i] - mean_y) ** 2
    ss_res += (Y[i] - y_pred) ** 2
r2 = 1 - (ss_res/ss_tot)
print("R2 Score")
print(r2)
R2 Score
0.6393117199570003

```

如你所见，我们的 R 平方值非常接近 1，这表明我们的模型运行良好，可以用于进一步的预测。

这就是使用 Python 实现最小二乘回归方法的全部过程。既然您已经了解了回归分析背后的数学原理，我相信您一定很想了解更多。这里有几个博客可以帮你入门:

1.  [数据科学数学和统计学完全指南](https://www.edureka.co/blog/math-and-statistics-for-data-science/)
2.  [关于统计和概率你需要知道的一切](https://www.edureka.co/blog/statistics-and-probability/)
3.  [举例介绍马尔可夫链——用 Python 实现马尔可夫链](https://www.edureka.co/blog/introduction-to-markov-chains/)
4.  [如何用 Python 实现贝叶斯网络？–贝叶斯网络举例说明](https://www.edureka.co/blog/bayesian-networks/)

说到这里，我们就到此为止了。如果你对这个话题有任何疑问，请在下面留下评论，我们会尽快回复你。

如果你希望报名参加人工智能和机器学习的完整课程，Edureka 有一个专门策划的 ***[机器学习工程师硕士项目](https://www.edureka.co/masters-program/machine-learning-engineer-training)*** ，它将使你精通监督学习、非监督学习和自然语言处理等技术。它包括人工智能&机器学习方面的最新进展和技术方法的培训，如深度学习、图形模型和强化学习。