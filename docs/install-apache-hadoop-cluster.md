# 30 分钟内在亚马逊 EC2 免费层 Ubuntu 服务器上安装 Apache Hadoop 集群

> 原文：<https://www.edureka.co/blog/install-apache-hadoop-cluster/>

在很短的时间内 **Apache Hadoop** 已经从一项新兴技术发展成为解决当今企业所面临的大数据问题的成熟解决方案。

另外，自 2006 年推出以来，**亚马逊网络服务** (AWS)已经成为*云计算*的同义词。CIA 最近与 Amazon 签订合同，在 CIA 的数据中心内建立私有云服务，这证明了 AWS 作为云计算供应商在各种组织中越来越受欢迎和可靠。

如果你是大数据、Hadoop 和云计算的爱好者，你可以在*亚马逊 EC2* 上创建一个 *Apache Hadoop 集群*，开始你的旅程，而不用从你的口袋里花一分钱！这个练习不仅会帮助你理解 Apache Hadoop 集群的本质，还会让你熟悉 *AWS 云计算生态系统*。查看此[大数据认证](https://www.edureka.co/blog/top-big-data-certifications)博客将帮助您指导和完成重要的 hadoop 认证。

亚马逊还提供了 Apache Hadoop 的托管解决方案，命名为**亚马逊弹性 MapReduce** **(EMR)** 。到目前为止，EMR 还没有免费的服务。只有**猪**和**蜂箱**可供使用。从这个[大数据课程](https://www.edureka.co/big-data-hadoop-training-certification)，你会对猪和蜂巢有更深入的了解。

### Amazon EC2 上的 Apache Hadoop 集群

第一个 Apache Hadoop 集群的第一步是**在亚马逊**上创建一个账户。

![Amazon Web Services](img/71acd4c6dddb360ab14de1ad6d68fd98.png "Amazon Web Services")

下一步是**启动亚马逊 EC2 服务器** **并将**这些 AWS EC2 服务器配置为 Apache Hadoop 安装。

### 整个过程可以总结为三个简单的步骤:

### 第一步:

创建自己的*亚马逊 AWS 账户*。它是免费的，其直观的设计非常出色！这是您开始云计算之旅的最佳地点。为您的集群启动**【t1 . micro】**服务器(免费层合格使用)。

### 第二步

为 Hadoop 安装准备这些 AWS EC2 服务器，即升级操作系统包，安装 JDK 1.6，设置主机和从主到从的无密码 SSH。

### 第三步

编辑下面的**核心 Hadoop 配置文件**来设置集群。

*   hadoop-env.sh
*   core-site.xml
*   hdfs-site.xml
*   mapred-site.xml
*   大师
*   奴隶

将这些配置文件复制到*二级名称节点*和*从节点。*启动 *HDFS* 和 *MapReduce 服务*。那么，在亚马逊 EC2 free tier Ubuntu 服务器上安装 **Apache Hadoop 集群，难道不容易吗？**

这本免费的云计算 pdf 指南提供了在 *AWS EC2* 上设置一个 *多节点 Apache Hadoop 集群* 的详细步骤和相应的屏幕截图。

**一些有用的参考:**

[http://aws.amazon.com/free](http://aws.amazon.com/free/)