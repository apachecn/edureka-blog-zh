# 2023 年你必须准备的 50 R 面试题

> 原文：<https://www.edureka.co/blog/interview-questions/r-interview-questions/>

下面是 2023 年你必须准备的*前 50 R 面试问答*。本博客涵盖了你在 R .上面试时可以问的所有重要问题。这些 R 面试问题将让你在蓬勃发展的分析市场中占据优势，在这个市场中，全球和本地企业，无论大小，都在寻找拥有 R 认证专业知识的 ***[【专业人士】。](https://www.edureka.co/r-for-analytics)***

T2 是一种编程语言，你想让它有多有用它就有多有用。这是一个供您使用的工具，可用于多种目的，如统计分析、数据可视化、数据处理、预测建模、预测分析等等。谷歌、脸书和推特等顶级公司都使用 r。

## **R 面试问题** :

### **1。R 中有哪些不同的数据结构？简单解释一下。**

一般来说，这些是 R: 中可用的数据结构

 <caption>#### **R 中的数据结构**</caption> 
| **数据结构** | **描述** |
| ***矢*** | **向量**是相同基本类型的数据元素序列。向量中的成员被称为**分量**。 |
| ***列表*** | **列表**是包含不同类型元素的 R 对象，如数字、字符串、向量或其他列表。 |
| ***矩阵*** | 一个**矩阵**是一个二维数据结构。矩阵用于绑定相同长度的向量。矩阵的所有元素必须是同一类型(数字、逻辑、字符、复杂)。 |
| ***数据帧*** | **数据帧**比矩阵更通用，即不同的列可以有不同的数据类型(数字、字符、逻辑等)。它 结合了矩阵和列表的特性，就像一个矩形列表。 |

### **2。如何在 R 中加载一个. csv 文件？**

*   在 R 中加载一个. csv 文件相当容易。
*   你需要做的就是使用“read.csv()”函数，指定文件的路径。

```
house<-read.csv("C:/Users/John/Desktop/house.csv")
```

**3。图形语法的不同组成部分是什么？**

从广义上讲，这些是图形语法中的不同成分:

*   数据层
*   美学层
*   几何图层
*   刻面层
*   坐标层
*   主题层

### **4。什么是 Rmarkdown？有什么用？**

RMarkdown 是 R 提供的一个报告工具，在它的帮助下，你可以为你的 R 代码创建高质量的报告。

Rmarkdown 的输出格式可以是:

*   HTML
*   PDF
*   字

### **5。如何在 R 中安装一个包？**

下面的命令用于在 R: 中安装包

```
`install.packages(“<package_name>”)`
```

我们来看一个例子:

![install-R Interview Questions-Edureka](img/264c5caa76a87964b22608e08f03611e.png)

R 面试问题

### **6。R 中建立和评估一个线性回归模型的步骤有哪些？**

这些是建立线性回归模型时需要遵循的连续步骤:

*   从将数据分为训练集和测试集开始，这一步至关重要，因为您将在训练集上构建模型，并在测试集上评估其性能。
    *   你可以使用“catools”包中的 sample.split()函数来完成。该功能提供了一个分流比选项，您可以根据自己的需要进行指定。

![split-R Interview Questions-Edureka](img/cb3ca3dad643bc603d3dfc5c12ca29aa.png)

R 面试问题

*   一旦将数据分成训练集和测试集，您就可以继续在训练集上构建模型。
    *   “lm()”函数用于建立模型。

![linear-R Interview Questions-Edureka](img/28a08c4ac860f5c25924963cb56d64ae.png)

R 面试问题

*   最后，您可以使用“predict()”函数来预测测试集上的值。

![predict-R Interview Questions-Edureka](img/9da08d447fa45518f993e514224ef7e4.png)

R 面试问题

*   最后一步是找出 RMSE，RMSE 值越低，预测越好。

**![rmse-R Interview Questions-Edureka](img/9b90aba8163464dc10a7564fa0d4afcd.png)**

R 面试问题

**7。说出一些 R 中的包，可以用于数据插补？**

这些是 R 中的一些包，可用于数据插补

*   老鼠

*   阿米莉亚
*   错过森林
*   Hmisc
*   米
*   过帐

**8。关于 R 中混淆矩阵的解释？**

混淆矩阵可以用来评估所建模型的准确性。它计算观察和预测类的交叉列表。这可以使用“caTools”包中的“confusionmatrix()”函数来完成。

![confusionMatrix-R Interview Questions-Edureka](img/ff33c004d347254dcd717fb4faa17a4f.png)

在这里，我们创建了一个混淆矩阵，给出了“实际”和“预测”值的列表。

**9。你如何用 R 编写一个自定义函数？举个例子。**

这是在 R: 中编写自定义函数的语法

<对象名称>=函数(x){

—

—

—

}

让我们来看一个在 R->T1 中创建自定义函数的例子

```
`fun1<-function(x){` `ifelse(x>5,100,0)` `}` 
```

```
`v<-c(1,2,3,4,5,6,7,8,9,10)`
```

```
`fun1(v)->v` 
```

### **10。说出“dplyr”包中一些可用的函数。**

dplyr 包中的函数:

*   过滤器
*   选择
*   变异
*   排列
*   计数

### **11。你将如何创建一个新的 R6 类？**

我们必须首先创建一个对象模板，它由类中的“数据成员”和“类函数”组成。

R6 对象模板由这些部分组成- >

*   类名
*   私有数据成员
*   公共成员函数

让我们通过代码->来了解对象模板

### **![R6Class-R Interview Questions-Edureka](img/9814d78f356c3c988d1c4b8952cb38f1.png)**

以上代码由以下部分组成:

*   类别名称—“员工”
*   私人数据成员—“姓名”&“称号”
*   公共成员函数-" set _ name()"&" set _ designation "

### **12。什么是随机森林？如何在 R 中构建和评估随机森林？**

随机森林是使用许多决策树模型制作的集成分类器。它结合了许多决策树模型的结果，这个结果通常比任何单个模型的结果都好。

我们将使用由以下几列组成的“出生”数据集:

### **![birth-R Interview Questions-Edureka](img/1a73bb55fd27f06f314434cc33cb6654.png)**

让我们在此基础上建立一个随机森林模型来预测“吸烟”一栏，即母亲是否吸烟。

*   让我们从将数据分为训练和测试开始->-

### **![train_test-R Interview Questions-Edureka](img/3d19ade47316358355d984f034053687.png)**

*   在列车上建立随机森林模型>-

```
`randomForest(smoke~.,birth)->mod1`
```

*   现在，我们将在测试集上预测模型- >

```
`predict(mod1,test)->result`
```

### **13。说说 shinyR 吧。**

Shiny 是一个 R 包，它使得直接从 R 构建交互式 web 应用变得容易。你可以在网页上托管独立的应用，或者将它们嵌入到 Rmarkdown 文档中，或者构建仪表板。您还可以用 CSS 主题、htmlwidgets 和 JavaScript 动作来扩展您的闪亮应用程序。

### **14。在 R 中使用 apply 函数族有什么好处？**

应用功能允许我们对数据帧和矩阵进行逐项更改。

R 中的用法如下:

apply(X，MARGIN，FUN，…)

其中:

X 是数组或矩阵；

MARGIN 是一个变量，决定函数是应用于行(MARGIN=1)、列(MARGIN=2)，还是两者(MARGIN=c(1，2))；

乐趣是要应用的功能。

如果 MARGIN=1，该函数接受 X 的每一行作为向量参数，并返回结果的向量。类似地，如果 MARGIN=2，该函数作用于 x 的列。最令人印象深刻的是，当 MARGIN=c(1，2)时，该函数应用于 x 的每个条目

优势:

使用应用功能，我们可以用一行命令编辑数据帧的每个条目。没有自动填充，没有浪费 CPU 周期。

### **15。R 中数据挖掘用的是什么包？**

R 中用于数据挖掘的一些包:

*   data.table-提供大文件的快速读取
*   rpart 和 caret——用于机器学习模型。
*   Arules-用于关联规则学习。
*   GGplot-提供 varios 数据可视化绘图。
*   tm-执行文本挖掘。
*   预测-提供时间序列分析功能

### **16。什么是集群？kmeans 聚类和层次聚类有什么区别？**

集群是属于同一类的一组对象。聚类是将一组抽象对象分成相似对象的类的过程。

让我们看看为什么在数据分析中需要聚类:

*   可伸缩性——我们需要高度可伸缩的集群算法来处理大型数据库。
*   处理不同种类属性的能力——算法应该能够应用于任何种类的数据，例如基于区间的(数字)数据、分类数据和二进制数据。
*   发现具有属性形状的聚类——聚类算法应该能够检测任意形状的聚类。它们不应该只局限于倾向于发现小尺寸球状星团的距离度量。
*   高维度——聚类算法不仅应该能够处理低维数据，还应该能够处理高维空间。
*   处理噪音数据的能力——数据库包含噪音、缺失或错误的数据。一些算法对此类数据很敏感，可能导致聚类质量差。
*   可解释性——聚类结果应该是可解释的、可理解的和可用的。

K 均值聚类:

K-means 聚类是一种众所周知的划分方法。在该方法中，物体被分类为属于 K 组之一。划分方法的结果是一组 K 个聚类，数据集的每个对象属于一个聚类。在每个聚类中，可以有质心或聚类代表。在我们考虑实值数据的情况下，一个聚类内所有对象的属性向量的算术平均值提供了一个适当的代表；在其他情况下，可能需要其他类型的质心。

例如:一个文档簇可以由在一个簇内最少数量的文档中出现的那些关键词的列表来表示。如果聚类的数量很大，可以进一步对质心进行聚类，以在数据集中产生层次结构。K-means 是一种对数据样本进行聚类的数据挖掘算法。为了对数据库进行聚类，K-means 算法使用了一种迭代方法。

R 代码

#确定集群数量

```
`wss <- (nrow(mydata)-1)*sum(apply(mydata,2,var))`
```

```
`for (i in 2:15) wss[i] <- sum(kmeans(mydata,`
```

```
`centers=i)$withinss)`
```

```
`plot(1:15, wss, type=”b”, xlab=”Number of Clusters”,`
```

```
`ylab=”Within groups sum of squares”)`
```

# K-均值聚类分析

```
`fit <- kmeans(mydata, 5) # 5 cluster solution`
```

# get cluster 表示

```
`aggregate(mydata,by=list(fit$cluster),FUN=mean)`
```

#追加集群分配

```
`mydata <- data.frame(mydata, fit$cluster)`
```

可以通过使用 pam()而不是 kmeans()来调用基于 mediods 的健壮版本的 K-means。fpc 包中的函数 pamk()是 pam 的包装器，它还根据最佳平均轮廓宽度打印建议的聚类数。

层次聚类:

这个方法创建一个给定数据对象集合的层次分解。我们可以根据层次分解是如何形成的来对层次方法进行分类。这里有两种方法:

1.  凝聚法
2.  分裂的方法

凝聚法:

这种方法也被称为自下而上的方法。在这里，我们从每个对象组成一个单独的组开始。它不断合并彼此靠近的对象或组。它继续这样做，直到所有的组合并成一个组，或者直到终止条件成立。

分裂法:

这种方法也被称为自顶向下的方法。在这里，我们从同一个集群中的所有对象开始。在连续迭代中，一个集群被分成更小的集群。直到一个集群中的每个对象或终止条件成立。这种方法是严格的，也就是说，一旦合并或拆分完成，就永远无法撤消。

R 代码

汽车示例

# mt cars 数据集内置于 R:

```
`help(mtcars)`
```

#我们将关注本质上连续而非离散的变量:

```
`cars.data <- mtcars[,c(1,3,4,5,6,7)]`
```

#除以每个变量的样本范围进行标准化

```
`samp.range <- function(x){`
```

```
`myrange <- diff(range(x))`
```

```
`return(myrange)`
```

```
`}`
```

```
`my.ranges <- apply(cars.data,2,samp.range)`
```

```
`cars.std <- sweep(cars.data,2,my.ranges,FUN=”/”)`
```

#获取距离矩阵:

T2`dist.cars <- dist(cars.std)`

#单联动:

T2`cars.single.link <- hclust(dist.cars, method=’single’)`

#绘制单连锁树状图:

T2`plclust(cars.single.link, labels=row.names(cars.data), ylab=”Distance”)`

#打开新窗口，同时保持前一个窗口打开

T2`windows()`

#完成联动:

```
`cars.complete.link <- hclust(dist.cars, method=’complete’)`
```

#绘制完整的连锁树状图:

```
`plclust(cars.complete.link, labels=row.names(cars.data), ylab=”Distance”)`
```

#平均联动:

```
`cars.avg.link <- hclust(dist.cars, method=’average’)`
```

#绘制平均连锁树:

```
`plclust(cars.avg.link, labels=row.names(cars.data), ylab=”Distance”)`
```

#平均连锁树状图似乎表明了两个主要的聚类，

#单个连锁树状图可能表示三个。

#单联动方案:

```
`cut.3 <- cutree(cars.single.link, k=3)`
```

#打印“聚类向量”

T2`cut.3`

```
`cars.3.clust <- lapply(1:3, function(nc) row.names(cars.data)[cut.3==nc])`
```

#根据汽车名称打印聚类

T2`cars.3.clust`

#集群 1 似乎大多是紧凑型车，集群 2 是跑车，集群 3 是大型豪华轿车

### **17。给出 R** 中“rbind()”和“cbind()”函数的例子

Cbind():顾名思义，用于将两列绑定在一起。绑定两列时要记住的一个事实是，两列中的行数需要相同。

我们用一个例子来理解这个:

这是“分数”数据集，由三个科目的分数组成- >

![marks-R Interview Questions-Edureka](img/84c8c10df599d19fd5b8f07408a4536c.png)

我们将它与一个新的数据集“Percentage”绑定，该数据集由两列组成:- >“总计”和“百分比”

![total-R Interview Questions-Edureka](img/e5824dcd54dd21ca1d727594853fc893.png)

让我们使用“cbind()”函数- > 将这两个数据集中的列组合起来

```
cbind(Marks,Percentage)
```

### **![cbind-R Interview Questions-Edureka](img/6a138deaae09e3f8f7a2228bc6d9ab37.png)**

由于两个数据集中的行数相同，我们在“cbind()”函数的帮助下合并了列

### **18。给出 r .**中 while 和 for 循环的例子

While 循环:

![while-R Interview Questions-Edureka](img/d2fd6c1ae4c2a8d53af92da786105120.png)

For 循环:

### **![for-R Interview Questions-Edureka](img/9ee7a98601a1860d3047c7d8253dca6d.png)**

### **19。给出“dplyr”包中“选择”和“过滤”函数的例子。**

![birth_weight_data_R Interview Questions-Edureka](img/85a6f40c6b8728619d81ac012cfe9733.png)

Select:该函数来自“dplyr”包，用于从数据集中选择一些特定的列

```
`Birth_weight %>% select(1,2,3)->birth`
```

![birth1_3-R Interview Questions-Edureka](img/6a82e99d79089586293acc61f46281ac.png)

```
Birth_weight %>% select(-5)->birth
```

**![birth-R Interview Questions-Edureka](img/8d3ce1810469b66ee608a35ec4089aa8.png)**

Filter:【DP lyr】包中的这个函数用于根据条件过滤掉一些行:

```
`Birth_weight %>% filter(mother_age>35)->birth`
```

![birth35-R Interview Questions-Edureka](img/22edb1cc630df7904484dcaff779cd47.png)

```
`Birth_weight %>% filter(baby_wt>125 & smoke=="smoker")->birth`
```

![birthsmoke-R Interview Questions-Edureka](img/37ddd5620c8f59b8f22ef6cba12881b2.png)

### **20。stringR 包有什么用？举一些 Stringr 中函数的例子。**

StringR 中的一些函数:

初始:

水果- >

![fruit1-R Interview Questions-Edureka](img/c0a1466d2d9b1f0d298950fdb821446b.png)

*   将字符串转换为大写:

```
str_to_upper(fruit)
```

### **![fruit_capital-R Interview Questions-Edureka](img/5b5ad585aaf1048c791c3917fe72de72.png)**

*   计算字母的数量:

```
str_count(fruit)
```

### **![count_str-R Interview Questions-Edureka](img/5c31af83b6f04979a2854be8be77608d.png)**

### **21。你对 R 里的拨浪鼓包了解多少？**

**拨浪鼓**是一个使用 [R](https://www.r-project.org/) 进行数据挖掘的流行 GUI。它提供数据的统计和可视化摘要，转换数据以便可以轻松建模，根据数据构建无监督和有监督的机器学习模型，以图形方式呈现模型的性能，并对新数据集进行评分以部署到生产中。*一个关键的特性是，你通过图形用户界面的所有交互都被捕获为一个 R 脚本，可以独立于 Rattle 界面在 R 中执行。*

### **22。在 R 语言中，如何在一个页面上绘制多个图形？**

使用基本图形在一个页面上绘制多个图非常容易:

例如，如果你想在同一个面板上绘制 4 个图形，你可以使用下面的命令:

```
par(mfrow=c(2,2))
```

![plot-R Interview Questions-Edureka](img/52b8e3df4ca71883fbc439a60c80c1f2.png)

### **![hist-R Interview Questions-Edureka](img/6b8bd9b2dd2dd1f9197babcbf8793780.png)**

### **23。如何使用 ggplot2 软件包创建散点图？**

散点图可用于同时显示两个或多个实体之间的相关性。

让我们举一个例子，了解如何使用 ggplot2 软件包- > 制作散点图

```
ggplot(iris,aes(y=Sepal.Length,x=Petal.Length))+geom_point()
```

### **![scatter-R Interview Questions-Edureka](img/5ccb9456b31a14fcc4a7b74c9eeac05d.png)**

### **24。你将如何使用 ggplot2 包对数据进行分面？**

让我们举个例子来了解一下用 ggplot2 刻面

初始:

```
ggplot(house,aes(y=price,x=waterfront))+geom_boxplot()
```

### **![boxpot-R Interview Questions-Edureka](img/cef61464a3b20e55b11cfe72fb33078b.png)**

```
ggplot(house,aes(y=price,x=waterfront))+geom_boxplot()+facet_grid(.~waterfront)
```

### ![box_facet-R Interview Questons-Edureka](img/4110baec79b6ef1e5370b583394c2142.png)

### **25。给定一个向量值，你如何将它转换成一个时间序列对象？**

假设这是我们的向量——>

```
a<-c(1,2,3,4,5,6,7,8,9)
```

将此转换成时间序列对象->-

```
as.ts(a)->a
```

### **![time-R Interview Questions-Edureka](img/c6260dbb88aec9a3d690ca2b7dac0109.png)**

我们来画一下这个:

```
ts.plot(a)
```

### **![time_series-R Interview Questions-Edureka](img/a3030109eada5f35c8aeae4333c2df8c.png)**

### **26。什么是白噪声模型，如何用 R 来模拟它？**

白噪声(WN)模型是一种基本的时间序列模型。这是平稳过程的最简单的例子。

白噪声模型具有:

*   一个固定的常数平均值
*   一个固定不变的方差
*   不随时间相关

模拟 R 中的白噪声模型:

```
arima.sim(model=list(order=c(0,0,0)),n=50)->wn
```

![white_noise-R Interview Questions-Edureka](img/4aed9a4e361cce3afe21b4250fc3231b.png)

```
ts.plot(wn)
```

### ![white_noise-R Interview Questions-Edureka](img/362b661e93c1252541096ef076f9595c.png)

### **27。什么是随机漫步模型，你如何用 R 来模拟它？**

随机行走是非平稳过程的一个简单例子。

随机漫步有:

*   没有指定的平均值或方差
*   对时间的强烈依赖性
*   它的变化或增量是白噪声

模拟 R 中的随机游走:

```
arima.sim(model=list(order=c(0,1,0)),n=50)->rw `ts.plot(rw)`
```

![Random_Walk-R Interview Questions-Edureka](img/15f40d8e0400f1ffbbe42d0718f178af.png)

### **28。什么是主成分分析，如何在 R 中创建 PCA 模型？**

主成分分析是一种降维方法。很多时候，一个观察值与多个维度(特征)相关，这会给数据带来很多混乱，这就是为什么减少维度的数量很重要。

主成分分析的概念是这样:

*   数据被转换到一个新的空间，具有相等或更少的维数。这些维度(特征)被称为主成分。
*   第一主成分从原始数据的特征中获取最大的变化量。
*   第二个主成分与第一个主成分正交，并捕获了剩余的最大可变性。
*   对于每个主成分来说也是如此，它们都是不相关的，并且每一个都不如前一个重要。

我们可以借助“prcomp()”函数在 R 中做 PCA。

```
`prcomp(iris[-5])->pca`
```

### **![pca-R Interview Questons-Edureka](img/04690c16e1cd5e793e593b7c1a0493c2.png)**

让我们看看不同主成分的可变性是如何降低的

```
screeplot(pca)
```

### **![pca-R Interview Questions-Edureka](img/42161b0212519d7f1441105cfc5b900c.png)**

### **29。你如何找出一列相对于另一列的意义？**

让我们对虹膜数据集进行操作:

![iris2-R Interview Questions-Edureka](img/78890ad99fff6d8ccf3951039f3830c9.png)

我们将使用马赛克包中的 mean()函数

```
`mean(iris$Sepal.Length~iris$Species)`
```

该命令给出了不同品种鸢尾花的萼片长度的平均值。

### **![mean-R Interview Questions-Edureka](img/ed5a5ad9e914e09dbbe718af16098ff1.png)**

我们观察到“virginica”的萼片长度最长，而“setosa”的萼片长度最短。

### **30。关于 R 中“initialize()”函数的解释？**

initialize()函数用于在声明对象时初始化私有数据成员。

### **![initialize-R Interview Questions-Edureka](img/4efd37f4d8428f96b189cab7288a554b.png)**

通过上面的代码，我们在 申报的时候初始化了“名称”和“成本”的值

### **![initialize-R Interview Questions-Edureka](img/c6cac959faa745edc34b767fe4033814.png)**

我们已经将“500”的值初始化为成本，将“披萨”的值初始化为名称

### **31。你如何在散点图上拟合一个线性模型？**

我们可以使用“ggplot2”包来实现。

我们将首先在 geom_point()函数的帮助下制作一个散点图，然后我们将通过在其上添加 geom_smooth()层来制作线性模型。

```
`ggplot(data = house,aes(y=price,x=living_area))+geom_point()`
```

![scatter-R Interview Questions-Edureka](img/f14f475570da09d967c43a2bfcef76a5.png)

我们将在此基础上添加 geom_smooth()层，以适应线性模型。

```
`ggplot(data = house,aes(y=price,x=living_area))+geom_point()+geom_smooth(method = "lm")`
```

![Rplot02-R Interview Questions](img/b18783979d927f129f0e29e62c52695c.png)

### **32。关于“统计建模”包** 中的 evaluate_model()函数，你知道些什么

这是“predict()”函数的替代方法。即它被用来预测所建立的模型的值。

这与预测函数的区别在于，它会自动选择比预测函数更合理的值。

### **![house-R Interview Questions-Edureka](img/1e073674af30cec9df9468e18d3bf49e.png)**

让我们在此基础上构建一个线性回归模型，然后使用 evaluate_model() 预测这些值

```
lm(price~.,data = house)->mod1
```

```
evaluate_model(mod1)->result
```

它给出了一个 数据集，该数据集还包括一个用于模型输出 的新列

### **![output-R Interview Questions-Edureka](img/020c87d67cf7861507f62c895f2967ac.png)**

### **33。你如何使用 plotly 建立一个散点图？**

在“plotly”的帮助下，我们可以创建令人惊叹的可视化效果。

这是在“plotly”包的帮助下创建一个令人惊叹的散点图的命令。

```
`plot_ly(house,y=~price,x=~living_area,color=~rooms)`
```

### **![Rplot-R Interview Questions-Edureka](img/ddbc381326b1714391eefc4862806169.png)**

### **34。条形图和直方图之间有什么区别？你在哪里使用条形图，在哪里使用柱状图？**

人们通常会弄不清在哪里使用直方图，在哪里使用条形图。需要记住的一个简单要点是，直方图用于绘制连续变量的分布，条形图用于绘制分类变量的分布。

![iris1-R Interview Questions-Edureka](img/aaedc7e28a9951c645da506705958e9f.png)

让我们在 ggplot2 软件包的帮助下绘制虹膜数据集的直方图:

```
`ggplot(data = iris,aes(x=Sepal.Length))+geom_histogram(fill="palegreen4",col="green")` 
```

我们绘制了“萼片。长度”-一个连续变量，在 x 轴上。

![Rplot-R Interview Questions-Edureka](img/b1e36ec5e172b03eca7861ff65cd147f.png)

现在，让我们制作一个条形图:

```
`ggplot(data = iris,aes(x=Species))+geom_bar(fill="palegreen4")` 
```

我们将在 x 轴上绘制“物种”——一个分类变量。

![Rplot01-R Interview Questions-Edureka](img/ed327f23c6deacf96c0b4f94b1a35c25.png)

### **35。你如何使用“plotly”创建一个方框图？**

这是在 R: 中创建方框图的命令

```
`plot_ly(house,y=~price,x=~rooms,color=~rooms,type="box")`
```

### **![boxplot-R Interview Quesitons-Edureka](img/bbfb7edd7d02dacac00d2d945a1ad31b.png)**

### **36。你如何在 R 中进行左右连接？**

我们将使用“dplyr”包的帮助来进行左连接和右连接。

我们有两个数据集- >雇员工资和雇员名称:

员工 _ 职务- >

![emp_desig-R Interview Questions-Edureka](img/6737f372679272427e53a908ce22e86d.png)

员工 _ 工资- >

### **![emp_sal-R-Interview-Questions-Edureka](img/4b0e295f71961a9d3fc9efbcc346c363.png)**

让我们使用 dplyr 包中的“left_join()”函数对这两个数据集进行左连接:

```
left_join(employee_designation,employee_salary,by="name")
```

结果- > ![left_join-R Interview Questions-Edureka](img/3b2ee3b93317da4141aea05a9498c832.png)

现在，让我们在这两个数据集之间执行右连接:

```
`right_join(employee_designation,employee_salary,by="name")` 
```

结果- > ![right_join-R Interview Questions-Edureka](img/ace093cb9230c4ea37ea138e8dd84384.png)

### **37。什么是因子？你如何在 R 中创造一个因子？**

从概念上讲，因子是 R 中的变量，它取有限数量的不同值；这种变量通常被称为分类变量。因子最重要的用途之一是在统计建模中；由于分类变量进入统计模型的方式不同于连续变量，因此将数据存储为因子可确保建模函数正确处理此类数据。

最初，我们有一个水果名称的特征向量，让我们把它转换成一个因子:

### **![fruit3-R Interview Questions-Edureka](img/995f2091b0c3659985ff01bda5e948ce.png)**

使用 as.factor()函数可以将字符向量转换成因子:

```
as.character(fruit)->fruit
```

### **![factor-R Interview Questions-Edureka](img/4fad8d8feec969bd7f2f9df15cc33c40.png)**

我们现在来看看向量的类别:

### **![factor1-R Interview Questions-Edureka](img/6b5c1d2f21bd2078cc4d5041715559a8.png)**

### **38。给定一个数字向量，你如何将数值转换成科学符号？**

我们有下面的向量:

```
`a<-c(0.1324,0.0001234,234.21341324,09.324324)`
```

我们可以使用“formatC()”函数将它转换成科学记数法:

```
formatC(a,format="e")
```

这是结果:

![scientific-R Inerview Questions-Edureka](img/0ec1a5c7d2c1a40694420e097e01d807.png)

**39。如何将多个字符串连接在一起？**

在 R 中连接字符串是一件非常简单的事情。我们可以借助“stringR”包中的“paste()”函数或“string_c()”函数来完成。

我们用一个例子来理解这个:

我们有一个由水果名称组成的“水果”向量，我们想在水果名称前添加字符串“水果”。让我们继续做那件事。

首先，让我们看一下“水果”这个向量。

```
print(fruit)
```

![fruit-R Interview Quesrtions-Edureka](img/27a6ff018127db1fe25506cfc30bfb0d.png)

现在，让我们使用粘贴功能:

```
paste("fruit",fruit)
```

### **![fruit-R Interview Questions-Edureka](img/3b6a4511c21a236ac1ca67636d6d1238.png)**

现在，让我们使用“stringR”包中的“str_c()”函数执行相同的任务。

```
`str_c("fruit",fruit,sep="-")`
```

![fruit-R Interview Questions-Edureka](img/5e1df0e1cd6e09f95981de76f7c44404.png)

**40。编写一个自定义函数，用平均值替换向量中所有缺失的值。**

让我们取这个向量:

```
a<-c(1,2,3,NA,4,5,NA,NA)
```

现在，让我们编写估算这些值的函数:

```
`mean_impute<-function(x){
ifelse(is.na(x),mean(x,na.rm = T),x)
}`
```

这是结果:

![impute-R Interview Questions-Edureka](img/f8ece230bb7a3f9cb335795145868962.png)

### **41。R 中有哪些不同的导入函数？**

可以将不同来源和不同格式的数据导入到 R 中。让我们来看看 R 中提供的不同导入功能:

*   read.csv()- >进行阅读。csv 文件
*   read_sas()- >用于读取. sas7bdat 文件
*   XL 工作表的 read _ excel()->
*   【spss 数据的 read _ sav()->

### **42。说出一些在 R 中可以用来调试的函数？**

这是 R: 中可以用来调试的一些函数

*   traceback()
*   debug()
*   浏览器()
*   trace()
*   恢复()

### **43。如何检查 R 中分类变量的分布？**

我们经常想知道一个分类变量的值是如何分布的。

我们可以用 table()函数来求分类值的分布。

```
table(iris$Species)
```

### **![table-R Interview Questions-Edureka](img/72216aa329eddd33adf804c33d3584a5.png)**

现在，让我们找出这些值的百分比分布。

```
`table(iris$Species)/nrow(iris)`
```

![percentage-R Interview Questions-Edureka](img/52a491360993e06c8277ca54081e2f9d.png)

### **44。如何重命名数据帧的列？**

大多数情况下，列名并不能传达关于列中值的正确信息，因此我们需要对它们进行重命名。

让我们举一个例子来说明如何重命名列。

这是水果数据集，由两列组成:

### **![fruits_dataset-R Interview Questions-Edureka](img/1f69eb62f14d234c11d79fce101b4c04.png)**

我们看到列名没有给出关于其中数据的任何信息，所以让我们继续重命名这些列。

" colnames()"函数用于重命名列。

```
colnames(fruits)<-c("name","cost")
```

现在，我们来看看结果: ![fruits_dataset-R Interview Questions-Edureka](img/4416a580ebb68e87a2a3a64086ffecf9.png)

### **45。如何找出数据集中缺失值的数量并将其全部移除？**

缺失值会给数据带来很多混乱。因此，在我们构建任何模型之前，处理缺失值总是很重要的。

我们来举个例子:

这是一个包含缺失值的员工数据集，让我们继续删除它们。

![employee_dataset-R Interview Questions-Edureka](img/e373d37cf7804a091c2865c54d93fad1.png)

此代码给出了缺失值的数量->-

```
sum(is.na(employee))
```

现在，让我们删除缺失的值:

```
na.omit(employee)
```

这是删除缺失值后的结果:

![employee_dataset-R Interview Questions-Edureka](img/bc7565ffa077437193e2fee281475088.png)

### **46。什么是相关性？你如何测量 R 中的相关性？**

相关性是一种衡量两个变量之间关联强度的方法。

我们可以用 R 中的 cor()函数来求相关系数。

我们将使用虹膜数据集:

![iris-R Interview Questions-Edureka](img/2cf12f285f47785b826a5e606d73b1f9.png)

让我们使用 cor()函数找出这些变量之间的相关程度

```
cor(iris[-5])
```

我们来看看结果:

![iris_correlation-R Interview Questions-Edureka](img/da4c81c303095dd96ce46fcce7051f7b.png)

如果相关系数更接近+1，那么变量之间存在很强的正相关关系。类似地，如果相关系数接近-1，那么这两个变量之间会有很强的负相关。

如果我们把“萼片。长度”和“花瓣。长度”，相关系数为 0.8717538，这意味着这两个变量之间有很强的正相关关系。

### **47。你如何从字符串中提取一个特定的单词？**

“stringR”包中的 string_extract_all()函数可用于从字符串中提取特定的模式。

```
`sparta<-"This is Sparta! This is Sparta! This is Sparta! This is Sparta! This is Sparta!"`
```

我们来提取模式“斯巴达！”从中。

![sparta-R Interview Questions-Edureka](img/9bf85136355d74bb3f346b1c0c174745.png)

### **48。从下面的数据集中，只提取那些年龄> 60 和性别=“F”的值。**

![AARP-R Interview Questions-Edureka](img/d116624c65501e4572eb59763ffd49ca.png)

我们可以使用“dplyr”软件包来完成。“dplyr”是一个提供了许多数据操作函数的包，其中一个函数就是 filter()。

让我们继续，使用 filter()函数执行所需的任务

```
AARP %>% filter(Age>60 & Sex=="F")
```

使用上面的命令，我们过滤掉那些年龄大于 60 且“性别”为女性的值。

![filter-R Interview Questions-Edureka](img/408db6b0baa0429992a922e012af1545.png)

### **49。您有一个雇员数据集，它由两列组成- >“姓名”和“职务”，添加第三列将显示当前日期和时间。**

这是员工数据集:

![employee-R Interview Questions-Edureka](img/27c0bd8a25c1ee4745390d9b9fa967ff.png)

我们可以使用 cbind()函数 添加日期

```
cbind(employee,date())
```

`![date-R Interview Questions-Edureka](img/aedafa194d19d0e558ab048efcb05283.png)`

### **50。你如何在 R 中做两个表的叉积？**

*【merge()*函数可以用来执行 R: 中的叉积

我们有两个表- >“员工 _ 职务”和“员工 _ 薪金”

员工 _ 职务表:由“姓名”和“职务” 组成

![employee_designation-R Interview Questions-Edureka](img/0c02f8ce9430a287adfcb63078120901.png)

员工 _ 薪资表:由“姓名”和“薪资”组成

![employee_salary-R Interview Questions-Edureka](img/4cc94f58aaa66ba351e316a614b9bf82.png)

通过执行下面的命令，我们将得到一个叉积:

```
merge(employee_designation,employee_salary,by=NULL)
```

![merge-R Interview Questions-Edureka](img/067083a2c31d3dbf2f17a3fed7edf9d5.png)

祝你面试顺利！

*查看 Edureka 提供的* **[*R 认证培训*](https://www.edureka.co/r-for-analytics/)** *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的数据分析与 R 培训将帮助您获得 R 编程、数据操作、探索性数据分析、数据可视化、数据挖掘、回归、情感分析方面的专业知识，并使用 RStudio 进行零售、社交媒体方面的真实案例研究。*