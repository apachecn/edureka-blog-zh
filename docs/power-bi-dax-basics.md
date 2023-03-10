# 从 DAX 的 Power BI 开始

> 原文：<https://www.edureka.co/blog/power-bi-dax-basics/>

这个博客主要是为刚接触 [***Power BI 桌面***](https://www.edureka.co/blog/power-bi-desktop/) 的用户设计的，旨在给你一个快速简单的公式语言 ***【数据分析表达式】*** 。如果你熟悉[***MS Excel***](https://www.edureka.co/blog/tutorial-on-advanced-excel-formulas/)或[***SQL***](https://www.edureka.co/blog/sql-commands)中的函数，这篇***Power BI DAX Basics***文章中的许多公式都会出现与你类似的情况。

说到这里，这里是概念，它们构成了所有 [Power BI 课程大纲](https://www.edureka.co/power-bi-certification-training)不可或缺的一部分，学完这些你应该对 DAX 中最基本的概念有了很好的理解。

*   [**力量 BI DAX 基础知识:DAX 是什么？**](#whatisdax)
*   [](#howdoesitwork)**[异能毕达克斯基础知识:如何工作？](#whatisdax)**
    *   [**语法**](#syntax)
    *   [**语境**](#context)
    *   [**功能**](#functions)
*   [](#calculatedcolumnsandmeasures)**[力量毕达克斯基础知识:计算列&措施](#whatisdax)**
    *   [**计算列**](#calculatedcolumns)
    *   [**措施** 措施](#measures)
    *   [**计算列 vs**](#calculatedcolumnsvsmeasures)
*   [](#typesoffunctionsinpowerbidax)**[Power BI DAX 基础知识:DAX](#whatisdax)** 中的函数类型
    *   [**聚合函数**](#aggregatefunctions)
    *   [**计数功能**](#countfunctions)
    *   [**日期时间功能**](#datetimefunctions)
    *   [**数学函数**](#mathematicalfunctions)
    *   [**逻辑函数**](#logicalfunctions)
    *   [**信息功能**](#informationfunctions)
    *   [**文字功能**](#textfunctions)
*   [](#creatingapowerbidaxmeasure)**[异能毕达克斯基础知识:创造你的第一招](#whatisdax)**

## **Power BI DAX 基础知识:DAX 是什么？**

所以，我们先从动力 BI DAX 的基础开始，好吗？

使用 Power BI 桌面创建报告非常容易，可以立即显示有价值的见解。

但是，如果您需要分析所有不同日期范围内所有产品类别的增长百分比，该怎么办呢？或者，你需要计算你的公司相对于市场巨头的年增长？

学习 DAX 将帮助你最大限度地利用你的 [***图表和可视化***](https://www.edureka.co/blog/power-bi-reports/) ，解决真实的商业问题。

***DAX 由函数、运算符和常数组成，它们可以放入公式中，借助模型中已有的数据来计算值。***

Power BI DAX 包括一个超过 200 个函数、运算符和构造的库。它的库提供了巨大的灵活性，可以为任何数据分析需求创建计算结果的方法。

[https://www.youtube.com/embed/FMR0ZVkJtDM](https://www.youtube.com/embed/FMR0ZVkJtDM)

## **Power BI DAX 基础知识:如何工作？**

首先，让我给你解释一下这是如何工作的。在很大程度上，我们将围绕三个基本概念来构建我们对 Power BI DAX 的理解: ***语法*** ， ***上下文*** ，以及 ***功能*** 。

当然，这里还有其他重要的概念，但是理解这三个概念将为你建立技能提供最好的基础。

### **语法**

***语法*** 由组成公式的各种组件以及公式的书写方式组成。L 看看这个简单的 DAX 公式。

当试图理解一个 DAX 公式时，将每个元素分解成你每天想和说的语言通常是有帮助的。因此，该公式包括以下语法元素:

**![Syntax - Power BI DAX - Edureka](img/ee58f3f4c0ff18e8297b8e23656ad8cc.png)**

**总销售额**是衡量名称。

**二世。****等号运算符(=)** 表示公式的开始。

**三世。** **SUM** 将列中的所有数字相加，**Sales【Sales amount】**。

**四世。**有这些**括号** **()** 将包含一个或多个参数的表达式括起来。所有函数都需要至少一个参数。

**销售**是引用的表。

**六。**一个**参数**将一个值传递给一个函数。被引用的列**【sales amount】**是一个参数，SUM 函数通过它知道必须对哪一列进行合计。

简单来说，你可以把它读作，**“*对于名为“总销售额”的度量，计算(=)销售额表中[销售额]列中值的总和。”***

*♠power bi DAX 编辑器包括一个建议功能，通过向您建议正确的元素来帮助您创建语法正确的公式。*

### **语境**

***上下文*** 是 3 个 DAX 概念中最重要的一个。当一个人谈到上下文时，这可能指两种类型之一； ***行上下文*** 和 ***过滤上下文*** 。

主要用于当谈到*措施*时， **行-上下文** 最容易被认为是当前行。每当公式中有一个函数应用筛选器来标识表中的单个行时，它都适用。

过滤上下文比行上下文更难理解一点。您可以很容易地将过滤器上下文视为在计算中应用的一个或多个过滤器。行上下文中不存在过滤器上下文。相反，它是前者的补充。看下面的 DAX 公式。

该公式包括以下语法元素:

**![Context - Power BI DAX - Edureka](img/c8027f4d6fb91adf487590047c5f25ba.png)**

**一、**措施名称**店铺销售额**。

**二世。****等号运算符(=)** 表示公式的开始。

**三世。****计算**函数计算一个表达式，作为一个参数。

**四世。**括号 **()** 将包含一个或多个自变量的表达式括起来。

**V.** A measure **【总销售额】**同表为表达式。

**六。**一个**逗号(，)**将第一个表达式参数与过滤器参数分开。

**七世。**完全限定的引用列**频道【频道名称】**是我们的行上下文。该列中的每一行都指定了一个渠道、商店、在线等。

**VIII。**、**存储的特定值**被用作过滤器。这是我们的过滤上下文。

***此公式确保** **的** **总销售额仅针对“渠道名称”列中值为“商店”的行进行计算，作为一个过滤器。***

### **功能**

***函数*** 是预定义的、结构化的、有序的公式。他们使用传递给他们的*参数*进行计算。这些参数可以是数字、文本、逻辑值或其他函数。

## **力量毕达克斯基础知识:** **计算列&措施**

在这篇博客中，我们将关注在计算中使用的幂 BI DAX 公式，在*测量*和*计算栏*中。

### **计算列**

在 Power BI 桌面上创建数据模型时，您可以通过创建新列来扩展表格。列的内容由 DAX 表达式定义，逐行计算或在表中当前行的上下文中计算。

然而，在 DAX 的数据模型中，所有计算列都占用内存空间，并且是在表处理期间计算的。

这种行为有助于获得更好的用户体验，但它使用了宝贵的 RAM，因此在生产中是一个坏习惯，因为每个中间计算都存储在 RAM 中，浪费了宝贵的空间。

### **措施**

在 DAX 模型中，还有另一种定义计算的方法，如果您需要对聚合值而不是逐行进行操作，这种方法会很有用。这些计算是测量。DAX 的需求之一是需要在表中定义一个度量。但是，该度量并不真正属于表。因此，您可以将度量从一个表移动到另一个表，而不会失去其功能。

### **计算列 vs 计量**

度量值和计算列都使用 DAX 表达式。区别在于评价的语境。度量值是在报表或 DAX 查询中计算的单元格的上下文中计算的，而计算列是在它所属的表中的行级别计算的。

即使看起来很相似，计算出的列和度量值之间也有很大的区别。计算列的值是在数据刷新期间计算的，并使用当前行作为上下文；它不依赖于报告中的用户交互。

因此，每当你想做以下事情时，你必须定义一个计算列；

*   将计算结果放在切片器中，或者在数据透视表的行或列中查看结果(相对于值区域)，或者在图表的轴中查看结果，或者将结果用作 DAX 查询中的筛选条件。
*   定义一个严格绑定到当前行的表达式。例如，Price * Quantity 不能计算两列的平均值或总和。
*   对文本或数字进行分类。例如，度量值的范围。

度量对当前上下文定义的数据聚合进行操作，这取决于报表中应用的筛选器，如数据透视表中的切片器、行和列选择，或应用于图表的轴和筛选器。

因此，每当您想要显示反映用户选择的结果计算值时，您必须定义一个度量，例如:

*   当你计算某一选定数据的利润百分比时。
*   当您计算一种产品相对于所有产品的比率，但保留按年份和地区的过滤器时。

## **Power BI DAX 基础知识:****DAX 中的函数类型**

## **1。聚合函数**

### **MIN**

此 DAX 函数 r 返回一列中或两个标量表达式之间的最小数值。

**语法**

`MIN(<column>)`

**例如**

`=MIN([ResellerMargin])`

### **矿山**

这个 DAX 函数 r 返回一列中的最小值，包括任何逻辑值和表示为文本的数字。

**语法**

`MINA(<column>)`

**例如**

`=MINA(([PostalCode])`

### **疯丫头**

这个 DAX 函数返回对表中每一行的表达式求值得到的最小数值。

**语法**

`MINX(<table>, < expression evaluated for each row>)`

**例如**

```
`=MINX( FILTER(InternetSales, InternetSales[SalesTerritoryKey] = 5), InternetSales[Freight] + InternetSales[TaxAmt])` 
```

### **MAX**

这个 DAX 函数 r 返回一列中的最大值，包括任何逻辑值和表示为文本的数字。

**语法**

`MAX(<column>)`

**例如**

`=MAX([ResellerMargin])`

### **t1【最大值】T2**

这个 DAX 函数 r 返回一列中的最大值，包括任何逻辑值和表示为文本的数字。

**语法**

`MAXA(<column>)`

**例如**

`=MAXA(([PostalCode])`

### **MAXX**

这个 DAX 函数返回对表中每一行的表达式求值得到的最大数值。

**语法**

`MAXX(<table>, < expression evaluated for each row>)`

**例如**

```
`=MAXX( FILTER(InternetSales, InternetSales[SalesTerritoryKey] = 5), InternetSales[Freight] + InternetSales[TaxAmt])` 
```

### **总和**

这个 DAX 函数 a dds 一列中的所有数字。

**语法**

`SUM(<column>)`

**例如**

`=SUM(Sales[Amt])`

### **平均值**

这个 DAX 函数 r 返回一列中数值的算术平均值。

**语法**

`AVERAGE(<column>)`

**例如**

`=AVERAGE(InternetSales[ExtendedSalesAmount])`

### **SUMX**

这个 DAX 函数 r 返回一个表达式对表中每一行计算的总和。

**语法**

`SUMX(<table>, <expression evaluated for each row>)`

**例如**

`=SUMX(FILTER(InternetSales, InternetSales[SalesTerritoryID]=5),[Freight])`

### **平均值 X**

这个 DAX 函数 c 计算一组表达式在一个表上的算术平均值。【T2

**语法**

`AVERAGEX(<table>, <expression evaluated for each row>)`

**例如**

`=AVERAGEX(InternetSales, InternetSales[Freight]+ InternetSales[TaxAmt])`

## **2。计数功能**

### 分开计数

这是一个 DAX 函数，用于返回一列中项目的非重复计数。因此，如果同一个项目有多个编号，该函数将把它计为一个项目。

**语法**

`DISTINCTCOUNT(<column>)`

**例如**

`=DISTINCTCOUNT(ResellerSales_USD[SalesOrderNumber])`

### **计数**

这是一个 DAX 函数，用于返回一列中的项目数。因此，如果同一个项目有多个编号，该函数将把它计为单独的项目，而不是单个项目。

**语法**

`COUNT(<column>)`

**例句**

`=COUNT([ShipDate])`

### **COUNTA**

这是一个 DAX 函数，用于返回非空列中的项目数。

**语法**

`COUNTA(<column>)`

**例如**

`=COUNTA('Reseller'[Phone])`

### **count rows**

这是一个 DAX 函数，计算指定表格或由表达式定义的表格中的行数。

**语法**

`COUNTROWS(<table>)`

**例如**

`=COUNTROWS('Orders')`

### **count blank**

这是一个 DAX 函数，计算一列中空白单元格的数量。【T2

**语法**

`COUNTBLANK(<column>)`

**例如**

`=COUNTBLANK(Reseller[BankName])`

## **3。日期时间功能**

### **日期**

这个 DAX 函数 r 以日期-时间格式返回指定的日期。

**语法**

`DATE(<year>, <month>, <day>)`

**例如**

`=DATE(2019,12,17)`

### **小时**

这个 DAX 函数 r 返回一个从 0 到 23(上午 12:00 到晚上 11:00)的指定小时数。

**语法**

`HOUR(<datetime>)`

**例如**

`=HOUR('Orders'[TransactionTime])`

### **今日**

这个 DAX 函数返回当前日期。

**语法**

`TODAY()`

### **现在**

此 DAX 函数 r 以日期时间格式返回当前日期和时间。

**语法**

`NOW()`

### **EOMONTH**

此 DAX 函数 r 以日期-时间格式返回一个月的最后一天的日期，在指定的月数之前或之后。【T2

**语法**

`EOMONTH(<start_date>, <months>)`

**例如**

`=EOMONTH("March 3, 2008",1.5)`

## **4。数学函数**

### **腹肌**

这个 DAX 函数 r 返回给定数字的绝对值。

**语法**

`ABS(<number>)`

**例如**

`=ABS([DealerPrice]-[ListPrice])`

### **EXP**

这个 DAX 函数 r 返回 e 的给定数字的幂。

**语法**

`EXP(<number>)`

**例如**

`=EXP([Power])`

### **事实 **

这个 DAX 函数 r 返回一个数的阶乘。

**语法**

`FACT(<number>)`

**例如**

`=FACT([Values])`

### **LN**

这个 DAX 函数 r 返回给定数字的自然对数。

**语法**

`LN(<number>)`

**例如**

`=LN([Values])`

### **日志**

此 DAX 函数 r 返回以给定数字为基数的对数。

**语法**

`LOG(<number>,<base>)`

**例如**

`All the following return the same result, 2.`

`=LOG(100,10)`

`=LOG(100)`

`=LOG10(100)`

### **π**

这个 DAX 函数 r 返回圆周率的值。

**语法**

`PI()`

### **力量**

这个 DAX 函数 r 返回第一个参数的值乘以第二个参数的幂。

**语法**

`POWER(<number>, <power>)`

**例如**

`=POWER(5,2)`

### **商**

这个 DAX 函数执行除法 r 返回商的整数部分。

**语法**

`QUOTIENT(<dividend>, <divisor>)`

**例如**

`=QUOTIENT(5,2)`

### **标志**

这个 DAX 函数返回一个给定数字的符号。

**语法**

`SIGN(<number>)`

**例如**

`=SIGN( ([Sale Price] - [Cost Price]) )`

### **SQRT**

这个 DAX 函数 r 返回给定数字的平方根。【T2

**语法**

`SQRT(<number>)`

**例如**

`=SQRT(25)`

## **5。逻辑功能**

### **和**

这个 DAX 函数对两个表达式执行逻辑 AND(合取)。对于和，要返回 true，必须满足指定的两个条件。

**语法**

`AND(<logical argument1>,<logical argument2>)`

**例如**

`=IF(AND(10 > 9, -10 < -1), "All true", "One or more false"`

`Because both conditions, passed as arguments, to the AND function are true, the formula returns "All True".`

### **或**

这个 DAX 函数对两个表达式执行逻辑或运算。要使或返回 true，必须满足指定的两个条件中的任何一个。

**语法**

`OR(<logical argument1>,<logical argument2>)`

**例如**

`=IF(OR(10 > 9, -10 >-1), "True", "False"`

`Because one of the conditions, passed as arguments, to the OR function is true, the formula returns "True".`

### **不是**

这个 DAX 函数对给定的表达式执行逻辑非运算。

**语法**

`NOT(<logical argument>)`

**例如**

`=NOT([CalculatedColumn1])`

`For each row in Calculated Column1, the NOT function returns the logical opposite of the given value.`

### **如果**

此 DAX 函数测试一系列输入，寻找满足参数中指定条件的输入。

**语法**

`IF(logical_test>,<value_if_true>, value_if_false)`

**例如**

`=IF([Calls]<200,"low",IF([Calls]<300,"medium","high"))`

### **IFERROR**

这个 DAX 函数 e 对一个表达式求值，如果表达式返回一个错误，则返回一个指定的值。【T2

**语法**

`IFERROR(value, value_if_error)`

**例如**

`=IFERROR(25/0,9999)`

## **6。信息功能**

### **为空白**

该 DAX 函数在 c 检查一个值是否为空后返回真或假。

**语法**

`ISBLANK(<value>)`

**例如**

`=IF( ISBLANK('CalculatedMeasures'[PreviousYearTotalSales]) , BLANK() , ( 'CalculatedMeasures'[Total Sales]-'CalculatedMeasures'[PreviousYearTotalSales] ) /'CalculatedMeasures'[PreviousYearTotalSales])`

### **ISNUMBER**

这个 DAX 函数在 c 检查一个值是否为数字后返回真或假。

**语法**

`ISNUMBER(<value>)`

**例如**

`=IF(ISNUMBER(0), "Is number", "Is Not number")`

### **文字文字**

这个 DAX 函数在 c 检查一个值是否为文本后返回真或假。

**语法**

`ISTEXT(<value>)`

**例如**

`=IF(ISTEXT("text"), "Is Text", "Is Non-Text")`

### **是上下文**

这个 DAX 函数在 c 检查一个值是否为非文本后返回真或假。

**语法**

`ISNONTEXT(<value>)`

**例如**

`=IF(ISNONTEXT("text"), "Is Non-Text", "Is Text")`

### **ISERROR**

这个 DAX 函数在 c 检查一个值是否错误后返回真或假。

**语法**

`ISERROE(<value>)`

**例如**

`=IF( ISERROR( SUM('ResellerSales_USD'[SalesAmount_USD]) /SUM('InternetSales_USD'[SalesAmount_USD]) ) , BLANK() , SUM('ResellerSales_USD'[SalesAmount_USD]) /SUM('InternetSales_USD'[SalesAmount_USD]) )`

## **7。文字功能**

### **串接**

这个 DAX 函数 j 将两个文本字符串连接成一个。

**语法**

`CONCATENATE(<text1>, <text2>)`

**例如**

`=CONCATENATE("Hello ", "World")`

### **concatenax**

这个 DAX 函数是一个表达式对表中每一行求值的结果。

**语法**

`CONCATENATEX(<table>, <expression>, [delimiter])`

**例如**

`=CONCATENATEX(Employees, [FirstName] & “ “ & [LastName], “,”)`

### **固定**

这个 DAX 函数 r 将一个数字舍入到指定的小数位数，并将结果作为文本返回。

**语法**

`FIXED(<number>, <decimals>, <no_commas>)`

**例如**

`=FIXED([PctCost],3,1)`

### **替换**

此 DAX 函数根据您指定的字符数，用不同的文本字符串替换部分文本字符串。

**语法**

`REPLACE(<old_text>, <start_num>, <num_chars>, <new_text>)`

**例如**

`=REPLACE('New Products'[Product Code],1,2,"OB")`

### **搜索**

这个 DAX 函数 r 返回一个特定文本字符串第一次出现的字符数。

**语法**

`SEARCH(<find_text>, <within_text>[, [<start_num>][, <NotFoundValue>]])`

**例如**

`=SEARCH("n","printer")`

`The formula returns 4 because "n" is the fourth character in the word "printer."`

### **上层**

这个 DAX 函数返回一个全大写的文本字符串。【T2

**语法**

`UPPER (<text>)`

**例如**

`=UPPER(['New Products'[Product Code])`

## **异能毕达克斯基础知识:创造你的第一招**

**先决条件:**你需要打开 ***这个给定权力的 BI 桌面文件*** 。

因为我假设这将是你的第一次，所以我会写得很详细，让你跟着读。

1.  在**报表视图**的字段列表中，右键点击**销售**表，后面是**新度量**。

2.  通过在*公式栏*中键入新的度量名称**上一季度销售额**，替换**度量**。

3.  在这个公式中，你要使用**计算**函数。所以，在等号后面，键入前几个字母 **CAL** ，然后双击想要使用的功能。

4.  **CALCULATE 函数至少有两个参数。**第一个是要计算的表达式，第二个是*过滤器*。

5.  在左**括号** **(** 对于**计算**函数，键入 **SUM** 后跟另一个左括号 **(** 以将参数传递给 **SUM** 函数。

6.  开始输入 **Sal** ，然后选择 **Sales【销售额】**，后面是右括号 **)** 。这是我们的**计算**函数的第一个表达式参数。

7.  键入一个**逗号(，)**，后跟一个空格以指定第一个过滤器，然后键入**前一季度**。这将是我们的过滤器。

8.  您将使用**上一季度**时间智能函数过滤上一季度的**总和**结果。

9.  在左括号 **(** 对于 PREVIOUSQUARTER 函数，键入**日历【日期】**。

10.  **previous quarter**函数有一个参数，即包含连续日期范围的列。在我们的例子中，这是日历表中的**日期键**列。

11.  通过键入两个闭括号**)**，确保传递给前一季度的参数和计算函数都被关闭。

12.  您的公式现在应该看起来像下面这样； **上一季度销售额= CALCULATE(SUM(Sales[Sales amount]))、上一季度(Calendar[DateKey])**

13.  单击公式栏中的复选标记或按 Enter 确认公式。

一旦你将它添加到你的模型中，瞧！您刚刚使用 DAX 创建了一个度量，而且不是一个简单的度量。

这个公式的作用是**根据报表中应用的过滤器计算上一季度的总销售额。**

因此，让我们假设我们必须将**销售额**和我们新的**上一季度销售额**放在一个图表中，然后添加**年**和**季度**作为*切片器，*我们会得到类似下面的结果；

*![Measure - Power BI DAX - Edureka](img/bdac2eba3c078f73ea8783283e7910fa.png)*

*现在，您已经对 Power BI DAX 中的概念有了基本的了解，您可以开始为自己的度量创建 DAX 公式了。的确，学习起来可能有点棘手，但是 DAX 已经存在好几年了，而且网上有很多可用的资源。通读这篇博客并做一点实验后，你可以学习通过 Power BI DAX 找到商业解决方案。*

如果你有兴趣学习 Power BI 并获得认证，那么你可以查看我们在班加罗尔的 [Power BI 课程](https://www.edureka.co/power-bi-certification-training-bangalore)或达拉斯的 [Power BI 课程](https://www.edureka.co/power-bi-certification-training-dallas)。掌握所有的商务智能概念，增加你在顶级公司工作的机会。