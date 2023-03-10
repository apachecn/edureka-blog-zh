# 决策树算法完全指南

> 原文：<https://www.edureka.co/blog/decision-tree-algorithm/>

随着用于解决工业级问题的机器学习算法的实现的增加，对更复杂和迭代算法的需求已经成为需要。决策树算法就是这样一种用于解决回归和分类问题的算法。

在这篇关于决策树算法的博客中，你将学习决策树的工作原理，以及如何实现它来解决现实世界中的问题。本博客将涵盖以下主题:

1.  [为什么要决策树？](#Why%20Decision%20Tree)
2.  [什么是决策树？](#What%20Is%20A%20Decision%20Tree)
3.  [决策树算法是如何工作的？](#How%20Does%20The%20Decision%20Tree%20Algorithm%20Work)
4.  [构建决策树](#Building%20A%20Decision%C2%A0Tree)
5.  [使用 R 的决策树算法的实际实现](#Practical%20Implementation%20Of%20Decision%20Tree%20Algorithm%20Using%20R)

要获得深入的数据科学知识，您可以报名参加 Edureka 提供的实时 [*数据科学认证培训*](https://www.edureka.co/data-science) ，该培训提供全天候支持和终身访问。

在我开始为什么使用决策树之前，这里有一个机器学习博客的列表，你应该浏览一下以了解基本知识:

*   [机器学习算法](https://www.edureka.co/blog/machine-learning-algorithms/)
*   [分类算法介绍](https://www.edureka.co/blog/classification-algorithms/)
*   [随机森林分类器](https://www.edureka.co/blog/random-forest-classifier/)

我们都知道有 n 种机器学习算法可以用于分析，那么为什么要选择决策树呢？在下面的部分，我列出了几个原因。

## **为什么要决策树算法？**

决策树被认为是最有用的机器学习算法之一，因为它可以用来解决各种问题。以下是您应该使用决策树的几个原因:

1.  它被认为是最容易理解的机器学习算法，可以很容易地解释。
2.  可用于分类和回归问题。
3.  与大多数机器学习算法不同，它可以有效地处理非线性数据。
4.  构建决策树是一个非常快速的过程，因为它只使用每个节点一个特征来分割数据。

## **什么是决策树算法？**

*A Decision Tree is a Supervised Machine Learning algorithm which looks like an inverted tree, wherein each node represents a predictor variable (feature), the link between the nodes represents a Decision and each leaf node represents an outcome (response variable). *

**为了更好地理解决策树，让我们看一个例子:**

**假设你举办了一个大型聚会，你想知道你的客人中有多少人是非素食者。为了解决这个问题，让我们创建一个简单的决策树。**

**![Decision Tree Example - Decision Tree Algorithm - Edureka](img/a3f131c114f2a58f478374e7b7be653e.png)**

***决策树示例–决策树算法–爱德华卡***

**在上图中，我创建了一个决策树，将客人分为素食者和非素食者。每个节点代表一个预测变量，这将有助于断定一个客人是否是非素食者。当你沿着树向下遍历时，你必须在每个节点做出决定，直到你到达一个死胡同。**

**现在你知道了决策树的逻辑，让我们定义一组与决策树相关的术语。**

### ****决策树的结构****

**![Decision Tree Structure - Decision Tree Algorithm - Edureka](img/926931ea1973bc0a348bd327a83942bb.png)**

***决策树结构——决策树算法——爱德华卡***

**决策树具有以下结构:**

***   **根节点:**根节点是一棵树的起点。此时，将执行第一次拆分。*   **内部节点:**每个内部节点代表一个最终导致预测结果的决策点(预测变量)。*   **叶/终端节点:**叶节点代表结果的最后一类，因此它们也被称为终端节点。*   **分支:**分支是节点间的连接，用箭头表示。每个分支代表一个响应，如“是”或“否”**

**这就是决策树的基本结构。现在让我们试着理解决策树的工作流程。**

## ****决策树算法是如何工作的？****

**决策树算法遵循以下步骤:**

****步骤 1:** 选择将数据集分类到所需类别的最佳特征(预测变量),并将该特征分配给根节点。 **步骤 2:** 从根节点向下遍历，同时在每个内部节点做出相关决策，使得每个内部节点对数据进行最佳分类。 **第三步:**返回第一步，重复直到你给输入数据分配一个类别。**

**上述步骤代表了用于分类目的的决策树的一般工作流程。**

**现在让我们试着理解决策树是如何创建的。**

## ****使用 ID3 算法构建决策树****

**构建决策树的方法有很多，在这篇博客中，我们将重点介绍如何使用 ID3 算法来创建决策树。**

### ****ID3 算法是什么？****

**ID3 或迭代二分法 3 算法是用于构建决策树的最有效的算法之一。它使用*熵*和*信息增益*的概念为给定的数据集生成决策树。**

****ID3 算法:****

**ID3 算法遵循以下工作流程来构建决策树:**

***   选择**最佳属性** (A)*   指派一个作为根节点的决策变量。*   对于的每个值，生成该节点的后代。*   将分类标签分配给叶节点。*   如果数据分类正确:停止。*   否则:遍历树。**

**该算法的第一步规定我们必须选择最佳属性。那是什么意思？**

***最佳属性(预测变量)是最有效地将数据集分成不同类别的属性，或者是最好地分割数据集的特征。***

**现在，你脑海中的下一个问题一定是，“*我如何决定哪个变量/特征最好地分割数据？***

**使用两种方法来确定最佳属性:**

***   信息增益*   熵**

### ****什么是熵？****

***Entropy measures the impurity or uncertainty present in the data. It is used to decide how a Decision Tree can split the data.*********Equation For Entropy:**

### **![Entropy formula - Decision Tree Algorithm - Edureka](img/0cc2a31f0d54409bdc40fb721fee607d.png)**

### **什么是信息增益？**

*Information Gain (IG) is the most significant measure used to build a Decision Tree. It indicates how much “information” a particular feature/ variable gives us about the final outcome.*

**信息增益很重要，因为它用来选择在决策树的每个节点上最好地分割数据的变量。具有最高 IG 的变量用于在根节点拆分数据。**

****信息增益(IG)方程:****

**![Information Gain formula - Decision Tree Algorithm - Edureka](img/4ed9a0551f4f9a51b3fabc85315284f3.png)**

**为了更好地理解如何使用信息增益和熵来创建决策树，让我们看一个例子。下面的数据集代表了基于某些参数的汽车速度。**

**![Speed Data Set - Decision Tree Algorithm - Edureka](img/6edf07c0f154b135662dc33445fdaf3c.png)**

***速度数据集——决策树算法——爱德华卡***

**你的问题陈述是研究这个数据集并创建一个决策树，根据以下预测变量将汽车速度(响应变量)分为慢或快:**

***   道路类型*   障碍*   速度限制**

**我们将使用这些变量构建一个决策树，以预测汽车的速度。正如我前面提到的，我们必须首先决定一个能最好地分割数据集的变量，并将该变量分配给根节点，并对其他节点重复同样的操作。**

**此时，您可能想知道如何知道哪个变量最好地分隔了数据？答案是，具有最高信息增益的变量最好地将数据划分到所需的输出类中。**

**因此，让我们从计算每个预测变量的熵和信息增益(IG)开始，从“道路类型”开始。**

**在我们的数据集中，“道路类型”列中有四个观察值，对应于“汽车速度”列中的四个标签。我们将从计算父节点的熵(汽车的速度)开始。**

**第一步是找出父节点中存在的两个类的比例。我们知道父节点中总共有四个值，其中两个样本属于“慢”类，另外两个属于“快”类，因此:**

***   p(慢)->父节点中“慢”结果的分数*   p(快速)->父节点中“快速”结果的分数**

**计算 P(慢)的公式为:**

***p(慢)=父节点中“慢”结果的数量/结果总数***

**![p(slow) formula - Decision Tree Algorithm - Edureka](img/64df81c159e45c81f2014893dfa152f7.png)**

**同样，计算 P(fast)的公式为:**

***p(fast) =父节点中“快速”结果的数量/结果总数***

**![p(fast) formula - Decision Tree Algorithm - Edureka](img/91e5bcb34096c5e5aff0a9a6fd7ddc36.png)因此，父节点的熵为:**

**![Entropy parent - Decision Tree Algorithm - Edureka](img/846a32c314fb8b71fe58d083261055f6.png)**

***熵(父)= –{ 0.5 log2(0.5)+0.5 log2(0.5)}**=–{-0.5+(-0.5)}**= 1***

**现在我们知道父节点的熵是 1，让我们看看如何计算“道路类型”变量的信息增益。请记住，如果“道路类型”变量的信息增益大于所有其他预测变量的信息增益，则只能使用“道路类型”变量来分割根结点。**

**为了计算“道路类型”变量的信息增益，我们首先需要通过“道路类型”变量来拆分根节点。**

***![Decision Tree (Road type) - Decision Tree Algorithm - Edureka](img/3b3dd2ee8af16bb6c50ab1104fa036b1.png)决策树(道路类型)——决策树算法——爱德华卡***

**在上图中，我们使用“道路类型”变量分割了父节点，子节点表示数据集中显示的相应响应。现在，我们需要测量子节点的熵。**

**右侧子节点(fast)的熵是 0，因为该节点中的所有结果都属于一个类(fast)。以类似的方式，我们必须找到左手边节点的熵(慢，慢，快)。**

**在这个节点中，有两种类型的结果(快速和慢速)，因此，我们首先需要计算这个特定节点的慢速和快速结果的比例。**

***P(慢)= 2/3 = 0.667*T2*P(快)= 1/3 = 0.334***

**因此，熵是:**

***熵(左子节点)= –{ 0.667 log2(0.667)+0.334 log2(0.334)}**=–{-0.38+(-0.52)}**= 0.9***

**我们的下一步是用加权平均计算熵(子代):**

***   父节点中的结果总数:4*   左侧子节点中的结果总数:3*   右子节点中的结果总数:1**

**带加权平均值的熵公式(子代)。：**

***[Weighted avg]Entropy(children) = (no. of outcomes in left child node) / (total no. of outcomes in parent node) * (entropy of left node) + (no. of outcomes in right child node)/ (total no. of outcomes in parent node) * (entropy of right node)***

****通过使用上面的公式你会发现，熵(儿童)与加权平均。is = 0.675****

****我们的最后一步是将上述加权平均值代入 IG 公式，以计算“道路类型”变量的最终 IG:****

****![Information Gain formula - Decision Tree Algorithm - Edureka](img/73e0cc85151cb218da6a909c62930856.png)因此，****

*****信息增益(道路类型)= 1–0.675 = 0.325*****

*****道路类型特征的信息增益为* 0.325。****

****像我前面提到的，决策树算法选择信息增益最高的变量来拆分决策树。因此，通过使用上述方法，您需要计算所有预测变量的信息增益，以检查哪个变量具有最高的 IG。****

****因此，通过使用上述方法，您必须获得每个预测变量的以下值:****

*****   *信息增益(道路类型)= 1–0.675 = 0.325**   *信息增益(障碍)= 1–1 = 0**   *信息增益(限速)= 1–0 = 1*****

****因此，这里我们可以看到“速度限制”变量具有最高的信息增益。因此，该数据集的最终决策树是使用“速度限制”变量构建的。****

****![Decision Tree (Speed limit) - Decision Tree Algorithm - Edureka](img/d181347e390b63d84768c55bc1185e0c.png)****

*****决策树(限速)——决策树算法——爱德华卡*****

****现在您已经知道了决策树是如何创建的，让我们运行一个简短的演示，通过实现决策树来解决一个现实世界中的问题。****

## ******R 中决策树的实现——决策树算法示例******

******问题陈述:**研究一个蘑菇数据集，以便预测给定的蘑菇对人类是可食用的还是有毒的。****

******数据集描述:** 给定的数据集包含总共 8124 个不同种类蘑菇的观察值及其属性，如气味、栖息地、种群等。下面的演示展示了数据集的更深入的结构。****

******逻辑:**建立决策树模型，通过研究蘑菇样品的气味、根、生境等属性，将蘑菇样品分类为有毒或可食用。****

****现在你知道了这个演示的目的，让我们开动脑筋，开始编码吧。对于这个演示，我将使用 R 语言来构建模型。****

****如果你想了解更多关于 R 编程的知识，你可以看看这段由我们的 R 编程专家录制的视频。****

## ******R 初学者教程| edu reka******

********

****[//www.youtube.com/embed/eDrhZb2onWY?rel=0&showinfo=0](//www.youtube.com/embed/eDrhZb2onWY?rel=0&showinfo=0)****

****这个视频将帮助你理解 R 工具的基本原理，并帮助你建立一个坚实的 R 基础****

****现在，我们开始吧。****

******步骤 1:** 安装并加载库****

```
 ****#Installing libraries
install.packages('rpart')
install.packages('caret')
install.packages('rpart.plot')
install.packages('rattle')

#Loading libraries
library(rpart,quietly = TRUE)
library(caret,quietly = TRUE)
library(rpart.plot,quietly = TRUE)
library(rattle)**** 
```

******第二步:**导入数据集****

```
 ****#Reading the data set as a dataframe
mushrooms <- read.csv ("/Users/zulaikha/Desktop/decision_tree/mushrooms.csv")**** 
```

****现在，要显示数据集的结构，可以使用名为 str()的 R 函数:****

```
 ****# structure of the data
> str(mushrooms)
'data.frame': 8124 obs. of 22 variables:
$ class : Factor w/ 2 levels "e","p": 2 1 1 2 1 1 1 1 2 1 ...
$ cap.shape : Factor w/ 6 levels "b","c","f","k",..: 6 6 1 6 6 6 1 1 6 1 ...
$ cap.surface : Factor w/ 4 levels "f","g","s","y": 3 3 3 4 3 4 3 4 4 3 ...
$ cap.color : Factor w/ 10 levels "b","c","e","g",..: 5 10 9 9 4 10 9 9 9 10 ...
$ bruises : Factor w/ 2 levels "f","t": 2 2 2 2 1 2 2 2 2 2 ...
$ odor : Factor w/ 9 levels "a","c","f","l",..: 7 1 4 7 6 1 1 4 7 1 ...
$ gill.attachment : Factor w/ 2 levels "a","f": 2 2 2 2 2 2 2 2 2 2 ...
$ gill.spacing : Factor w/ 2 levels "c","w": 1 1 1 1 2 1 1 1 1 1 ...
$ gill.size : Factor w/ 2 levels "b","n": 2 1 1 2 1 1 1 1 2 1 ...
$ gill.color : Factor w/ 12 levels "b","e","g","h",..: 5 5 6 6 5 6 3 6 8 3 ...
$ stalk.shape : Factor w/ 2 levels "e","t": 1 1 1 1 2 1 1 1 1 1 ...
$ stalk.root : Factor w/ 5 levels "?","b","c","e",..: 4 3 3 4 4 3 3 3 4 3 ...
$ stalk.surface.above.ring: Factor w/ 4 levels "f","k","s","y": 3 3 3 3 3 3 3 3 3 3 ...
$ stalk.surface.below.ring: Factor w/ 4 levels "f","k","s","y": 3 3 3 3 3 3 3 3 3 3 ...
$ stalk.color.above.ring : Factor w/ 9 levels "b","c","e","g",..: 8 8 8 8 8 8 8 8 8 8 ...
$ stalk.color.below.ring : Factor w/ 9 levels "b","c","e","g",..: 8 8 8 8 8 8 8 8 8 8 ...
$ veil.color : Factor w/ 4 levels "n","o","w","y": 3 3 3 3 3 3 3 3 3 3 ...
$ ring.number : Factor w/ 3 levels "n","o","t": 2 2 2 2 2 2 2 2 2 2 ...
$ ring.type : Factor w/ 5 levels "e","f","l","n",..: 5 5 5 5 1 5 5 5 5 5 ...
$ spore.print.color : Factor w/ 9 levels "b","h","k","n",..: 3 4 4 3 4 3 3 4 3 3 ...
$ population : Factor w/ 6 levels "a","c","n","s",..: 4 3 3 4 1 3 3 4 5 4 ...
$ habitat : Factor w/ 7 levels "d","g","l","m",..: 6 2 4 6 2 2 4 4 2 4 ...**** 
```

****输出显示了许多用于预测蘑菇输出类别(有毒或可食用)的预测变量。****

******第三步:**数据清洗****

****在这个阶段，我们必须寻找任何空值或缺失值以及不必要的变量，以便我们的预测尽可能准确。在下面的代码片段中，我删除了“veil.type”变量，因为它对结果没有影响。这种不一致和冗余数据必须在这一步得到解决。****

```
 ****# number of rows with missing values
nrow(mushrooms) - sum(complete.cases(mushrooms))

# deleting redundant variable `veil.type`
mushrooms$veil.type <- NULL**** 
```

******第四步:**数据探索与分析****

****为了更好地理解 21 个预测变量，我为每个预测变量与类别类型(响应/结果变量)创建了一个表，以了解特定的预测变量对于检测输出是否重要。****

****我只显示了“气味”变量的表格，您可以按照下面的代码片段为每个变量创建一个表格:****

```
 ****# analyzing the odor variable
> table(mushrooms$class,mushrooms$odor)
a&nbsp; &nbsp; &nbsp;&nbsp;c&nbsp; &nbsp; &nbsp; f&nbsp; &nbsp; &nbsp; &nbsp;l&nbsp; &nbsp; &nbsp; &nbsp;m&nbsp; &nbsp; &nbsp; &nbsp;n&nbsp; &nbsp; &nbsp; &nbsp;p&nbsp; &nbsp; &nbsp; &nbsp; s&nbsp; &nbsp; &nbsp; y
e&nbsp; &nbsp;400&nbsp; &nbsp; &nbsp;0&nbsp; &nbsp; &nbsp; 0&nbsp; &nbsp; &nbsp;400&nbsp; &nbsp; &nbsp;0&nbsp; &nbsp; 3408&nbsp; &nbsp; 0&nbsp; &nbsp; &nbsp; &nbsp;0&nbsp; &nbsp; &nbsp; 0
p&nbsp; &nbsp;0&nbsp; &nbsp; &nbsp; 192&nbsp; &nbsp;2160&nbsp; 0&nbsp; &nbsp; &nbsp; 36&nbsp; &nbsp; &nbsp;120&nbsp; &nbsp; 256&nbsp; 576&nbsp; 576**** 
```

****在上面的片段中，“e”代表可食用类，“p”代表蘑菇的有毒类。****

****上面的输出显示气味值为' c '，' f '，' m '，' p '，' s '和' y '的蘑菇明显有毒。并且具有杏仁气味(400)的蘑菇是可食用的。这样的观察将帮助我们更准确地预测输出类。****

****我们在数据探索阶段的下一步是预测哪个变量是分裂决策树的最佳变量。出于这个原因，我绘制了一个图表，表示 21 个变量中每个变量的分割，输出如下所示:****

```
 ****number.perfect.splits <- apply(X=mushrooms[-1], MARGIN = 2, FUN = function(col){
t <- table(mushrooms$class,col)
sum(t == 0)
})

# Descending order of perfect splits
order <- order(number.perfect.splits,decreasing = TRUE)
number.perfect.splits <- number.perfect.splits[order]

# Plot graph
par(mar=c(10,2,2,2))
barplot(number.perfect.splits,
main="Number of perfect splits vs feature",
xlab="",ylab="Feature",las=2,col="wheat")**** 
```

****![rpart.plot - Decision Tree Algorithm - Edureka](img/491b5ae6d2f70140c34ff8dd7220a0bf.png)****

*****r part . plot–决策树算法–edu reka*****

****输出结果表明,“气味”变量在预测蘑菇的输出类别中起着重要作用。****

******第五步:**数据拼接****

****数据拼接是将数据拆分为训练集和测试集的过程。训练集用于构建决策树模型，测试集用于验证模型的效率。拆分是在下面的代码片段中执行的:****

```
 ****#data splicing
set.seed(12345)
train <- sample(1:nrow(mushrooms),size = ceiling(0.80*nrow(mushrooms)),replace = FALSE)
# training set
mushrooms_train <- mushrooms[train,]
# test set
mushrooms_test <- mushrooms[-train,]**** 
```

****为了让这个演示更有趣，也为了尽量减少误归类为可食用的毒蘑菇的数量，我们将指定一个比因显而易见的原因将一种可食用蘑菇归类为有毒的惩罚大 10 倍的惩罚。****

```
 ****# penalty matrix
penalty.matrix <- matrix(c(0,1,10,0), byrow=TRUE, nrow=2)**** 
```

******第六步:**建立模型****

****在这一阶段，我们将使用 rpart (递归分区和回归树)算法构建一个决策树:****

```
 ****# building the classification tree with rpart
tree <- rpart(class~.,
data=mushrooms_train,
parms = list(loss = penalty.matrix),
method = "class")**** 
```

****第七步:将树可视化****

****在这一步中，我们将使用 rpart.plot 库来绘制最终的决策树:****

```
 ****# Visualize the decision tree with rpart.plot
rpart.plot(tree, nn=TRUE)**** 
```

******![Decision Tree - Decision Tree Algorithm - Edureka](img/27b65095b61770a8df4ff8523ab27a37.png)******

*****决策树——决策树算法——爱德华卡*****

******步骤 8:** 测试模型****

****现在，为了测试我们的决策树模型，我们将对我们的模型应用测试数据集，如下所示:****

```
 ****#Testing the model
pred <- predict(object=tree,mushrooms_test[-1],type="class")**** 
```

******第九步:**计算精度****

****我们将使用混淆矩阵来计算模型的准确性。代码如下:****

```
 ****#Calculating accuracy
t <- table(mushrooms_test$class,pred) > confusionMatrix(t)
Confusion Matrix and Statistics

pred
e&nbsp; &nbsp; &nbsp; p
e&nbsp; 839&nbsp; &nbsp; 0
p&nbsp; 0&nbsp; &nbsp; &nbsp;785

Accuracy : 1
95% CI : (0.9977, 1)
No Information Rate : 0.5166
P-Value [Acc > NIR] : < 2.2e-16

Kappa : 1
Mcnemar's Test P-Value : NA

Sensitivity : 1.0000
Specificity : 1.0000
Pos Pred Value : 1.0000
Neg Pred Value : 1.0000
Prevalence : 0.5166
Detection Rate : 0.5166
Detection Prevalence : 0.5166
Balanced Accuracy : 1.0000

'Positive' Class : e**** 
```

****输出显示测试数据集中的所有样本都已被正确分类，我们在测试数据集上获得了 100%的准确率，置信区间为 95%(0.9977，1)。因此，我们可以使用决策树模型正确地将蘑菇分类为有毒或可食用。****

****既然你已经知道了决策树算法是如何工作的，我相信你一定很想了解更多关于各种机器学习算法的知识。这里有一个博客列表，深入涵盖了不同类型的机器学习算法:****

*****   [线性回归](https://www.edureka.co/blog/linear-regression-in-r/)*   [逻辑回归](https://www.edureka.co/blog/logistic-regression-in-r/)*   [支持向量机](https://www.edureka.co/blog/support-vector-machine-in-r/)*   [随机森林](https://www.edureka.co/blog/random-forest-classifier/)*   [K-表示](https://www.edureka.co/blog/k-means-clustering-algorithm/)****

****就这样，我们结束了这篇博客。我希望你们都觉得这篇博客内容丰富。如果你有任何想法分享，请在下面评论。敬请关注更多类似的博客！****

*****如果你正在寻找数据科学的在线结构化培训，edureka！有专门策划的  [数据科学课程](https://www.edureka.co/data-science) ，帮助您获得统计学、数据争论、探索性数据分析、机器学习算法(如 K 均值聚类、决策树、随机森林、朴素贝叶斯)方面的专业知识。您将学习时间序列的概念、文本挖掘以及深度学习的介绍。本课程的新批次即将开始！！*********