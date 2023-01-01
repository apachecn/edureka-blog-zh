# 有用的 Hadoop Shell 命令

> 原文：<https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/>

HDFS 代表“**H**adoop**D**distributed**F**ile**S**system”。HDFS 是 Apache Hadoop 项目的一个子项目。这个 Apache Software Foundation 项目旨在提供一个容错文件系统，该系统设计用于在商用硬件上运行。HDFS 是通过一组 shell 命令访问的，这将在本文中讨论。

*开始之前的简短说明:所有 Hadoop Shell 命令都是由 bin/hadoop 脚本调用的。*

## **用户命令:**

*   **运行 DFS 文件系统:**

用法:Hadoop fsck –/

[![Run-DFS-file-system (1)](img/552ac55721c10fcb9af78967fd9aaacb.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/Run-DFS-file-system-1.png)

*   Hadoop 的 C **heck 版本**:

用法:Hadoop 版本

[![Hadoop Version ](img/0fd987a6fcdbd7b1adcd84ef1c173a13.png "Hadoop Version")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/HadoopVersion-1.png)

## **FS Shell 命令:**

Hadoop fs 命令运行与 MapR 文件系统(MapR-FS)交互的通用文件系统用户客户端。

*   **查看文件列表:**

用法:hadoop fs -ls hdfs :/

[![View File Listing in Hadoop](img/70a60b2ce9b32573707b1a8ca0320190.png "View File Listing in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/ViewFileListing-1.png)

*   **检查内存状态:**

用法:hadoop fs -df hdfs :/

[![Command to check memory status](img/e4d797cd7a44c5985ee5eb1767a7dea4.png "Command to check memory status")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **指定路径和文件模式下的目录、文件和字节数:**

用法:hadoop fs -count hdfs :/

[![Command to Count Directories, Files and Bytes in specified path and file pattern](img/8587299a0ec1d28a183b99d456a9440a.png "Command to Count Directories, Files and Bytes in specified path and file pattern")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **将文件从一个位置移动到另一个位置:**

用法:-mv

[![Command to Move file from one location to another](img/9cb7b817a740ce3b58db68c641615c01.png "Command to Move file from one location to another")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **将文件从源复制到目的地**:

用法:-cp

[![Command to Copy file from source to destination](img/eae6825a9fba7b6c1463fa798749a891.png "Command to Copy file from source to destination")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **删除文件:**

用法:-RM〔t0〕

[![Command to Delete File](img/6cbd55ebb93f455766c6b9603374a67d.png "Command to Delete File")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **将文件从本地文件系统放入 Hadoop 分布式文件系统:**

用法:-put <localsrc>…</localsrc>

[![Command to Put file from the Local file system to HDFS](img/55a98203cabefc820eb5f029b6519029.png "Command to Put file from the Local file system to HDFS")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **将文件从本地复制到 HDFS:**

用法:-copyFromLocal <localsrc>…</localsrc>

[![Command to Copy file from Local to HDFS](img/fccd8f4f41ac1cf36509cfcee2fcdb6c.png "Command to Copy file from Local to HDFS")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **在 Hadoop 分布式文件系统中查看文件**:

用法:-cat

[![Command to View file in HDFS](img/3279c4bd8761ebd135189b1f52df6c44.png "Command to View file in HDFS")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

## **管理命令:**

*   **格式化 namenode** :

用法:Hadoop NameNode-格式

[![Format Namenode in Hadoop](img/4aa0969087cdf7a40016645467e50669.png "Format Namenode in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/FormatNamenode-1.png)

*   **启动辅助命名节点:**

用法:hadoop secondrynamenode

[![Command for Starting Secondary namenode](img/52648012bc4ca818a7c5ead82704a65c.png "Command for Starting Secondary namenode")](https://www.edureka.co/blog/helpful-hadoop-shell-commands-2/)

*   **运行 namenode** :

用法:hadoop namenode

[![Run Namenode in Hadoop](img/646db9c5b1d1d4baf019c98ae91f6357.png "Run Namenode in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/RunNamenode-1.png)

*   **运行** **数据节点**:

用法:hadoop datanode

[![Datanode in Hadoop](img/37461b30f90c755a5a7a3899e0fe2671.png "Datanode in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/RunDatanode-1.png)

*   **集群平衡**:

用法:hadoop 平衡器

[![Cluster Balancing in Hadoop](img/952f9ddb37814fd731d4f466b7ff2c54.png "Cluster Balancing in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/ClusterBalancing-1.png)

*   **运行 MapReduce 作业跟踪器节点:**

用法:hadoop jobtracker

[![Run MapReduce Job tracker node in Hadoop](img/963e3c0cd40400fcda095e3f4cfbf7cb.png "Run MapReduce Job tracker node in Hadoop")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/MapreduceJobTracker-1.png)

*   **运行 MapReduce 任务跟踪器节点:**

用法:hadoop tasktracker

[![Using Hadoop Task Tracker](img/be07ba79ebac23d8ae69f1c577ff86ed.png "Using Hadoop Task Tracker")](https://cdn.edureka.co/blog/wp-content/uploads/2013/12/MapreduceTaskTracker-1.png)

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)

[Hadoop 集群配置文件](https://www.edureka.co/blog/hadoop-cluster-configuration-files/)

[阿帕奇猪](https://www.edureka.co/blog/operators-in-apache-pig/)