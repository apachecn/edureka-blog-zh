# Mahout 中的集群介绍

> 原文：<https://www.edureka.co/blog/introduction-to-clustering-in-mahout/>

Mahout 主要支持三种用例，推荐、集群和分类，这里我们讨论的是集群。群集指的是一小组对象。Mahout 中的集群意味着将任何形式的数据分组到特征相似的数据集组中。换句话说，聚类是将数据点分成同类或同类，使得同一组中的点尽可能相似，而不同组中的点尽可能不相似。当给定一组对象时，它们根据相似性被分组。

[//www.youtube.com/embed/r99_cmBa-zw](//www.youtube.com/embed/r99_cmBa-zw)

## Mahout 中的聚类类型

*   [K-均值聚类](https://www.edureka.co/blog/k-means-clustering/ "K-Means Clustering")
*   [模糊 K 均值聚类](https://www.edureka.co/blog/fuzzy_k-means/ "Fuzzy K-Means Clustering")
*   分层聚类
*   树冠集群

继续这篇关于 Mahout 中的集群的文章，让我们看看 K-Means 集群

## **K-均值聚类**

K-means 聚类是由 Macqueen 在 1967 年发现的，是解决众所周知的聚类问题的最简单的无监督学习算法之一。

K-Means 聚类是一种矢量量化方法，它最初来自信号处理，是数据挖掘中一种流行的聚类分析技术。

如果定义了 k，则执行 k-means 算法的步骤如下:

*   将对象划分成 k 个非空子集。
*   识别当前分区的聚类质心(平均点)。
*   将每个点分配给特定的簇。
*   找出每个点到质心的距离，并将点到质心的距离最小的点分配到聚类中。
*   在重新分配点之后，识别新形成的聚类的质心。

继续这篇关于 Mahout 中的聚类的文章，让我们看一个 K-Means 聚类的例子。

## **K-Means:必胜客聚类示例:**

让我们考虑一个考虑到必胜客配送点的例子。我们可以使用 K-Means 聚类来解决这个问题，K-Means 聚类是聚类算法的一部分。

该算法产生一个质心，并从那里计算质心和点之间的距离。然后，它会找出最小距离，并尝试将所有这些点组合在一起。当我们有了比萨饼的送货地点时，首先，我们需要对送货地点进行分组。如果我们需要三个交付位置，或三个集群，或我们获得的数据记录组，然后，我们找出质心和交付点之间的距离。

如果分组不充分或者没有给出最接近的结果，我们重新定位最接近这些点的质心，并且尝试将它们分组在一起，以便优化聚类质心点和数据点之间的距离。话说回来，我们需要找到距离。这不需要手动完成，因为一切都是由算法完成的。一个人唯一要做的事情就是研究推断统计学。这个 Mahout 算法的结果，你可以从中推断出我们得到的是对还是错。

一旦我们发现了这一点，我们必须将相似的数据集分组，这些数据集具有非常小的距离，并且共享数据集的相似特征，然后，我们继续将它们分组在一起。通过这种方式，聚类将相似类型的数据或公共信息集合在一起。

这里要确定的一件事是，不要有过去的历史记录集，它既有输入也有输出。只有在这种情况下，才需要进行聚类。

看看这个由 Edureka 设计的 [NLP 课程](https://www.edureka.co/python-natural-language-processing-course)，将你的人工智能技能提升到下一个水平

***注:如果万一有过去历史记录集的数据，既有输入又有输出，可以直接进入分类模式。***

这就把我们带到了“Mahout 中的集群”这篇文章的结尾。您还可以查看以下相关帖子:

**相关帖子**

中的模糊 K 均值聚类

[跟看象人](https://www.edureka.co/mahout-self-paced)开始机器学习

*![mahout](img/79f983367b11a169caab02bf47305a0b.png)有问题吗？在评论区提到它们，我们会给你回复。*