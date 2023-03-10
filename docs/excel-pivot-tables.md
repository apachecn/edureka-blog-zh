# 什么是 Excel 透视表，如何创建？

> 原文：<https://www.edureka.co/blog/excel-pivot-tables/>

Excel 提供了几个优秀的特性，其中之一就是数据透视表。Excel 数据透视表在世界各地被信息技术、会计、管理等不同背景的人广泛使用。在本 Excel 数据透视表教程中，您将了解到关于数据透视表的所有知识，以及如何使用数据透视表来可视化数据透视表。

在继续之前，让我们快速浏览一下这里讨论的所有主题:

*   [Excel 中的透视表是什么？](#pivottables)
*   [Excel 透视表的特性](#features)
*   [准备表格数据](#data)
*   [创建数据透视表](#create)
*   [过滤器](#filter)
*   [改变字段](#changingfields)
*   [透视表明细](#details)
*   [排序](#sorting)
*   [值字段设置](#valuefield)
*   [分组](#grouping)
*   [添加多个字段](#multiplefields)
*   [格式化数据透视表](#formatting)
*   [为数据透视表创建数据透视图](#pivotcharts)

## **Excel 中的透视表是什么？**

Excel 中的数据透视表是一种统计表，它浓缩了那些具有大量信息的表中的数据。汇总可以基于数据透视表以简单和智能的方式表示的任何字段，如销售额、平均值、总和等。

## **Excel 透视表的特性:**

Excel 数据透视表有许多显著的特性，例如:

*   允许您显示想要分析的确切数据
*   这些数据可以从不同的角度来看
*   您可以根据自己的需求关注任何部分的数据
*   使数据比较变得非常容易
*   数据透视表可以检测不同的模式、关系、数据趋势等
*   允许您创建即时数据
*   创建准确的报告

既然您已经了解了什么是 Excel 数据透视表，那么让我们继续来看看如何实际创建它们。

## **准备表格数据:**

在实际开始创建数据透视表之前，您需要在 Excel 中记下要创建数据透视表的数据。为了创建用于此目的的表格，请记住以下几点:

*   数据必须排列成**行和**列
*   对于每一列来说，**第一行**应该有一个**短且唯一的标题**
*   **列**应该只保存一个**单一类型的数据**
*   **行**应包含**单次记录**的数据
*   **不应出现空白行**
*   **没有列**应该是**完全空白**
*   **通过在表格和其他数据之间至少留出一行和一列空间，使表格与工作表中的其他数据分开**

例如，请看下表:

![Table-Excel Pivot Tables Tutorial-Edureka](img/9c2faf530fa7b92a84cb9e39f6ba7389.png)

如您所见，我已经创建了一个表，其中保存了不同城市不同个人的水果销售信息及其金额。该表中没有空行或空列，第一行对每一列都有唯一的名称，即订单 ID、日期、名称等。这些列分别包含相同类型的数据，即 id、日期、姓名等。

## **创建数据透视表:**

按照给定的步骤创建 Excel 数据透视表:

1.  从工作表中选择要为 ![Table for pivot table-Edureka](img/9718d35273a7c9f4ebae68ea2b80aa2f.png)创建数据透视表的整个区域
2.  点击[功能区](https://www.edureka.co/blog/excel-tutorial/#screenoptions)中的插入选项卡
3.  从表组 ![Insert PivotTable Excel-Edureka](img/045e11fecd5b97dcffbb65e797edfbcc.png)中选择透视表
4.  完成后，您将看到以下对话框 ![Create PT-Excel Pivot Tables Tutorial-Edureka](img/7eca9a4eecaee092d63d65698ec70257.png)
5.  指定要创建数据透视表的表格范围和位置，即新的[工作表](https://www.edureka.co/blog/excel-tutorial/#workbooksandworksheets)或现有工作表
6.  如果选择“新建工作表”选项，将为数据透视表创建一个新的工作表
7.  如果选择“现有工作表”选项，则必须选择数据透视表的起始单元格

完成后，您将看到一个空的数据透视表已创建，并且您将看到 Excel 窗口右侧的“数据透视表字段”窗格打开，您可以使用该窗格配置数据透视表，如下图所示:

![configuring Pivot Tables-Edureka](img/72b74a62cf111191cc27be45b30dfd20.png)

该窗格提供 4 个区域，即过滤器、列、行和值，其中，

*   过滤器允许您根据某些标准过滤出数据
*   列将表示要放入列中的字段
*   行将代表您要放入行中的字段
*   值字段只能用于表中的数字

表中的所有字段将在“数据透视表字段”窗格中显示为一个列表。要将任何字段添加到任何区域，只需将其拖放到那里，如下所示:

### **选择的字段:**

![Fields-Edureka](img/df31d6d94d30af1a6af8588d2f379a77.png)

### **数据透视表:**

![adding fields-Excel Pivot Tabes Tutorial-Edureka](img/849bb5fb0fc00dff6ba9b056ac95860c.png)

上表显示了一个二维数据透视表，其中行是供应商名称，项目是列。因此，这张表显示了每个供应商销售了什么，以及每个供应商获得了多少。最后一列显示每个供应商的总金额，最后一行显示每个项目的总金额。

如果希望创建一维数据透视表，可以通过只选择行或列标签来实现。看一下下面的例子，我只选择了行标签来表示城市以及金额的总和:

## **![one-dim pivot table-Edureka](img/9f51a031a6acf2d152936162c9b62072.png)**

## **过滤器:**

如果您想过滤掉某个特定城市的数据，您只需从数据透视表中打开城市的下拉菜单，然后选择您选择的城市。例如，如果从上表中过滤掉芝加哥的统计数据，您将看到下表:

![Pivot Chicago-Edureka](img/a2496728721aae674598bc81949b9d44.png)

## **改变字段:**

为了改变数据透视表中的字段，你所要做的就是在四个区域中的任何一个拖放你想要看到的字段。如果您想删除这些字段中的任何一个，您只需将该字段拖回到列表中。例如，如果将行标签从供应商名称更改为项目名称，将列标签更改为每个项目的数量，您将看到下表:

![Change Field-Exel-Edureka](img/d9811b867ae4502adddb66adf08ed91e.png)

在上面的表格中，您可以看到所有的项目都与它们各自的数量对应起来，并且表格中列出了所有城市中每个项目收到的金额。你可以看到香蕉是所有水果中卖得最多的，总量为 2300。

现在，如果您想查看某个特定城市的相同统计数据，只需从过滤器的下拉列表中选择合适的城市。例如，如果您过滤掉纽约的数据，您将看到下表:

![Change filters-Excel-Edureka](img/a8b53dafe8daa4ac6a6c91273775c4a5.png)

同样，您可以为您选择的任何字段创建各种数据透视表。

## **透视表明细:**

在上面的例子中，你已经看到了在纽约卖水果收到的总金额。如果您想查看数据透视表中显示的每个统计数据的详细信息，只需双击所需的统计数据，您将看到一个新的工作表已经创建，其中有一个表格向您显示如何获得最终结果的详细信息。例如，如果您双击苹果的数量，您将看到下表:

![Details Pivot Table-Edureka](img/d3f656769f00ba454683cae737d0662c.png)

如你所见，罗杰和拉法在纽约有 26 个苹果，每个售价 500 美元。因此，所有苹果的最终接收数量为 1000。

## **排序:**

如果你想按升序或降序排列表格，你可以这样做:

*   创建数据透视表，然后右键单击金额
*   从列表中选择排序，并在最大到最小和最小到最大选项之间进行选择

![Sort Excel-Edureka](img/545add0c47f2e763e25703d0a6f14ae0.png)

正如您在图中看到的，数据透视表已经排序，以显示每个供应商收到的金额，从最低金额到最高金额。

## **值字段设置:**

正如您在前面的示例中所看到的，Excel 通过合计每一项的金额来显示总计。如果您想更改此项以便查看其他数字，如平均值、项目计数、产品等，只需右键单击任何金额值的总和，并选择**值字段设置**选项。您将出现以下对话框:

![Change value field-Edureka](img/62e421891739099cee84bfa2f7798b2c.png)

您可以从给定列表中选择任何选项。例如，如果您选择计数，数据透视表将显示每个供应商名称在表中出现的次数，并在最后显示其总数。

![Change value field2-Edureka](img/915d3fedbe959917841e2de6e15137f3.png)

现在，如果您想查看这些名称出现的详细信息，请双击任何名称，您将看到在新创建的 Excel 表中为其创建了一个新表。例如，如果你双击拉法，你会看到下面的细节:

![Rafa Pivot Table-Edureka](img/09c4caf76bac2905dab0a76fedaaa5a1.png)

## **分组:**

Excel 允许您在创建数据透视表时对相似的数据进行分组。为了对一些数据进行分组，只需选择该数据，然后右键单击它，并从列表中单击 **Group** 选项。

请看下图，我将苹果和香蕉归入第一组，将橘子和菠萝归入第二组，并计算了每组的数量。

![Group Pivot tables-Edureka](img/5636d31009decf19c107393ea47da262.png)

如果不想看到每个组中的单个对象，只需从右键菜单中的展开/折叠选项中选择折叠即可折叠该组。

![Collapse group-Edureka](img/5a8385ef5ec615c7e8d3fabf352eedb2.png)

## **添加多个字段:**

Excel 还允许您向“数据透视表字段”窗口中的每个区域添加多个字段。您所要做的就是在相应的区域中拖放所需的字段。

例如，如果要查看每个城市中销售的商品数量，只需将“商品和数量”字段拖到行区域，将“城市”字段拖到列区域。这样做时，生成的数据透视表将如下所示:

![Multiple rows-Excel Pivot Tables Tutorial-Edureka](img/b8174eddda9bbacf4bca9de2d5897e4b.png)

类似地，将多个字段添加到列和值区域。在下一个示例中，我向值区域添加了另一个金额字段。为此，只需第二次将 Amount 字段拖放到 values 区域。您将看到另一个 Sum of Amount 字段将被创建，Excel 也将相应地填充这些列。在下面的示例中，我已经更改了第二个值字段，以计算每个项目出现的次数以及每个城市的数量。

![Multiple Values-Edureka](img/349634b4a3788b6bb56806abd0db3810.png)

## **格式化数据透视表:**

要设置数据透视表的格式，请单击功能区栏中的“设计展示”。从这里，您将能够按照自己的意愿配置该表。例如，让我更改表的设计并删除表中的总计。此外，我将为数据透视表创建带状行。

![format pivot table-Excel Pivot Tables Tutorial-Edureka](img/aef0a982ab878f1e836e3fdc424c5f40.png)

你可以尝试许多其他的选择。

## **为数据透视表创建数据透视图:**

数据透视表可以用来非常容易地创建频率分布表，可以使用数据透视表图表来表示。因此，如果您想为上限和下限之间的金额字段创建一个数据透视表，请按照以下步骤操作:

*   将金额字段拖动到行区域，并再次拖动到值区域 ![PC-Excel-Edureka](img/39f75a66410251b090def4c2c57ef3c6.png)
*   根据您的喜好分组价格范围 ![Group PC-Edureka](img/a1b40fd2c41be9516470e127b92873f0.png) ![Group PC2-Edureka](img/91d186bc5cd39498bb84917f721429ca.png)

选择 Home 选项卡中的 Pivot Chart 选项，然后您将看到一个窗口，允许您在各种类型的图表之间进行选择。在下面给出的例子中，我选择了条形类型:

![Pivot Chart-Edureka](img/efde83fab84733e42e29bb88e194c475.png)

这就把我们带到了 Excel 数据透视表教程这篇文章的结尾。我希望你清楚已经与你分享的一切。 ***确保你尽可能多地练习，恢复你的经验。***

*要深入了解任何趋势技术及其各种应用，您可以注册参加实时 **[Edureka MS Excel 在线培训](https://www.edureka.co/advanced-ms-excel-self-paced)** ，24/7 全天候支持和终身访问。*

此外，如果你想提高自己的能力，学习更多关于数据可视化的知识，成为商业智能专家。现在，请浏览我们的 [Tableau 培训课程](https://www.edureka.co/tableau-certification-training)，获取您应该了解的关于这款强大软件的所有信息。