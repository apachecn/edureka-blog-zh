# 解释 Hadoop 配置

> 原文：<https://www.edureka.co/blog/explaining-hadoop-configuration/>

[//www.youtube.com/embed/By_bibVn_x0](//www.youtube.com/embed/By_bibVn_x0)

这篇博文讨论了重要的 Hadoop 配置文件，并提供了相关的例子。透彻理解这一主题对于获得您的 ***[大数据架构师大师认证](https://www.edureka.co/masters-program/big-data-architect-training#projects)*** 以及执行其所有项目至关重要。让我们从主从概念开始，这对理解 Hadoop 的配置文件至关重要。

## **奴隶&主人:**

从服务器包含一个主机列表，每行一个，需要这些主机来托管 DataNode 和 TaskTracker 服务器。主服务器包含主机列表，每行一个，这些主机是托管辅助 NameNode 服务器所必需的。Masters 文件向 Hadoop 守护进程通知辅助 NameNode 位置。主服务器上的' **Masters** '文件包含主机名和节点服务器的辅助名称。

Hadoop-env.sh，core-ite.xml，hdfs-site.xml，mapred-site.xml，master and slave 都在 Hadoop 安装目录的‘conf’目录下。

## **Core-site.xml 和 hdfs-site.xml:**

core-site.xml 文件通知 Hadoop 守护进程 NameNode 在集群中的哪个位置运行。它包含 Hadoop 核心的配置设置，例如 HDFS 和 MapReduce 通用的 I/O 设置。

hdfs-site.xml 文件包含 hdfs 守护程序的配置设置；NameNode、辅助 NameNode 和 DataNodes。在这里，我们可以配置 hdfs-site.xml 来指定 hdfs 上的默认数据块复制和权限检查。实际的复制次数也可以在创建文件时指定。如果在创建时未指定复制，则使用默认值。成为数据工程师 si 的最佳途径获得亚特兰大 [Azure 数据工程课程](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-atlanta) 。

## **在 hdfs-site.xml 中定义 HDFS 细节:**

![Hadoop Configuration](img/446094ee1351da3b381aad8684e392d3.png "Hadoop Configuration")

## **Mapred-site.xml:**

![Hadoop Configuration](img/e6cc87054cbd42ae007d06b9574dc4fd.png "Hadoop Configuration")

mapred-site.xml 文件包含 MapReduce 守护程序的配置设置；工作跟踪器和任务跟踪器。

## **定义 mapred-site.xml:**

![Hadoop Configuration](img/bf8ee347567fe9bc41ac93ad21a6605e.png "Hadoop Configuration")

以下链接提供了有关配置文件的更多详细信息:

*   http://hadoop.apache.org/docs/r1.1.2/core-default.html
*   http://hadoop.apache.org/docs/r1.1.2/mapred-default.html
*   http://hadoop.apache.org/docs/r1.1.2/hdfs-default.html

## **Per-process 运行时环境:**

![Hadoop Configuration](img/1c6e834127307ae1d4a51df20c657bec.png "Hadoop Configuration")

该文件提供了一种为每台服务器提供客户参数的方法。Hadoop-env.sh 来源于安装的“conf/”目录中提供的整个 Hadoop 核心脚本。

*以下是一些可以指定的环境变量的例子:*

export Hadoop _ DATANODE _ heap size = " 128 "

export Hadoop _ TASKTRACKER _ heap size = " 512 "

“hadoop-metrics.properties”文件控制报告，默认条件设置为不报告。

## **关键属性:**

*   文件系统默认名称
*   Hadoop.tmp.dir
*   Mapred.job.tracker

## **网络需求:**

Hadoop 核心使用 Shell (SSH)来启动从节点上的服务器进程，这需要主节点与所有从节点和辅助节点之间的无密码 SSH 连接。

## **Web UI 网址:**

*   NameNodestatus:http://localhost:50070/DFS health . JSP
*   JobTrackerstatus:http://localhost:50030/job tracker . JSP
*   TaskTrackerstatus:http://localhost:50060/tasktracker . JSP
*   DataBlockScanner 报告:http://localhost:50075/blockScannerReport

## **脸书 Hadoop 集群:**

脸书使用 Hadoop 来存储内部日志和维度数据源的副本，并将其用作报告、分析和机器学习的来源。目前，脸书有两个主要的集群:一个 1100 机器的集群，有 800 个核心和大约 12 PB 的原始存储。另一个是 300 机器集群，具有 2，400 个核心和大约 3 PB 的原始存储。每个商用节点都有 8 个内核和 12 TB 存储。

脸书大量使用流媒体和 Java API，并使用 Hive 构建了一个更高级的数据仓库框架。他们还开发了一种应用于 HDFS 上空的引信。

通过 [蔚蓝数据工程课程](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 可以更好的理解。

## **样本集群配置:**

![Hadoop Configuration](img/afc73fdc34ef821df16b84629ae7381d.png "Hadoop Configuration")

## **Hadoop 集群——典型用例:**

![Hadoop Configuration](img/1f37471dddba731447daed28b96e1a28.png "Hadoop Configuration")

上图清楚地解释了每个节点的配置。NameNode 对内存的要求很高，会有大量的 RAM，并且不需要大量的硬盘内存。辅助 NameNode 的内存需求没有主 NameNode 高。每个 DataNode 都需要 16 GB 的内存，并占用大量硬盘空间，因为它们应该存储数据。他们也有多个驱动器。通过此[大数据课程](https://www.edureka.co/big-data-hadoop-training-certification)了解更多关于 Hadoop 集群、HDFS 和其他重要主题的信息，成为 Hadoop 专家。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**![edureka](img/dfabd28e4a5cfa1361af3cbb4724380e.png)相关帖子:**

[大数据和 Hadoop 培训](https://www.edureka.co/big-data-and-hadoop)

[Hadoop 集群配置文件](https://www.edureka.co/blog/hadoop-cluster-configuration-files/ "Hadoop Cluster Configuration Files")