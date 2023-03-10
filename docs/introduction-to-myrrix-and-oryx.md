# Myrrix 和 Oryx 简介

> 原文：<https://www.edureka.co/blog/introduction-to-myrrix-and-oryx/>

[//www.youtube.com/embed/kwDnWOd2jBk](//www.youtube.com/embed/kwDnWOd2jBk)

## **什么是 Myrrix？**

在 2005 年，有一个开源项目叫做 Taste，它只是为了推荐而存在。当 Mahout 在 2008 年出现时，它取代了 Taste。2011 年，Myrrix 作为一个独立的项目开始，成为一个独立的 Apache 项目，也是出于推荐的目的，只考虑推荐系统。

*   Myrrix 是一个完整的、实时的、可扩展的推荐系统，由 Apache Mahout 发展而来。
*   正如我们想当然地认为轻松访问强大、经济的存储和计算一样，Myrrix 将让您想当然地认为轻松访问大规模数据学习。
*   它能吸收新信息。
*   它可以计算推荐。
*   它使用 REST APIs 实时工作。
*   它还可以利用 Hadoop 的可扩展性，在后台高效地优化推荐模型。
*   Myrrix 可以在任何平台上运行，并且可以使用大多数 Hadoop 发行版中的集群。
*   如果需要，它是专门设计来使用 Amazon EC2 和 EMR 进行即时部署的。

2013 年 12 月，Myrrix 被 Cloudera 收购，并被转移到名为 Oryx 的新项目中。

## **大羚羊是什么？**

Oryx 是一个开源项目，它还提供实时大规模机器学习和预测分析基础设施。但问题是，当 Oryx 来自 Mahout 时，一般的印象会是:它只负责推荐系统。但 Cloudera 也在研究机器学习算法。他们将其他聚类分类算法编码到这个项目中。现在，它不仅有推荐系统，还有分类和聚类算法。截至目前，这个项目相当于 Mahout。

*   它实现了业务应用程序中常用的几类算法，比如协同过滤/推荐、分类/回归和聚类。
*   它可以使用 Apache Hadoop 从大规模数据流中持续构建模型。
*   它还通过 HTTP REST API 实时提供这些模型的查询，还可以更新模型以响应新的数据流。
*   其两层设计包括计算层和服务层。
*   它实现了 Lambda 架构。
*   在 Oryx 中，模型以 PMML 格式交换。

假设您正在创建一个推荐系统，您可以用 REST API 调用这个推荐系统。因此，您可以将单独开发特定推荐系统与其他应用程序集成在一起。该应用不必是 Java。它可能是在。net 或任何其他。

这里需要注意的一点是，它不是一个库、可视化工具、探索性分析工具或环境。Oryx 只是代表了 Myrrix 和 Cloudera/ml 项目的统一延续。这个项目还处于初级阶段，可能会有一些错误。由于他们正在努力，预计到今年年底，他们可能会推出测试版，这意味着当你安装 Cloudera 发行版时，Oryx 也会默认安装。

## **羚羊建筑**

Oryx 架构有服务层客户端。可以有许多服务层。为了可扩展性，它还使用了 Hadoop 和 HDFS。输入文件将在 HDFS，计算层将从 HDFS 获取这些文件。它还可以运行 MapReduce 的东西。这个计算层和两个服务层将被一个配置文件绑定。所以一旦你安装了 Oryx，如果你想试用的话，会有一个 oryx.config 文件，你要对输入文件位置，输出文件位置，模型位置进行配置。一旦设置完成，那么只有您可以运行这个计算层和服务层。

看看这个由 Edureka 提供的 [NLP 课程](https://www.edureka.co/python-natural-language-processing-course)，将你的人工智能技能提升到一个新的水平。

***![hadoop-logo-3](img/7505121b16d1c0be62f8f3998db6b200.png)有问题吗？在评论区提到它们，我们会给你回复。***

**相关帖子**

[驯象人简介](https://www.edureka.co/blog/videos/introduction-to-mahout/ "Introduction to Mahout")

[跟看象人一起踏入机器学习](https://www.edureka.co/mahout-self-paced "Step into Machine Learning with Mahout")