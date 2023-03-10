# 2023 年 Hadoop MapReduce 面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-mapreduce/>

## **Hadoop MapReduce 面试问题**

寻找雇主经常问的 Hadoop MapReduce 面试问题？

我希望你没有错过这个面试问题博客系列的前一篇博客，它包含了雇主最常问的 50 个 Hadoop 面试问题。这肯定会帮助你开始大数据工程师的职业生涯，并成为认证大数据专家。现在，在继续这篇 Hadoop MapReduce 访谈问题博客之前，让我们先简要了解一下 MapReduce 框架及其工作原理:

*   ***定义:***

MapReduce 是一个编程框架，它允许我们在分布式环境中对大型数据集执行分布式和并行处理。

*   ***MapReduce 2.0 或纱架构:***
    *   MapReduce 框架也遵循主/从拓扑结构，其中主节点(资源管理器)管理和跟踪在从节点(节点管理器)上执行的各种 MapReduce 作业。
    *   资源管理器由两个主要组件组成:
        *   **应用程序管理器:**它接受作业提交，为 ApplicationMaster 协商容器，并在执行 MapReduce 作业时处理故障。
        *   **调度器:**调度器分配运行在 Hadoop 集群上的各种 MapReduce 应用所需的资源。
*   ***MapReduce 工作原理:***
    *   顾名思义，MapReduce 阶段发生在 mapper 阶段完成之后。
    *   所以，第一个是映射作业，读取并处理数据块，产生键值对作为中间输出。
    *   reducer 从多个 map 作业接收键值对。
    *   然后，reducer 将这些中间数据元组(中间键-值对)聚集成一个更小的元组或键-值对集，这是最终的输出。

被怀疑困扰的头脑无法专注于通往胜利的道路。

*——阿瑟·高顿*

