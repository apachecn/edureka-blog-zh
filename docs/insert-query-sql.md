# 插入查询 SQL–关于插入语句您需要知道的一切

> 原文：<https://www.edureka.co/blog/insert-query-sql/>

[结构化查询语言或俗称 SQL](https://www.edureka.co/blog/sql-commands) ，是关系数据库中最流行的语言之一。这种语言用于处理数据库，并在查询的帮助下操作数据。一个这样的查询是**插入查询**。所以，在这篇关于插入查询 SQL 的文章中，您将按以下顺序理解 INSERT INTO 语句:

![SQL - Insert Query SQL - Edureka](img/da752ce4512e8070f2ce0a64cdf669c5.png)

## **什么是 SQL 中的插入查询？**

SQL INSERT INTO 语句用于为数据库向表中添加新的元组。在这个 SQL 查询的帮助下，您可以将数据插入特定的列或所有列。此外，您可以将数据从另一个表插入到特定表中的一行或多行。那么，现在你知道什么是 SQL 中的插入查询，让我们向前看，看看这个查询的语法。

## **插入语法**

有两种方法可以实现插入查询。

### **带列名和值**

```
INSERT INTO Tablename (Column1, Column2, Column3, ...,ColumnN) VALUES (Value1, Value2, Value3, ...);

```

### **带值**

```
INSERT INTO Tablename VALUES (Value1, Value2, Value3, ...);

```

**注意:** 当您使用第二种方法时，您必须确保这些值的顺序与列名的顺序相同。

现在，您已经知道了 INSERT 语句的语法，接下来，在这篇关于 Insert query SQL 的文章中，让我们看一个例子。

## **INSERT 语句示例**

考虑下面的表，表名为 SampleData:

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| one | 桑杰（男子名） | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | thirty thousand |
| Two | 瑞亚 | Thirty | Nine billion nine hundred and seventy-seven million seven hundred and forty-two thousand two hundred and thirty-four | One hundred and fifty thousand |
| three | Vipul | Thirty-two | Nine billion eight hundred and ninety-eight million nine hundred and eighty-nine thousand eight hundred and ninety-eight | One hundred and seventy-five thousand |
| four | 希姆兰 | Twenty-eight | Nine billion nine hundred and fifty-five million five hundred and fifty-five thousand four hundred and thirty-three | Sixty-five thousand |
| five | 阿克萨里 | Thirty-four | Nine billion six hundred and forty-six million four hundred and thirty-four thousand four hundred and thirty-seven | Two hundred thousand |

现在，假设您想在这个表中插入一行。然后，你可以以下面的方式使用上面的语法:

```
#With column names and values
INSERT INTO SampleData(ID, Name, Age, PhoneNumber, Salary) VALUES ('6', 'Rohit','25', '9924388761', '35000');
#With values only
INSERT INTO SampleData VALUES ('6', 'Rohit','25', '9924388761', '35000');

```

一旦您执行了查询，您将会看到下面的输出:

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| one | 桑杰（男子名） | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | thirty thousand |
| Two | 瑞亚 | Thirty | Nine billion nine hundred and seventy-seven million seven hundred and forty-two thousand two hundred and thirty-four | One hundred and fifty thousand |
| three | Vipul | Thirty-two | Nine billion eight hundred and ninety-eight million nine hundred and eighty-nine thousand eight hundred and ninety-eight | One hundred and seventy-five thousand |
| four | 希姆兰 | Twenty-eight | Nine billion nine hundred and fifty-five million five hundred and fifty-five thousand four hundred and thirty-three | Sixty-five thousand |
| five | 阿克萨里 | Thirty-four | Nine billion six hundred and forty-six million four hundred and thirty-four thousand four hundred and thirty-seven | Two hundred thousand |
| six | rohit！rohit | Twenty-five | Nine billion nine hundred and twenty-four million three hundred and eighty-eight thousand seven hundred and sixty-one | Thirty-five thousand |

嗯，这是关于向表中插入一条新记录。但是，在其他一些场景中，您可能会希望使用 SQL。场景可以如下:

*   如何从表格中复制特定的行？
*   将一个表的所有列插入到另一个表的方法是什么？
*   如何将表格中的特定列插入到另一个表格中？

这些问题的答案是使用 SELECT 语句和 INSERT 语句。 所以，接下来在这篇关于插入查询的 SQL 文章中，让我们了解如何在 INSERT INTO 中使用 SELECT 语句。

## **在插入到**中使用选择查询

SELECT 查询与 INSERT INTO 语句一起使用，从另一个表中选择数据。以下是在 SQL 中使用带有插入查询的 SELECT 语句的各种方法:

1.  从表格中复制特定的行
2.  中的插入表格的所有列
3.  插入表格的特定列

### **从表格中复制特定的行**

通过使用带有 WHERE 子句的 SELECT 语句，可以将一个表中的一组特定行插入到另一个表中。

#### **语法:**

```
INSERT INTO Table1 SELECT * FROM Table2 WHERE condition;

```

这里，您试图根据一个条件将表 2 中的值插入到表 1 中。

#### **举例:**

考虑一个例子，你必须根据条件 Age > 30 从上面的表(SampleData)插入几行到一个新表(New_Data)

```
INSERT INTO New_Data SELECT * FROM SampleData WHERE Age &amp;amp;amp;gt; 30;

```

**输出:**

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| three | Vipul | Thirty-two | Nine billion eight hundred and ninety-eight million nine hundred and eighty-nine thousand eight hundred and ninety-eight | One hundred and seventy-five thousand |
| five | 阿克萨里 | Thirty-four | Nine billion six hundred and forty-six million four hundred and thirty-four thousand four hundred and thirty-seven | Two hundred thousand |

### **中的**插入表格的所有列****

通过在 INSERT INTO 查询中使用星号(*)，可以将一个表中的所有列插入到另一个表中。

#### **语法:**

```
INSERT INTO Table1 SELECT * FROM Table2;

```

在这里，您试图插入表 2 到表 1 中所有列值。

#### **举例:**

考虑一个例子，您必须将上面的表(SampleData)中的所有列插入到一个新表(ExampleData)中。 另外，假设 ExampleData 已经有了以下数据:

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| seven | Suhas | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and thirty-nine | Forty-two thousand |
| eight | 米娜 | Thirty-one | Nine billion seven hundred and sixty-five million four hundred and twelve thousand three hundred and forty-five | One hundred and ninety-two thousand |

现在，执行以下查询，将 SampleData 中的所有列和行插入到上表中。

```
INSERT INTO ExampleData SELECT * FROM SampleData;

```

**输出:**

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| seven | Suhas | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and thirty-nine | Forty-two thousand |
| eight | 米娜 | Thirty-one | Nine billion seven hundred and sixty-five million four hundred and twelve thousand three hundred and forty-five | One hundred and ninety-two thousand |
| one | 桑杰（男子名） | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | thirty thousand |
| Two | 瑞亚 | Thirty | Nine billion nine hundred and seventy-seven million seven hundred and forty-two thousand two hundred and thirty-four | One hundred and fifty thousand |
| three | Vipul | Thirty-two | Nine billion eight hundred and ninety-eight million nine hundred and eighty-nine thousand eight hundred and ninety-eight | One hundred and seventy-five thousand |
| four | 希姆兰 | Twenty-eight | Nine billion nine hundred and fifty-five million five hundred and fifty-five thousand four hundred and thirty-three | Sixty-five thousand |
| five | 阿克萨里 | Thirty-four | Nine billion six hundred and forty-six million four hundred and thirty-four thousand four hundred and thirty-seven | Two hundred thousand |

### **插入表格的特定列**

通过使用 SELECT 语句，可以将一组特定的列从一个表插入到另一个表中。

#### **语法:**

```
INSERT INTO Table1(Column_Names) SELECT Column_Names FROM Table2;

```

在这里，您试图将特定的列从表 2 插入到表 1。

#### **举例:**

考虑一个例子，你必须从表(ExampleData)向表(SampleData)插入列(ID，Name)。

```
INSERT INTO SampleData(ID,Name) SELECT ID, Name, FROM ExampleData;

```

#### **输出:**

| **ID** | **名称** | **年龄** | **电话号码** | **工资** |
| one | 桑杰（男子名） | Twenty-three | Nine billion eight hundred and seventy-six million five hundred and forty-three thousand two hundred and ten | thirty thousand |
| Two | 瑞亚 | Thirty | Nine billion nine hundred and seventy-seven million seven hundred and forty-two thousand two hundred and thirty-four | One hundred and fifty thousand |
| three | Vipul | Thirty-two | Nine billion eight hundred and ninety-eight million nine hundred and eighty-nine thousand eight hundred and ninety-eight | One hundred and seventy-five thousand |
| four | 希姆兰 | Twenty-eight | Nine billion nine hundred and fifty-five million five hundred and fifty-five thousand four hundred and thirty-three | Sixty-five thousand |
| five | 阿克萨里 | Thirty-four | Nine billion six hundred and forty-six million four hundred and thirty-four thousand four hundred and thirty-seven | Two hundred thousand |
| seven | Suhas | 空 | 空 | 空 |
| eight | 米娜 | 空 | 空 | 空 |

至此，我们结束了这篇关于插入查询 SQL 的文章。我希望您了解如何在 SQL 中使用 INSERT INTO 查询。 我们已经看到了使用插入查询的各种方法。 本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。

*有问题吗？请在“**插入查询 SQL** ”的评论部分提及，我会回复您。*