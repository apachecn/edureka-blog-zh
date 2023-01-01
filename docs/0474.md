# PySpark 编程–将速度与简单性相结合

> 原文：<https://www.edureka.co/blog/pyspark-programming/>

Python 和 Apache Spark 是分析行业最热门的词汇。Apache Spark 是一个流行的开源框架，它确保以闪电般的速度处理数据，并支持各种语言，如 Scala、Python、Java 和 r。然后，它归结为您的语言偏好和工作范围。通过这篇 PySpark 编程文章，我将讨论 Spark 和 Python，以展示 Python 如何利用 Apache Spark 的功能。

在我们开始 PySpark 编程之旅之前，让我列出我将在本文中涉及的主题:

*   [什么是 PySpark](#Learnpysparkprogramming) ![PySpark logo - PySpark Programming - Edureka](img/1bbc61d7ff2e1742091f15a54d10c65e.png)

*   [数据帧](#dataframe)
*   [PySpark SQL](#pysparksql)
*   [PySpark 流](#pysparkstreaming)
*   机器学习(ml lib)

那么，让我们从列表上的第一个话题开始，也就是 PySpark 编程。

## **PySpark 编程**

PySpark 是 Apache Spark 和 Python 的协作。

**Apache Spark** 是一个开源的集群计算框架，围绕速度、易用性和流分析而构建，而 **Python** 是一种通用的高级编程语言。它提供了广泛的库，主要用于机器学习和实时流分析。

换句话说，它是一个用于 Spark 的 Python API，让您可以利用 Python 的简单性和 Apache Spark 的强大功能来驯服大数据。向 [蔚蓝数据工程师助理](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 了解更多大数据及其应用。

![PySpark - PySpark Programming - Edureka](img/23dd454a3bec249de9f6861fdff58bdd.png)

你可能想知道，既然有其他语言可用，为什么我选择 Python 来使用 Spark。为了回答这个问题，我列出了 Python 的一些优势:

*   Python 非常容易学习和实现。
*   它提供了简单而全面的 API。
*   使用 Python，代码的可读性、维护性和熟悉度都要好得多。
*   它为数据可视化提供了各种选项，使用 Scala 或 Java 很难做到这一点。
*   Python 附带了大量的库，如 numpy、pandas、scikit-learn、seaborn、matplotlib 等。
*   它得到了一个庞大而活跃的社区的支持。

既然你已经知道了 PySpark 编程的优点，那我们就简单的深入一下 PySpark 的基础知识吧。

## **PySpark 编程| PySpark 培训| edu reka**



[//www.youtube.com/embed/nw68ok9HCR4?rel=0&showinfo=0](//www.youtube.com/embed/nw68ok9HCR4?rel=0&showinfo=0)

*这段视频将让你深入了解 PySpark* 的基本概念

[rdd](https://www.edureka.co/blog/pyspark-rdd/)是任何 Spark 应用程序的构建模块。RDDs 代表:

*   ***弹性:*** 它具有容错能力，能够在出现故障时重建数据。
*   ***分布式:*** 数据分布在集群中的多个节点上。
*   ***数据集:*** 带有值的分区数据的集合。

是分布集合之上的一层抽象数据。它本质上是不可改变的，遵循的惰性转化。

使用 RDDs，您可以执行两种类型的操作:

1.  **转换:**这些操作用于创建一个新的 RDD。
2.  **动作:**这些 操作被应用到 RDD 上，以指示 Apache Spark 应用计算并将结果传递回驱动程序。

## **数据帧**

PySpark 中的[*data frame*](https://www.edureka.co/blog/pyspark-dataframe-tutorial/)是结构化或半结构化数据的分布式集合。Dataframe 中的这个 数据存储在命名列下的行中，这类似于关系数据库表或 excel 表。

它还与 RDD 有一些共同的属性，如本质上不可变，遵循惰性评估，以及本质上是分布式的。它支持 JSON、CSV、TXT 等多种格式。此外，您可以从现有的 rdd 或通过编程指定模式来加载它。

## **PySpark SQL**

PySpark SQL 是 PySpark 核心之上的高级抽象模块。它主要用于处理结构化和半结构化数据集。它还提供了一个优化的 API，可以从包含不同文件格式的各种数据源中读取数据。因此，使用 PySpark，您可以利用 SQL 和 HiveQL 来处理数据。因为这个特性，PySparkSQL 慢慢地在数据库程序员和 Apache Hive 用户中流行起来。

#### 订阅我们的 YouTube 频道获取新的更新...