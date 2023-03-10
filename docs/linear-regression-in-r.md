# R 中线性回归的逐步指南

> 原文：<https://www.edureka.co/blog/linear-regression-in-r/>

## **线性回归 R:**

线性回归是最广泛使用的[机器学习算法](https://www.edureka.co/blog/machine-learning-algorithms/)之一，但是尽管它很流行，我们中的许多人并不完全了解这种算法的工作和实现。在这篇关于 R 中的线性回归的博客中，你将理解线性回归背后的数学，以及使用 [R 语言](https://www.edureka.co/blog/r-programming-language)的实现。

要获得关于数据科学和各种机器学习算法的深入知识，您可以报名参加 Edureka 提供的实时 ***[数据科学认证培训](https://www.edureka.co/data-science)*** ，24/7 全天候支持和终身访问。

本博客将涵盖以下主题:

1.  [什么是回归分析？](#What%20is%20Regression%20Analysis)
2.  [回归类型](#Types%20of%20Regression)
    1.  [线性回归](#Linear%20Regression)
    2.  [逻辑回归](#Logistic%20Regression)
    3.  [多项式回归](#Polynomial%20Regression)
3.  [线性回归简介](#Introduction%20to%20Linear%20Regression)
4.  [利用 R 建立线性回归模型](#Build%20a%20linear%20regression%20model%20using%20R)

## **什么是回归分析？**

*回归分析是一种统计、预测建模技术，用于研究因变量与一个或多个自变量之间的关系。* 让我们用一个例子来试着理解回归分析。

假设您收到了一份纽约市的房价数据集。该数据集包含诸如大小、位置、房屋中卧室的数量等信息。 你在这里的任务是通过研究给你的数据集来预测房子的价格。 你会如何处理这样的问题？

嗯，这很简单。你要建立因变量和自变量之间的关系模型。

*![Regression Analysis - Linear Regression In R - Edureka](img/2a7c3ce0c77e9d7d43a6c74b1a22dcfe.png)回归分析——R 中线性回归——爱德华卡*

但是什么是因变量和自变量呢？

关于房子的数据，如卧室的数量，房子的大小等等，被称为自变量或预测变量。这些预测变量用于预测响应变量。

在我们的例子中，响应变量是房子的价格。响应变量也称为因变量，因为它们的值取决于自变量的值。

因此，给定房子的相关数据，我们手头的任务是预测新房子的价格。这类问题可以用一种叫做回归分析的统计方法来解决。

回归分析广泛应用于商业领域，用于销售或市场预测、风险分析、运营效率、发现新趋势等。

## **回归分析的类型**

回归分析技术有很多，但使用最广泛的三种回归模型是:

1.  线性回归
2.  逻辑回归
3.  多项式回归

## **什么是线性回归？**

线性回归是最基本、应用最广泛的机器学习算法之一。它是一种预测建模技术，用于在给定一个或多个自变量的情况下预测连续的因变量。

![Linear Regression - Linear Regression In R - Edureka](img/edc75f159313a356e66f226fae5bb686.png)

*线性回归–R 中的线性回归–爱德华卡*

在线性回归模型中，因变量和自变量之间的关系总是线性的，因此，当你试图绘制它们之间的关系时，你会发现更多的是直线而不是曲线。

以下等式用于表示线性回归模型:

**![Linear Regression Formula - Edureka](img/aa4f1660a9f51a678c6e70a255ab446f.png) ** * 线性回归中 R–edu reka*

## **什么是逻辑回归？**

[逻辑回归](https://www.edureka.co/blog/logistic-regression-in-r/)是一种用于解决分类问题的机器学习算法。它被称为“逻辑回归”，因为它的基本技术与线性回归非常相似。

逻辑回归是一种预测分析技术，用于预测因变量，给定一组自变量，*使得因变量是分类的。*

![Logistic Regression - Linear Regression In R - Edureka](img/7ac8d277604ef72c0b5ac3fd7ce5fd12.png)

*逻辑回归——R 中的线性回归——爱德华卡*

当我说分类变量时，我的意思是，它包含 1 或 0、是或否、真或假等值。

以下等式用于表示逻辑回归模型中因变量和自变量之间的关系:

**![Logistic Regression Formula - Edureka](img/064204a2018bd32f57e8098ed0ef1884.png)**

*逻辑回归——爱德华卡*

如果你想了解更多关于线性和逻辑回归的知识，请观看我们机器学习专家的视频。

## **线性回归 vs 逻辑回归|爱德华卡**



[//www.youtube.com/embed/OCwZyYH14uw?rel=0&showinfo=0](//www.youtube.com/embed/OCwZyYH14uw?rel=0&showinfo=0)

*这个关于线性回归 Vs 逻辑回归的 Edureka 视频涵盖了线性和逻辑回归模型的基本概念。*

## **什么是多项式回归？**

多项式回归是一种用于处理非线性数据的方法。非线性可分数据基本上是当你不能画出一条直线来研究因变量和自变量之间的关系时。

![Polynomial Regression - Linear Regression In R - Edureka](img/51abca2e1c5cbc9a568078974ce50480.png)

*多项式回归–R 中的线性回归–爱德华卡*

因此，在该算法中，最佳拟合线不是直线，而是拟合数据点的曲线。之所以称之为“多项式”回归，是因为一些自变量的幂大于 1。

以下等式用于表示多项式回归模型:

**![Polynomial Regression Formula - Edureka](img/71ef66af981e326de26643aaed7ac642.png) ** *多项式回归公式——爱德华卡* 

现在你对回归分析的基础有了很好的理解，让我们把重点放在线性回归上。

## **线性回归简介**

线性回归是一种监督学习算法，用于根据自变量(X)的值预测一个*连续因变量(Y)* 。这里要注意的重要一点是，线性回归模型的因变量总是连续的，然而，自变量可以是连续的也可以是离散的。

你可能会问，什么是连续变量？

连续变量有无限多种可能性。比如一个人的体重。有人可能重 160 磅，他们可能重 160.11 磅，或者他们可能重 160.1134 磅。重量的可能性是无限的。这就是连续变量。

我来举例说明一下线性回归。

让我们假设你想预测一段时间内的股票价格。对于这类问题，你可以通过*研究因变量股票价格和自变量时间*之间的关系，利用线性回归。

![Predict Stock price - Linear Regression In R - Edureka](img/168efcbdaa6314744ba4fbf847f18127.png)

*预测股票价格——R 中的线性回归——爱德华卡*

在我们的例子中，股票价格是因变量，因为股票价格随时间而变化。请注意，股票的价值总是一个连续的量。

另一方面，时间是独立变量，可以是连续的，也可以是离散的。这个自变量用来决定因变量的值。

线性回归的第一步是使用最佳拟合直线绘制出因变量和自变量之间的关系。

![Linear Regression In R - Edureka](img/e9118fcd177e364286d43ec9017006d1.png)

*线性回归中的 R–爱德华卡*

我们称之为“L 线性”回归，因为两个变量都是线性变化的。这意味着，在绘制两个变量之间的关系时，我们将得到更多的直线而不是曲线。

现在让我们讨论一下线性回归背后的数学原理。

下面的等式用于得出自变量(X)和因变量(Y)之间的关系。我们都知道数学上一条直线的方程是 y=mx + c，所以线性回归方程是沿着同一个方程表示的:

*![Linear Regression Model - Linear Regression In R - Edureka](img/01a5884ee31e1c10c4db106ff626760c.png)线性回归模型——R 中的线性回归——爱德华卡*

*   Y 代表需要预测的因变量。
*   B0 是 Y 轴截距，其基本上是线上与 Y 轴接触的点。
*   B1 是直线的斜率(斜率可以是负的，也可以是正的，取决于因变量和自变量之间的关系。)
*   这里的 X 代表用于预测我们的合成因变量的独立变量。
*   E 表示计算中的误差

既然你对线性回归有了很好的理解，让我们开始实施吧。

## **利用 R 建立线性回归模型**

很多人心里都有这个疑问， **线性回归中的 R 代表什么？**

答案是，R 基本上是一种用于数据分析、数据操作和数据可视化的开源编程和统计语言。它是一种多用途编程语言，广泛应用于[机器学习、](https://www.edureka.co/blog/machine-learning-tutorial/)人工智能、[数据科学](https://www.edureka.co/blog/r-for-data-science/)领域。

**数据集描述:**

为了理解线性回归模型是如何工作的，我们将使用一个简单的数据集，其中包含 30 名不同年龄的人的收缩压水平。

**问题陈述:**

建立一个线性回归模型，通过与相应年龄建立具有统计显著性的线性关系，可以用来预测一个人的血压。我们将创建一个线性回归模型来研究血压水平和相应年龄之间的关系。

让我们来看看我们数据集的前 5-6 个观察值:

```
head(trainingSet)
  age y
1 39 144
2 47 220
3 45 138
4 47 145
5 65 162
6 46 142

```

建立回归模型的第一步是以图形方式理解我们的数据。我们需要通过可视化数据来理解自变量和因变量之间的关系。我们可以利用各种图，如箱线图、散点图等:

## **散点图**

散点图是用于通过 x 轴和 y 轴绘制数据点的图形表示。散点图的主要目的是表示因变量和自变量之间的关系或它们之间的相关性。

```
scatter.smooth(x=trainingSet$age, y=trainingSet$y, main="Blood pressure ~ Age") # scatterplot

```

![Scatter Plot - Linear Regression In R - Edureka](img/5533a1eb6d400ed659f8acf00c38c4f0.png)

*散点图–R 中的线性回归–爱德华卡*

在上图中，散点图显示了“年龄”和“血压”变量之间的线性正相关关系。

*这说明响应(因变量)和预测(自变量)变量之间的关系是线性的*，这是线性回归模型的基本原理之一。

## **方框图**

箱线图主要用于解释性数据分析。箱线图代表数据的分布及其可变性。箱形图包含上四分位数和下四分位数，因此箱形图基本上跨越了四分位数之间的范围(IQR)。

使用箱线图的一个主要原因是检测数据中的异常值。由于箱形图跨越了 IQR，因此它会检测位于此范围之外的数据点。这些数据点被称为异常值。

```
# Divide the graph area in 2 columns
par(mfrow = c(1, 2))
# Boxplot for X
boxplot(trainingSet$age, main='age', sub=paste('Outliers: ', boxplot.stats(trainingSet$x)$out))
# Boxplot for Y
boxplot(trainingSet$y, main='blood pressure', sub=paste('Outliers: ', boxplot.stats(trainingSet$y)$out))

```

![Box plot - Linear Regression In R - Edureka](img/77c0c7aba93f3df11af226a005f57a27.png)

*箱线图–R 中的线性回归–爱德华卡*

## **关联**

线性回归的下一个重要指标是相关性。

相关性是一种统计方法，显示两个或多个变量一起变化的程度。有两种类型的相关性:

1.  正相关范围在 0 和+1 之间。它表明因变量和自变量相互对应地增加或减少。所以基本上，强正相关意味着，随着一个人年龄的增长，血压也会随之增长。这种关系的相关性将更接近于 1。
2.  负相关范围在-1 和 0 之间。它显示了一个变量随着另一个变量的减少而增加的程度。强烈的负相关性表明，随着一个人年龄的增加，血压降低，反之亦然，在这种情况下，年龄和血压之间的相关性将更接近于-1。

如果因变量和自变量之间的相关值更接近于零，则表明它们之间的关系较弱。相关性的值非常重要，因为它表明因变量是否真的根据自变量而变化。

范围(-0.2 至 0.2)内的相关性表明反应变量和预测变量之间的关系较弱，因此表明因变量相对于自变量基本上没有变化。在这种情况下，寻找更好的预测变量被认为是明智的。

```
# Finding correlation
cor(trainingSet$age, trainingSet$y)
[1] 0.6575673

```

在研究了因变量和自变量之间的关系并计算了它们之间的相关性之后，现在是建立线性回归模型的时候了。

## **建立回归模型**

### **R 中的 lm()函数是什么？**

R 带有预定义的函数，用于构建线性回归模型。这个函数称为 lm()函数。lm()函数的语法如下:

*【lm(公式，数据)*

我们来了解一下两个参数:

*   **公式:** 公式是 x 和 y 关系的表示
*   **数据:** 数据是应用公式的数据帧

```
# Fitting Simple Linear regression
regressor = lm(formula = y ~ age, data = trainingSet)
print(regressor)

Call:
lm(formula = y ~ age, data = trainingSet)

Coefficients:
(Intercept)    age
98.7147     0.9709

```

上图显示了我们的线性回归模型以及系数。系数部分有两个参数:

1.  拦截
2.  年龄

这些系数也称为β系数，用于计算响应变量(血压)的值。

这里使用的公式是:

*【血压=截距+ (b1 *年龄)*

## **线性回归分析**

到目前为止，我们已经建立了线性回归模型，还计算出了在给定年龄的情况下计算血压所需的公式。那么，接下来呢？

我们的下一步是检查我们模型的效率。我们需要认识到这个模型在统计上是否足够强大，足以做出预测。

为了确定模型是高效的，我们来看看模型的总结:

```
summary(regressor)

Call:
lm(formula = y ~ age, data = trainingSet)

Residuals:
Min 1Q Median 3Q Max
-21.724 -6.994 -0.520 2.931 75.654

Coefficients:
            Estimate Std. Error t value Pr(>|t|)
(Intercept) 98.7147    10.0005   9.871  1.28e-10 ***
age         0.9709     0.2102    4.618  7.87e-05 ***
---
Signif. codes: 0 &lsquo;***&rsquo; 0.001 &lsquo;**&rsquo; 0.01 &lsquo;*&rsquo; 0.05 &lsquo;.&rsquo; 0.1 &lsquo; &rsquo; 1

Residual standard error: 17.31 on 28 degrees of freedom
Multiple R-squared: 0.4324, Adjusted R-squared: 0.4121
F-statistic: 21.33 on 1 and 28 DF, p-value: 7.867e-05

```

上面的总结告诉我们一些事情:

*   **调用:**是对线性回归模型的函数调用
*   **残差:**该度量用于通过计算实际值与预测值之间的差值来检查模型的效率。理想情况下，残差的和大约为零或尽可能低。然而，在现实世界的问题中，情况并非如此，残差总是预期的
*   **系数:**表示贝塔系数及其统计显著性。

*密切关注系数的 p 值，(1.28e-10 和 7.87e-05)*

简单来说，p 值表示你的回归模型有多强。在确保模型的显著性时，p 值是一个非常重要的度量。只有当两个 p 值都小于预定的统计显著性水平(理想情况下为 0.05)时，线性模型才具有统计显著性。每个系数的 p 值被表示为概率 *Pr( > |t|)。*

在我们讨论 *Pr( > |t|)，*之前，让我们讨论一下与 p 值相关的另一个重要概念，也就是零备假设

## **零假设和替代假设**

*   零假设表明与因变量相关的系数等于零，这意味着因变量和自变量之间没有任何关系。
*   另一方面，另一种假设认为系数不等于零，这意味着自变量和因变量之间存在关系。

在模型总结中，注意另一个重要参数，叫做 t 值。 较大的 *t 值*表明替代假设为真，系数不等于零纯属偶然。

*Pr( > |t|)* 基本上是零假设成立时，得到的 t 值高于观测值的概率。 *简而言之，如果 Pr( > |t|)的值低于 0.05，则这些系数在线性回归模型的计算中是必不可少的，但是**t 如果 Pr( > |t|)高，则这些系数不是必不可少的。*

在我们的例子中，

*   截距的 p 值为 1.28e-10，远低于 0.05。
*   年龄的 p 值为 7.87e-05 **，**也远低于标准统计水平。

变量的 p 值越小，预测响应变量的值就越有意义。p 值对应的星星表示各自变量的显著性。由于在我们的模型中，两个 p 值都有一个 3 星，这表明这两个变量在预测因变量(Y)时都非常重要。

## **R 平方和调整后的 R 平方**

R 平方是一种统计方法，代表预测变量(X)解释响应变量(Y)变化的程度。 例如，如果 R-square 为 0.7，这表明反应变量中 70%的变异是由预测变量解释的。因此，R 的平方越高，预测变量就越重要。

一般只有一个预测变量时用 R-square，但如果有多个预测变量呢？

R 平方的问题是，它要么保持不变，要么随着更多变量的增加而增加，即使它们与输出变量没有任何关联。

这就是 ***调整后的 R 方块*** 出现的地方。调整的 R-square 限制您添加不会提高回归模型性能的变量。 因此，如果您正在使用多个预测变量构建回归模型，建议您测量调整后的 R 平方，以检测模型的有效性。

## 【残差标准差】

如前所述，残差用于通过计算实际值和预测值之间的差异来检查模型的效率，当残差标准误差(RSE)被计算为零时(这在现实世界的问题中是极不可能的)，则模型完全符合数据。RSE 主要用于检查模型的准确性，RSE 越低，模型的预测就越准确。

## **F 统计量**

F 统计量是一种统计量，用于判断是否至少有一个自变量具有非零系数。高 F 统计值导致统计上可接受的 p 值(即 p < 0.05)。

在我们的例子中，F 统计值为 21.33，导致 p 值为 7.867e-05，这是非常显著的。

在选择有效的线性回归模型时，我上面讨论的统计方法非常重要。只有当模型在统计上显著时，它才能用于预测因变量。

## **预测线性模型**

有趣的部分来了。在检查了我们的模型的有效性之后，现在让我们在一个单独的测试数据集上测试我们的模型。

因此，我已经创建了一个单独的测试数据框架，我将使用这个数据集来测试模型。

**第一步:**导入测试数据集

```
# Importing test data
testSet = read.csv('/Users/zulaikha/Desktop/test.csv')

```

**第二步:**使用您之前建立的线性回归模型，预测测试数据上的响应变量(血压)

```
# Predicting the test results
regressor = lm(formula = y ~ age, data = trainingSet)
y_pred = predict(regressor, newdata = testSet)

```

**第三步:**评估模型总结

```
summary(regressor)

Call:
lm(formula = y ~ age, data = trainingSet)

Residuals:
Min 1Q Median 3Q Max
-21.724 -6.994 -0.520 2.931 75.654

Coefficients:
            Estimate Std. Error t value Pr(>|t|)
(Intercept) 98.7147   10.0005    9.871   1.28e-10 ***
age         0.9709    0.2102     4.618   7.87e-05 ***
---
Signif. codes: 0 &lsquo;***&rsquo; 0.001 &lsquo;**&rsquo; 0.01 &lsquo;*&rsquo; 0.05 &lsquo;.&rsquo; 0.1 &lsquo; &rsquo; 1

Residual standard error: 17.31 on 28 degrees of freedom
Multiple R-squared: 0.4324, Adjusted R-squared: 0.4121
F-statistic: 21.33 on 1 and 28 DF, p-value: 7.867e-05

```

在上图中，模型 p 值和自变量 p 值小于预先确定的标准显著性水平(0.05)。 由此，我们可以断定我们的模型在统计上是显著的。

注意 R-Sq 和 Adj R-Sq，它们与根据训练数据创建的原始模型比较相似。

**第四步:**计算预测精度

可以通过比较实际值和预测值来测试准确性。

```
#Finding accuracy
actuals_preds <- data.frame(cbind(actuals=testSet$y, predicted=y_pred))
correlation_accuracy <- cor(actuals_preds)
head(actuals_preds)
actuals predicted
1&nbsp; 144&nbsp; &nbsp;136.5787
2&nbsp; 220&nbsp; &nbsp;144.3456
3&nbsp; 138&nbsp; &nbsp;142.4039
4&nbsp; 145&nbsp; &nbsp;144.3456
5&nbsp; 162&nbsp; &nbsp;161.8213
6&nbsp; 142&nbsp; &nbsp;143.3748

```

在上面的输出中，你可以看到预测值和实际值相差不是很远。为了提高准确性，我们可以在更大的数据集上训练模型，并尝试使用其他预测变量。

所以，这就是从零开始在 R 中构建线性回归模型的全部内容。

既然你已经知道了线性回归是如何工作的，我相信你一定很想了解更多关于各种机器学习算法的知识。这里有一个博客列表，深入涵盖了不同类型的机器学习算法

1.  [逻辑回归](https://www.edureka.co/blog/logistic-regression-in-r/)
2.  [支持向量机](https://www.edureka.co/blog/support-vector-machine-in-r/)
3.  [决策树](https://www.edureka.co/blog/decision-trees/)
4.  [K-表示](https://www.edureka.co/blog/k-means-clustering-algorithm/)

这样，我们就结束了 R blog 中的这个线性回归。我希望你觉得这篇博客内容丰富。

请继续关注更多关于趋势技术的博客。

*要深入了解不同的机器学习算法及其各种应用，您可以[在此](https://www.edureka.co/data-science)注册参加实时在线培训，24/7 全天候支持和终身访问。*

*有问题吗？在这篇“R 中的线性回归”博客的评论部分提到它们。*