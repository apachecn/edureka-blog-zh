# 关于 UiPath 中的变量、数据类型和活动，您需要知道的一切

> 原文：<https://www.edureka.co/blog/variables-data-types-activities-in-uipath>

自从自动化出现的那一天起，用于迎合自动化的各种工具就存在了。无论是用于 windows 桌面自动化的简单工具，还是企业用来自动化庞大任务的工具，每个工具都有自己的功能。 [UiPath](https://www.edureka.co/blog/uipath-tutorial/) 就是这样一个工具， [证明](https://www.edureka.co/robotic-process-automation-training) 里面的可以 把你作为 [RPA 开发者](https://www.edureka.co/blog/rpa-developer-roles-and-responsibilities/) 。因此，在这篇文章中，让我们学习一些非常基本的主题，比如变量、数据类型和 UiPath 中的活动。

以下是本文涵盖的主题:

*   [UiPath 概述](#UiPath%20Overview)
    *   [ui path 中的项目](#Projects%20in%20UiPath)
    *   [UiPath 仪表盘](#UiPath%20Dashboard)
    *   [流程图和顺序图](#Flowcharts%20and%20Sequences)
*   [变量](#Variables)
    *   [创建，删除&管理变量](#Create,%20Remove%20and%20Manage%20Variables)
    *   [变量类型](#Types%20of%20Variables)
*   [数据类型](#Data%20Types)
*   [活动](#Activities)
    *   [消息框](#Message%20Box)
    *   [分配](#Assign)
    *   [写 CSV](#Write%20CSV)
    *   [如果](#If)
    *   [对于每个](#For%20Each)
    *   [而](#While)
    *   [Do-While](#Do-While)
    *   [开关](#Switch)

所以，朋友们让我们现在开始吧。

## **ui path | edu reka**中的变量、数据类型和活动



[https://www.youtube.com/embed/rcI5-hk91WQ?rel=0&showinfo=0](https://www.youtube.com/embed/rcI5-hk91WQ?rel=0&showinfo=0)

本视频将涵盖 UiPath 的基本概念，如变量、数据类型和 UiPath 中的活动。

## **UiPath 概述**

UiPath 是 [RPA 工具](https://www.edureka.co/blog/rpa-tools-list-and-comparison/)的主要市场领导者之一。该工具用于自动化重复性任务，并提供拖拽和拖放功能。因此，您希望执行的任何操作都可以通过拖放到工作窗格中的活动来满足。 现在，要在 UiPath 中自动化任务，您必须根据您的需要创建项目。因此，接下来在本文中，让我们来看看 UiPath 中的各种项目。

### UiPath 中的 **项目**

![Projects in UiPath - Variables,Data Types and Activities in UiPath - Edureka](img/7e0bfdc0473911d63ac602ef981e0e45.png)

UiPath 中主要有五种项目。参考下文。

*   **流程**–流程是一个简单的空白项目，用于设计新的自动化流程。
*   **库**–这种项目用于创建可重用的组件，然后将它们发布为库。
*   **交易流程**–这种类型的项目用于创建流程图形式的流程。
*   **代理流程改进**–这种项目会触发自动化，以响应鼠标或键盘事件。
*   机器人企业框架(Robotic Enterprise Framework)这种类型的项目创建了一个遵循大规模部署最佳实践的事务性业务流程。

现在，一旦您选择了项目的类型，您将被重定向到 UiPath 仪表板。接下来，让我们看看 UiPath 仪表板中的不同窗格。

### **UiPath 仪表盘**

除了工作区之外，UiPath 仪表板主要有四个窗格来设计自动化。参考下文。

**![UiPath Dashboard - Variables,Data Types and Activities in UiPath - Edureka](img/603766ac54657a481857a324aaf58c87.png)**

*   **活动窗格:**该窗格包含用于满足不同功能的活动，如打印输出、for 循环、if-else 循环等。
*   **Ribbon:** Ribbon 由保存、运行、数据抓取、记录等选项组成。
*   **属性窗格:**属性窗格由您拖放到自动化中的活动的属性组成。
*   **输出窗格:**输出窗格显示自动化的输出。

现在，既然您知道 UiPath 的窗格，让我告诉您，当您拖放一个活动时，您可以创建一个流程图或一个序列。所以让我们理解这些术语。

### **流程图和顺序图**

**![Flowcharts and Sequences - Variables,Data Types and Activities in UiPath - Edureka](img/a6a0335f54f4f796cc1d18f68361d44f.png)流程图:**ui path 中的流程图提供了多个分支逻辑操作符，以创建复杂的业务流程，并以多种方式连接活动。

**序列:**用于无缝地从一个活动转到另一个活动。因此，当您将一组活动放在一个序列中时，它们将作为单个块活动。

因此，您可以在流程图中使用序列，也可以在序列中使用流程图。

现在，让我们从 UiPath 中的变量这个主题开始。

## **ui path 中的变量**

变量用于表示未知的字段，如文件、文件夹、字母、数字等。UiPath 中的变量类似于任何其他编程知识中的变量。因此，您可以创建、删除和管理变量。接下来，在这篇文章中，让我们看看同样的。

### **创建，删除&管理变量**

#### **创建变量**

要在 UiPath 中创建变量，以下是两个可用选项。

*   在**属性面板的**输出部分**中选择**一个活动**并按下 **Ctrl + K** 。**
*   点击**变量窗格**，如下图。

![Variable Pane in UiPath - Variables,Data Types and Activities in UiPath - Edureka](img/136e51962305313ee747159ce708eb71.png)

#### **删除变量**

要删除 UiPath 中的变量，有以下两个选项。

*   从**变量窗格中选择变量**->-**右键** - >选择**删除。**
*   从**设计选项卡中选择选项**移除未使用的变量**。**

![Delete Variables - Variables,Data Types and Activities in UiPath - Edureka](img/38c4c5d40bbdae90ead0e8e429f1a67f.png)第一个选项将只删除选中的变量，第二个选项将删除序列中所有未使用的变量。

#### **管理变量**

要管理 UiPath 中的变量，您必须考虑以下两个参数。参考下文。

*   提及变量的**范围**。
*   提及**默认值**(您不必提及每个变量的默认值)。

现在，让我们向前看，看看各种类型的变量。

### **变量类型**

各种类型的变量如下:

*   **文本变量–**此类变量用于存储文本值。
*   **真/假变量—**这种类型的变量用于存储布尔值。
*   **数字变量—**这种类型的变量用于存储整数值。
*   **数组变量—**这种类型的变量用于存储整数或字符串的数组。
*   **日期和时间变量—**这类变量用于存储日期和时间变量。
*   **数据表变量—**这类变量用于存储数据表，以表格的形式存储数值。
*   **通用变量—**这种类型的变量用于存储通用类型，如邮件合并、数据库等。

现在，让我们进入下一个主题，即 UiPath 中的**数据类型。**

## **ui path 中的数据类型**

数据类型对变量值的类型进行分类。在 UiPath 中，它可以是整数、字符串、布尔值、泛型或。

因此，要选择变量的数据类型，您必须转到**变量窗格**，然后选择**变量类型**。参考下文。

![Variables Types in UiPath - Variables,Data Types and Activities in UiPath - Edureka](img/d762844602e8750049c7974d55120cae.png)现在，让我们进入本文的下一个话题，即 UiPath 中的**活动。**

## **ui path 中的活动**

UiPath 中的 Activities 提供了各种操作，您需要这些操作来自动化不同的应用程序。对于每一个功能，UiPath 中有各种各样的活动，但是我将只讨论下面的几个活动。

所以让我们开始吧。

### **消息框**

显示一个消息框，其中包含必须向用户显示的给定文本。您可以直接在消息框中显示消息，也可以使用变量在消息框中显示消息。让我们逐一研究一下。

#### **直接在消息框中显示消息**

拖动一个**消息框活动**和**提及你希望在消息框中显示的文本**。您将看到一个消息框的输出，显示您提到的文本。参考下文。

#### **![Message Box with Variables - Variables,Data Types and Activities in UiPath - Edureka](img/e95615b584a83c0deef00651975f17ba.png)使用变量在消息框中显示消息**

**步骤 1:** 拖动一个**输入对话框**并提及**标题**和**标签**。这里我想把输入作为名称提及，所以我把**标题作为“名称”**提及，把**标签作为“提及你的名字”**。参考下文。

![Input Dialog - Variables,Data Types and Activities in UiPath - Edureka](img/125e68a87ca3bd305e2d5ed515d2122a.png) **第二步:**接下来，在该活动的**属性窗格**中，转到**输出部分**，按下 **Ctrl + K** 来创建一个变量。在这里我创建了一个**变量** ' ***示例'*** '的**字符串**类型。

**第三步:**拖动一个**消息框活动**和**提变量*‘例’****。*您会看到一个消息框的输出，显示您必须提到的名字。参考下文。

![Message Box with Variables to Print a Message - Variables,Data Types and Activities in UiPath - Edureka](img/7cf6b3a9d0d78c99e3eef07c27515802.png)

现在，让我们进入下一项活动，即分配活动。

### **分配活动**

此活动使您能够为变量赋值。为了向您解释此活动的功能，让我们创建一个自动化任务来计算目录中存在的文件数量。

#### **统计文件数量**

**第一步:** 创建变量***【NumberOfFiles】******source path***。现在，将 ***sourcepath 变量*** 的默认值赋给源目录 的 ***路径。参考下文。***

![Mention the Variables - Variables,Data Types and Activities in UiPath - Edureka](img/0cac5207ac90ef9e156a3c3e5dccb510.png)

**第二步:** 拖动 **赋值** **活动** 并将 **到** 段赋值到**NumberOfFiles**并将 **值** 段赋值到 **目录。GetFiles(sourcepath)** 函数。这将从源路径中获取所有文件。

**![Assign Activity - Variables,Data Types and Activities in UiPath - Edureka](img/d35f0440bad6da600ad070b6c048f91b.png)第三步:**拖动一个**消息框**并提及**“在文件夹中找到的文件数是->+Number of files . count . tostring .**这将统计文件夹中的文件数。

因此，这将显示如下输出。

![Output of Assign Activity - Variables,Data Types and Activities in UiPath - Edureka](img/7b29defdbe625ab899f9f7c7aa282950.png)

现在，让我们前进到下一个活动，即编写 CSV 活动。

### **写 CSV 活动**

此活动用于将指定的数据表保存到一个. csv 文件中。为了向您解释此活动的功能，让我们创建一个自动化任务，将抓取的数据存储到 Write CSV 活动中。

#### **提. csv 文件中的刮取数据**

**第一步:**使用**功能区**的**数据抓取选项**，从选择的网站抓取数据。这里我选了，Flipkart 网站。在下面的对话框中，按下 **下一步** 。

![Select Element in UiPath - Variables,Data Types and Activities in UiPath - Edureka](img/ca7d95c78794633fb1703015e08b3f94.png)

**第二步:** 将鼠标悬停在某个数据源字段上，然后点击该数据源字段。

![Data Scraping - Variables,Data Types and Activities in UiPath - Edureka](img/6138259ab85499c0625f2175928c2e53.png)

**第三步:** 之后，你会看到另一个**对话框**，要求你选择**第二元素**来创建一个图案。

**第四步:** 一旦你选择第二个元素来创建一个模式，你会得到一个 **配置列** 的选项。在打开的对话框中，您可以重命名列名并提取 URL。之后点击**下一个**。参考下文。

![Configure-Activities, Variables, Data Types in UiPath - Edureka](img/7f559a4d32b9d0b49209326f7c13922a.png)

**第五步:** 现在，要从网站提取其他数据源，点击  **提取相关数据** 选项，重复上述步骤。

**第六步:** 提取完所有需要的数据后，点击 **完成** 。此操作将打开一个对话框，询问您是否希望将数据分布在多个页面上。参考下文。

**![Span Multiple Pages-Activities, Variables and Data Types in UiPath -Edureka](img/a43b8a1fbd5ca0853e7ee1f62d01f875.png)第七步:** 要跨多个页面，选择 **是** 并将鼠标悬停在该区域，可重定向至下一页面。然后，您将被重定向到您的 UiPath 仪表板。

**第八步:** 现在将提取的所有数据保存到一个. csv 文件中，拖动  **将 CSV 活动** 写入  **中做**部分的  **数据抓取**。

**第九步:** 在 **文件的** 段中提到了这个活动的 ***路径。csv 文件*** 你要存储提取的数据然后在  **数据表段**中提到***extract DataTable 变量*** 。参考下文。

**![Write CSV Activities - Activities, Variables and Data Types in UiPath - Edureka](img/ce851f371af8271ba1d4fe0afc5d610e.png)**

*NOTE:The ExtractDataTable variable is the output variable that is automatically generated from the Data Scraping Wizard. You can find this variable in the Extract Structured Data activity.*

**您将看到一个输出，所有从网站提取的数据都存储在提到的。csv 文件。**

**现在，让我们进入下一项活动，即 If 活动。**

### ****如果活动****

**该活动决定是否执行某个活动或某个活动块。为了向您解释此活动的功能，让我们创建一个自动化任务来确定一个数字是偶数还是奇数。**

#### ****求一个数是否是偶数/奇数****

****第一步:**拖动一个**输入对话框**并提及标题和标签。这里我想把输入称为数字，所以我把**标题称为“数字”**，把**标签称为“数字”**。参考下文。**

**![Input Dialog for Displaying Number- Variables,Data Types and Activities in UiPath - Edureka](img/49c4fa6bd7f8c268d15a0a69dade42c3.png) **步骤 2:** 在该活动的**属性窗格**中，转到**输出部分**，按下 **Ctrl + K** 创建一个变量。这里我创建了一个**变量** ' ***号'*** 的 **Int32** 类型。**

****第三步:**拖动一个**如果活动**并且在**条件段**中提到**号 mod 2 = 0。**之后，在**然后**部分拖动一个**消息框**并提及**号。ToString +"是一个偶数"**，在 **Else** 部分拖动一个**消息框**并提及**号。ToString +"是奇数"。**参考下文。**

**![If Loop - Variables,Data Types and Activities in UiPath - Edureka](img/364bcdc06a277954ffbee137c4d4b4eb.png)**

**当您执行这个特定的序列时，您将得到一个输入对话框来输入一个数字。如果你输入的数字是偶数，那么你会看到一个偶数的输出，否则你会看到一个奇数的输出。**

**![Output of If Activity - Variables,Data Types and Activities in UiPath - Edureka](img/7d464a73801e742d3f97c63bddadefaf.png)**

**现在，让我们进入下一项活动，即每项活动。**

### ****为每项活动****

**该活动使您能够逐个迭代每个数据和流程。为了向您解释这个活动的功能，让我们创建一个自动化任务来打印斐波那契数列。**

#### ****打印斐波那契数列****

****步骤 1:** 为每个活动拖动**，并在值部分提及一个变量**【数字】**。现在，在这里提到变量之前，创建一个 **Int32[] type** 的变量，并在默认值部分提到**斐波那契数列**。参考下文。****

****![Create Variable for For Each Activity - Variables,Data Types and Activities in UiPath - Edureka](img/30129aa4abf35b9272c8f80bc312f766.png)第二步:**在**主体的**部分为每个活动拖动一个消息框，并提及**"这个斐波那契数列的长度= "+数字。Length.ToString +"包含元素- > " + item.ToString.** 参考下文。**

**![For Each Activity - Variables,Data Types and Activities in UiPath - Edureka](img/9b479aa4b469d011a285b8dd608f72f6.png) 上述步骤将产生如下输出。**

**![Message Box Output - Variables,Data Types and Activities in UiPath - Edureka](img/409ce55531287365dd967886037ae9c5.png)**

**现在，让我们进入下一项活动，即 While 活动。**

### ****趁着活动****

**此活动使您能够在满足特定条件时重复执行特定流程。为了向您解释这个活动的功能，让我们创建一个自动化任务来打印数字 1-10。**

#### ****打印数字 1-10****

****第一步:**拖动**同时活动**，在**条件段**提条件**计数< 10** 。但是，在此之前创建变量**计数**。**

****第二步:**在该活动的**主体部分**中，拖动一个**赋值活动**，将**到**部分赋值给 **count** ，将**值**部分赋值给 **count + 1** 函数。这将使计数器增加 1，直到满足条件。参考下文。**

****![Assign Activity For Printing Numbers - Variables,Data Types and Activities in UiPath - Edureka](img/56e5346d652ff0b5c13c4e61bfbf3758.png)第三步:**拖动 **Append Line 活动**并提及**文件名、**您要在其中存储您将在该活动中引用的文本。在这里，我提到的文本是**“计数器现在是”+ count。ToString +“”。**。参考下文。**

**![Append Line Activity - Variables,Data Types and Activities in UiPath - Edureka](img/66a25537e77563518bb2164d2e3835f9.png)**

**您最终的执行和输出流程如下所示。**

**![Final Flow of While Loop and Output - Variables,Data Types and Activities in UiPath - Edureka](img/50209d0673155e56e36e062dc8f8e2aa.png)**

**现在，让我们进入下一项活动，即“边做边做”活动。**

### ****边做边活动****

**此活动使您能够在满足条件时执行自动化的指定部分。为了向您解释这个活动的功能，让我们创建一个自动化任务来打印数字 1-10。**

#### ****打印数字 1-10****

****步骤 1:** 拖动**边做边活动**和**条件段**提条件**计数< 10** 。但是，在此之前创建变量**计数**。**

****第二步:**在该活动的**主体部分**中，拖动一个**赋值活动**，将**到**部分赋值为 **count** ，将**值**部分赋值为 **count + 1** 。这将使计数器增加 1，直到满足条件。参考下文。**

****![Assign Activity For Printing Numbers - Variables,Data Types and Activities in UiPath - Edureka](img/eb17ce8319d37200e4e02b783b2a2066.png)第三步:**拖动 **Append Line 活动**并提及**文件名、**您要在其中存储您将在该活动中引用的文本。在这里，我提到的文本是**“计数器现在是”+ count。ToString +“”。**。参考下文。**

**![Append Line Activity for le Activity - Variables,Data Types and Activities in UiPath - Edureka](img/b3a0a6bdb67473f2dd9a7a5767386743.png)**

**![Final Flow of Do-While Loop and Output - Variables,Data Types and Activities in UiPath - Edureka](img/9a3e4b16b0cde2fb78b5d46b5591ba68.png)**

**现在，让我们进入下一项活动，即交换活动。**

### ****开关活动****

**此活动使您能够根据指定表达式的值从多个选项中选择一个选项。为了向您解释此活动的功能，让我们创建一个自动化任务来确定两个数之和是偶数还是奇数。**

#### ****两个数之和是偶数/奇数****

****步骤 1:** 拖动一个**输入对话框**并提及**标题**和**标签**。这里我想把输入作为第一个数字，所以我把**标题作为“输入第一个数字”**，把**标签作为“第一个数字”**。**

****步骤 1.1:** 在该活动的**属性窗格**中，转到**输出部分**，按下 **Ctrl + K** 创建一个变量。在这里我创建了一个**变量**'***first number****'**' int 32 的类型。***

****第二步:**再次拖动**输入对话框**并提及**标题**和**标签**。这里我想把输入作为第二个数字，所以我把**标题作为“输入第一个数字”**，把**标签作为“第一个数字”**。**

****步骤 2.1:** 在该活动的**属性窗格**中，转到**输出部分**，按下 **Ctrl + K** 创建一个变量。在这里我创建了一个**变量**'***second number****'**' int 32 的类型。参考下文。***

****![Input Dialog For Input Numbers - Variables,Data Types and Activities in UiPath - Edureka](img/9f3f60fb65786ee50e24e1d1dcc44956.png)第三步:**之后拖动**分配活动**，将**到**段分配给**合计**，将**值**段分配给**first number+second number**。这将使计数器增加 1，直到满足条件。(这里 total 是一个 Int32 类型的变量，您必须创建它)。**

****![Assign Activity for Switch Examples - Variables,Data Types and Activities in UiPath - Edureka](img/21cf1f6600bfc2c204a31a9ed6441145.png)第四步:**拖动**开关活动**并在**表达式部分**提及**总 mod 2 = 0** 。现在，在**默认部分**拖动一个**消息框**显示输出**“数字是偶数”**。同样在**案例 1 部分**拖动**消息框**显示输出**“数字是奇数”**。**

****![Switch Activity - Variables,Data Types and Activities in UiPath - Edureka](img/d3ac14e33d146707271ffa11add7ac39.png)****

**当你执行这个特定的序列时，你会得到两个输入对话框，一个接一个地输入一个数字。如果你输入的数字之和是偶数，那么你会看到一个偶数的输出，否则你会看到一个奇数的输出。**

**所以，朋友们，这篇关于 UiPath 中的活动、变量和数据类型的文章到此结束。我希望你喜欢阅读这篇文章，学习如何使用 UiPath 的基础知识。如果你想了解更多关于 UiPath 的内容，那么你可以参考我们关于 UiPath 自动化示例、 [UiPath PDF 数据提取](https://www.edureka.co/blog/uipath-pdf-data-extraction/)和 UiPath 中的[错误处理的文章。](https://www.edureka.co/blog/error-handling-in-uipath/)**

**如果您希望进一步了解机器人流程自动化，并成为一名  [RPA 开发人员](https://www.edureka.co/blog/rpa-developer-roles-and-responsibilities/)，那么您可以使用 UiPath 查看我们关于  ***[机器人流程自动化的课程。](https://www.edureka.co/robotic-process-automation-training)*** 本课程将让您增强 RPA 方面的知识，并让您在 [UiPath](https://www.edureka.co/blog/uipath-tutorial/) 方面获得丰富的实践经验。**

**有问题要问我们吗？请在这篇 **文章的评论部分提及 UiPath** 文章中的活动、变量、数据类型，我们会给你回复。**