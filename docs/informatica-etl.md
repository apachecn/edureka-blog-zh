# Informatica ETL:使用 Informatica PowerCenter 理解 ETL 的初学者指南

> 原文：<https://www.edureka.co/blog/informatica-etl/>

Informatica ETL 的目的不仅是为用户提供一个从源系统中提取数据并将其放入数据仓库的过程，还为用户提供一个公共平台来集成来自不同平台和应用程序的数据。这导致了对 ***[持证信息专业](https://www.edureka.co/informatica)*** 的需求增加。在讲 Informatica ETL 之前，我们先来了解一下为什么需要 ETL。

## **我们为什么需要 ETL？**

如今，每家公司 都不得不 处理来自不同来源的大量数据。需要对这些数据进行处理，以便为制定业务决策提供有见地的信息。但是，此类数据通常面临以下挑战:

*   大公司会产生大量的数据，如此庞大的数据块可以是任何格式。它们将在多个数据库和许多非结构化文件中可用。
*   这些数据必须被整理、组合、比较，并作为一个无缝的整体工作。但是不同的数据库不能很好地通信！
*   许多组织已经实现了这些数据库之间的接口，但是他们面临以下挑战:
    *   每对数据库都需要一个独特的接口。
    *   如果您更改一个数据库，许多接口可能需要升级。

下面你可以看到一个组织的各种数据库及其交互:

![Various Dataset of an Organisation - Informatica - ETL - Edureka](img/c4664e2c4a03a83adf073cd5f5eef38c.png)

   Various Databases used by different departments of an organization



![Different Interface Between the Databases - Informatica - ETL - Edureka](img/207784fec34a7e5a6b9929d8ded263a6.png)

                                Different Interactions of the Databases in an Organisation



如上所述，一个组织的不同部门可能有不同的数据库，它们之间的交互变得难以实现，因为必须为它们创建不同的交互界面。为了克服这些挑战，最好的解决方案是使用数据集成的概念，这将允许来自不同数据库和格式的数据相互通信。下图有助于我们理解数据集成工具是如何成为各种数据库之间通信的通用接口的。

![Data Integration-Informatica ETL-Edureka](img/02db822716136677ab680da849c275ac.png)

              Various Databases connected via Data Integration



但是有不同的流程可以执行数据集成。在这些过程中，ETL 是最优、高效和可靠的过程。通过 ETL，用户不仅可以从各种来源获取数据，还可以在将数据存储到最终目标之前对数据执行各种操作。

在市场上各种可用的 ETL 工具中，Informatica PowerCenter 是市场上领先的数据集成平台。经过对近 500，000 种平台和应用组合的测试，Informatica PowerCenter inter 可以在尽可能广泛的不同标准、系统和应用上运行。现在让我们理解 Informatica ETL 过程中涉及的步骤。

## **计算机 ETL |计算机架构|计算机动力中心教程| Edureka**

*本 Edureka Informatica 教程帮助您详细了解使用 Informatica Powercenter 进行 ETL 的基础知识。*

## **Informatica ETL 过程中的步骤:**

在我们进入 Informatica ETL 所涉及的各个步骤之前，让我们对 ETL 有一个概述。在 ETL 中，提取是指从同构或异构数据源中提取数据，转换是指将数据转换为适当的格式或结构进行存储，以便进行查询和分析，加载是指将数据加载到最终的目标数据库、运营数据存储、数据集市或数据仓库中。下图将帮助你理解 Informatica ETL 过程是如何发生的。

![ETL Process - Informatica - ETL - Edureka](img/bc9a6b21578bccda45d63eca1711c884.png)

                                                                   ETL Process Overview



如上所述，Informatica PowerCenter 可以从各种来源加载数据，并将它们存储到一个数据仓库中。现在，让我们看看 Informatica ETL 过程中涉及的步骤。

Informatica ETL 过程主要有 4 个步骤，现在让我们深入了解一下:

1.  提取或捕获
2.  擦洗或清洁
3.  变换
4.  负载和索引

**1。提取或捕获:** 如下图所示，捕获或提取是 Informatica ETL 过程的第一步。 它是从数据源获取所选数据子集的快照的过程，这些数据必须加载到数据仓库中。快照是数据库中数据的只读静态视图。提取过程可以有两种类型:

*   **完全提取:**从源系统中完全提取数据，无需跟踪自上次成功提取以来数据源的变化。
*   **增量提取:**这将仅捕获自上次完全提取以来发生的更改。

![ETL Step-1 Extract -Informatica ETL-Edureka](img/9e0a72625f2252291d962ec697812ca1.png)

                                  Phase 1: Extract or Capture



**2。擦洗或清理:**这是通过使用各种模式识别和人工智能技术来清理来自数据源的数据的过程，以提升数据的质量。通常，拼写错误、日期错误、字段使用错误、地址不匹配、数据缺失、数据重复、不一致等错误会被突出显示，然后在此步骤中被纠正或删除。此外，解码、重新格式化、时间戳、转换、密钥生成、合并、错误检测/记录、定位丢失数据等操作也在此步骤中完成。如下图所示，这是 Informatica ETL 过程的第二步。

![ETL Step-2 Scrub - Informatica ETL-Edureka](img/57491e98f2be22c3a2b3aa41fa838e46.png)

                              Phase 2: Scrubbing or Cleaning of data



**3。转换:**如下图所示，这是 Informatica ETL 过程的第三步，也是最重要的一步。转换是将数据从源系统格式转换到数据仓库框架的操作。一个转换基本上是用来表示一组规则的，这些规则定义了数据流以及数据是如何加载到目标中的。要了解更多关于转换的信息，请查看 Informatica 博客中的[转换。](https://www.edureka.co/blog/informatica-transformations/)

![ETL Step-3 Transform - Informatica ETL-Edureka](img/f0e7c17d801ed4539c9701fe202ecab0.png)

                                  Phase 3: Transformation



**4。加载和索引:**这是 Informatica ETL 过程的最后一步，如下图所示。在这个阶段，我们将转换后的数据放入仓库，并为数据创建索引。根据加载过程，有两种主要类型的数据加载可用。:

*   **满载或批量装载** : 我们第一次做的时候的数据装载过程。该作业从源表中提取全部数据，并在应用所需的转换后加载到目标数据仓库中。这将是一个一次性的作业运行，之后将单独捕获更改，作为增量提取的一部分。
*   **增量加载或刷新加载** **:** 修改后的数据会在目标中单独更新，然后再满负荷。通过将创建或修改日期与作业的上次运行日期进行比较，可以捕获这些更改。 修改后的数据单独从源中提取，并将在目标中更新而不影响现有数据。

![ETL Step-4 Load and Index - Informatica ETL - Edureka](img/dbe128a1fd1574a23f2e5301f9d6eafb.png)

                                    Phase 4: Load and Index



如果你已经理解了 Informatica ETL 过程，我们现在就能更好地理解为什么 Informatica 是这种情况下的最佳解决方案。

## 信息 ETL 的特点:

对于所有的数据集成和 ETL 操作，Informatica 为我们提供了 *Informatica PowerCenter* 。现在让我们看看 Informatica ETL 的一些关键特性:

*   提供用图形用户界面指定大量转换规则的功能。
*   生成程序转换数据。
*   处理多个数据源。
*   支持数据提取、清理、聚合、重组、转换和加载操作。
*   自动生成数据提取程序。
*   目标数据仓库的高速加载。

以下是使用 Informatica PowerCenter 的一些典型场景:

1.  **数据迁移:**

一家公司为其会计部门购买了一个新的应付账款应用程序。PowerCenter 可以将现有的帐户数据移动到新的应用程序中。下图将帮助您了解如何使用 Informatica PowerCenter 进行数据迁移。在数据迁移过程中，Informatica PowerCenter 可以轻松地为税务、会计和其他法定目的保留数据血统。

![Data Migration - Informatica - ETL - Edureka](img/112f97ec2d9fcfa58cda36a98d2f5981.png)

 Data Migration from an Older Accounting application to a new Application



2.  **应用集成:**

假设 A 公司收购了 B 公司。因此，为了获得整合的好处，B 公司的计费系统必须集成到 A 公司的计费系统中，这可以使用 Informatica PowerCenter 轻松完成。下图将帮助您了解如何使用 Informatica PowerCenter 来整合公司之间的应用程序。

![Application Integration - Informatica - ETL - Edureka](img/f051338ccd2b8fe0d211e98f6ed53061.png)

                  Integrating Application between Companies



3.  **数据入库**

数据仓库中需要的典型动作有:

*   将许多来源的信息结合在一起进行分析。
*   将数据从多个数据库转移到数据仓库。

使用 Informatica PowerCenter 可以轻松完成上述所有典型案例。在下面，你可以看到 Informatica PowerCenter 被用来合并来自各种数据库的数据，如 Oracle、SalesForce 等。并将其带到由 Informatica PowerCenter 创建的公共数据仓库中。

![Data Warehouse - Informatica - ETL - Edureka](img/9a3a1227b72c4f2d7dcbb5c43c439d41.png)

            Data From various databases integrated to a common Data warehouse



4.  **中间件**

假设一家零售组织将 SAP R3 用于其零售应用，将 SAP BW 用作其数据仓库。由于缺少通信接口，这两个应用程序之间的直接通信是不可能的。但是，Informatica PowerCenter 可以用作这两个应用程序之间的中间件。在下图中，您可以看到 Informatica PowerCenter 如何被用作 SAP R/3 和 SAP BW 之间的中间件。来自 SAP R/3 的应用程序将其数据传输到 ABAP 框架，然后该框架将数据传输到 SAP 销售点(POS)和 SAP 服务账单(BOS)。Informatica PowerCenter 帮助将数据从这些服务转移到 SAP Business Warehouse (BW)。

![SAP retail architecture-Informatica ETL-Edureka](img/6e469562b633b64a6d1f95f2fb100154.png)

Informatica PowerCenter 作为 SAP 零售架构中的中间件

虽然您已经看到了 Informatica ETL 的一些关键特性和典型场景，但我希望您理解为什么 Informatica PowerCenter 是 ETL 过程的最佳工具。现在让我们看一个 Informatica ETL 的用例。

## **用例:连接两个表得到一个单独的明细表**

假设您希望为员工提供部门交通工具，因为这些部门位于不同的地点。要做到这一点，首先你需要知道每个雇员属于哪个部门以及该部门的位置。但是，雇员的详细信息存储在不同的表中，您需要将部门的详细信息与所有雇员的详细信息一起加入到现有的数据库中。为此，我们首先将两个表加载到 Informatica PowerCenter，对数据执行源限定符转换，最后将细节加载到目标数据库。让我们开始吧:

**第一步** **:** 打开 PowerCenter Designer。

![Launching Designer - Informatica - ETL - Edureka](img/191261070e2a6ebfb88d4cf209b64f31.png)

下面是 Informatica PowerCenter Designer 的主页。

![Designer Hompage - Informatica - ETL - Edureka](img/883cd00c32104ea9aa5e140c33de943a.png)

现在让我们连接到存储库。如果你还没有配置你的库或者面临任何问题，你可以查看我们的 [Informatica 安装](https://www.edureka.co/blog/informatica-installation/)博客。

**第二步:**右键单击您的存储库并选择连接选项。

![Connect to Repository - Informatica - ETL - Edureka](img/1fd39fa21b7bf04fe69582f2818bc063.png)

点击“连接”选项，会出现以下屏幕提示，要求输入您的存储库用户名和密码。

![Connecting to Repository - Informatica - ETL - Edureka](img/1875e27442b672e40acfac114ade7138.png)

一旦你连接到你的存储库，你必须打开你的工作文件夹，如下所示:

![Working Folder - Informatica - ETL - Edureka](img/141ece85ecabdef9dbc49af442caa066.png)

将会提示您询问映射的名称。指定映射的名称，然后单击 OK(我将其命名为 **m-EMPLOYEE** )。

![Mapping Name - Informatica - ETL - Edureka](img/6ac717100cdc1b8fdbb8726f437e12ce.png)

**步骤 3:** 现在让我们从数据库中加载表，首先连接到数据库。为此，选择 Sources 选项卡并从数据库导入选项，如下所示:

![Selecting source-Informatica ETL-Edureka](img/475d12bc7bd7e8c3aec94b27fcec18dc.png)

点击从数据库导入，会出现如下屏幕提示，询问您数据库的详细信息及其连接的用户名和密码(我使用的是 oracle 数据库和 HR 用户)。

![Source Database Details-Informatica ETL-Edureka](img/f40a84a6ddddd586936a59d054863a2e.png)

点击连接，连接到您的数据库。

![Connecting to Source Database-Informatica ETL-Edureka](img/9c3130ec816b7b103893cac40426cc2e.png)

**第四步:**由于我希望加入**雇员**和**部门**表，我将选择它们并单击确定。 ![Datasets - Informatica - ETL - Edureka](img/1d1835a03973d65cb37800eeac28ba84.png) 源代码将在您的 mapping designer 工作区中可见，如下所示。

![Source Mapping-Informatica ETL-Edureka](img/960fa4f933d428fe16c65a520819e459.png)

**第五步:**同理加载目标表到映射。

![Source Target Mapping-Informatica ETL-Edureka](img/c4bb9544c2acf495d9ce9e0a07dfc10c.png)

**步骤 6:** 现在让我们链接源限定符和目标表。右击工作区的任意空白处，选择自动链接，如下图:

![Autolink - Informatica ETL - Edureka](img/e7244d44ed744572a944057a02f3a633.png)

下面是 Autolink 链接的映射。

![Linked Mapping-Informatica ETL-Edureka](img/4f5eb96f98ec699b992940d6226028e0.png)

**第 7 步:**因为我们需要将两个表都链接到源限定符，所以选择 Department 表的列，并将其放在源限定符中，如下所示:

![Selecting Colums from Source -Informatica ETL-Edureka](img/00f5799cfb899183db51a94d121eb1d4.png)

将列值放到源限定符 **SQ_EMPLOYEES** 中。

![Droping Colums to Source Qualifier - Informatica ETL - Edureka](img/6b922af4da26d26702c206bad99c66e9.png)

下面是更新后的源限定词。

![Updated Mapping - Informatica ETL - Edureka](img/451b6e7d3dd0d388775744363c70d26d.png)

**步骤 8:** 双击源限定符来编辑转换。

![Editing Source Qualifier - Informatica ETL - Edureka](img/a8f5fcc196cea62943a70165d799f4fe.png)

你将得到如下所示的编辑转换弹出窗口。单击属性选项卡。

![Edit Source Transformations - Informatica ETL - Edureka](img/16a35178a904df3ced79d512be3a81d7.png)

**第 9 步:**在 Properties 选项卡下，点击用户定义连接行 的 Value 字段。

![Source Qualifier Properties - Informatica ETL - Edureka](img/064763209ed594671615139a1aa3f1a1.png)

您将得到下面的 SQL 编辑器:

![SQL Editor - Informatica ETL - Edureka](img/31489ff097a99063178336187f6de70c.png)

**第十步:**输入**员工。部门标识=部门。DEPARTMENT_ID** 作为 SQL 字段中连接两个表的条件，并单击 OK。

![User Join Condition - Informatica ETL - Edureka](img/4909f89eb780860113fb5a01a54c67ca.png)

**步骤 11:** 现在点击 SQL 查询行，生成用于连接的 SQL，如下所示:

![SQL Query Option - Informatica ETL - Edureka](img/943288c598caece9d2b267ce43dfa157.png)

你将得到下面的 SQL 编辑器，点击生成 SQL 选项。

![Genetating SQL - Informatica ETL - Edureka](img/75e7c118632dfaf671005223e19f30be.png)

下面的 SQL 将根据我们在上一步中指定的条件生成。点击确定。

![User Defined Join SQL - Informatica ETL - Edureka](img/27eea01d9479faf1a1393821f40d0d0d.png)

**第十二步:**点击应用，确定。

![Updating Source Qualifier - Informatica ETL-Edureka](img/0687729595df997da6beb02de59c16de.png)

下面是完成的贴图。

![Updated Source Qualifier Mapping - Informatica ETL - Edureka](img/451b6e7d3dd0d388775744363c70d26d.png)

我们已经完成了如何将数据从源传输到目标的设计。然而，实际的数据传输仍未发生，为此我们需要使用 PowerCenter 工作流设计。工作流的执行将导致数据从源传输到目标。要了解更多关于工作流的信息，请查看我们的[信息教程:工作流](https://www.edureka.co/blog/informatica-tutorial)博客

**步骤 13:** L et 我们现在通过点击 W 图标启动工作流管理器，如下图所示:

![Launching Workflow - Informatica ETL - Edureka](img/23dc425c348266bb5b8abc4e6bc56c2d.png)

下面是工作流设计器的主页。

![Workflow Manager Hompage - Informatica ETL - Edureka](img/4000d206e0a190232267d2a25c757f5a.png)

**步骤 14:** 现在让我们为我们的映射创建一个新的工作流。单击工作流选项卡并选择创建选项。

![Creating Workflow - Informatica ETL - Edureka](img/ce03ce0339fbf2fd1819336e24d5b62a.png)

您将看到下面的弹出窗口。指定工作流的名称，然后单击“确定”。

![Workflow Naming - Informatica ETL - Edureka](img/2e6dcc1dd71ff3271a8a677f91a79eb7.png)

**第 15 步**:一旦创建了一个工作流，我们就会在 Workflow Manager 工作区中看到开始图标。

![Start Icon - Informatica ETL - Edureka](img/037f2b7beaea2747706c9573bd85fbda.png)

现在，让我们点击会话图标并点击工作区，向工作区添加一个新会话，如下图所示:

![Creating Session - Informatica ETL - Edureka](img/1118bcc637115febba30246045462780.png)

点击工作区以放置会话图标。

![Adding Session Icon - Informatica ETL-Edureka](img/90f50d8204dc2aa2933bfd1b964d9271.png)

**步骤 16:** 添加会话时，您必须选择您在上述步骤中创建并保存的映射。(我已经保存为 m-EMPLOYEE)。

![Selecting Mapping - Informatica ETL - Edureka](img/8ea43b3805a3876a71999fe22c5c93c3.png)

下图是添加会话图标后的工作区。

![Updated Workflow - Informatica ETL - Edureka](img/048a97f3e085256d5ebcb864df701c93.png)

**步骤 17** :现在您已经创建了一个新的会话，我们需要将它链接到开始任务。我们可以通过点击链接任务图标来完成，如下图所示:

![Adding Link - Informatica ETL - Edureka](img/f3d3a0a0be01388f322f21cbd659a372.png)

首先点击开始图标，然后点击会话图标建立链接。

![Linking Icon - Informatica etl - Edureka](img/fd47e21fba316e7fadd73e7dcad60490.png)

下面是一个连接的工作流程。

![Linked Workflow - informatica etl - edureka](img/a66a45c4fa4cdeda7acc7df4f6dd65a5.png)

**第 18 步:**现在我们已经完成了设计，让我们开始工作流程。单击工作流选项卡，并选择启动工作流选项。

![Starting Workflow - Informatica ETL - Edureka](img/f0a9c724b0ab8a58d1c5d29c82b05401.png)

工作流管理器启动工作流监控程序。

![Launching Workflow Moniter - Informatica ETL - Edureka](img/75c9c3b419f1ade09c17f1cd07d2232d.png)

**第 19 步**:一旦我们开始工作流，工作流管理器自动启动，允许您监控工作流的执行。下面你可以看到工作流监视器显示了你的工作流的状态。

![Workflow Moniter - Informatica ETL - Edureka](img/47cb0b9d7ac31e2b049461fb763a6597.png)

**步骤 20:** 要检查工作流的状态，右键单击工作流并选择获取运行属性，如下所示:

![Getting Run Properties - Informatica - ETL - Edureka](img/4ac2cb4c4899441e93b1f3e92e2b1c02.png)

选择源/目标统计选项卡。

![Source Target Statistics - Informatica ETL - Edureka](img/02a9574049bcfaf9ef345550f2c5a415.png)

下面您可以看到转换后在源和目标之间传输的行数。

![Source Target Properties - Informatica - ETL - Edureka](img/3c8b8ed6a3006dee540cd6ec2bdc65c8.png)

您也可以通过检查目标表来验证您的结果，如下所示。

![Target Database - Informatica - ETL - Edureka](img/328b58c0398bfdad0ddf3a580128eaa0.png)

我希望这篇 Informatica ETL 博客有助于您理解使用 Informatica 进行 ETL 的概念，并激发您学习更多 Informatica 知识的兴趣。

如果你觉得这个博客很有帮助，你也可以看看我们的 Informatica 教程博客系列[什么是 Informatica:Informatica PowerCenter 的初学者教程](https://www.edureka.co/blog/what-is-informatica/)、 [Informatica 教程:理解 Informatica‘Inside Out’](https://www.edureka.co/blog/informatica-tutorial)和 [Informatica 转换:Informatica power center 的核心和灵魂](https://www.edureka.co/blog/informatica-transformations/)。如果你正在寻找 Informatica 认证的细节，你可以查看我们的博客 [Informatica 认证:所有需要知道的事情](https://www.edureka.co/blog/informatica-certification-all-there-is-to-know/)。

如果你已经决定以信息学为职业，我推荐你看看我们的[信息学培训](https://www.edureka.co/informatica)课程页面。Edureka 的 Informatica 认证培训将通过现场讲师指导课程和使用真实案例的实践培训，使您成为 Informatica 专家。