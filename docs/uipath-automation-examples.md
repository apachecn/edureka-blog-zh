# 您可以练习的 5 个 UiPath 自动化示例

> 原文：<https://www.edureka.co/blog/uipath-automation-examples>

***自动化是什么意思？如何使用 RPA 工具自动化任务？有哪些 UiPath 自动化的例子？***

我相信你一定想知道这些问题的答案是什么。嗯，在这篇关于 UiPath 自动化示例的文章中，我将回答您所有关于[机器人流程自动化](https://www.edureka.co/blog/what-is-robotic-process-automation/)如何在 [RPA 工具](https://www.edureka.co/blog/rpa-tools-list-and-comparison/)的帮助下帮助我们自动化繁琐的任务的问题，例如 [UiPath](https://www.edureka.co/blog/uipath-tutorial/) 、[蓝棱镜](https://www.edureka.co/blog/rpa-blue-prism/)和[自动化 Anywhere](https://www.edureka.co/blog/rpa-automation-anywhere/) 。除此之外，如果你希望精通 [RPA](https://www.edureka.co/blog/rpa-tutorial/) 成为 [RPA 认证专家](https://www.edureka.co/robotic-process-automation-training)，那么我相信这篇文章会帮助你学习各种自动化如 PDF、Excel、Email、Web 等等。

本文将涵盖以下主题:

*   什么是自动化？
*   [什么是 UiPath？](#What%20is%20UiPath?)
*   [自动化实例](#Automation%20Examples)
    *   [将文件从一个源文件夹移动到目的文件夹](#Moving%20Files%20from%20one%20Source%20Folder%20to%20Destination%20Folder)
    *   [网络自动化](#Web%20Automation)
    *   [电子邮件自动化](#Email%20Automation)
    *   [Excel 自动化](#Excel%20Automation)
    *   [PDF 自动化](#PDF%20Automation)

那么，让我们开始吧。

## **什么是自动化？**

考虑一个场景，其中一个人的唯一工作是从多个来源收集数据，然后将它们汇总到一个 Excel 文件中。参考下图。现在，你认为这个人应该每天做这项工作，还是应该自动完成这项任务，以更好地发挥他的才能？显然，第二种选择听起来更好。

因此，人们可以通过使用机器人流程自动化来自动完成从各种来源收集数据并将它们汇总到一个文件中的任务。如果我必须为您定义自动化，那么自动化就是减少人力并同时提高绩效的技术。为了自动化任务，我们需要 RPA 工具来完成，UiPath 就是这样的工具之一。因此，在这篇关于 UiPath 自动化例子的文章中，让我简单地告诉你什么是 UiPath。

## **什么是 UiPath？**

![UiPath Logo - UiPath Automation Examples - Edureka](img/112f5b779fb647d72ea1a84aeb1c6c33.png)

UiPath 是一个[机器人流程自动化](https://www.edureka.co/blog/robotic-process-automation/)工具，它通过活动的拖放功能提供桌面自动化。这个工具有一个终身免费的社区版。所以，如果你是自动化新手，那么你可以开始学习自动化任务，通过使用这个工具消除人工干预。

如果你想要一个关于 UiPath 中顶级自动化例子的视频讲座，你可以参考下面的视频:

## **UiPath 自动化示例| ui path**中排名前五的自动化示例



[https://www.youtube.com/embed/-KAjgwWF0hY?rel=0&showinfo=0](https://www.youtube.com/embed/-KAjgwWF0hY?rel=0&showinfo=0)

本视频涵盖了您可以使用 UiPath 执行的不同类型的自动化。

现在，让我们进入主题，从 UiPath 自动化示例开始。

## **UiPath 自动化实例**

在本文的这一部分，我们将逐一看到不同类型的自动化。以下是您将看到的自动化:

*   将文件从源文件夹移动到目标文件夹
*   网络自动化
*   电子邮件自动化
*   Excel 自动化
*   PDF 自动化

因此，人们让我们从这篇关于 UiPath 自动化示例的文章开始。

### **将文件从源文件夹移动到目的文件夹**

#### **任务**

目的是自动化将文件从源文件夹移动到目标文件夹的过程。

#### **自动化步骤**

遵循以下步骤实现目标:

*   将源目录分配给变量。
*   使用 ***计数器*** 变量计算要移动的文件数量。
*   在 ***移动文件*** 活动中提到目的路径。
*   对于源路径中的每一项，使用计数器变量将文件移动到目标路径。

#### **解决方案**

**步骤 1:** 创建变量***source path***和 ***Counter*** 。现在，将 ***sourcepath 变量*** 的默认值赋给源目录 的 ***路径。参考下文。***

**![Create Variable - UiPath Automation Examples - Edureka](img/c2ee45bbc061ac49086f325d68224061.png)第二步:**拖动**赋值** **活动**，将**到**段赋值给 *** NumberOfFiles *** 段，将**值**段赋值给 ***目录。**GetFiles(source path)*函数。这将从源路径中获取所有文件。

**第三步:**在消息框中输出要移动的文件数量。为此，拖动**消息框**活动并提及 ***NumberOfFiles。Count.ToString+"要移动的文件"*** 。这将计算源文件夹中的文件数，并将输出打印为要移动的 x 个文件。参考下文。

**![Message Box Output - UiPath Automation Examples - Edureka](img/080058996b19c1a5c35197146510e7f2.png) ** **第四步:**创建一个 ***计数器变量*** 然后拖动一个**赋值活动**。现在，在分配活动中，将 To 部分分配给计数器变量，将 value 部分分配给 0。这将把计数指定为 0。到目前为止，您的序列应该如下所示。

**![Assign Activity - UiPath Automation Examples - Edureka](img/2d4af34f23a8516aa45866e3fd439562.png)第五步:**现在，拖动中每个活动的**，并提及 **NumberOfFiles 中的每个项目，**你要将文件移动到目标路径。为此，请遵循以下步骤:**

**步骤 5.1:** 在该活动的**主体**部分，拖动**移动文件活动**，在**属性窗格**的**目的地**部分提及 ***目的地路径*** 。

**步骤 5.2:** 到**的 ***属性段*** 对于每个**活动，在**类型参数**中提到 ***字符串*** 。请参考下面的快照。

**![Properties section of For Each Activity - UiPath Automation Examples - Edureka](img/e972435bd55cd4746f96c508e3afe0eb.png)步骤 5.3:** 将所有文件从源文件夹移动到目的文件夹，拖动**赋值活动**，将**到**的值赋给 ***计数器变量*** ，将**值**段赋给 ***计数器+ 1。*** 参考下文。

![For Each Activity - UiPath Automation Examples - Edureka](img/fb92cdb79d136c8efed01b04fbaf77ee.png)

**步骤 6:** 点击**运行**按钮，执行该序列。您会看到源文件夹中的所有文件都被移动到了目标文件夹中。

现在，在这篇关于 UiPath 自动化示例的文章中，让我们转到下一个自动化，即 Web 自动化。

### **网络自动化**

#### **任务**

目的是从网站上抓取数据，并将其存储在一个. csv 文件中。

#### **自动化步骤**

遵循以下步骤实现目标:

*   使用数据抓取工具并记录您想要提取的数据。
*   相应地提取相关值。
*   使用 ***编写 CSV*** 活动并提及路径。csv 文件

#### **解决方案**

**第一步:**选择要从中提取数据的网站。

**第二步:**从功能区选择**数据抓取**选项，选择您想要选择的元素。在下面的对话框中按下**下一步**。

**![Select Element - UiPath Automation Examples - Edureka](img/8b1a84e8804c412e77a85e5141f93eb6.png)**

**步骤 2.1:** 将鼠标悬停在数据源字段上，然后单击数据源字段。

**![Select Element on Website - UiPath Automation Examples - Edureka](img/e6ab125677c7369c11fd7c63300c1400.png)第三步:**之后，你会看到另一个对话框，要求你选择第二个元素来创建一个图案。

![Select Second Element - UiPath Automation Examples - Edureka](img/73018297bd88c38ed195e1801c81393f.png)

**步骤 4:** 一旦您选择第二个元素来创建模式，您将得到一个选项来**配置列**。在打开的对话框中，您可以重命名列名并提取 URL。之后，点击下一步。参考下文。

**![Configure Columns - UiPath Automation Examples - Edureka](img/92fd3c7198e307aa5d4410d1c9eb4d6e.png)第五步:**你会看到下面的输出。现在，要从网站提取其他数据源，点击 ***提取相关数据*** 选项，重复上述步骤。

**![Extract Correlated Data - UiPath Automation Examples - Edureka](img/8e15ff9ff2199db9113c2ee3c5a57508.png)第六步:**提取完所有需要的数据后，点击**完成**。此操作将打开一个对话框，询问您是否希望将数据分布在多个页面上。参考下文。

**![Span Multiple Pages - UiPath Automation Examples - Edureka](img/e2c57a3793172bbe8336a20331c82eb0.png)第七步:**要跨越多个页面，选择**是**，将鼠标悬停在该区域，将重定向到下一页。然后，您将被重定向到您的 UiPath 仪表板。参考下文。

**![Choose Multiple Pages - UiPath Automation Examples - Edureka](img/5c937e2bff1bf2c39b81a386d7296b3e.png)第八步:**现在将提取的所有数据保存到一个. csv 文件中，拖动一个**写 CSV 活动**到**数据抓取**的 **Do** 段中。

**第九步:**在本活动的**文件路径部分**中，提到的*路径。csv 文件* 在您想要存储提取数据的地方，然后在**数据表部分**中提及 ***ExtractDataTable 变量*** 。参考下文。

**![Automation Workflow of Web Automation - UiPath Automation Examples - Edureka](img/ec9616c93322e31c7a92b6acf1d052f1.png)**

*NOTE: The ExtractDataTable variable is the output variable that is automatically generated from the Data Scraping Wizard. You can find this variable in the Extract Structured Data activity.*

****步骤 10:** 点击**运行**按钮，执行该序列。您会看到数据存储在。csv 文件如下。**

### ****![Web Automation Output - UiPath Automation Examples - Edureka](img/6347f1992f906c6d0a70b22f63fdc5bd.png)****

**现在，在这篇关于 UiPath 自动化示例的文章中，让我们转到下一个自动化，即电子邮件自动化。**

### ****邮件自动化****

#### ****任务****

**目的是保存标题行中有关键字的前 30 封电子邮件的附件。附件将存储在特定的文件夹中。**

#### ****自动化步骤****

**遵循以下步骤实现目标:**

***   将电子邮件地址分配给一个变量，并在 ***获取密码*** 活动中提及密码。*   使用“获取 IMAP 邮件”活动，并提及文件夹、端口号和服务器。*   对于每封邮件，提及你想考虑的关键词，然后使用 If-else 循环。*   在 If 部分，使用 Save Attachments 活动并提到目标目录。**

#### ****解决方案****

****步骤 1:** 分别创建**变量**如 ***电子邮件*** 、 ***密码*** 和***getmail messages***的字符串、字符串和列表<邮件消息>。参考下文。**

****![Create Variables for Email Automation - UiPath Automation Examples - Edureka](img/1c66f3dc32d088a1b30908eda290f30a.png)第二步:**拖动**分配活动**，将活动的**到**部分分配给 ***电子邮件变量*** 和**值**到 ***电子邮件地址*** ，您希望从该地址读取详细信息。**

****步骤 3:** 拖动 Get Password 活动，并在 Properties 窗格的 Password 部分提到您的电子邮件 ID 的 Password。另外，在结果窗格中提到密码变量。**

****步骤 4:** 拖动 **Get IMAP Mail Message 活动**，在**属性窗格中提及以下细节。****

**在的部分:**

***   邮件文件夹-“收件箱”*   端口–993*   服务器 u*   电子邮件–电子邮件变量*   密码–密码变量*   前 30 名*   消息–getmail messages**

**请参考下面的快照。**

### ****![IMAP Mail Message Properties Pane - UiPath Automation Examples - Edureka](img/698bde144f031afb09ad71bef2f66035.png)****

**直到上面的步骤，你的执行应该如下所示。**

****![Assign, Get Password and Get IMAP mail message Activity - UiPath Automation Examples - Edureka](img/63916e5b4353eecad4da1a81c29620e3.png)第五步:**拖动每个活动的，然后在 item 部分提到 mail，在变量表达式部分提到 GetMailMessages。**

****第六步:**现在，在这个活动的主体部分，拖动 **If 活动**。在本练习中，如果主题行包含关键字，您必须指定保存附件的条件。为此，请遵循以下步骤。**

****步骤 6.1:**If 活动**的**条件段**中的**，提及 ***邮件。Subject.Contains("example ")，*** 其中' example '是必须考虑的关键字。**

****步骤 6.2:** 进入 *****属性段***** 中的为每个活动 ****并在**** 类型参数中提及 *****系统。Net.Mail.Message*** 。**参考下面的快照。**

****![Properties section of For Each Activity Email Automation - UiPath Automation Examples - Edureka](img/53ca658f2779e7e4fdf33a07a2d0b006.png)步骤 6.3:**中的****然后在 **If-activity** 的部分，拖动**保存附件 activity** 。在本活动中，提及邮件消息区域中的 **mail** 变量以及保存所有附件的文件夹路径。参考下文。**

****![For Each Activity in Email Automation - UiPath Automation Examples - Edureka](img/a15baa3e4a2bb4477e163a41e448fc89.png)第七步:**点击**运行**按钮执行该序列。你会看到所有在主题行中有关键字 example 的电子邮件都会被阅读，附件会存储在提到的文件夹中。**

**现在，在这篇关于 UiPath 自动化示例的文章中，让我们转到下一个自动化，即 Excel 自动化。**

### ****Excel 自动化****

#### ****任务****

**目的是从存储在. csv 文件中的数据自动填充 google 表单。**

#### ****自动化步骤****

**遵循以下步骤实现目标:**

***   创建一个谷歌表单，并提及您想要填写的详细信息。*   创建一个. csv 文件，并提及您想要在 google 表单中填写的所有细节。*   现在使用 ***打开浏览器活动*** 并提及网址。*   对 Excel 表格中的每一行 使用 ***，通过将 ***类型配置为*** 活动来填充 google 表单中的值。****   使用 ***鼠标点击活动*** 并将鼠标悬停在提交按钮上。*   然后，使用 ***延迟活动*** 并提及您要考虑延迟的时间。*   拖动 ***返回活动*** 以便再次重定向到 Google 表单，并多次填写详细信息。**

#### ****解决方案****

****第一步:**创建一个数据表类型的变量**数据表**。参考下文。**

****![Create Variable for Excel Automation - UiPath Automation Examples - Edureka](img/b4540eff797bcec12f002d6c0164aab7.png)第二步:**创建一个. csv 文件，并提及你想在谷歌表单中填写的所有细节。现在，拖动一个**读取 CSV**活动和*提及 CSV 文件 的路径。在本活动的**输出部分**中提到变量 ***数据表*** 。参考下文。***

****![Read CSV Activity - UiPath Automation Examples - Edureka](img/76966d08810f203cde808b1e20a1f203.png)第三步:**现在拖动另一个序列，然后拖动一个**打开浏览器活动**。在本活动中，请用双引号将 google 表单的 URL 括起来。**

****步骤 4:** 在该活动的**做**部分，拖动每一行活动的**，在**数据表中提及每一行。******

****第 5 步:接下来，该活动的**主体**部分的**将**类型拖入活动中。到目前为止，你的序列应该如下图所示。****

****![Open Browser - UiPath Automation Examples - Edureka](img/85768faf309390ad95199b9fcf3f672a.png)第 5.1 步:**现在，在屏幕上，也就是在谷歌表单上，指出你想填写数据的地方。参考下文。**

****![Indicate Element on Screen - UiPath Automation Examples - Edureka](img/5d06b94a083c819161fbc97fa6ad649a.png)第 5.2 步:**中的**进入活动**，提 ***行(“全名”)。ToString *** ，其中全名是 CSV 文件的行名。**

****步骤 6:** 现在，您必须为您想要在 Google 表单中填写的所有值重复上述步骤。在这里，我要填写 ***的电话号码、过去的工作经验、学历、技能、**T5 和 ***的职位。*** 所以，提 ***排(“电话号码”)。ToString，row(“体验”)。ToString，row(“学历”)。ToString，row(“技能集”)。ToString，row("Position ")。ToString* 分别为**。参考下文。***

****![Type Into Activity - UiPath Automation Examples - Edureka](img/d1e0644fd362efa765b3906ef9a40428.png)第七步:**现在，在指明所有的元素之后，你必须点击提交按钮。为此，拖动点击活动，然后在**提交按钮**上进行指示，如下所示。**

****![Submit Button - UiPath Automation Examples - Edureka](img/62c4dd67b1cf22078ea17999087b927e.png)第八步:**添加**延时活动*****提到持续时间为 3-5 秒*** 。这样做是为了考虑 google 表单的页面加载时间。**

****步骤 9:** 现在，如果您必须从。csv 文件，为此，你必须拖动**回到活动序列的最后**。自动化的最后三个步骤应该如下所示。**

****![Go Back and Delay activity - UiPath Automation Examples - Edureka](img/367e808d5b1d63e39078cd2791db37dd.png)步骤 10:** 现在将流程图起点连接到包含 Read CSV 活动的序列，然后将这个特定节点连接到包含所有与 Google Form 相关的动作的序列。**

**![Final Flow of Automation - UiPath Automation Examples - Edureka](img/1c3fb37e9e801ce4242e188619afd38e.png)**

****步骤 11:** 点击**运行**按钮，执行该序列。您会看到所有的细节都是从。csv 文件，并将自动填写在谷歌的形式。**

**现在，在这篇关于 UiPath 自动化示例的文章中，让我们转到下一个自动化，即 PDF 自动化。**

### ****PDF 自动化****

#### ****任务****

**目的是从 PDF 文件中提取文本和图像，并将输出存储在消息框/文本文件中。**

#### ****自动化步骤****

**遵循以下步骤实现目标:**

***   要仅提取文本，请使用 Read PDF Text 活动，并使用消息框显示输出。*   要提取图像中的文本，请使用 Read PDF with OCR 活动，并使用消息框显示输出。**

#### ****解决方案****

****步骤 1:** 按照以下步骤，仅从 PDF 文档中提取文本。**

****步骤 1.1:** 拖动  **阅读 PDF 文本活动**。在活动中，提及要从中提取数据的 PDF 文档的路径。**

****步骤 1.2:** 现在，在  **属性窗格中的****读取 PDF 文本活动**，提一个输出变量查看输出。要设置一个输出变量，按下  **CTRL + K，**并给出一个名称。这里我已经提到作为  **输出。****

****步骤 1.3:** 之后，以同样的顺序拖动一个消息框，并在其中提及输出变量。**

****步骤 1.4:** 点击**运行**按钮执行该序列。您的完整序列和输出应该分别如下面的快照所示。**

**![Read PDF Text Activity-UiPath Automation Examples - Edureka](img/8f2ec4646806efbd4c5c7fa3893577a4.png)**

****步骤 2:** 现在，同样，如果你想提取图像中的文本，请遵循以下步骤。**

****步骤 2.1:** 拖拽**用 OCR 读取 PDF 活动。**在活动中， ***提到要从中提取数据的 PDF 文档*** 的路径。**

****步骤 2.2:** 现在，搜索一个 OCR 引擎，根据安装的任意一个拖拽一个 **OCR 引擎**。这里我用过  **Google OCR 引擎**。**

****步骤 2.3:** 现在，在  **属性窗格**中的  **用 OCR 活动**读取 PDF，提一个输出变量来查看输出。要设置输出变量，按下  **CTRL + K，** 并给出名称。这里我已经提到作为  **输出。****

****步骤 2.4:** 之后，在序列中拖动一个**消息框**，然后在其中提及输出变量。**

****步骤 2.5:** 点击**运行**按钮执行该序列。您的完整序列和输出应该分别如下面的快照所示。**

**![Read PDF with OCR Activity-UiPath Automation Examples -Edureka](img/8f9fabe1b207c33f671fca9943b02193.png)**

**如果您希望进一步了解如何从 PDF 文档中提取特定元素，请参考关于 [UiPath PDF 提取](https://www.edureka.co/blog/uipath-pdf-data-extraction/)的文章。**

**伙计们，关于 UiPath 自动化示例的这篇文章到此结束。我希望您喜欢阅读这篇关于 UiPath 自动化示例的文章，并学会如何自动化任务。如果您希望进一步了解机器人流程自动化，并成为一名 [RPA 开发人员](https://www.edureka.co/blog/rpa-developer-roles-and-responsibilities/)，那么您可以使用 UiPath 查看我们关于  ***[机器人流程自动化的课程。](https://www.edureka.co/robotic-process-automation-training)*** 本课程将帮助您增强 RPA 方面的知识，并为您提供大量 UiPath 实践经验。**

**有问题要问我们吗？请在这篇 **UiPath 自动化示例**文章的评论部分提到它，我们会给你回复。**