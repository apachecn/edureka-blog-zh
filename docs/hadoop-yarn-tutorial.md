# Hadoop YARN 教程–了解 YARN 架构的基础知识

> 原文：<https://www.edureka.co/blog/hadoop-yarn-tutorial/>

Hadoop YARN 将 Hadoop 的存储单元即 HDFS (Hadoop 分布式文件系统)与各种处理工具编织在一起。对于那些对这个话题完全陌生的人来说，YARN 代表“**Y**et**A**N**R**e source**N**ego tiator”。我还建议您在继续学习 Apache Hadoop YARN 之前，先阅读一下我们的 ***[Hadoop 教程](https://www.edureka.co/blog/hadoop-tutorial/)*** 和 ***[MapReduce 教程](https://www.edureka.co/blog/mapreduce-tutorial/)*** 。我将在这里解释以下主题，以确保在这篇博客结束时，你对 Hadoop YARN 的理解是清楚的。

*   [为什么是纱线？](#Why%20YARN?)
*   [Hadoop 纱线简介](#Introduction%20to%20Hadoop%20YARN)
*   [纱线的成分](#Components%20of%20YARN)
*   [申请提交中纱](#Application%20Submission%20in%20YARN)
*   [Hadoop 中的应用工作流](#Application%20Workflow)

## **为什么是纱线？**

在 Hadoop 版本 1.0 中，也称为 MRV1(MapReduce 版本 1)，MapReduce 执行处理和资源管理功能。它包括一个单一的主作业跟踪器。作业跟踪器分配资源、执行调度并监控正在处理的作业。它将 map 和 reduce 任务分配给多个称为任务跟踪器的从属进程。任务跟踪器定期向作业跟踪器报告他们的进度。

![MapReduce Version 1.0 - Hadoop YARN - Edureka](img/a35989ec582949586347188ac673a449.png)

由于单一的作业跟踪器，这种设计导致了可扩展性瓶颈。 IBM 在其文章中提到，根据雅虎这种设计的实际限制是由 5000 个节点和 40，000 个任务同时运行的集群来实现的。 除了这个限制，MRV1 中计算资源的利用效率很低。此外，Hadoop 框架变得仅限于 MapReduce 处理范式。

为了克服所有这些问题，Yahoo 和 Hortonworks 于 2012 年在 Hadoop 版本中引入了 YARN。YARN 背后的基本思想是通过接管资源管理和作业调度的职责来减轻 MapReduce 的负担。YARN 开始让 Hadoop 能够在 Hadoop 框架内运行非 MapReduce 作业。

您也可以观看下面的视频，我们的 [***Hadoop 认证培训***](https://www.edureka.co/big-data-and-hadoop) 专家正在详细讨论 YARN 概念& it 架构。

## **Hadoop Yarn 教程| Hadoop Yarn 架构| edu reka**

[//www.youtube.com/embed/2poZMI7it74?rel=0&showinfo=0](//www.youtube.com/embed/2poZMI7it74?rel=0&showinfo=0)

随着 YARN 的引入， ***[Hadoop 生态系统](https://www.edureka.co/blog/hadoop-ecosystem)*** 彻底革命化。它变得更加灵活、高效和可扩展。当雅虎在 2013 年第一季度上线 YARN 时，它帮助该公司将其 Hadoop 集群的规模从 40，000 个节点缩减到 32，000 个节点。但是工作数量翻了一番，达到每月 2600 万。

## **Hadoop 纱线简介**

既然我已经向您介绍了对 YARN 的需求，那么让我向您介绍 Hadoop v2.0 的核心组件 *YARN* 。YARN 允许不同的数据处理方法，如图形处理、交互处理、流处理以及批处理，来运行和处理存储在 HDFS 中的数据。因此，YARN 向 MapReduce 之外的其他类型的分布式应用程序开放了 Hadoop。

![Hadoop v1.0 vs Hadoop v2.0 - Hadoop YARN - Edureka](img/79c300d5b08f9943b1b1b9620e9d43d7.png)

YARN 通过使用多种工具使用户能够根据需要执行操作，如用于实时处理的 ***[【火花】](https://www.edureka.co/blog/spark-tutorial/)***；用于 SQL 的[***Hive***](https://www.edureka.co/blog/hive-tutorial/)；用于 NoSQL 等的[***h base***](https://www.edureka.co/blog/hbase-tutorial)。

除了资源管理，YARN 还执行任务调度。YARN 通过分配资源和调度任务来执行所有的处理活动。Apache Hadoop YARN 架构由以下主要组件组成:

1.  **资源管理器** **:** 运行在主守护进程上，管理集群中的资源分配。
2.  **节点管理器:** 它们运行在从守护进程上，负责每一个数据节点上任务的执行。
3.  **应用主:** 管理单个应用的用户作业生命周期和资源需求。它与节点管理器一起工作，并监视任务的执行。
4.  **容器:** 单个节点上的资源包，包括 RAM、CPU、网络、HDD 等。

## **纱线的成分**

您可以将 YARN 视为 Hadoop 生态系统的大脑。下图代表了纱线架构。

![Components of YARN - Hadoop YARN - Edureka](img/92b5256ce32964909b703f3ec0a9c891.png)

纱线架构的**第一个组成部分**是，

### **资源经理**

*   是资源分配的最终权威*。*
*   在接收到处理请求时，它相应地将部分请求传递给相应的节点管理器，在那里进行实际的处理。
*   它是群集资源的仲裁者，决定竞争应用程序的可用资源分配。
*   优化集群利用率，就像根据各种约束(如容量保证、公平性和 SLA)保持所有资源始终处于使用状态。
*   它有两个主要组件: a)调度器b应用管理器

***a)调度器***

*   调度器负责根据容量、队列等的限制，将资源分配给各种正在运行的应用程序。
*   在 ResourceManager 中，它被称为纯调度程序，这意味着它不执行任何对应用程序状态的监控或跟踪。
*   如果出现应用程序故障或硬件故障，调度程序不保证重新启动失败的任务。
*   根据应用程序的资源需求执行调度。
*   它有一个可插入的策略插件，负责在各种应用程序之间划分集群资源。有两个这样的插件:**容量调度器**和**公平调度器**，目前在 ResourceManager 中作为调度器使用。

***b)应用管理器***

*   它负责接受工作提交。
*   从资源管理器协商第一个容器，用于执行应用特定的应用主机。
*   管理集群中应用主机的运行，并提供故障时重启应用主机容器的服务。

来到**第二个部件**也就是 :

#### **节点管理器**

*   它负责 Hadoop 集群中的各个节点，而 管理给定节点上的用户作业和工作流。
*   它向资源管理器注册，并发送带有节点健康状态的心跳。
*   它的主要目标是管理资源管理器分配给它的应用程序容器。
*   它与资源管理器保持同步。
*   Application Master 通过向节点管理器发送容器启动上下文(CLC)向其请求分配的容器，该上下文包括应用运行所需的一切。节点管理器创建请求的容器进程并启动它。
*   监控单个容器的资源使用情况(内存、CPU)。
*   执行日志管理。
*   它还按照资源管理器的指示杀死容器。

Apache Hadoop 线程的**第三个组件**是，

##### **应用大师**

*   应用程序是提交给框架的单个作业。每个这样的应用程序都有一个与之相关联的唯一的应用程序主机，它是一个框架特定的实体。
*   它是协调应用在集群中的执行并管理故障的进程。
*   它的任务是从资源管理器协商资源，并与节点管理器一起执行和监控组件任务。
*   它负责从 ResourceManager 协商合适的资源容器，跟踪它们的状态并监控进度。
*   一旦启动，它会定期向资源管理器发送心跳信号，以确认其健康状况并更新其资源需求记录。

**第四个成分**是:

###### **集装箱**

*   它是一个物理资源的集合，例如单个节点上的 RAM、CPU 内核和磁盘。
*   纱线容器由容器启动上下文管理，即容器生命周期(CLC)。该记录包含环境变量的映射、存储在可远程访问的存储器中的依赖性、安全令牌、节点管理器服务的有效负载以及创建该过程所必需的命令。
*   它授予应用程序使用特定数量资源(内存、CPU 等)的权利。)在特定的主机上。 从 [数据工程认证](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 了解更多大数据及其应用。

## **申请提交中纱**

参考图片，看看 Hadoop YARN 提交申请的步骤:

1)提交作业

2) 获取申请 ID

3)申请提交上下文

4 a)启动集装箱发射

b)启动应用程序主机

5)分配资源

6 a)容器

b)启动

7)执行

![Application Submission - Hadoop YARN - Edureka](img/c70541bd6313f6be823111d1e2b643ef.png)

## **Hadoop 中的应用工作流**

参考给定的图片，可以看到 Apache Hadoop YARN 的应用工作流程涉及到以下步骤:你可以通过 [在印度的数据工程培训](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-india) 更好的理解。

1.  客户提交申请
2.  资源管理器分配一个容器来启动应用管理器
3.  应用程序管理器向资源管理器注册
4.  应用程序管理器向资源管理器请求容器
5.  应用程序管理器通知节点管理器启动容器
6.  应用程序代码在容器中执行
7.  客户端联系资源管理器/应用程序管理器以监控应用程序的状态
8.  应用程序管理器向资源管理器注销

![Application Workflow - Hadoop YARN - Edureka](img/8580df76aba3b92319cf42488f5e4f25.png)

*既然你已经知道了 Apache Hadoop YARN，那就来看看 Edureka 的Hadoop 培训吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的[大数据工程课程](https://www.edureka.co/masters-program/big-data-architect-training)使用零售、社交媒体、航空、旅游、金融领域的实时用例，帮助学习者成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*