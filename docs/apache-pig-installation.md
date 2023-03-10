# Linux 上的 Apache Pig 安装

> 原文：<https://www.edureka.co/blog/apache-pig-installation>

在这篇文章中，我将谈论在 Linux 上安装 *Apache Pig。让我们从阿帕奇猪和猪拉丁的基本定义开始。*

*Apache Pig* 是一个工具/平台，用于创建和执行与 Hadoop 一起使用的 Map Reduce 程序。它是一个分析大量数据的工具/平台。你可以说，Apache Pig 是 MapReduce 的抽象。不太擅长 Java 的程序员过去常常在 Hadoop 上苦苦挣扎，主要是在写 MapReduce 作业的时候。所以，学习和掌握 ***[大数据 Hadoop 认证](https://www.edureka.co/big-data-and-hadoop)*** 是一个重要的课题。Apache Pig 有自己的语言 *Pig Latin* 这对贫穷的程序员来说是福音。

## **猪拉丁语基础介绍会帮助你更好的理解:**

Apache Pig 平台使用的高级过程语言叫做 *Pig Latin* 。Apache Pig 以“Pig Latin”为特色，这是一种相对简单的语言，可以在 Hadoop 文件系统(HDFS)上的分布式数据集上运行。在 Apache Pig 中，您需要使用 Pig 拉丁语编写 Pig 脚本，当您运行 Pig 脚本 时，它会被转换为 MapReduce 作业。Apache Pig 有各种操作符，用于执行读、写、处理数据等任务。要了解 Apache Pig 操作符，请访问我们的博客“**[*Apache Pig 中的操作符:第 1 部分——关系操作符*](https://www.edureka.co/blog/operators-in-apache-pig/)** ”。

现在您已经对 Apache Pig 有了基本的了解，让我们从在 Linux 上安装 Apache Pig 开始。

## **Linux 上的阿帕奇猪安装:**

下面是在 Linux (使用 Linux VM 的 ubuntu/centos/windows)上安装 Apache Pig 的步骤。我在下面的设置中使用的是 Ubuntu 16.04。

**第一步:** 下载 **Pig** **tar** 文件。

**命令:**wget http://www-us . Apache . org/dist/pig/pig-0 . 16 . 0/pig-0 . 16 . 0 . tar . gz**T5**

![Download Pig - Pig Installation - Edureka](img/bcbb5b39ad42f5fe6e04fbc8c55f4917.png)

**第二步:** 使用 tar 命令提取 **tar** 文件。在下面的 tar 命令中， **x** 表示提取一个存档文件， **z** 表示通过 gzip 过滤一个存档文件， **f** 表示一个存档文件的文件名。

**命令:【pig-0.16.0.tar.gz】tar-xzf**

**命令:** ls

![Untar Pig File - Pig Installation - Edureka](img/2d63391001924a527d7835ee35dbe968.png)

**第三步:** 编辑**。bashrc** 文件来更新 Apache Pig 的环境变量。我们正在设置它，以便我们可以从任何目录访问 pig，我们不需要转到 pig 目录来执行 pig 命令。此外，如果任何其他应用程序正在查找 Pig，它将从该文件中了解 Apache Pig 的路径。

**命令:** sudo gedit。巴沙尔

在文件末尾添加以下内容:

***#集猪 _ 首页***

***导出 PIG _ HOME =/HOME/edu reka/PIG-0 . 16 . 0******导出路径= $ PATH:/HOME/edu reka/PIG-0 . 16 . 0/bin******导出 PIG _ class PATH = $ HADOOP _ CONF _ DIR***

此外，确保也设置了 hadoop 路径。

运行以下命令，使更改在同一终端中得到更新。

**命令:**来源。巴沙尔

**第四步:** 查猪版。这是为了测试 Apache Pig 安装是否正确。万一你没有得到 Apache Pig 版本，你需要验证你是否正确地遵循了上面的步骤。

**命令:**猪头版

![Pig Version - Pig Installation - Edureka](img/94574564c1005d0fd3206828413801e3.png)

**第五步** : 检查小猪帮助查看所有小猪命令选项。

**命令:**猪帮

![Pig Help - Pig Installation - Edureka](img/133b002ec27406682d6d0e207df7cf66.png)

**第六步** : 跑猪开始咕哝壳。Grunt shell 用于运行 Pig 拉丁文脚本。

**命令:**猪

![Pig Shell - Pig Installation - Edureka](img/234186e5aba118a1d61fc38f0e14733e.png)

如果你没看错上图，Apache Pig 有两种运行模式，默认情况下它选择 MapReduce 模式。可以运行 Pig 的另一种模式是本地模式。让我告诉你更多这方面的情况。

## **阿帕奇猪中的执行模式:**

*   *MapReduce 模式*–这是默认模式，需要访问 Hadoop 集群和 HDFS 安装。由于这是默认模式，所以没有必要指定-x 标志(您可以执行 *pig* 或 *pig -x mapreduce* )。这种模式下的输入和输出出现在 HDFS 上。
*   *本地模式*–通过访问单台机器，使用本地主机和文件系统安装并运行所有文件。这里本地模式使用'-x flag' ( *pig -x local* )指定。这种模式下的输入和输出存在于本地文件系统中。

**命令:**猪 x 本地

![Pig Local Mode - Apache Pig Installation - Edureka](img/b374d9b03149b918e6153360b7a9b281.png)

你可以通过下面的视频观看 Apache Pig 在 Linux 上的安装:

**Apache Pig 安装| Linux 上的 Pig 安装| edu reka**

现在您已经完成了在 Linux 上安装 Apache Pig，下一步是在 Pig Grunt shell 上尝试一些关系 Pig 操作符。因此，下一篇博客“**[*Apache Pig 中的运算符:第 1 部分-关系运算符*](https://www.edureka.co/blog/operators-in-apache-pig/)** ”将帮助您掌握 Pig 运算符。

*现在您已经在 Linux 上安装了 Apache Pig，请查看 Edureka 的 **[Hadoop 培训](https://www.edureka.co/big-data-and-hadoop)*** *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 大数据 Hadoop 认证培训课程使用零售、社交媒体、航空、旅游和金融领域的实时用例，帮助学员成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*