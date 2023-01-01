# 2023 年 Hadoop 面试问题—设置 Hadoop 集群

> 原文：<https://www.edureka.co/blog/interview-questions/hadoop-interview-questions-hadoop-cluster/>

## **Hadoop 集群面试问题**

寻找雇主经常问的 Hadoop 集群面试问题？这是 Hadoop 集群面试问题的第二个列表，涵盖了如何设置 Hadoop 集群。我希望您一定没有错过我们 Hadoop 面试问题系列的第一部分，它涵盖了***[50 大 Hadoop 面试问题](https://www.edureka.co/blog/interview-questions/top-50-hadoop-interview-questions-2016/)*** 。

永远记住，只有理论知识是不足以破解面试的。雇主希望候选人具备 Hadoop 方面的实用知识和实践经验。所以，这个 Hadoop 集群面试问题将帮助你获得 Hadoop 框架的实用知识。

如果你有兴趣在自己的系统上安装 Hadoop 集群，可以通过我们的博客 ***[单节点 Hadoop 集群设置](https://www.edureka.co/blog/install-hadoop-single-node-hadoop-cluster)*** 和 ***[多节点 Hadoop 集群设置](https://www.edureka.co/blog/setting-up-a-multi-node-cluster-in-hadoop-2.X)*** 。

## **1。Hadoop 可以运行的模式有哪些？**

我们有三种模式可以运行 Hadoop，它们是:

 <caption>#### **运行 Hadoop 的模式**</caption> 
| **模式** | **描述** |
| ***【单机(本地)*** | 

*   Using local file system for input and output operation is the default mode of Hadoop.
*   This mode is mainly used for debugging purposes, and HDFS is not supported.
*   绘制红色网站。XML、core-site.xml、hdfs-site.xml 文件不需要自定义配置. .

 |
| ***伪分布式*** | 

*   You need to configure all the above three files.
*   All daemons run on one node.
*   Two master & slave nodes are on the same machine.

 |
| ***全分布*** | 

*   This is a production stage of Hadoop.
*   Data is distributed on multiple nodes in Hadoop cluster.
*   Separate nodes are assigned as master nodes and slave nodes.

 |

## **2。单机(本地)模式有什么特点？**

*   在独立模式下，没有守护进程，所有东西都在一个 JVM 上运行。
*   它没有 DFS，使用本地文件系统。
*   独立模式仅适用于在测试开发期间运行 MapReduce 程序。
*   这是最少使用的环境之一。

## **3。伪模式有什么特点？**

在开发和测试环境中都使用伪模式。在伪模式下，所有的守护进程都运行在同一台机器上。

## **4。全分布式模式有什么特点？**

这是一个重要的问题，因为在生产环境中使用完全分布式模式，我们有“n”台机器组成一个 Hadoop 集群。Hadoop 守护进程运行在一个机器集群上。有一台运行 Namenode 的主机和其他运行 Datanodes 的主机。节点管理器安装在每个 DataNode 上，它负责在每个 DataNode 上执行任务。所有这些节点管理器都由 ResourceManager 管理，resource manager 接收处理请求，然后相应地将部分请求传递给相应的节点管理器。

## **5。/etc/hosts 中配置了什么，在设置 Hadoop 集群中有什么作用？**

这是一个挑战你基本概念的技术问题。/etc/hosts 文件包含该主机的主机名及其 IP 地址。它将 IP 地址映射到主机名。在 Hadoop 集群中，我们将所有主机名(主服务器和从服务器)及其 IP 地址存储在/etc/hosts 中，以便我们可以轻松地使用主机名而不是 IP 地址。

## **6。NameNode，resource manager&MapReduce job history 服务器的默认端口号是多少？**

如果你正在使用 Hadoop，你应该记住基本的服务器端口号。对应守护进程的端口号如下:

Namenode-' 50070 '

资源管理器—‘8088’

MapReduce 作业历史服务器-“19888”。

## **7。有哪些主要的 Hadoop 配置文件？**

♣提示:通常，通过讲述 Hadoop 中的 4 个主要配置文件并给出它们的简要描述来展示你的专业知识。

*   **core-site . XML:**core-site . XML 通知 Hadoop 守护进程 NameNode 在集群上运行的位置。它包含了 Hadoop 内核的配置设置，比如 HDFS & MapReduce 通用的 I/O 设置。

*   **hdfs-site . XML:**HDFS-site . XML 包含 HDFS 守护进程的配置设置(即 NameNode、DataNode、Secondary NameNode)。它还包括 HDFS 的复制因子和数据块大小。

*   **mapred-site . XML**:mapred-site . XML 包含 MapReduce 框架的配置设置，比如可以并行运行的 JVM 数量、映射器和 reducer 的大小、进程可用的 CPU 内核等。

*   **yarn-site . XML:**yarn-site . XML 包含了 ResourceManager 和 NodeManager 的配置设置，如应用内存管理大小、程序需要的操作&算法等。

这些文件位于 hadoop 目录下的 *conf/hadoop/* 目录中。

## **8。Hadoop 类路径如何在 Hadoop 守护进程的启动或停止中起到至关重要的作用？**

♣提示:为了检查你对 Hadoop 的了解，面试官可能会问你这个问题。

CLASSPATH 包括所有包含启动/停止 Hadoop 守护进程所需的 jar 文件的目录。类路径设置在***/etc/Hadoop/Hadoop-env . sh***文件中。

## **9。RAM 的溢出系数是多少？**

♣提示:这是一个理论上的问题，但是如果你给它添加一点实用的味道，你可能会得到一个偏好。

地图输出存储在内存缓冲器中；当该缓冲区几乎满时，溢出阶段开始，以便将数据移动到临时文件夹。

地图输出首先被写入缓冲区，缓冲区大小由*MapReduce . task . io . sort . MB*属性决定。默认情况下，它将是 100 MB。

当缓冲区达到某个阈值时，它将开始向磁盘溢出缓冲区数据。该阈值在*MapReduce . map . sort . spill . percent 中指定。*

## **10。提取 tar.gz 格式的压缩文件的命令是什么？**

这是一个很简单的问题，***tar-xvf/file _ location/filename . tar . gz***命令会解压 tar.gz 压缩文件。

## **11。你将如何检查 Java 和 Hadoop 是否安装在你的系统上？**

通过使用以下命令，我们可以检查是否安装了 Java 和 Hadoop，以及它们的路径是否在内部设置。bashrc 文件:

用于检查 Java-***Java-版本***

用于检查 Hadoop—***Hadoop 版本***

## **12。什么是默认复制因子，您将如何更改它？**

默认的复制因子是 3。

*♣提示:默认的复制因子可以通过三种方式改变。三种方式都回答会显示你的专长。*

1.  通过将该属性添加到***HDFS-site . XML***:

```
<property>
<name>dfs.replication</name>
<value>5</value>
<description>Block Replication</description>
</property>

```

2.  或者您可以使用以下命令基于每个文件更改复制因子:

***Hadoop fs–set rep–w3/file _ location***

3.  或者您可以使用以下命令更改目录中所有文件的复制因子:

***Hadoop fs–set rep–w3-R/directory _ location***

## **13。fsck 的完整形式是什么？**

fsck 的完整形式是*文件系统检查。* HDFS 支持 fsck(文件系统检查)命令来检查各种不一致。它旨在报告 HDFS 文件的问题，例如，文件的缺失块或复制不足的块。

## **14。hdfs-site.xml 的主要属性是什么？**

HDFS-site . XML 的三个主要属性是:

1.  ***dfs.name.dir*** 给出 NameNode 存储元数据(FsImage 和编辑日志)的位置以及 dfs 所在的位置——在磁盘上还是在远程目录上。
2.  ***dfs.data.dir*** 它给出了 DataNodes 的位置，数据将存储在这里。
3.  ***fs . check point . dir***是文件系统上的目录，次 NameNode 存储编辑日志的临时镜像，需要合并，以及备份的 FsImage。

## **15。如果您在键入 hadoop fsck /时得到“连接被拒绝 java 异常”会发生什么？**

如果您在键入 hadoop fsck 时收到“连接被拒绝 java 异常”,这可能意味着 NameNode 没有在您的虚拟机上工作。

## **16。我们如何通过 HDFS 命令查看压缩文件？**

我们可以在 HDFS 使用***Hadoop fs-text/filename****命令*查看压缩文件。

## **17。进入安全模式和退出安全模式的命令是什么？**

♣提示:解决这个问题时，首先解释安全模式，然后转到命令。

Hadoop 中的安全模式是 NameNode 的一种维护状态，在此期间，NameNode 不允许对文件系统进行任何更改。在安全模式下，HDFS 群集是只读的，不会复制或删除数据块。

*   要了解安全模式的状态，可以使用命令:***HDFS DFS admin-safe mode get***

*   进入安全模式: ***hdfs dfsadmin -safemode 进入***

*   退出安全模式: ***hdfs dfsadmin -safemode 离开***

## **18。“jps”命令有什么作用？**

***jps*** 命令用于检查所有 Hadoop 守护进程，如 NameNode、DataNode、ResourceManager、NodeManager 等。在机器上运行。

## **19。如何重启 Namenode？**

这个问题有两个答案，回答两个都会给你加分。我们可以通过以下方法重启 NameNode:

1.  您可以使用 ***单独停止 NameNode。******/sbin/Hadoop-daemon . sh 停止 namenode*** 命令，然后使用 ***启动 namenode。******/sbin/Hadoop-daemon . sh start NameNode***
2.  使用。 ***/sbin/stop-all。******sh***然后用。***/sbin/start-all . sh***命令将首先停止所有守护进程，然后启动所有守护进程。

## **20。我们如何检查 NameNode 是否在工作？**

要检查 NameNode 是否工作，使用 ***jps*** 命令，这将显示所有正在运行的 Hadoop 守护进程，在那里您可以检查 NameNode 守护进程是否正在运行**。**

## **21。如何在 web 浏览器 UI 中查看 Namenode？**

如果您想在浏览器中查找 NameNode，NameNode web 浏览器 UI 的端口号为 ***50070*** 。我们可以使用*http://master:50070/DFS health . JSP*在网络浏览器中查看。

## **22。用于启动和关闭 Hadoop 守护进程的不同命令有哪些？**

♣提示:解释停止和启动 Hadoop 守护进程的三种方式，这将展示你的专业知识。

1.  ***。/sbin/start-all.sh*** 来启动所有的 Hadoop 守护进程和。***/sbin/stop-all . sh***停止所有 Hadoop 守护进程。
2.  然后，您可以使用 ***一起启动所有的 dfs 守护程序。******/sbin/start-DFS . sh***，纱守护进程一起使用 ***。******/sbin/start-yarn . sh***和 MR 作业历史服务器使用 ***。******/sbin/Mr-job history-daemon . sh 启动 historyserver*** 。要停止这些守护进程，我们可以使用 ***。******/sbin/start-yarn . sh***， ***。/sbin/start-yarn . sh****&****。******/sbin/Mr-job history-daemon . sh 停止 historyserver*** 。
3.  最后一种方法是单独启动所有守护进程，并单独停止它们:

***。/sbin/Hadoop-daemon . sh start NameNode***

***。/sbin/hadoop-daemon.sh 启动 datanode***

***。/sbin/yarn-daemon.sh 启动资源管理器***

***。/sbin/yarn-daemon.sh 启动节点管理器***

***。/sbin/mr-jobhistory-daemon.sh 启动 historyserver***

并以同样的方式阻止他们。

## **23。从文件由什么组成？**

Slaves 文件包含一个主机列表，每行一个，该列表包含运行节点管理器服务器的 DataNode 位置。

## **24。主文件由什么组成？**

masters 文件包含辅助 NameNode 服务器位置。

## **25。hadoop-env.sh 是做什么的？**

***hadoop-env . sh***为 Hadoop 提供运行的环境。比如 JAVA_HOME，CLASSPATH 等等。被安置在这里。

## **26。hadoop-env.sh 文件在哪里？**

正如我们之前讨论的，所有的配置文件都驻留在那里，因此 hadoop-env.sh 文件存在于 */etc/hadoop* 目录中。

## **27。在 Hadoop_PID_DIR 中，PID 代表什么？它是做什么的？**

PID 代表“进程 ID”。该目录存储正在运行的服务器的进程 ID。

## **28。hadoop-metrics.properties 文件是做什么的？**

*♣提示:由于这个文件只有在特殊情况下才手动配置，所以回答这个问题会给面试官留下深刻印象，表明你对配置文件的专业知识。*

***Hadoop-metrics . properties***用于'*性能* *报告*目的。它控制 Hadoop 的报告。API 是抽象的，因此它可以在各种度量客户端库之上实现。客户端库的选择是一个配置选项，同一应用程序中的不同模块可以使用不同的指标实现库。这个文件存放在 ***/etc/hadoop*** 里面。

## **29。Hadoop 的网络要求是什么？**

您应该回答这个问题，因为 Hadoop 核心使用 Shell (SSH)与从属节点通信，并在从属节点上启动服务器进程。它需要一个*无密码*的 SSH 连接在主设备和所有从设备以及从设备之间，所以每次它都不需要请求认证，因为主设备和从设备需要严格的通信。

## **30。为什么在全分布式环境中我们需要无密码的 SSH？**

在全分布式环境中，我们需要一个*无密码* SSH，因为当集群在全分布式环境中实时运行时，通信过于频繁。DataNode 和 NodeManager 应该能够快速向主服务器发送消息。

## **31。这会导致安全问题吗？**

不，一点也不。Hadoop 集群是一个孤立的集群，通常与互联网无关。它有一种不同的结构。我们不必担心那种安全漏洞，例如，有人通过互联网入侵，等等。Hadoop 有一种非常安全的方式来连接到其他机器以获取和处理数据。

## **32。SSH 在哪个端口上工作？**

SSH 工作在端口号为 **22、**的端口上，尽管它可以被配置。 **22** 是默认端口号。

## **33。你能告诉我们更多关于宋承宪的事吗？**

SSH 只不过是一种安全的外壳通信，它是一种在 22 号端口上工作的协议，当你使用 SSH 时，你真正需要的是一个密码，以连接到另一台机器。SSH 不仅仅是主从之间，还可以是两台主机之间。

## **34。当 ResourceManager 关闭时，NameNode 会发生什么情况？**

当资源管理器关闭时，它将不起作用(用于提交作业),但 NameNode 将存在。因此，如果 NameNode 工作，即使 ResourceManager 不工作，集群也是可访问的。

## **35。我们如何格式化 HDFS？**

♣提示:从格式化 HDFS 的命令开始尝试这个问题，然后解释这个命令的作用。

Hadoop 分布式文件系统(HDFS)可以使用***bin/Hadoop NameNode-format***命令进行格式化。该命令通过 NameNode 格式化 HDFS。该命令仅在第一次执行时执行。格式化文件系统意味着初始化由 dfs.name.dir 变量指定的目录。如果您在现有的文件系统上运行这个命令，您将丢失存储在 NameNode 上的所有数据。格式化 Namenode 不会格式化 DataNode。它将格式化 FsImage 并编辑存储在 NameNode 上的日志数据，并将丢失有关存储在 HDFS 的数据块位置的数据。通过本次[大数据课程](https://www.edureka.co/big-data-hadoop-training-certification)更好地了解 HDFS。

切勿格式化、启动和运行 Hadoop 文件系统。您将丢失存储在 HDFS 中的所有数据。

## **36。Hadoop 可以用 Windows 吗？**

Red *Hat Linux* 和 *Ubuntu* 是 Hadoop 的最佳操作系统。Windows 不经常用于安装 Hadoop，因为 Windows 附带了许多支持问题。因此，Windows 不是 Hadoop 的首选环境。

我希望这些 Hadoop 集群面试问题对你有所帮助。这只是我们 Hadoop 面试问题系列的开始。我建议您浏览整个系列，深入了解 Hadoop 面试问题。加强你的基础永远不会太晚。在使用真实用例的同时，向行业专家学习 Hadoop。

*有问题吗？请在评论区提及它们，我们将会回复您。*