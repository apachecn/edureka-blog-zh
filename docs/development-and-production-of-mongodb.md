# MongoDB 的开发和生产

> 原文：<https://www.edureka.co/blog/development-and-production-of-mongodb/>

[//www.youtube.com/embed/x5UZolhOkP0](//www.youtube.com/embed/x5UZolhOkP0)

## **MongoDB 开发环境**

可以使用应用程序驱动程序或 Mongo 客户端直接连接到 Mongod。另一个选项是必须构建的群集。Mongod 可以作为集群的单个节点工作。在这种情况下，人们可以从你的 Mongos 连接 Mongod，它将在应用程序驱动程序或 Mongod 客户端或 Mongod 之间运行。

从应用程序驱动程序或 Mongo 客户端，可以连接到 Mongos，Mongos 将在内部连接到 Mongod。在开发环境中，只有一个节点。如果应用程序驱动程序中有多个节点，则不需要连接到多个节点。你只需要连接到 Mongos，它们就会连接到多个节点并收集数据。为此，Mongos 借助了一个名为 Configdb 的配置数据库。Mongos 是一个查询路由器，在 Mongo 和 Mongod 集群之间运行。配置数据库实际上包含保存在集群或节点中的元数据。

## **MongoDB 制作概述**

在上图中，一个节点是一个分片集群。有多个集群，其中 Mongos 是接口之一，它充当查询路由器。从应用程序驱动程序或 Mongo 客户端，而不是连接到多个节点，连接到 Mongo，它们将执行查询分发。Mongos 得到了配置数据库的帮助，并包含了这个集群的元数据。

在生产场景中，有多个 mongo，在 mongo 之上通常有一个负载平衡器。它要么是一个 HTDP 负载平衡器，要么是一个硬件负载平衡器，因此它有一个连接所有 Mongos 的客户端亲缘关系。从您的应用程序驱动程序中，您可以使用负载平衡器连接到多个 Mongos。所有不同的蒙哥工作方式相似。

复制在图像中的框内工作。例如，在 shard 1 列中，有一个配置好的复制机制，这个盒子包含 256 GB 的数据。它被称为这个碎片的主要成员。其他两个成员被称为次要成员。一个碎片不是一个 Mongod 进程，但它应该是一个副本集 Mongod 进程的组合。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[MongoDB Vs 卡珊德拉](https://www.edureka.co/blog/mongodb-vs-cassandra/)

[入门 MongoDB](https://www.edureka.co/mongodb)