# Hadoop 流:用 Python 编写 Hadoop MapReduce 程序

> 原文：<https://www.edureka.co/blog/hadoop-streaming-mapreduce-program/>

随着数字媒体、物联网以及其他发展的出现，每天生成的数字数据量呈指数级增长。这种情况给创建下一代工具和技术来存储和操作这些数据带来了挑战。这就是 Hadoop 流的用武之地！下图描绘了自 2013 年以来全球每年生成的数据的增长情况。IDC 预计，2025 年每年创建的数据量将达到 180 Zettabytes！

![data-by-2025-hadoop-streaming](img/669233d6020011e413c7a3be3327ce3d.png)

资料来源:国际数据中心

IBM 表示，每天都有近 2.5 万亿字节的数据被创建，其中 90%的数据是在过去两年中创建的！存储如此庞大的数据量是一项具有挑战性的任务。Hadoop 可以比传统的企业数据仓库更高效地处理大量结构化和非结构化数据。它将这些巨大的数据集存储在分布式计算机集群中。Hadoop Streaming 使用 MapReduce 框架，该框架可用于编写处理海量数据的应用程序。

由于 MapReduce 框架是基于 Java 的，你可能会想，如果一个开发人员没有 Java 方面的经验，他/她怎么能使用它呢？嗯，开发人员可以使用他们喜欢的语言编写 mapper/Reducer 应用程序，并且不需要太多的 Java 知识，使用 *Hadoop Streaming* 而不是切换到新的工具或技术，如 Pig 和 Hive。借助由大数据平台顶级行业专家设计的[大数据课程](https://www.edureka.co/big-data-hadoop-training-certification)，了解更多关于猪和蜂巢的知识。

## **什么是 Hadoop 串流？**

Hadoop Streaming 是 Hadoop 发行版附带的一个实用程序。可以用来执行大数据分析的程序。Hadoop 流可以使用 Python、Java、PHP、Scala、Perl、UNIX 等语言来执行。该实用程序允许我们使用任何可执行文件或脚本作为映射器和/或缩减器来创建和运行映射/缩减作业。比如:

$ HADOOP _ HOME/bin/HADOOP jar $ HADOOP _ HOME/HADOOP-streaming . jar

-输入 myInputDirs

-output myOutputDir

-映射器/箱/猫

-减速器/料仓/厕所

#### **参数描述 :**

![parameters-description-hadoop-streaming](img/ecc7cf10bbc8a4d9b10676c5f6f07cc9.png)

### **Python MapReduce 代码:**

```
mapper.py
#!/usr/bin/python
import sys
#Word Count Example
# input comes from standard input STDIN
for line in sys.stdin:
line = line.strip() #remove leading and trailing whitespaces
words = line.split() #split the line into words and returns as a list
for word in words:
#write the results to standard output STDOUT
print'%s	%s' % (word,1) #Emit the word

```

![1-python-mapreduce-code-hadoop-streaming](img/fd916ec0cdfee260b3387a6376d833b9.png)

reducer.py

```
#!/usr/bin/python
import sys
from operator import itemgetter
# using a dictionary to map words to their counts
current_word = None
current_count = 0
word = None
# input comes from STDIN
for line in sys.stdin:
line = line.strip()
word,count = line.split('	',1)
try:
count = int(count)
except ValueError:
continue
if current_word == word:
current_count += count
else:
if current_word:
print '%s	%s' % (current_word, current_count)
current_count = count
current_word = word
if current_word == word:
print '%s	%s' % (current_word,current_count)

```

![2-mapreduce-01-hadoop-streaming](img/c18a64e282f0875ea7d027fe76494f45.png)

**运行:**

1.  创建一个包含以下内容的文件，并将其命名为 word.txt.

猫老鼠狮子鹿老虎狮子大象狮子鹿

2.  将 mapper.py 和 reducer.py 脚本复制到上述文件所在的同一文件夹中。

![2-mapper-reducer-scripts-hadoop-streaming](img/6c0701d2a27a377bf793116ad613600e.png)

2.  打开终端，找到文件所在的目录。命令:ls:列出目录中的所有文件 cd:更改目录/文件夹

![3-directory-hadoop-streaming](img/f25979aeb5de011d095741e5cef74dcc.png)

4.  查看文件的内容。 命令:猫*文件名*

![4-cat-hadoop-streaming](img/1ee99986a57f8ad05fc53cdc1835a249.png)

>mapper . py 的内容

*命令:cat mapper . py*

![5-cat-mapper-hadoop-streaming](img/a991b1b53a996ae6116567e80a869d56.png)

>reducer . py 的内容

命令:cat*reducer . py*

![6-cat-reducer-hadoop-streaming](img/aee21bd7d3892e585b00f56e0ad51bb8.png)

![7-cat-reducer-hadoop-streaming](img/96fd6ad47d1525aa306c85164fe2a19c.png)

我们可以在本地文件(例如:word.txt)上运行 mapper 和 reducer。为了在 Hadoop 分布式文件系统(HDFS)上运行 Map 和 reduce，我们需要 *Hadoop Streaming jar。*所以在我们在 HDFS 上运行脚本之前，让我们在本地运行它们，以确保它们工作正常。

>运行映射器

命令:*cat word . txt | python mapper . py*

![7-python-mapper-hadoop-streaming](img/c970e877136e4a976bc84abbd5d84c3b.png)

>运行 reducer.py

命令:*cat word . txt | python mapper . py | sort-k1，1 | python reducer . py*

![8-run-reducer-hadoop-streaming](img/3846c5a36472dd64be69d57cb05118bc.png)

我们可以看到映射器和缩减器正在按预期工作，因此我们不会面临任何进一步的问题。

**在 Hadoop 上运行** **Python 代码**

在 Hadoop 上运行 MapReduce 任务之前，将本地数据(word.txt)复制到 HDFS

>举例:*HDFS DFS-put source _ directory Hadoop _ destination _ directory*

命令:*HDFS DFS-put/home/edu reka/MapReduce/word . txt**/user/edu reka*

![9-python-code-on-hadoop-streaming](img/bf0d985eb8a9a2a9ef4cc13a2b0c3d6f.png)

**复制 jar 文件的路径**

基于 jar 版本的 Hadoop Streaming jar 路径为:

*/usr/lib/Hadoop-2.2 . x/share/Hadoop/tools/lib/Hadoop-streaming-2.2 . x . jar*

因此，在您的终端上找到 Hadoop Streaming jar 并复制路径。

命令:

ls/usr/lib/Hadoop-2 . 2 . 0/share/Hadoop/tools/lib/Hadoop-streaming-2 . 2 . 0 . jar

![10-jar-hadoop-streaming](img/a2a85e44cb4626df95a0c110200ced31.png)

**运行 MapReduce 作业**

命令:

*Hadoop jar/usr/lib/Hadoop-2 . 2 . 0/share/Hadoop/tools/lib/Hadoop-streaming-2 . 2 . 0 . jar-file/home/edu reka/mapper . py-file/home/edu reka/reducer . py-reducer . py-input/user/edu reka/word-output/user/edu reka/word count*

![11-word-count-hadoop-streaming](img/d8d0cbadcf31ab28e61ccab5d65194c5.png)

![13-word-count-hadoop-streaming](img/4276d3ac2571dc5140bd4a562c58463c.png)

Hadoop 为统计和信息提供了一个基本的 web 界面。Hadoop 集群运行时，在浏览器中打开 http://localhost:50070。下面是 Hadoop web 界面的截图。

![15-hadoop-web-interface-hadoop-streaming](img/7ca694a4805a206e5a5a95419a34d6e0.png)

现在浏览文件系统，找到生成的字数统计文件，查看输出。下面是截图。

![16-word-counter-file-hadoop-streaming](img/5ecd23c91bd3cdc6a40b948c17da6706.png)

我们可以使用这个命令在终端上看到输出

命令:*Hadoop fs-cat/user/edu reka/word count/part-00000*

![17-output-hadoop-streaming](img/839091e41fe31ddce2625135a623555d.png)

您现在已经学会了如何使用 Hadoop Streaming 执行用 Python 编写的 MapReduce 程序！

*Edureka 有一个关于大数据& Hadoop 的现场和讲师指导课程，由行业从业者共同创建，以获得[大数据认证](https://www.edureka.co/blog/top-big-data-certifications)。Edureka 的[大数据硕士课程](https://www.edureka.co/masters-program/big-data-architect-training)使用零售、社交媒体、航空、旅游、金融领域的实时用例，帮助学习者成为 HDFS、Yarn、MapReduce、Pig、Hive、HBase、Oozie、Flume 和 Sqoop 领域的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*