# 利用 R 实现 K-均值聚类对银行客户进行分类

> 原文：<https://www.edureka.co/blog/clustering-on-bank-data-using-r/>

在我们继续使用 R 分析银行数据之前，让我简单介绍一下 R。R 是一个定义明确的集成软件套件，用于数据操作、计算和图形显示。

## R 的核心特性包括:

*   高效快速的数据处理和存储设备。
*   一组用于计算数组、列表、向量等的运算符。
*   用于数据分析和可视化的大型集成工具集。
*   使用图形和直接在计算机或纸上显示的数据分析工具。
*   一种实现良好且有效的编程语言，称为“S ”, R 就是在它的基础上构建的。
*   一个完整的软件包来扩展和丰富 r。

我们称 R 为一个集成了许多经典和现代统计技术的环境。R 提供了大约 25 个软件包，通过综合 R 档案网络(CRAN)家族的互联网站点(通过 http://CRAN.R-project.org)和其他地方可以获得大约 3000 多个软件包。

**Note: Going ahead when I use the word ‘R’ it would be for complete R environment.**

## 什么时候应该使用 R？

虽然 R 是一个伟大的软件，但它并不是解决所有问题的合适工具。在使用 R 之前，您应该很好地了解它问题和局限性。r 非常擅长绘制图形、分析数据，以及使用适合计算机内存的数据来拟合统计模型。它不擅长在复杂的结构中存储数据，有效地查询数据，或者处理不适合计算机内存的数据。

这就是我在将大文件转移到 R 中之前使用 Hadoop 预处理大文件的原因。虽然您也可以在 R 中使用 R 正则表达式和绑定操作来完成相同的任务，但对于初学者来说，这是相当新且复杂的。另外，R 使用 RAM 来保存数据集。因此，如果你没有大的内存，你就不能在 R 中保存大的值。为了保存大型数据文件，我通常使用 MySQL 之类的数据库，或者 Hadoop 之类的框架。

## R 比它的商业同行好在哪里？

**能力**

r 中有数以千计的统计和数据分析算法，没有一个同类产品能提供 CRAN 所能提供的如此多样的功能。

**社区**

全世界有数百万的 R 用户，而且由于它的强大功能，他们还在呈指数级增长。您可以随时通过各种论坛与他们分享您的知识、疑问或建议。

**性能**

与其他商业分析包相比，r 的性能非常出色。r 在处理之前将数据集加载到内存中。您唯一应该拥有的是一台好的配置机器，以便最大限度地使用它的功能。我认为现在每个人都可以选择更高内存的机器，因为现在的内存比 R 开发出来的时候要便宜得多。这可能是 R 用户以这种速度增长的最大原因之一。

## 数据挖掘步骤:

从数据中寻找和解释模式的整个过程包括重复应用以下步骤:

1.  加载并培养对以下内容的理解:
    *   应用程序域
    *   相关的先验知识
    *   最终用户的目标
2.  创建一个目标数据集:选择一个数据集，或者关注一个变量子集，或者数据样本，在其上执行发现。
3.  数据清洗和预处理。
    *   去除噪声或异常值。
    *   收集必要的信息来模拟或解释噪声。
    *   处理缺失数据字段的策略。
    *   说明时序信息和已知的变化。
4.  数据简化和投影。
    *   根据任务的目标寻找有用的特征来表示数据。
    *   使用降维或变换方法来减少所考虑的变量的有效数量，或找到数据的不变表示。
5.  选择数据挖掘任务。
    *   决定 KDD 过程的目标是否是分类、回归、聚类等。
6.  选择数据挖掘算法。
    *   选择用于在数据中搜索模式的方法。
    *   决定哪些模型和参数可能是合适的。
    *   将特定的数据挖掘方法与 KDD 进程的总体标准相匹配。
7.  数据挖掘。
    *   以特定的表示形式或一组表示(如分类规则或树、回归、聚类等)搜索感兴趣的模式。
8.  解释挖掘出的模式。
9.  巩固发现的知识。

**第一步:加载并理解数据**

我们将保存在 HDFS 的文件从名为“combined_out”的 Pig 导入到 Hadoop 中

***##为 R 环境下的 Hadoop 设置 Hadoop 变量***

```
Sys.setenv(JAVA_HOME="/home/abhay/java")
Sys.setenv(HADOOP_HOME="/home/abhay/hadoop")
Sys.setenv(HADOOP_CMD="/home/abhay/hadoop/bin/hadoop")
Sys.setenv(HADOOP_STREAMING="/home/abhay/hadoop/share/hadoop/tools/lib/hadoop-streaming-2.2.0.jar")
```

***# #加载 RHadoop 包***

```
library(rmr2)
library(rhdfs)
hdfs.init()
```

***# #设置 Hadoop 根路径并从 HDFS 读取文件***

```
hdfs.root <- '/bank_project'
hdfs.data <- file.path(hdfs.root, 'combined_out/part-r-00000')
final_bank_data <- hdfs.read.text.file(hdfs.data)
content<-hdfs.read.text.file(hdfs.data)
clickpath<-read.table(textConnection(content),sep=",")
```

**步骤 2:创建目标数据集**

***# # #命名从 HDFS** 取出的所有列*

```
colnames(clickpath) <- c("ac_id","disposal_type","age","sex","card_type","dist","avg_sal","unemp_rate","entrepreneur_no","trans_sum","loan_amount","loan_status")
```

**第三步:数据清理和预处理**

***# #检查取出数据的结构***

str(点击路径)

概要(点击路径) [![summary_2 (1) (1)](img/5c4a00e75fb71d09ec19015c10af8877.png "summary_2 (1) (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/summary_2-1-11.png)

***# #缺失值行列表***

```
clickpath[!complete.cases(clickpath),]
```

***# #缺少值的列列表***

```
clickpath[,!complete.cases(clickpath)]
```

**##如果有任何缺失值，则忽略它们**

```
clickpath <- na.omit(clickpath,na.action=TRUE)
```

**步骤 4:数据简化和投影**

***# # #仅选择数值数据并删除 ac_id 列***

```
mydata <- clickpath[,c(3,7:11)]
```

**#首先检查整套组件是否有异常值**

框打印(soap 数据)[t1](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/boxplot_whole-11.png)

**##从上面的图中我们可以看出，avg_sal、unemp_rate 和 loan amount 在数据中有一些异常值。这三个我们都单独分析一下吧。**

**# avg _ sal 中的异常值**

boxplot(mydata[，c(2)][![box_avg_sal (1)](img/4093e72a7c4354f5bd1d62ef892ac450.png "box_avg_sal (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/box_avg_sal-11.png)

因为 avg_sal 是最有用的东西之一，我们不能不经过调查就简单地忽略它。因此，我们将检查这个条目的散点图，以便更加清楚。

```
plot(mydata[,c(2)])
```

[![scater_avg_sal (1)](img/06a4ea5fd015f3a8010316511fb85e79.png "scater_avg_sal (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/scater_avg_sal-11.png)

从该图中，我们观察到有许多条目的值属于异常值类别。因此，删除这个异常值并不是一个好主意。

**# unemp _ rate 中的异常值**

boxplot(mydata[，c(3)][![box_3 (1)](img/c2a5290fe4da3d5ed70e62bb01074261.png "box_3 (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/box_3-11.png)

从这个图表中我们可以看到有一些条目是异常值。由于这个值不是必需的，因此我们可以决定减少这个条目中的异常值。可能有许多方法可以去除异常值。我选择用大约 1.5 的最大值来代替异常值。

**##定义函数替换异常值**

```
library(data.table)
 outlierReplace = function(dataframe, cols, rows, newValue = NA) {
 if (any(rows)) {
 set(dataframe, rows, cols, newValue)
 }
 }
```

**#调用条目 unemp_rate 的异常值替换函数，替换所有类别值最大的异常值。**

```
outlierReplace(clickpath, "unemp_rate", which(mydata$unemp_rate > 1.5), 1.5)
```

**##现在检查条目的五个数字摘要，以验证离群值是否已被替换。**

```
fivenum(mydata$unemp_rate)
```

**# loan _ amount 异常值**

boxplot(mydata[，c(6)][![box_loan (1)](img/df590e1e0c781fa85c8a8f74406b5afc.png)](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/box_loan-11.png)

plot((mydata[,c(6)])) [![scatter-loan (1)](img/3cfc51cfbc92d848b1f17c640a0d708a.png "scatter-loan (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/scatter-loan-12.png)

从该图中，我们观察到有许多条目的值属于异常值类别。考虑到这个条目的敏感性，删除这个异常值并不是一个好主意。

由于数据属性的种类不同，其规模也不同。为了保持统一的可伸缩性，我们对列进行了伸缩。

```
mydata <- scale(mydata[,1:7])
```

**第五步:选择数据挖掘任务**

**##计算方差并存储在 wss 中的第一个索引处**

```
wss <- (nrow(mydata)-1)*sum(apply(mydata,2,var))
```

**步骤 6:选择数据挖掘算法**

我们将使用 k-means 算法进行聚类。

聚类分析？？

聚类分析或聚类的任务是将一组对象分组，使得同一组(称为聚类)中的对象与其他组(聚类)中的对象彼此相似(在某种意义上)。它是探索性数据挖掘的主要任务，也是统计数据分析的常用技术，用于许多领域，包括机器学习、模式识别、图像分析、信息检索和生物信息学。

聚类分析本身不是一项自动任务，而是一个知识发现或交互式多目标优化的迭代过程，涉及试验和失败。

K-Means 算法属性

总有 K 个集群。

每个群中总是至少有一个项目。

这些集群是非分层的，并且它们不重叠。

一个群集的每个成员都比其他任何群集更接近它的群集，因为接近程度并不总是涉及群集的“中心”。

K 均值算法过程

*   数据集被划分成 K 个聚类，并且数据点被随机分配给聚类，导致聚类具有大致相同数量的数据点。
*   对于每个数据点:计算从数据点到每个聚类的距离。
*   如果数据点最接近它自己的聚类，就让它留在原处。如果数据点不是最接近其自己的聚类，则将其移动到最近的聚类中。
*   重复上述步骤，直到完整地遍历所有数据点，没有数据点从一个聚类移动到另一个聚类。此时，聚类是稳定的，聚类过程结束。

初始划分的选择可以极大地影响最终的聚类，这是根据聚类间和聚类内的距离和内聚性而产生的。

**##遍历 wss 数组 15 次，将每次迭代中的所有方差相加，存储在 wss 数组**

```
for(i in 2:15)wss[i]<- sum(fit=kmeans(mydata,centers=i,15)$withinss)
```

**##绘制每次迭代以显示肘图**

```
plot(1:15,wss,type="b",main="15 clusters",xlab="no. of cluster",ylab="with clsuter sum of squares")
```

[![without_outlier_kmeans_plot (1)](img/7136fac5275a290f01c0eb8b3179598c.png "without_outlier_kmeans_plot (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/without_outlier_kmeans_plot-11.png)

**步骤 7:以特定的表现形式搜索感兴趣的模式**

**# #从上面的输出中我们可以看到，图形的斜率在 3 次迭代中变化很大，因此我们认为优化的聚类数为 3，在此情况下我们可以获得最佳结果**

```
fit <- kmeans(mydata,3)
```

##让我们检查 kmeans 对象的摘要

>合体 [![fit_sam (1)](img/7d7eaa7a8efe6b37da13cb23f11358e3.png "fit_sam (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/fit_sam-11.png)

kmeans 返回一个类的对象，它有一个 print 和一个 fitted 方法。这是一个至少包含以下内容的列表:

| `cluster` | 一个整数向量(从 1:k 开始),表示每个点被分配到的簇。 |
| `centers` | 集群中心矩阵。 |
| `totss` | 平方和的总和。 |
| `withinss` | 类内平方和的向量，每个类一个分量。 |
| `tot.withinss` | 总类内平方和，即`sum(withinss)`。 |
| `betweenss` | 类间平方和，即`totss-tot.withinss`。 |
| `size` | 每个簇中的点数。 |
| `iter` | (外部)迭代的次数。 |
| `ifault` | 整数:可能的算法问题的指示器——供专家使用。 |

**##检验范围，即每个簇的簇内结合强度因子**

```
fit$withinss
```

**##检查组间距离，即组间距离**

```
fit$betweenss
```

```
fit$size
```

**步骤 8:解释挖掘模式**

```
plot(mydata,col=fit$cluster,pch=15)
 points(fit$centers,col=1:8,pch=3)
```

[![simple_kmeans_plot (1)](img/75d5a570aba8c085db48e7200e50a21e.png "simple_kmeans_plot (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/simple_kmeans_plot-11.png)

```
library(cluster)
 library(fpc)
 plotcluster(mydata,fit$cluster)
points(fit$centers,col=1:8,pch=16)
```

[![numberplot (1)](img/7c9c6531814dd276720739452b875d7f.png "numberplot (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/numberplot-11.png)

```
clusplot(mydata, fit$cluster, color=TRUE, shade=TRUE, labels=2, lines=0)
```

[![circ (1)](img/1cb1d447ef740eed9b4c5c8d377ec529.png "circ (1)")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/circ-11.png)

**##每个集群中每个对象的检查均值**

**通常，作为一个*k*-均值聚类分析的结果，我们会检查每个维度上每个聚类的均值，以评估我们的 *k* 聚类的不同程度。**

```
mydata <- clickpath[,c(3,7:12)]
 mydata <- data.frame(mydata,fit$cluster)
 cluster_mean <- aggregate(mydata[,1:8],by = list(fit$cluster),FUN = mean)
 cluster_mean
```

[![mean](img/e8a3c0dc0f489ef21253af3070fa4a9d.png "mean")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/mean.png)

K-means 聚类特别是在使用诸如 Lloyd's 算法的试探法时，即使在大型数据集上也相当容易实现和应用。它已经成功地应用于各个领域，包括市场细分、计算机视觉、地质统计学、天文学和农业。它通常被用作其他算法的预处理步骤，例如寻找一个起始配置。

在下一篇博客中，我们将学习逻辑回归和购物篮分析在银行数据中的应用。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[在银行领域实施 Hadoop 和 R 解析技巧](https://www.edureka.co/blog/implementing-hadoop-and-r-analytic-skills-in-banking-domain/)

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)

[数据科学入门](https://www.edureka.co/data-science)