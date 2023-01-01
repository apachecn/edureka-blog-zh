# Mahout 中的模糊 K-均值聚类

> 原文：<https://www.edureka.co/blog/fuzzy_k-means/>

[//www.youtube.com/embed/ENvawqb3vT0](//www.youtube.com/embed/ENvawqb3vT0)

模糊 K-means 是与 K-Means 完全相同的算法，K-Means 是一种流行的简单聚类技术。唯一的区别是，它不是将一个点专门分配给一个聚类，而是可以在两个或多个聚类之间具有某种模糊性或重叠。以下是描述模糊 K 均值的关键点:

*   不像 K-Means 寻找硬聚类，其中每个点属于一个聚类，模糊 K-Means 寻找重叠的软聚类。
*   软聚类中的单个点可以属于一个以上的聚类，对于每个点具有特定的亲和力值。
*   亲和度与该点到聚类质心的距离成比例。
*   类似于 K-Means，模糊 K-Means 作用于定义了距离度量的对象，并且可以在 *n-* 维向量空间中表示。

## 模糊 K-Means MapReduce 流量

K-均值和模糊 K-均值的 MapReduce 流程没有太大的区别。两者在 Mahout 中的实现是相似的。

以下是实现模糊 K 均值的**个基本参数**:

*   你需要一个向量数据集作为输入。
*   必须有 RandomSeedGenerator 来播种初始的 k 个簇。
*   对于距离度量，SquaredEuclideanDistanceMeasure 是必需的。
*   如果使用了距离度量的平方值，则收敛阈值的值较大，例如–CD 1.0
*   最大值；默认值是-x 10。
*   归一化系数或模糊因子，其值大于-m 1.0

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子**

[结合实例理解 K-Means 聚类](https://www.edureka.co/blog/k-means-clustering/ "K-Means Clustering")

[监督学习中的阿帕奇](https://www.edureka.co/blog/supervised-learning-technique-in-mahout/ "Supervised Learning in Apache Mahout")

[机器学习跟看象人](https://www.edureka.co/mahout-self-paced "Machine Learning with Mahout")