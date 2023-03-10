# 安装 Hadoop:设置单节点 Hadoop 集群

> 原文：<https://www.edureka.co/blog/install-hadoop-single-node-hadoop-cluster>

## **安装 Hadoop:设置单节点 Hadoop 集群**

你一定对 Hadoop、HDFS 及其架构有了一个理论上的概念。但是要获得 Hadoop 认证，您需要良好的实践知识。我希望你会喜欢我们之前关于 ***[HDFS 架构](https://www.edureka.co/blog/apache-hadoop-hdfs-architecture/)*** 的博客，现在我将带你了解关于 Hadoop 和 HDFS 的实用知识。第一步是安装 Hadoop。

Hadoop 有两种安装方式，即**单节点**和**多节点**。

**单节点集群**意味着只有一个 DataNode 在一台机器上运行并设置所有的 NameNode、DataNode、ResourceManager 和 NodeManager。这是用于研究和测试的目的。例如，让我们考虑医疗保健行业内的一个样本数据集。因此，为了测试 Oozie 作业是否已经按正确的顺序调度了所有的过程，比如收集、聚合、存储和处理数据，我们使用了一个单节点集群。与包含分布在数百台机器上的万亿字节数据的大型环境相比，它可以在较小的环境中轻松高效地测试顺序工作流。

而在  **多节点集群**中，有多个 DataNode 在运行，每个 DataNode 运行在不同的机器上。多节点集群在组织中实际用于分析大数据。考虑上面的例子，当我们实时处理数 Pb 的数据时，它需要分布在数百台机器上进行处理。因此，这里我们使用一个多节点集群。

在这篇博客中，我将向您展示如何在单节点集群上安装 Hadoop。你可以从班加罗尔的 [Hadoop 管理培训中获得更好的理解。](https://www.edureka.co/hadoop-administration-training-certification-bangalore)

## **先决条件**

*   *虚拟箱*:用于安装操作系统。
*   *操作系统*:可以在基于 Linux 的操作系统上安装 Hadoop。Ubuntu 和 CentOS 是非常常用的。在本教程中，我们使用的是 CentOS。
*   *JAVA* :你需要在你的系统上安装 Java 8 包。
*   *HADOOP* :你需要 Hadoop 2.7.3 包。

## **安装 Hadoop**

### **第一步:** [点击这里](https://goo.gl/ipdJJa)下载 Java 8 包。将该文件保存在您的主目录中。

### **第二步:**提取 Java Tar 文件。

***命令*:【jdk-8u101-linux-i586.tar.gz】tar-xvf**

![Untar Java - Install Hadoop - Edureka](img/450d16cc638e6a66f7537f65694d79e5.png)

*图:Hadoop 安装——提取 Java 文件*

### **第三步:**下载 Hadoop 2.7.3 包。

***命令*:**wget https://archive . Apache . org/dist/Hadoop/core/Hadoop-2 . 7 . 3/Hadoop-2 . 7 . 3 . tar . gz

![Download Hadoop Package - Install Hadoop - Edureka](img/f1ef5357a59881167bee95f0514d97ee.png)

*图:Hadoop 安装——下载 Hadoop*

### **第四步:**提取 Hadoop tar 文件。

***命令***:tar-xvf hadoop-2.7.3.tar.gz

![Extract Hadoop Package - Install Hadoop - Edureka](img/e38c3cb0faf07086861d691c965d5e0e.png)

*图:Hadoop 安装——提取 Hadoop 文件*

### **第五步:**在 bash 文件中添加 Hadoop 和 Java 路径(。bashrc)。

打开**。** **巴沙尔**文件。现在，添加 Hadoop 和 Java 路径，如下所示。

通过 [Hadoop 认证](https://www.edureka.co/big-data-hadoop-training-certification)，了解更多关于 Hadoop 生态系统及其工具的信息。

***命令* :** 六。bashrc

![Open bash - Install Hadoop - Edureka](img/17530a25397594a3140898a87cc375f2.png)

![Add Java and Hadoop variables in bash - Install Hadoop - Edureka](img/ca9cde49b9504a16b1ee59afd346a663.png)

*图:Hadoop 安装–设置环境变量*

然后，保存 bash 文件并关闭它。

为了将所有这些更改应用到当前终端，执行 source 命令。

***命令* :** 来源。bashrc

![Apply changes to Bash - Install Hadoop - Edureka](img/5f855ca04e6940017df1fe902bf82947.png)

*图:Hadoop 安装——刷新环境变量*

为了确保 Java 和 Hadoop 已经正确安装在您的系统上，并且可以通过终端访问，e 执行 java -version 和 hadoop version 命令。

***命令*:**Java-版本

![Check Java version - Install Hadoop - Edureka](img/7dd7947e06d0e4d4d3ea02a4814574b1.png)

*图:Hadoop 安装——检查 Java 版本*

***命令* :** hadoop 版本

![Check Hadoop version - Install Hadoop - Edureka](img/ef45fd771c79e6e6779108257c42a05a.png)

*图:Hadoop 安装——检查 Hadoop 版本*

### **第六步** **:** 编辑 [**Hadoop 配置文件**](https://www.edureka.co/blog/explaining-hadoop-configuration/) 。

***命令:***CD Hadoop-2 . 7 . 3/etc/Hadoop/

***命令:*** ls

所有的 Hadoop 配置文件都位于 **hadoop-2.7.3/etc/hadoop** 目录中，如下图所示:

![Hadoop configuration files - Install Hadoop - Edureka](img/5032b2a6bc41d3ab0bff9342b069f227.png)

*图:Hadoop 安装–Hadoop 配置文件*

### **第七步** **:** 打开 *core-site.xml* ，在配置标签中编辑下面提到的属性:

*core-site.xml* 通知 Hadoop 守护进程 NameNode 在集群中运行的位置。它包含了 Hadoop 内核的配置设置，比如 HDFS & MapReduce 通用的 I/O 设置。

***命令* :** vi core-site.xml

![Editing Core-site - Install Hadoop - Edureka](img/a26563e35067934199aecb6fb26f684e.png)

![Property of core-site - Install Hadoop - Edureka](img/a3fb77e9947a43729b4aa10643d1a754.png)

*图:Hadoop 安装-配置 core-site.xml*

```
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name>fs.default.name</name>
<value>hdfs://localhost:9000</value>
</property>
</configuration>

```

### **第八步:**编辑 *hdfs-site.xml* 并编辑配置标签内的下述属性:

*hdfs-site.xml* 包含 hdfs 守护进程(即 NameNode、DataNode、辅助 NameNode)的配置设置。它还包括 HDFS 的复制因子和数据块大小。

***命令* :** vi hdfs-site.xml

![Editing Hdfs-site - Install Hadoop - Edureka](img/b876c1cf74fdd3080b8276590964aec6.png)

![Property of hdfs-site - Install Hadoop - Edureka](img/cd9e2c696b350ac397124cf6146ea9d9.png)

*图:Hadoop 安装——配置 hdfs-site.xml*

```
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name>dfs.replication</name>
<value>1</value>
</property>
<property>
<name>dfs.permission</name>
<value>false</value>
</property>
</configuration>

```

### **第九步** **:** 编辑 *mapred-site.xml* 文件，并在配置标签中编辑下面提到的属性:

*mapred-site.xml* 包含 MapReduce 应用程序的配置设置，如可以并行运行的 JVM 数量、映射器和 reducer 进程的大小、进程可用的 CPU 内核等。

在某些情况下，mapred-site.xml 文件不可用。所以，我们必须使用 mapred-site.xml 模板创建 mapred-site.xml 文件T3。

***命令*:**CP mapred-site . XML . template mapred-site . XML

***命令* :** vi 地图红色- 站点。 xml 。

![Creating mapred-site - Install Hadoop - Edureka](img/855f3d7d36a5e9da73139b80bd822156.png)

![Editing mapred-site - Install Hadoop - Edureka](img/7d087281bcf963a9d80a1b0a14c04e8a.png)

![Property of mapred-site - Install Hadoop - Edureka](img/8c3de9e391401ac49cd9efa0366a7bde.png)

*图:Hadoop 安装-配置 mapred-site.xml*

```
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name>mapreduce.framework.name</name>
<value>yarn</value>
</property>
</configuration>

```

### **第十步:**编辑 *yarn-site.xml* 并在配置标签中编辑下面提到的属性:

*yarn-site.xml* 包含 ResourceManager 和 NodeManager 的配置设置，如应用内存管理大小，程序&算法需要的操作等。

你甚至可以用海得拉巴 的 [Azure 数据工程认证查看大数据的细节。](https://www.edureka.co/microsoft-azure-data-engineering-certification-course-hyderabad-city)

***命令* :** vi yarn-site.xml

![Editing YARN-site - Install Hadoop - Edureka](img/db5cdea635a23b9d6988a64f1fc8894d.png)

![Property of YARN-site - Install Hadoop - Edureka](img/adc8d539921a2be5be90824a5fa7c449.png)

*图:Hadoop 安装-配置 yarn-site.xml*

```
<?xml version="1.0">
<configuration>
<property>
<name>yarn.nodemanager.aux-services</name>
<value>mapreduce_shuffle</value>
</property>
<property>
<name>yarn.nodemanager.auxservices.mapreduce.shuffle.class</name>
<value>org.apache.hadoop.mapred.ShuffleHandler</value>
</property>
</configuration>

```

### **第十一步:**编辑 *hadoop-env.sh* 添加 Java 路径如下:

*hadoop-env . sh*包含脚本运行 Hadoop 时使用的环境变量，如 Java home path 等。

***命令*:**VIHadoop–env。sh

![Editing Hadoop-env - Install Hadoop - Edureka](img/2b4168f1b29c39b671fc7f4841f3d8fc.png)

![Property of hadoop-env - Install Hadoop - Edureka](img/d335f3369d3a3b32a612688abdd93b96.png)

*图:Hadoop 安装——配置 hadoop-env.sh*

### **第十二步:**转到 Hadoop 主目录，格式化 NameNode。

***命令* :** cd

***命令* :** cd hadoop-2.7.3

***命令*:**bin/Hadoop NameNode-format

![Formatting NameNode - Install Hadoop - Edureka](img/720e1c615f9ac91012d56cfbecd33d1f.png)

*图:Hadoop 安装-格式化 NameNode*

这将通过 NameNode 格式化 HDFS。该命令仅在第一次执行时执行。格式化文件系统意味着初始化由 dfs.name.dir 变量指定的目录。

切勿格式化、启动和运行 Hadoop 文件系统。您将丢失存储在 HDFS 中的所有数据。

你甚至可以通过 [数据工程师培训](https://www.edureka.co/microsoft-azure-data-engineering-certification-course) 查看大数据的细节。

### **第十三步:**NameNode 格式化后，进入 hadoop-2.7.3/sbin 目录，启动所有守护进程。

***命令:*** cd hadoop-2.7.3/sbin

您可以用一个命令启动所有守护程序，也可以单独启动。

***命令:**。/*start-all . sh

以上命令是 ***start-dfs.sh，start-yarn . sh******Mr-job history-daemon . sh***的组合

或者您可以单独运行所有服务，如下所示:

### **开始命名节点:**

NameNode 是 HDFS 文件系统的核心。它保存 HDFS 中存储的所有文件的目录树，并跟踪集群中存储的所有文件。

***命令:*** 。/ hadoop-daemon.sh 启动 namenode

![Start NameNode - Install Hadoop - Edureka](img/e46ee7032f552b35c0bee8ef3fca73f2.png)

*图:Hadoop 安装-启动 NameNode*

### **启动 DataNode:**

启动时，DataNode 连接到 Namenode，并响应来自 Namenode 的不同操作请求。

***命令:*** 。/ hadoop-daemon.sh 启动 datanode

![Start DataNode - Install Hadoop - Edureka](img/43c1e45152ee03a43848c4a732095a80.png)

*图:Hadoop 安装-启动 DataNode*

### **启动资源管理器:**

ResourceManager 是仲裁所有可用集群资源的主机，因此有助于管理在 YARN 系统上运行的分布式应用程序。它的工作是管理每个节点管理器和每个应用程序的 ApplicationMaster。

***命令:*** 。/yarn -daemon.sh 启动资源管理器

![Start ResourceManager - Install Hadoop - Edureka](img/0fd1554def1b6b0eaa1ab835cdd99ea2.png)

*图:Hadoop 安装-启动资源管理器*

### **开始节点管理:**

每个机器框架中的节点管理器是负责管理容器、监控它们的资源使用并向资源管理器报告的代理。

***命令:*** 。/yarn-daemon . sh start node manager

![Start NodeManager - Install Hadoop - Edureka](img/1f0b5ad5de3e8a03e693ea326fb0c3ff.png)

*图:Hadoop 安装-启动节点管理器*

### **启动 JobHistoryServer:**

JobHistoryServer 负责处理来自客户的所有与作业历史相关的请求。

***命令* :** 。/mr-jobhistory-daemon.sh 启动 historyserver

### **第 14 步:**要检查所有的 Hadoop 服务都启动并运行，运行下面的命令。

***命令:*** jps

![Start Job history - Install Hadoop - Edureka](img/c0b68b02e8b665b5e6f2ac5a851b5fe7.png)

*图:Hadoop 安装-检查守护进程*

### **第十五步:**现在打开 Mozilla 浏览器，进入**localhost**:**50070/DFS health . html**查看 NameNode 接口。

![Hadoop NameNode UI - Install Hadoop - Edureka](img/16696397d0ba1de99ae8d1e192a514af.png)

*图:Hadoop 安装-启动 WebUI*

恭喜您，您一气呵成成功安装了单节点 Hadoop 集群。 在我们的下一篇 ***[Hadoop 教程系列](https://www.edureka.co/blog/hadoop-tutorial/)*** 的博客中，我们也将介绍如何在多节点集群上安装 Hadoop。

*现在您已经了解了如何安装 Hadoop，请查看 Edureka 的 **[Hadoop 管理课程](https://www.edureka.co/hadoop-administration-training-certification)** ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka [大数据工程师课程](https://www.edureka.co/masters-program/big-data-architect-training)使用零售、社交媒体、航空、旅游、金融领域的实时用例，帮助学习者成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 方面的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*