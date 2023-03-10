# Hadoop 教程:关于 Hadoop 你需要知道的一切！

> 原文：<https://www.edureka.co/blog/hadoop-tutorial/>

如果你渴望以正确的方式学习 **Hadoop** ，那么你已经来到了一个完美的地方。在这篇 Hadoop 教程文章中，您将通过一种非常简单和透明的方法，从基础学到高级 Hadoop 概念。您也可以观看以下视频，我们的 **[Hadoop 培训](https://www.edureka.co/big-data-hadoop-training-certification)专家**正在讨论 Hadoop 概念以及**实际例子。**

## Apache Hadoop 教程| Hadoop 初学者教程|大数据 Hadoop | Hadoop 培训| Edureka



[https://www.youtube.com/embed/mafw2-CVYnA?rel=0&showinfo=0](https://www.youtube.com/embed/mafw2-CVYnA?rel=0&showinfo=0)This Edureka “Hadoop tutorial For Beginners” will help you to understand the problem with traditional system while processing Big Data and how Hadoop solves it.

在这篇 **Hadoop 教程**文章中，我们将涉及以下主题:

*   [这一切是如何开始的？](#How_It_All_Started)
*   [什么是大数据？](#WhatIsBigData)
*   [大数据与 Hadoop:餐厅类比](#RestaurantAnalogy)
*   [什么是 Hadoop？](#WhatisHadoop)
*   [Hadoop 即解决方案](#HadoopAsASolution)
*   [Hadoop 的特性](#HadoopFeatures)
*   [Hadoop 核心组件](#HadoopCoreComponents)
*   [Hadoop 最后。FM 案例研究](#lastFMCaseStudy)

## **这一切是如何开始的？**

在进入这篇 Hadoop 教程文章的技术细节之前，让我先讲一个有趣的故事*Hadoop 是如何诞生的？*和*为什么现在在业内这么流行？*。

所以，这一切都是从两个人开始的，**迈克·卡法雷拉**和**道格·卡丁，**他们正在建造一个能够索引 10 亿页的*搜索引擎系统*。经过他们的研究，他们估计这样一个系统的硬件成本大约为 50 万美元，每月运行成本为 3 万美元，相当昂贵。然而，他们很快意识到他们的架构不足以处理数十亿的网页。

![google-logo-png-hd-11](img/7fb702d4578c90b23d0f5f58a123a503.png)

他们看到了一篇发表于 **2003 年的论文，**描述了 [**谷歌的分布式文件系统，**](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf) 称为 **GFS，**在 **[谷歌](https://www.google.org/)的生产中被使用。**现在，这篇关于 [**GFS**](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf) 的论文证明是他们一直在寻找的东西，很快，他们意识到它将解决他们存储非常大的文件的所有问题，这些文件是作为 **web 爬网**和**索引**过程的一部分而生成的。

2004 年晚些时候，谷歌又发表了一篇论文，向世界介绍了[](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)。最后，这两篇论文导致了名为“ [**Hadoop**](https://hadoop.apache.org/docs/stable/) ”的框架的基础。 **Doug** 引述谷歌对 Hadoop 框架开发的贡献:

***谷歌活在未来几年，给我们其他人发送信息。***

至此，你应该已经意识到 Hadoop 的强大了。 现在，在继续讨论 Hadoop 之前，让我们从引领 Hadoop 发展的 [**大数据**](https://www.edureka.co/blog/big-data-tutorial) 开始讨论。

获得行业级项目认证&快速跟踪你的职业 [<button>看看吧！</button>](https://www.edureka.co/big-data-and-hadoop/)

## **什么是大数据？**

你是否曾想知道技术是如何发展以满足新兴需求的？

**例如:**

![hadoop tutorial landline to smart phones](img/b2523c60fd3155c9cd3458a70d334805.png)

早先我们有**座机**电话，但现在我们已经转向**智能手机。**同样，你们中有多少人记得在 90 年代广泛使用的*软驱*？这些软驱已经被硬盘所取代，因为这些软驱的存储容量和传输速度非常低。

![hadoop tutorial floppy to disk](img/07dd0c04951f1dc6a5f82d8be58d7f46.png)

因此，这使得软驱不足以处理我们今天处理的数据量。事实上，现在我们可以在云上存储万亿字节的数据，而不会受到大小限制的困扰  。

现在，让我们来谈谈有助于数据生成的各种驱动因素。

**听说过 *[物联网](https://www.edureka.co/blog/iot-tutorial/)* 吗？**

![hadoop tutorial IoT](img/54c58bc51d69c451f9f736b37d11397e.png)

**物联网**将你的物理设备连接到互联网，让它变得更智能。如今，我们有智能空调、电视等。您的智能空调会持续监控您的室温和室外温度，并相应地决定房间的温度。现在想象一下，安装在成千上万个家庭中的智能空调一年将产生多少数据。由此，你可以理解 ***[物联网](https://www.edureka.co/blog/iot-tutorial/)*** 是如何为大数据做出重大贡献的。

现在，让我们来谈谈大数据的最大贡献者，不是别人，正是**社交媒体**。

社交媒体是大数据发展中最重要的因素之一，因为它提供了关于人们行为的信息。您可以查看下图，了解每分钟生成的数据量:

![Social Media - Hadoop Tutorial - Edureka](img/772d0cccc422e2c7a1570eb576074acf.png) 图:Hadoop 教程——社交媒体数据生成统计

除了数据生成的速度之外，第二个因素是这些数据集中缺乏适当的格式或结构，这使得处理成为一个挑战。

## **Hadoop 教程:大数据&Hadoop–餐厅类比**

让我们以一家餐馆为例，了解与大数据相关的问题以及 Hadoop 如何解决该问题。

鲍勃是一个商人，他开了一家小餐馆。最初，在他的餐馆里，他曾经每小时收到**两份订单**，他的餐馆里有一名厨师和一个食品架，足以处理所有订单。

![Traditional Restaurant Analogy - Hadoop Tutorial - Edureka](img/ffa58b229b77a81b05e529d749fcf15e.png)

图:Hadoop 教程——传统餐厅场景

现在让我们将餐馆的例子与传统场景进行比较，在传统场景中，数据以稳定的速率生成，我们的传统系统，如[](https://www.edureka.co/blog/dbms-tutorial/)有足够的能力处理这些数据，就像鲍勃的厨师一样。在这里，您可以将数据存储与餐厅的食品货架相关联，将传统处理单元与厨师相关联，如上图所示。

![Traditional Scenario Failed - Hadoop Tutorial - Edureka](img/e0cfd6afdca11b665f021880e40e16c7.png)

图:Hadoop 教程–传统场景

几个月后，Bob 想扩大他的业务，因此，他开始接受网上订单，并在餐厅的菜单上增加了一些菜系，以吸引更多的顾客。由于这种转变，他们接受订单的速度上升到每小时 10 个订单的惊人数字，一个厨师很难应付目前的情况。意识到订单处理中的情况，Bob 开始思考解决方案。

![Distributed Chef - Hadoop Tutorial - Edureka](img/19ae4d1451afb3449cd490b2756ae548.png)

图:Hadoop 教程——分布式处理场景

同样，在大数据场景中，由于引入了各种数据增长驱动因素，如**社交媒体、智能手机**等，数据开始以惊人的速度生成。

现在，传统的系统，就像鲍勃餐厅的厨师一样，不足以有效处理这种突然的变化。因此，需要一种不同的解决策略来处理这个问题。

经过大量研究后，Bob 想出了一个解决方案，他雇佣了 4 名厨师来处理大量的订单。一切都进行得很顺利，但是这个解决方案导致了另一个问题。由于四个厨师共用同一个食物架，这个食物架成了整个过程的瓶颈。因此，解决方案并不像 Bob 认为的那样有效。![Distributed System Limitations - Hadoop Tutorial - Edureka](img/19ef587c4b8e52b0ebaa4dab2db4f1c6.png)

图:Hadoop 教程——分布式处理场景失败

类似地，为了解决处理巨大数据集的问题，安装了多个处理单元来并行处理数据(就像 Bob 雇佣了 4 名厨师一样)。但是即使在这种情况下，使用多个处理单元也不是一个有效的解决方案，因为集中式存储单元成为了瓶颈。

换句话说，整个系统的性能是由中央存储单元的性能驱动的。因此，一旦我们的中央存储出现故障，整个系统都会受到威胁。因此，再次需要解决这个单点故障。![Restaurant Solution - Hadoop Tutorial - Edureka](img/964b4e1b4bce07184f3c8c2a2711f795.png)

图:Hadoop 教程——餐厅问题解决方案

鲍勃想出了另一个高效的解决方案，他将所有的厨师分成两个等级，即一个**初级**和一个**厨师长**，并给每个初级厨师分配一个食物架。我们假设这道菜是肉酱。现在，根据鲍勃的计划，一个初级厨师准备肉，另一个初级厨师准备酱料。接下来，他们将把肉和酱都转给主厨，主厨将在混合两种配料后准备肉酱，然后作为最终订单交付。

![Hadoop as a Solution - Restaurant Analogy - Hadoop Tutorial - Edureka](img/20e3b1f0085cb22b4634b3e360a53288.png)

图:Hadoop 教程——餐厅类比中的 Hadoop

**Hadoop** 的功能类似于鲍勃的餐馆。由于食品货架分布在鲍勃的餐厅中，类似地，在 Hadoop 中，数据以一种带有复制的[](https://www.edureka.co/blog/hdfs-tutorial)分布式方式存储，以提供**容错。**对于并行处理，首先由从节点处理数据，并存储一些中间结果，然后由主节点合并这些中间结果以发送最终结果。

现在，您一定知道为什么大数据是一个问题陈述，以及 Hadoop 如何解决它。 正如我们刚才讨论的，大数据面临三大挑战:

*   **第一个问题是存储海量数据**

![hadoop tutorial colossal data](img/4b6bfd941dc9ad56d3f158002fffb5d1.png)

在传统系统中存储大量数据是不可能的。原因很明显，存储将被限制在一个系统中，而数据正以惊人的速度增长。

*   **第二个问题是存储异构数据**

![hadoop tutorial- types of data](img/01edd2016edfde6ce9082244c8db65d9.png)

现在我们知道储存是个问题，但让我告诉你这只是问题的一部分。数据不仅巨大，而且以各种格式呈现，即非结构化、半结构化和结构化。因此，您需要确保您有一个系统来存储从各种来源生成的不同类型的数据。

*   **最后让我们来关注第三个问题，也就是处理速度**

![hadoop tutorial processing speed](img/b88ecfadd9763fba15beea61fbfc5a7e.png)

现在，由于要处理的数据太大，处理这些海量数据所需的时间非常长。

为了解决存储问题和处理问题，在 Hadoop 中创建了两个核心组件——[](https://www.edureka.co/blog/hdfs-tutorial)[**纱**](https://www.edureka.co/blog/apache-hadoop-2-0-and-yarn/) 。HDFS 解决了存储问题，因为它以分布式方式存储数据，并且易于扩展。此外，YARN 通过大幅缩短加工时间解决了加工问题。向前看，让我们了解什么是 Hadoop？

## **什么是 Hadoop？**

![hadoop tutorial](img/f6792baef1ccf65a99bb08ca83e2a1a7.png)

**Hadoop** 是一个开源软件框架，用于在大型商用硬件集群上以分布式方式存储和处理**大数据**。Hadoop 在 Apache v2 许可下获得许可。

**Hadoop** 是基于 Google 写的论文在 [**MapReduce**](https://www.edureka.co/blog/videos/mapreduce-tutorial/) 系统上开发的，它应用了函数式编程的概念。Hadoop 是用 [**Java 编程语言**](https://www.edureka.co/blog/java-tutorial/) 编写的，位列最高级别的 Apache 项目。Hadoop 是由 **Doug Cutting** 和**Michael****j . Cafarella 开发的。**

让我们来了解一下 Hadoop 如何为我们到目前为止所讨论的大数据问题提供解决方案。

***![Hadoop-as-a-Solution - What is Hadoop - Edureka](img/a06946f7d96a40f1a2b4df61df4798ff.png)***

图:Hadoop 教程–Hadoop 即解决方案

*   第一个问题是存储大量数据。

如上图所示， **HDFS** 提供了一种分布式方式来存储**大数据。**你的数据存储在 **DataNodes** 的块中，你指定每个块的大小。假设您有 **512 MB** 的数据，并且您已经配置了 HDFS，这样它将创建 **128 MB** 的数据块。现在，HDFS 将数据分成 **4 个块**作为 **512/128=4** 并跨不同的 DataNodes 存储。在将这些数据块存储到数据节点时，数据块会在不同的数据节点上复制，以提供**容错。**

Hadoop 遵循**水平扩展**而不是垂直扩展。在水平扩展中，您可以根据需要在运行时向 HDFS 集群添加**新节点**，而不是增加每个节点中的硬件堆栈。

*   下一个问题是存储各种数据。

如上图所示，在 HDFS 你可以存储各种数据，无论是**结构化、半结构化**还是**非结构化。**在 HDFS，没有*预倾销模式验证。*它还遵循一次写入和多次读取模式。由于这个原因，你可以只写一次任何类型的数据，你可以多次阅读它来寻找见解。

*   **第三个挑战是如何更快地处理数据**。

为了解决这个问题，我们**将处理单元移动到数据**而不是将数据移动到处理单元。

**那么，把计算单元移到数据上是什么意思呢？**

这意味着**处理逻辑**被发送到**节点**存储数据，每个节点可以并行处理一部分数据，而不是将数据从不同的节点移动到单个主节点进行处理。最后，每个节点产生的所有中间输出被合并在一起，最终响应被发送回**客户机。**有了 [Azure 数据工程认证](https://www.edureka.co/microsoft-azure-data-engineering-certification-course)可以更好的理解。

## **Hadoop 的特性**

***![Hadoop Features - Hadoop Tutorial - Edureka](img/08236eb0b804d1e6595705e7edc5d831.png)***

图:Hadoop 教程——Hadoop 特性

### **可靠性**

当机器作为一个单元工作时，如果其中一台机器发生故障，另一台机器将接管责任，以可靠的和容错的方式工作。Hadoop 基础架构具有内置的容错功能，因此 Hadoop 高度可靠。

### **经济实惠**

Hadoop 使用商用硬件(如您的 PC、笔记本电脑)。例如，在一个小型的 [**Hadoop 集群**](https://www.edureka.co/blog/hadoop-clusters) 中，您的所有 DataNodes 都可以具有普通配置，如 8-16 GB RAM、5-10 TB 硬盘和至强处理器。

但是，如果我将基于硬件的 **RAID** 与 **Oracle** 一起用于同样的目的，我最终的花费至少会增加 5 倍。因此，基于 Hadoop 的项目的拥有成本**被最小化。**维护 Hadoop 环境更容易，也更经济。此外，Hadoop 是**开源**软件，因此没有许可成本。

### **扩展性**

Hadoop 具有与**基于云的**服务无缝集成的内在能力。因此，如果您在云上安装 Hadoop，您不需要担心可扩展性因素，因为您可以随时购买更多硬件并在几分钟内扩展您的设置。

就处理各种数据的能力而言，Hadoop 非常灵活。我们在之前关于 **[大数据教程](https://www.edureka.co/blog/big-data-tutorial)** 的博客中讨论了**【多样性】**，其中数据可以是任何类型，Hadoop 可以存储和处理所有数据，无论是结构化、半结构化还是非结构化数据。

这四个特征使得 **Hadoop** 成为**应对大数据挑战的解决方案的领跑者**。现在我们知道了什么是 Hadoop，我们可以探索 Hadoop 的核心组件了。 让我们了解一下，Hadoop 的核心组件有哪些。

## **Hadoop 核心组件**

在设置 Hadoop 集群时，您可以选择许多服务作为您的 Hadoop 平台的一部分，但有两项服务对于设置 Hadoop 来说是必不可少的。一个是 **HDFS(仓储)**一个是**纱线(加工)**。HDFS 代表 **Hadoop 分布式文件系统**，它是 Hadoop 的可扩展存储单元，而 YARN 用于处理数据，即以分布式和并行的方式存储在 HDFS 中。

让我们先从 HDFS 开始吧。t的主要组件是 **NameNode** 和 **DataNode** 。让我们来详细谈谈这两个组件的作用。

**![HDFS - Hadoop Tutorial - Edureka](img/b2f69f9074a17cd4b2f9c1e5156d62fd.png)**

图:HDFS Hadoop 教程

#### **NameNode**

*   主守护进程维护和管理数据节点(从节点)
*   记录集群中存储的所有块的**元数据**，如存储块的位置、文件大小、权限、层次等。
*   它记录了**文件系统元数据** 发生的每一次变化
*   如果在 HDFS 删除了一个文件，NameNode 会立即将此记录在**编辑日志**T3 中
*   它定期接收来自集群中所有数据节点的**心跳**和阻塞报告，以确保数据节点处于**活动状态**
*   它记录了 **HDFS** 和**数据节点**中存储的所有块
*   它具有高可用性和联合特性，我将在 **[HDFS 架构](https://www.edureka.co/blog/hdfs-tutorial)** 中详细讨论这些特性

#### DataNode

*   在每台从机上运行的是**从守护进程**
*   **实际数据**存储在数据节点上
*   负责服务来自客户端的**读**和**写请求**
*   它还负责**创建块、删除块**以及**根据命名节点**做出的决定复制相同的
*   它定期向 NameNode 发送**心跳**来报告 HDFS 的整体健康状况，默认情况下，该频率设置为 **3 秒**

所以，简而言之，这就是 HDFS。现在，让我们前进到 Hadoop 的第二个基本单元，即 YARN。

### **纱**

YARN 由两大部分组成: **ResourceManager** 和 **NodeManager** 。

**![YARN - Hadoop Tutorial - Edureka](img/bf4d5c6aff5ef18590b6c6360978bfbe.png)**

图:Hadoop 教程——YARN

#### **资源管理器**

*   它是一个**集群级**(每个集群一个)组件，运行在主机上
*   它管理**资源**和**调度**在线程之上运行的应用
*   它有两个组件:**调度器** & **应用管理器**
*   调度器负责**分配资源**给各种运行的应用
*   application manager 负责**接受作业提交**并协商执行应用的第一个容器
*   它跟踪来自节点管理器的**心跳**

#### **节点管理器**

*   它是一个**节点级的**组件(每个节点一个)，运行在每个从机上
*   负责管理**个集装箱**和**监控**每个集装箱的资源利用情况
*   它还跟踪**节点健康**和**日志管理**
*   持续与**资源管理器**通信，以保持**最新**

## **Hadoop 生态系统**

到目前为止，你应该已经明白 Hadoop 既不是一种编程语言，也不是一种服务，它是一个解决大数据问题的平台或框架。您可以将它视为一个套件，其中包含大量用于接收、存储和分析巨大数据集的服务，以及用于配置管理的工具。

![Hadoop Ecosystem - Hadoop Tutorial - Edureka](img/cc92c97c58d90a591388931a640ad502.png)

图:Hadoop 教程——Hadoop 生态系统

我们已经在我们的 ***[Hadoop 生态系统博客](https://www.edureka.co/blog/hadoop-ecosystem)*** 中详细讨论了 Hadoop 生态系统及其组件。现在，在这个 Hadoop 教程中，让我们了解一下 **Last.fm 如何将 Hadoop 作为其解决方案策略**的一部分。

## **Hadoop 教程** **:最后。FM 案例分析**

![Hadoop tutorial last.fm](img/5a0d2fdbdf686c0dc123625fa0346195.png)

**最后。FM** 是**网络电台**和**社区驱动的**音乐发现服务，成立于 **2002 年。**用户将信息传递到最后。FM 服务器指示他们正在听的歌曲。接收到的数据被处理和存储，以便用户能够以图表的形式访问它。因此，最后。FM 可以做出智能的品味和兼容的决策来产生推荐。你甚至可以在金奈 [Azure 数据工程认证查看大数据的详细信息](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-chennai) 。数据从以下两个来源之一获得:

*   **scrobble:** 用户播放自己选择的曲目，并将信息发送到 Last。FM 通过客户端应用程序。
*   **收音机** **收听:**当用户调成最后一首时。调频广播电台和流媒体歌曲。

最后。FM 应用程序允许用户喜欢、跳过或禁止他们所听的每首歌曲。该音轨监听数据也被传输到服务器。

*   每月超过**4000 万**独立访客和**500 万**页面浏览量
*   *   高达每秒 800 个滚动条
    *   每天超过 4000 万个金币
    *   迄今超过 750 亿次滚动
*   **电台统计:**
    *   超过**1000 万秒**每月治疗时间
    *   日均超过 **40 万**独特站
*   每个 **scrobble** 和 **radio** listen 生成至少一个**log line**

### **终于 Hadoop 了。FM**

*   **100 个**节点
*   **每节点 8 核**(双四核)
*   **每节点 24GB** 内存
*   **8TB** (4 个 2TB 的磁盘)
*   **配置单元集成**运行优化的 **SQL 查询**进行分析

**最后。FM** 在 **2006** 开始使用 Hadoop，因为用户从**数千增长到数百万。**在 Hadoop 的帮助下，他们每天、每月和每周处理数百项工作，包括网站统计和指标、图表生成(即跟踪统计)、元数据更正(例如艺术家的拼写错误)、搜索索引、组合/格式化数据以提供建议、数据洞察、评估&报告。这有助于持续。FM 迅速成长，并找出用户的口味，在此基础上，他们开始推荐音乐。

我希望这篇博客能提供信息，增加你的知识。在我们下一篇关于 *[**Hadoop 生态系统**](https://www.edureka.co/blog/hadoop-ecosystem) ，*的博客中，我们将详细讨论 Hadoop 生态系统中的不同工具。

*现在，您已经了解了 Hadoop 及其特性，请查看 Edureka 在钦奈举办的* ***[大数据培训](https://www.edureka.co/big-data-and-hadoop-training-chennai)*** *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的[大数据工程课程](https://www.edureka.co/masters-program/big-data-architect-training)使用零售、社交媒体、航空、旅游、金融领域的实时用例，帮助学习者成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

*有问题吗？请在评论区提出来，我们将回复您或参加我们在勒克瑙的 [Hadoop 培训。](https://www.edureka.co/big-data-hadoop-training-certification-lucknow)*