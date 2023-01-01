# 2023 年前 75 个面试问题和答案

> 原文：<https://www.edureka.co/blog/interview-questions/talend-interview-questions/>

据说 Talend 是云数据集成软件的下一代领导者，目前占有 19.3%的市场份额。这意味着在不久的将来会有对拥有 [Talend 认证](https://www.edureka.co/talend-for-big-data)的专业人士的巨大需求。我认为这是抓住这个机会的好时机，让自己做好准备，在竞争中胜出。在这个关于面试问题的博客中，我挑选了 75 个最有帮助的问题，帮助你在面试中脱颖而出。我把这个 Talend 面试问题列表分成了 4 个部分:

*   [通才面试题](#General)
*   [数据整合 Talend 面试题](#DataIntegration)
*   [大数据 Talend 面试题](#BigData)
*   [选择题](#MCQ)

## **Talend 面试问答| Talend 在线培训| Talend 教程| edu reka**



[https://www.youtube.com/embed/whM2Ffs2I50?rel=0&controls=0&showinfo=0](https://www.youtube.com/embed/whM2Ffs2I50?rel=0&controls=0&showinfo=0)*This Edureka video on Talend Interview Questions will help you to learn about the most frequently asked Talend questions and their answers which will set you apart in the interview process.*

## **通用——塔伦德面试试题**

![Talend-Logo-Edureka](img/be7f268730dc1587f37d8bb84915e848.png)

1.  ### **为什么要使用 Talend 而不是市面上的其他 ETL 工具。**

    以下是 Talend 的一些优势:

     <caption>#### **Talend ETL 工具的特点**</caption> 
    | **特色** | **描述** |
    | ***更快*** | Talend 会自动执行任务，并为您进一步维护它们。 |
    | ***少花钱*** | Talend 提供可以免费下载的开源工具。此外，随着处理速度的加快，开发人员的速度也会降低。 |
    | ***未来证明*** | Talend 包含您可能需要的一切，以满足现在和未来的市场需求。 |
    | ***统一平台*** | 根据组织的需求，Talend 在产品的共同基础上满足我们的所有需求。 |
    | ***庞大的社区*** | 作为开源软件，它有一个庞大的社区作为后盾。 |

2.  ### **什么是 Talend？**

    Talend 是一个开源软件集成平台/供应商。

    *   它提供数据集成和数据管理解决方案。
    *   该公司为大数据、云存储、数据集成、数据管理、主数据管理、数据质量、数据准备和企业应用提供各种集成软件和服务。
    *   但是 Talend 的第一个产品，即用于数据集成的 Talend Open Studio，更通俗的说法是 Talend。
3.  ### **什么是 Talend Open Studio？**

    Talend Open Studio 是一个基于 Eclipse RCP 的开源项目。它支持面向 ETL 的实现，通常用于内部部署。它充当代码生成器，生成数据转换脚本和 Java 中的底层程序。它提供了一个交互式的、用户友好的 GUI，允许您访问包含在 Talend 中执行的每个过程的定义和配置的元数据存储库。

4.  ### **Talend 中的项目是什么？**

    “项目”是最高的物理结构，它捆绑并存储所有类型的业务模型、工作、元数据、例程、上下文变量或任何其他技术资源。

5.  ### **形容在塔伦德的一份工作设计。**

    作业是使用 Talend 构建的任何东西的基本可执行单元。从技术上讲，它是一个单一的 Java 类，借助图形表示定义了可用信息的工作和范围。它通过将业务需求转化为代码、例程和程序来实现数据流。

6.  ### **Talend 中的‘成分’是什么？**

    组件是用于在 Talend 中执行单一操作的功能块。在调色板上，你能看到的都是组件的图形表示。您可以通过简单的拖放来使用它们。在后端，组件是作为作业的一部分生成的 Java 代码片段(基本上是一个 Java 类)。这些 Java 代码在保存作业时由 Talend 自动编译。

7.  ### **解释 Talend 中可用的各种连接类型。**

    Talend 中的连接定义了是否必须处理数据、数据输出或作业的逻辑顺序。Talend 提供的各种连接类型有:

    1.  **行:**行连接处理实际的数据流。以下是 Talend 支持的行连接类型:
        *   主
        *   查找
        *   过滤器
        *   拒绝
        *   错误拒绝
        *   输出
        *   唯一/重复
        *   多路输入/输出
    2.  **Iterate:**Iterate 连接用于对目录中包含的文件、文件中包含的行或数据库条目执行循环。
    3.  **触发器:** 触发器连接用于创建作业或子作业之间的依赖关系，这些作业或子作业根据触发器的性质依次被触发。触发连接归纳为两类:
        1.  **子作业触发**
            *   OnSubjobOK
            *   OnSubjobError
            *   运行如果
        2.  **组件触发**
            *   OnComponentOK
            *   on component 错误
            *   运行如果
    4.  **Link:**Link 连接用于将表模式信息传递给 ELT mapper 组件。
8.  ## **Distinguish between "OnComponentOk" and "OnSubjobOk".** 

    | **OnComponentOk** | **OnSubjobOk**  |
    | 1。 It belongs to the component trigger | 1\. It belongs to sub-job trigger |
    | 2\. Only when the current component successfully completes its execution will the linked subtasks start to execute | 2\. Only when the previous sub-job completely completes its execution, the linked sub-job starts to execute |
    | 3 This link can be used for any component | 3 in job . This link can only be used for the first component |

    of subtask
9.  ### **为什么 Talend 被称为代码生成器？**

    Talend 提供了一个用户友好的图形用户界面，您可以简单地拖放组件来设计作业。当作业被执行时，Talend Studio 会在后端自动将其翻译成 Java 类。作业中的每个组件都被分成 Java 代码的三个部分(开始、主要和结束)。这就是为什么 Talend studio 被称为代码生成器。

10.  ### **Talend 支持的各种类型的模式有哪些？**

    Talend 支持的一些主要模式类型有:

    1.  **储存库模式:**该模式可以在多个作业中重用，所做的任何更改都将自动反映到使用它的所有作业中。
    2.  **通用模式:**该模式不依赖于任何特定的数据源&被用作跨多种类型数据源的共享资源。
    3.  **固定模式:**这些是只读模式，将预定义一些组件。
11.  ### **解释套路。**

    例程是可重用的 Java 代码片段。使用例程，您可以用 Java 编写自定义代码，以便优化数据处理、提高工作能力和扩展 Talend Studio 功能。

    Talend 支持两种类型的例程:

    *   **系统例程:**这些是只读代码，您可以在任何工作中直接调用。
    *   **用户程序:**这些程序可以由用户通过创建新程序或修改现有程序来自定义创建。
12.  ### **能否在 Talend 中定义运行时模式？**

    在运行时不能定义模式。由于模式定义了数据的移动，因此必须在配置组件时进行定义。

13.  ### **Distinguish between' built-in' and' repository'**

    | **There is a built-in repository** | Stored locally in job | 1\. It is stored in the repository |
    | 2\. | 2 can only be used by local jobs. |
    | 3 can be used globally by any job in the project You can easily update | 3 during the operation. The data in job is read-only |

14.  ### **什么是上下文变量，为什么在 Talend 中使用？**

    上下文变量是 Talend 使用的用户定义参数，在运行时传递给作业。随着工作从开发升级到测试和生产环境，这些变量可能会改变它们的值。上下文变量可以用三种方式定义:

    1.  嵌入的上下文变量
    2.  储存库上下文变量
    3.  外部环境变量
15.  ### **你能定义一个可以从多个作业中访问的变量吗？**

    是的，你可以通过在一个例程中声明一个静态变量来实现。然后，您需要在例程本身中为这个变量添加 setter/getter 方法。一旦完成，该变量将可从多个作业中访问。

16.  ### **什么是子作业，如何将数据从父作业传递到子作业？**

    子作业可以定义为单个组件或由*数据流*连接的多个组件。一个作业至少可以有一个子作业。要将值从父作业传递到子作业，您需要使用上下文变量。

17.  ### **定义 TOS 中‘大纲视图’的使用。**

    Talend Open Studio 中的 Outline 视图用于跟踪组件中可用的返回值。这也将包括在 tSetGlobal 组件中配置的用户定义的值。

18.  ### **解释 tMap 的成分。列出您可以使用它执行的不同功能。**

    tMap 是 Talend“加工”系列的核心组件之一。它主要用于将输入数据映射到输出数据。tMap 可以执行以下功能:

    *   添加或删除列
    *   对任何类型的字段应用转换规则
    *   使用约束条件过滤输入和输出数据
    *   拒绝数据
    *   复用和解复用数据
    *   连接并交换数据
19.  ### **Distinguish between tMap and tJoin. The second power of T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, TMAP, T14, T15, T16, T17, T18, T0t3 This is a powerful component that can handle complex situations 1\. Only the basic connection conditions 2 can be processed. You can accept multiple input links (one is the main link and the rest are search links) 2\. Only two input links (main link and search link) 3 can be accepted. There can be multiple output links 3\. There can only be two output links (main link and reject link) 4\. Support various types of connection models, such as unique connection, first connection and all connections. 4。 Only unique connections 5 are supported. Support internal connection and left external connection 5\. Only internal connections 6 are supported. You can use the filter expression to filter data 6\. You can't do this**

20.  ### **什么是调度程序？**

    调度程序是一种软件，它从队列中选择进程，并将它们加载到内存中执行。Talend 不提供内置的调度程序。

    ## **数据整合——Talend 面试题**

21.  ### **描述 ETL 过程。**

    ETL 代表提取、转换和加载。它是指将原始数据从其来源移动到数据仓库、商业智能系统或大数据平台所需的三个过程。

    *   ***提取:*** 这一步包括访问所有存储系统中的数据，如 RDBMS、Excel 文件、XML 文件、平面文件等。
    *   ***转换:*** 在这个步骤中，分析整个数据，并对其应用各种函数，以将其转换成所需的格式。
    *   ***加载:*** 在该步骤中，通过利用最少的资源，将处理后的数据，即提取和转换后的数据，加载到通常为数据库的目标数据储存库中。
22.  ### **Distinguish ETL from ELT.** 

    | **ETL** | **ELT**  |
    | 1。 First extract the data, and then convert it before loading it into the target system | 1\. First, extract the data, and then load it into the target system, where |
    | 2 will be further converted. As the amount of data increases, the processing speed slows down, because the whole ETL process needs to wait for the conversion to be completed | 2\. Processing does not depend on the data size |
    | 3\. Easy to implement | 3 A thorough understanding of tools is needed to implement |
    | 4\. No data lake support | 4 is provided. Provide data lake support |
    | 5\. Support relational data | 5\. Support unstructured data |

23.  ### **我们可以在 SFTP 连接中使用 ASCII 或二进制传输模式吗？**

    不，传输模式不能用于 SFTP 连接。SFTP 不支持任何类型的传输模式，因为它是 SSH 的扩展，并假设底层安全通道。

24.  ### **你如何在 Talend 安排工作？**

    为了在 Talend first 中安排作业，您需要将作业导出为独立程序。然后使用操作系统的本地调度工具(Windows 任务调度器、Linux、Cron 等)。)你可以安排你的工作。

25.  ### **解释 tDenormalizeSortedRow 的目的。**

    tDenormalizeSortedRow 属于组件的“处理”系列。它有助于合成排序的输入流，以节省内存。它将所有已排序的输入行组合成一个组，其中不同的值用项分隔符连接。

26.  ### **区分“插入或更新”和“更新或插入”。**

    **插入或更新:**在这个动作中，首先 Talend 试图插入一个记录，但是如果一个具有匹配主键的记录已经存在，那么它就更新那个记录。

    **更新或插入:**在这个动作中，Talend 首先尝试用匹配的主键更新一个记录，但是如果没有匹配的主键，则插入该记录。

27.  ### **解释 tContextLoad 的用法。**

    tContextLoad 属于“杂项”系列组件。该组件有助于动态修改活动上下文的值。基本上，它用于从流中加载上下文。如果在输入中定义的参数没有在上下文中定义，并且如果上下文没有在传入数据中初始化，它将发出警告。

28.  ### **讨论 XMX 和 XMS 参数的区别。**

    XMS 参数用于指定 Java 中的初始堆大小，而 XMX 参数用于指定 Java 中的最大堆大小。

29.  ### **Talend 中的表达式编辑器有什么用？**

    从表达式编辑器中，所有的表达式，如输入、变量或输出，以及约束语句都可以方便地查看和编辑。表达式编辑器带有一个专用视图，用于编写任何函数或转换。数据转换所需的必要表达式可以直接在 **表达式编辑器** 中编写，或者您也可以打开 **表达式生成器** 对话框，您可以在其中编写数据转换表达式。

30.  ### **解释 Talend 中的错误处理。**

    有几种方法可以处理 Talend 中的错误:

    *   对于简单的任务，可以依赖 Talend Open Studio 的*异常抛出*过程，它在运行视图中显示为红色堆栈跟踪。
    *   每个子任务和组件必须返回一个代码，该代码导致额外的处理。子任务正常/错误和组件正常/错误链接可用于将错误导向错误处理程序。
    *   处理错误的基本方法是定义一个错误处理子作业，每当出现错误时，该子作业都应执行。
31.  ### **Distinguish the usage of tJava, tJavaRow and tJavaFlex components.**

    [TT At the beginning of subtask T57, execute T58, T59 and T60 only once: yes, t61, t62, t63, t64, no, t65, t66, t67, t68, no, t69, t70 Need to input flow Required output flow The first component Can be used as different sub-jobs The main process or iterator process There are three parts of Java code Data

    | **Functions** | **Tjava** T3]  **tJavaRow** | **tJavaFlex**  |
    | 1。 Java code | that can be used for integration customization is | is | is |
    | No | Yes | No | No | Only when the output mode is defined | Only when the output mode is defined | that can be used for work is | No | is | Yes | No | Yes | is allowed to have two pairs | . Only the main process | has two pairs | No | No | Yes | No | No | Yes |

32.  ### **你怎样才能远程执行一个 Talend 作业？**

    您可以从命令行远程执行 Talend 作业。您需要做的就是，导出作业及其依赖项，然后从终端访问它的指令文件。

33.  ### **在加载数据之前，可以从输入文件中排除页眉和页脚吗？**

    是的，在从输入文件加载数据之前，可以很容易地排除页眉和页脚。

34.  ### **解释解决‘堆空间问题’的过程。**

    当 JVM 试图向堆空间区域添加比可用空间更多的数据时，就会出现“堆空间问题”。要解决这个问题，您需要修改分配给 Talend Studio 的内存。然后你要修改相关的工作室。ini 配置文件，根据您的系统和需要。

35.  ### **‘tXMLMap’组件的用途是什么？**

    该组件将来自一个或多个来源的数据转换并路由到一个或多个目的地。它是一个高级组件，专为转换和路由 XML 数据流而设计。尤其是当我们需要处理大量 XML 数据源时。

    ## **大数据——Talend 面试问题**

36.  ### **区分数据集成的 TOS 和大数据的 TOS。**

    Talend Open Studio for Big Data 是 Talend 用于数据集成的超集。它包含 TOS 为 DI 提供的所有功能，以及一些附加功能，如支持大数据技术。也就是说，用于 DI 的 TOS 只生成 Java 代码，而用于 BD 的 TOS 生成 MapReduce 代码和 Java 代码。

37.  ### **Talend 支持的各种大数据技术有哪些？**

    在面向 BD 的 TOS 中，大数据家族非常庞大，最常用的技术很少:

    *   卡桑德拉
    *   CouchDB
    *   谷歌存储
    *   HBase
    *   HDFS
    *   鼠标
    *   映射关系数据库
    *   MongoDB
    *   猪
    *   Sqoop 等。
38.  ### **如何在 Talend 内并行运行多个作业？**

    由于 Talend 是一个 java 代码生成器，所以可以执行多线程中的各种作业和子作业，以减少作业的运行时间。基本上，在 Talend 数据集成中有三种并行执行的方式:

    1.  *多线程*
    2.  *t 平行分量*
    3.  *自动并列*
39.  ## **连接到 HDFS 需要哪些强制配置？**

    为了连接到 HDFS，您必须提供以下详细信息:

    *   分布
    *   NameNode URI
    *   用户名
40.  ### **在 Talend Studio 和 HBase 之间协调事务时，哪项服务是必需的？**

    Zookeeper 服务对于协调 TOS 和 HBase 之间的事务是强制性的。

41.  ### **用于 Pig 脚本的语言叫什么名字？**

    Pig 拉丁语用于 Pig 中的脚本编写。

42.  ### **什么时候使用 tKafkaCreateTopic 组件？**

    这个组件创建一个 Kafka 主题，其他 Kafka 组件也可以使用这个主题。它允许您可视化地生成命令，以在主题级别创建具有各种属性的主题。

43.  ### **解释 tPigLoad 组件的用途。**

    一旦数据通过验证，这个组件就可以在一个事务中将原始输入数据加载到输出流中。它为当前事务建立到数据源的连接。

44.  ### **主作业一执行完就自动关闭一个 Hive 连接，需要用什么组件 **？****

    使用 tPostJob 和 tHiveClose 组件，您可以自动关闭配置单元连接。

    ## **MCQ–塔伦德面试问题**

45.  ### **In Talend Studio, where can I find the components needed to create jobs?** 

    1.  储存库

    2.  运行视图

    3.  设计师工作区

    4.  调色板【年】
46.  ### **In the component view, where can you change the name of the component?** 

    1.  基础设置
    2.  高级设置
    3.  文档
    4.  视图【年】
47.  ### **HDFS components can only be used for big data batch or big data stream jobs.** 

    1.  真
    2.  假〔岁〕t1]
48.  ## **In which perspective of Talend Studio can the contents of Hive table be analyzed?** 

    1.  剖析【Ans】
    2.  整合
    3.  大数据
    4.  调解
49.  ### **In the design workspace, what does the asterisk next to the work order name mean?** 

    1.  这是一个活动工单
    2.  作业包含未保存的更改【Ans】
    3.  作业当前正在运行
    4.  作业包含错误
50.  ### **Suppose you design a large data batch with MapReduce framework. Now you want to use Map Reduce to execute it on the cluster. In the Hadoop configuration tab of the run view, which configurations are mandatory?** 

    1.  名称节点[Ans]
    2.  数据节点
    3.  资源经理
    4.  工作追踪系统【Ans】
51.  ### **How to find the configuration error information of components?**

    1.  右击组件并选择“显示问题”
    2.  将鼠标悬停在设计器视图中的错误符号上【Ans】
    3.  打开错误视图
    4.  打开作业视图
52.  ### **What is the process of connecting two input columns in the tMap configuration window?**

    1.  将主输入表中的一列拖动到另一个输入表中的一列【Ans】
    2.  右击输入表中的一列，选择“连接”
    3.  在两个不同的输入表中选择两列，右键单击，然后选择“连接”
    4.  在两个不同的输入表中选择两列，并将它们拖到输出表中
53.  ### **To import a file from FTP, which of the following components are required?**

    1.  tFTPConnection，tFTPPut
    2.  tFTPConnection，tFTPFileList，tFTPGet
    3.  tFTPConnection，tFTPGet [Ans]
    4.  tFTPConnection，tFTPExists，tFTPGet
54.  ### **Suppose y** **You have three tasks, of which task 1 and task 2 are executed in parallel. Job 3 will not be executed until Job 1 and Job 2 are finished. Which of the following components can be used to set up this feature?**

    1.  突尼斯
    2.  tPostJob [Ans]
    3.  tRunJob
    4.  tparal alize[ans]
55.  ### **What is the default field delimiter parameter for tFileInputDelimited component?** 

    1.  半结肠〔ans〕t1〕
    2.  管道
    3.  逗号
    4.  冒号
56.  ### **When saving changes to tMap configuration, sometimes Talend will ask you to confirm to propagate the changes. Why?** 

    1.  因为您的更改会影响输出模式，并且源组件应该有一个匹配的模式
    2.  因为你的更改影响了输出模式，目标组件应该有一个匹配的模式【Ans】
    3.  因为您的更改影响了一个输入模式，并且相关的源组件应该有一个匹配的模式
    4.  因为您的修改还没有保存
57.  ### **In Talend, how do you add shapes to the business model?** 

    1.  从调色板中点击放置
    2.  从存储库中拖动它
    3.  点击快速访问工具栏中的
    4.  从调色板中拖放【Ans】
58.  ### **How to create a line link between two components?**

    1.  将目标组件拖到源组件上
    2.  右击源组件，然后点击目标组件
    3.  将源组件拖到目标组件上
    4.  右键单击源组件，单击行，后跟行类型，然后单击目标组件【Ans】
59.  ### **Talend Open Studio generates job documents in which of the following formats?** 

    1.  HTML [Ans]
    2.  正文
    3.  CSV
    4.  XML
60.  ### **We can modify the generated code directly in Talend.** 

    1.  真
    2.  假〔岁〕t1]
61.  ### **What is the default date mode in Talend Open Studio?**

    1.  MM-DD-YY
    2.  DD-MM-YY [Ans]
    3.  DD-MM-YYYY
    4.  YY-MM-DD
62.  ### **MDM 代表**

    1.  元数据管理
    2.  移动设备管理
    3.  主数据管理【Ans】
    4.  模拟数据管理
63.  ### **In order to encapsulate the collected log data and deliver it to the output, which components must be used together with tLogCatcher?**

    1.  twan[岁]
    2.  这是【年】
    3.  状态捕获器
    4.  捕手
64.  ### **Which component do you need to use in order to read data line by line from the input stream and store data entries in the iterative global variables?**

    1.  tIterateToFlow
    2.  tFileList
    3.  tft low terate[ans]
    4.  tLoop
65.  ### **tMemorizeRows 属于塔伦德中的哪个组件族？**

    1.  杂项【年】t1]
    2.  编排
    3.  互联网
    4.  文件
66.  ### **_ _ _ _ _ _ _ _ _ is a powerful input component that can replace many other components in the file family.**

    1.  tfileinput ldif
    2.  tFileInputRegex【Ans】
    3.  tFileInputExcel
    4.  tFileInputJSON
67.  ### **Which component do you need to prevent unnecessary commit in MySQL database?**

    1.  tMysqlRollback [Ans]
    2.  tMysqlCommit
    3.  tMysqlLookupInput
    4.  tmysqllow
68.  ## **The database connection defined in the repository can be reused by any job in the project.**

    1.  真[岁]
    2.  假
69.  ### Which component can be used to integrate the personalized pig code with the [ Talend T5] program?

    1.  tPigCross
    2.  tPigMap
    3.  tPigDistinct
    4.  tPigCode [Ans]
70.  ### **What kind of data type of message is received by TkafKaOutput component?**

    1.  字节
    2.  字节[【ans]
    3.  字符串[]
    4.  整数
71.  ### **Which two component families do the THDFS Properties component belong to?**

    1.  大数据和杂项
    2.  流程编排和大数据
    3.  文件和大数据【Ans】
    4.  大数据和互联网
72.  ### **This component is used to read data from the cache for high-speed data access**

    1.  tHashInput [Ans]
    2.  tfileinput ldif
    3.  tHDFSInput
    4.  tfileinput XML
73.  ### **Which component can be used to calculate the processing time of one or more subtasks in the main task?**

    1.  t 流量计
    2.  tChronometerStart【Ans】

    3.  tflowmetercacher

    4.  状态捕获器
74.  ### **Which two families do tremolite components belong to?**

    1.  文件和处理
    2.  杂项和信息
    3.  流程编排和消息传递
    4.  编排和处理【Ans】
75.  ### **How many parts of Java code can you add to your work with tjavaFlex?**

    1.  一个
    2.  两个
    3.  三个【答案】
    4.  四个

This brings us to the end of this blog on Talend interview questions. I hope it was informative. To learn more about Talend you can refer to my [**Talend Tutorial **](https://www.edureka.co/blog/talend-tutorial-data-integration/)blogs.*If you found this Talend interview questions **blog, relevant, **check out the Talend for DI and Big Data Certification Training**by Edureka, a trusted online learning company with a network of more than 250,000 satisfied learners spread across the globe. The Edureka Talend for DI and Big Data Certification Training course helps you to master Talend and Big Data Integration Platform and easily integrate all your data with your Data Warehouse and Applications, or synchronize data between systems.**Got a question for us? Please mention it in the comments section and we will get back to you.*