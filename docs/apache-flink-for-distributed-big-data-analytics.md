# Apache Flink:用于流和批量数据处理的下一代大数据分析框架

> 原文：<https://www.edureka.co/blog/apache-flink-for-distributed-big-data-analytics>

Apache Flink 是一个用于分布式流和批处理数据处理的开源平台。它可以在 Windows、Mac OS 和 Linux OS 上运行。在这篇博文中，我们来讨论一下如何在本地设置 Flink 集群。它在许多方面与 Spark 相似——它拥有类似 Apache Spark 的图形和机器学习处理 APIs 但 Apache Flink 和 Apache Spark 并不完全相同。

要设置 Flink cluster，您必须在系统上安装 java 7.x 或更高版本。由于我在 CentOS ( Linux)上安装了 Hadoop-2.2.0，所以我下载了与 Hadoop 2.x 兼容的 Flink 包。

**命令:**wget[http://archive . Apache . org/dist/flink/flink-1 . 0 . 0/flink-1 . 0 . 0-bin-Hadoop 2-Scala _ 2.10 . tgz](http://archive.apache.org/dist/flink/flink-1.0.0/flink-1.0.0-bin-hadoop2-scala_2.10.tgz)

![Command-Apache-Flink](img/3b26a0fab33ae36d3bcbe456a708223f.png)

解压缩文件以获取 flink 目录。

**命令:** tar -xvf 下载/flink-1 . 0 . 0-bin-Hadoop 2-Scala _ 2.10 . tgz

**命令:** ls

![Flink-directory-Apache-Flink](img/941899c31b65c17ec79837f58a423040.png)

在中添加 Flink 环境变量。bashrc 文件。

**命令:** sudo gedit。bashrc

![Variables-Apache-Flink](img/da5cb840f471ed9846fb1102e32e8d11.png)

您需要运行下面的命令，以便。bashrc 文件被激活

**命令:**来源。bashrc

现在转到 flink 目录，在本地启动集群。

**命令:** cd flink-1.0.0

**命令:** bin/start-local.sh

一旦启动了集群，您将能够看到一个新的守护程序 JobManager 正在运行。

**命令:** jps

![Job-manager-Apache-Flink](img/f6d6844ff7bdb3afb0ff1c8888224231.png)

打开浏览器，进入 http://localhost:8081 查看 Apache Flink web UI。

![Web-UI-Apache-Flink](img/f7038f0c2403a9af6ccbd27205b3cb5e.png)

让我们使用 Apache Flink 运行一个简单的字数统计示例。

在运行示例之前，请在您的系统上安装 netcat(sudo yum install NC)。

现在在一个新的终端中运行下面的命令。

**命令:** nc -lk 9000

![Command2-Apache-Flink](img/245f31de209ea5897f79a2888adbabc1.png)

在 flink 终端中运行下面给出的命令。此命令运行一个程序，该程序将流数据作为输入，并对该流数据执行字数统计操作。

**命令:** bin/flink 运行示例/streaming/sockettextstreamwordcount . jar–主机名本地主机–端口 9000

![Streamed-data-Apache-Flink](img/baf57021fe100c7298e7cb8d42c88de5.png)

在 web ui 中，您将能够看到处于运行状态的作业。

![Running-jobs-Apache-Flink](img/26db935e254f03c83eb30af4ee90a5b4.png)

![Web-dashboard-Apache-Flink](img/f3bb8a91454f86ea9fba93e87d9dc8d0.png)

在一个新的终端中运行下面的命令，这将打印流和处理的数据。

**命令:**tail-f log/flink-*-job manager-*。在外

![Job-manager-2-Apache-Flink](img/8842f05ab8f94960150dc0511650577f.png)

现在转到启动 netcat 的终端，键入一些内容。

![Terminal-Apache-Flink](img/1f47f609bca3e5a3b523da5f1e613c1c.png)

在 netcat 终端上输入一些数据后，当您按下关键字上的 enter 按钮时，wordcount 操作将应用于该数据，输出将在毫秒内打印在此处(flink 的 jobmanager 日志)!

![Job-manager-log-Apache-Flink](img/e526b55321fa650bfc4f99d0d2e1cd6b.png)

在很短的时间内，数据将被流式传输、处理和打印。

关于 Apache Flink 还有很多需要学习的地方。在我们即将发布的博客中，我们会涉及到其他的 Flink 主题。

有问题要问我们吗？在评论区提到它们，我们会回复你。

**相关帖子:**

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop "Get started with Big Data & Hadoop")

[Apache Falcon:Hadoop 生态系统的新数据管理平台](https://www.edureka.co/blog/apache-falcon-new-data-management-platform-for-hadoop-ecoystem)