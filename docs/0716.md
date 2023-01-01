# MongoDB 中的分片概念

> 原文：<https://www.edureka.co/blog/concept-of-sharding-in-mongodb/>

[//www.youtube.com/embed/zBPqAp9DGWc](//www.youtube.com/embed/zBPqAp9DGWc)

**MongoDB** 是一个 NoSQL 数据库，以键-值对的形式存储数据，具有跨平台工作模式的能力。分片是 MongoDB 非常重要的概念之一。用外行人的话来说，这意味着将大的表格数据分解成更小的子集。

让我们从这篇文章开始，

## **是什么问题？**

当数据量如此之大时，它无法在单台机器中存储和扩展。将指数级增长的数据存储在一台机器上成本太高。此外，随着数据量的增加，单台机器中的数据存储可能无法提供可接受的读写吞吐量。

## **什么是分片？**

分片是跨多台机器存储数据记录的过程。它为满足数据增长的需求提供支持。这不是复制数据，而是从不同的机器上积累不同的数据。分片允许对存储在多个分片中的数据进行水平缩放。通过分片，我们可以添加更多的机器来满足不断增长的数据 的 需求以及读写操作的需求。你添加的机器越多，你的数据库能支持的读写操作就越多。

## **我们为什么需要分片？**

*   在复制中，所有写入都将进入主节点。主节点对延迟敏感。
*   每个副本集都有 12 个节点的限制
*   当活动数据集足够大时，内存不能足够大。主存的增加是有限度的。
*   本地磁盘不够大，无法存储大量数据。
*   垂直扩展成本太高，例如 RDBMS

## **分片架构**

mongodb 集群中有许多副本集，每个副本集包含 3 个或更多 MongoDB 节点。簇中有多个碎片。Mongos 与每个碎片通信，应用服务器又与查询路由器 Mongos 通信。这样，数据就被分区了。

例如，如果有 600 万份员工文档，它们不能存储在一台机器上，因为它的存储容量和读写吞吐量是有限的。在这种情况下，分片有助于跨多个分片存储和管理数据。如果数据被水平划分到 6 个分片上，根据每个雇员的雇员 id，每个分片将有 100 万个雇员 id。通过这种方式，大型数据集可以轻松扩展。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[MongoDB:用于大数据处理的数据库](https://www.edureka.co/blog/mongodb-the-database-for-big-data-processing/ "MongoDB: The Database for Big Data Processing")

[真实世界用例 MongoDB](https://www.edureka.co/blog/real-world-use-cases-of-mongodb/ "Real World Use Cases of MongoDB")

[学 MongoDB](https://www.edureka.co/mongodb "Learn MongoDB Development and Administration")

![mongoDB](img/716679304e4e9b6128ab067136aab9ba.png)