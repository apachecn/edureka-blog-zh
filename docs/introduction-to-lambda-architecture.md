# Lambda 架构简介

> 原文：<https://www.edureka.co/blog/introduction-to-lambda-architecture/>

[//www.youtube.com/embed/wLUYv_oLpH0](//www.youtube.com/embed/wLUYv_oLpH0)

## **什么是 Lambda 架构？**

Lambda 架构容纳了速度层和批处理层，数据冗余地进入这两层进行处理。两者的结合称为 Lambda 架构。

首先，数据到达数据中心，然后到达两个层。当工作流进入批处理层时，数据可以保存到 HDFS 中，然后工作流会定期运行。

在速度层，数据通过不同的功能实时传递。然后，在 batch 或 speed layer 计算机视图中执行查询。值得注意的是，服务层是数据以某种形式存储在 NoSQL 或 HDFS 的地方。

一旦数据在 Hadoop 平台上得到处理，我们就可以将数据保存在 HDFS 或 NoSQL。

查询可以使用 NoSQL 图层或使用 HIVE 对数据集运行查询。因此，服务层服务于查询。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[阿帕奇风暴到底是怎么回事？](https://www.edureka.co/blog/videos/aboutapachestorm/)