上面的引述反映了在参加面试之前以及在浏览 Hadoop MapReduce 面试问题博客时明确自己的基础知识的重要性。因此，我会建议你通过 [***MapReduce 教程***](https://www.edureka.co/blog/mapreduce-tutorial/) 博客来温习你的基础知识。

从这个由大数据专业人士设计的 [**大数据课程**](https://www.edureka.co/big-data-hadoop-training-certification) 中，你将获得 100%的实时项目经验，如 Hive、MapReduce 命令和概念等 Hadoop 工具。这里列出了 *Hadoop MapReduce 面试问题*，将帮助你不辜负雇主的期望。

## **Hadoop 面试问答|爱德华卡**

## **1。在 Hadoop 中使用 MapReduce 有什么优势？**

 <caption>#### **MapReduce 的优势**</caption> 
| **优势** | **描述** |
| ***灵活*** | Hadoop MapReduce 编程可以访问和操作不同类型的结构化和非结构化 |
| ***并行处理*** | MapReduce 编程划分并行执行的任务 |
|  | 具有容错能力，能够快速识别故障&，然后隐式应用快速恢复解决方案 |
| ***可扩展*** | Hadoop 是一个高度可扩展的平台，可以在大量服务器上存储和分发大型数据集 |
| ***性价比*** | Hadoop 的高可扩展性也使其成为满足不断增长的数据存储需求的经济高效的解决方案 |
| ***简单*** | 它基于一个简单的编程模型 |
| ***安稳*** | Hadoop MapReduce 在安全措施方面与 HDFS 和 HBase 安全保持一致 |
| ***速度*** | 它使用分布式文件系统进行存储，甚至可以在几分钟内处理大型非结构化数据集 |

## **2。你说的数据局部性是什么意思？**

*   ***[数据位置](https://www.edureka.co/blog/mapreduce-tutorial/#data_locality)*** 谈的是将计算单元移动到数据，而不是将数据移动到计算单元。
*   MapReduce 框架通过本地处理数据实现数据局部性
*   这意味着数据处理发生在存在数据块的节点管理器的节点上。

## **3。在 MapReduce 中设置输入输出类型/格式是必须的吗？**

不，在 MapReduce 中设置输入和输出类型/格式不是强制性的。默认情况下，群集将输入和输出类型视为“文本”。

## **4。我们可以重命名输出文件吗？**

是的，我们可以通过实现*多格式输出类*来重命名输出文件。

## **5。MapReduce 中的洗牌排序是什么意思？**

在完成映射任务后，进行混排和排序，其中每个缩减器的输入根据关键字进行排序。基本上，系统对 map 任务的键值输出进行排序并将其传输到 reducer 的过程称为 shuffle。

## **6。解释一下 MapReduce 中溢出的过程？**

地图任务的输出被写入循环内存缓冲区(RAM)。缓冲区的默认大小设置为 100 MB，可以使用 mapreduce.task.io.sort.mb 属性进行调整。溢出是指当缓冲区的内容达到某个阈值大小时，将数据从内存缓冲区复制到磁盘的过程。默认情况下，在 80%的缓冲区填满后，后台线程开始将内容从内存溢出到磁盘。因此，对于 100 MB 大小的缓冲区，溢出将在缓冲区的内容达到 80 MB 大小后开始。

**注意:**可以使用 MapReduce . map . sort . spill . percent 更改溢出阈值，默认设置为 0.8 或 80%。

## **7。什么是 MapReduce 框架中的分布式缓存？**

分布式缓存可以解释为，MapReduce 框架提供的一种设施，用来缓存应用需要的文件。一旦你为你的工作缓存了一个文件，Hadoop 框架将使它在你映射/减少任务运行的每一个数据节点上可用。因此，用户可以在映射器或缩减器作业中将缓存文件作为本地文件进行访问。

## **8。什么是合并器，你应该在哪里使用它？**

组合器就像一个迷你的 reducer 函数，它允许我们在映射输出转换到 reducer 阶段之前对其进行本地聚合。基本上，它通过减少从映射器传输到缩减器的数据量来优化 MapReduce 任务期间的网络带宽使用。

## **9。为什么地图任务的输出被存储(溢出)到本地磁盘而不是 HDFS？**

map 任务的输出是中间的键值对，然后由 reducer 处理产生最终的聚合结果。一旦 MapReduce 作业完成，就不需要地图任务产生的中间输出。因此，将这些中间输出存储到 HDFS 并复制它将产生不必要的开销。

## **10。当运行 map 任务的节点在 map 输出被发送到 reducer 之前失败时会发生什么？**

在这种情况下，映射任务将被分配一个新的节点，整个任务将再次运行以重新创建映射输出。

## **11。MapReduce 分区器的作用是什么？**

划分器将 map 任务产生的中间键值对划分成分区。分区的总数等于归约器的数量，其中每个分区由相应的归约器处理。使用基于单个键或一组键的散列函数来完成分区。Hadoop 中的默认分区器是 *HashPartitioner* 。

## **12。我们如何保证关于特定键的值到达同一个归约器？**

通过使用分割器，我们可以控制特定的键值进入同一个 reducer 进行处理。

## **13。输入拆分和 HDFS 块有什么区别？**

HDFS 块定义了数据在 HDFS 的物理划分方式，而输入分割定义了处理数据所需的记录的逻辑边界。

## **14。你说的 InputFormat 是什么意思？**

输入格式描述了 MapReduce 作业的输入规范。MapReduce 框架依赖于作业的输入格式来:

*   验证作业的输入规格。
*   将输入文件拆分成逻辑输入拆分实例，然后将每个实例分配给一个单独的映射器。
*   提供 RecordReader 实现，用于从逻辑 InputSplit 中读取记录，以供映射器处理。

## **15。TextInputFormat 的用途是什么？**

TextInputFormat 是 MapReduce 框架中的默认输入格式。在 TextInputFormat 中，输入文件被生成为 LongWritable 类型的键(文件中行开始的字节偏移量)和 Text 类型的值(行的内容)。

## **16。Hadoop MapReduce 中 RecordReader 的作用是什么？**

InputSplit 定义了一个工作的切片，但是没有描述如何访问它。“RecordReader”类从数据源加载数据，并将其转换为适合“Mapper”任务读取的(键，值)对。“RecordReader”实例由“输入格式”定义。

## **17。运行 MapReduce 作业需要哪些配置参数？**

“MapReduce”框架中需要用户指定的主要 ***[配置参数](https://www.edureka.co/blog/mapreduce-tutorial/#explanation_of_mapreduce_program)*** 有:

*   分布式文件系统中作业的输入位置
*   作业在分布式文件系统中的输出位置
*   数据的输入格式
*   数据输出格式
*   包含地图功能的类
*   包含 reduce 函数的类
*   包含映射器、缩减器和驱动程序类的 JAR 文件

## **18。什么时候应该使用 SequenceFileInputFormat？**

SequenceFileInputFormat 是一种用于在序列文件中读取的输入格式。它是一种特定的压缩二进制文件格式，针对在一个“MapReduce”作业的输出到另一个“MapReduce”作业的输入之间传递数据进行了优化。

序列文件可以生成为其他 MapReduce 任务的输出，并且是从一个 MapReduce 作业传递到另一个作业的数据的有效中间表示。

## **19。什么是身份映射器和身份缩减器？**

身份映射器是 Hadoop 框架提供的默认映射器。当 MapReduce 程序中没有定义 mapper 类时，它运行，它只是传递 reducer 阶段的输入键-值对。

与 Identity Mapper 一样，Identity reducer 也是 Hadoop 提供的默认 Reducer 类，如果没有定义 Reducer 类，它会自动执行。它也不执行任何计算或处理，而是简单地将输入键-值对写入指定的输出目录。

## **20。什么是地图边连接？**

映射端连接是映射器连接两个数据集的过程。

## **21。在 MapReduce 中使用地图边连接有什么好处？**

在 MapReduce 中使用地图端连接的优势如下:

*   在 shuffle 和 reduce 阶段，地图端连接有助于最小化排序和合并的成本。
*   通过减少完成任务的时间，地图端连接还有助于提高任务的性能。

## **22。什么是 MapReduce 中的 reduce 边连接？**

顾名思义，在 reduce 端联接中，减速器负责执行联接操作。它比 map side join 实现起来相对简单和容易，因为排序和改组阶段将具有相同键的值发送到同一个 reducer，因此，默认情况下，数据是为我们组织的。

♣ **提示**:我建议你去 MapReduce 的***[reduce side join](https://www.edureka.co/blog/mapreduce-example-reduce-side-join/)***专门的博客，里面有一个例子详细解释了 reduce side join 的整个过程。

## 23。你对 NLineInputFormat 了解多少？

NLineInputFormat 将“n”行输入拆分为一个拆分。

## **24。把减压器任务数设置为零合法吗？在这种情况下，输出将存储在哪里？**

是的，如果不需要缩减器，将缩减任务的数量设置为零是合法的。在这种情况下，map 任务的输出被直接存储到在 setOutputPath(Path)中指定的HDFS 中。

## **25。用 Java 写 MapReduce 作业有必要吗？**

不，MapReduce 框架支持多种语言，如 Python、Ruby 等。

## **26。如何优雅地停止正在运行的作业？**

用户可以使用以下命令优雅地停止 MapReduce 作业:*Hadoop job-kill JOBID*

## **27。你将如何提交额外的文件或数据(如 jar、静态文件等)。)用于运行时的 MapReduce 作业？**

分布式缓存用于将 map/reduce 作业所需的大型只读文件分发到集群。在该节点上执行作业的任何任务之前，框架会将必要的文件从 URL 复制到从属节点上。每个作业只复制一次文件，因此应用程序不应修改这些文件。

## **28。MapReduce 中的 inputsplit 如何正确确定记录边界？**

RecordReader 负责提供有关输入拆分中记录边界的信息。

## **29。减速器之间是如何沟通的？**

这是一个棘手的问题。“MapReduce”编程模型不允许“reducers”相互通信。“减速器”孤立运行。

## **30。定义投机执行**

如果一个节点执行任务的速度比预期的慢，主节点可以在另一个节点上冗余地执行同一任务的另一个实例。然后，首先完成的任务将被接受，而其他任务将被取消。这个过程称为推测性执行。

我希望这篇关于 Hadoop MapReduce 面试问题的博客对你有所帮助。欢迎您在下面的评论区提出您的疑问和反馈。在这篇博客中，我只讨论了 MapReduce 的面试问题。为了节省您访问多个网站询问与每个 Hadoop 组件相关的采访问题的时间，我们准备了一系列采访问题博客，涵盖 Hadoop 框架中的所有组件。请参考下面给出的链接，探索所有与 Hadoop 相关的面试问题，巩固您的基础知识:

*   [***50 强 Hadoop 面试问题***](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)
*   [***Hadoop 集群面试题***](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hadoop-cluster/)
*   **[*Hadoop HDFS 面试题*](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hdfs-2/)**
*   ***[猪面试问题](https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-pig/)***
*   [***蜂巢面试问题***](https://www.edureka.co/blog/interview-questions/hive-interview-questions/)
*   [***HBase 面试题***](https://www.edureka.co/blog/interview-questions/hbase-interview-questions/)