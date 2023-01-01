# SQL Datetime:您需要知道的一切

> 原文：<https://www.edureka.co/blog/sql-datetime/>

有时，在 SQL 中处理日期和时间会非常棘手。虽然日期和时间实际上是完全不同的数据类型，但它们通常合并为 datetime 日期数据类型。 **SQL 日期和时间**本身非常简单，但是将两者结合起来可能是最痛苦的任务之一。在本文中，将详细了解 SQL datetime 类型。

*   [什么是日期时间数据类型？](#datetime)
*   [日期时间描述](#description)
*   [将其他日期和时间类型转换为日期时间数据类型](#converting)

## **什么是日期时间数据类型？**

在 SQL 中， **datetime** date 数据类型用于包含日期和时间的值。 **[微软](https://technet.microsoft.com/en-us/library/ms187819(v=sql.105).aspx)将其定义为一个*日期和一天中基于 24 小时制的时间*。**

特别是 SQL，有许多数据类型结合了日期和时间表示，使事情变得更加复杂。使用最广泛的是 DATETIME，因为它从 SQL 的早期版本就存在了。SQL 检索并以“YYYY-MM-DD hh: mm: ss”格式显示日期时间值。支持的范围是“1753-01-01 00:00:00”到“9999-12-31 23:59:59.997”。让我们更详细地研究日期时间类型。

## **日期时间描述**

请查看下表以了解有关 SQL 日期时间类型的更多信息。

| **属性** | **值** |
| **语法** | 日期时间 |
| **用途** | 声明@MyDatetime 日期时间创建表 Table1(列 1 日期时间 ) |
| **格式** | YYYY-MM-DD 时:分:秒 |
| **时间范围** | 00:00:00 到 23:59:59.997 |
| **元素范围** | 

*   YYYY is a four-digit number from 1753 to 9999, representing a year.
*   MM is a two-digit number, ranging from 01 to 12, representing a month in a specified year.
*   DD is a two-digit number, ranging from 01 to 31 according to the month, and represents a day in the specified month.
*   Hh is a two-digit number, ranging from 00 to 23, representing hours.
*   Mm is a two-digit number, ranging from 00 to 59, representing minutes.
*   Ss is a two-digit number, ranging from 00 to 59, representing seconds.
*   N* is zero to three digits, ranging from 0 to 999, representing fractional seconds.

 |
| **存储大小** | 8 字节 |
| **默认值** | 1900-01-01 00:00:00 |
| **日历** | 公历(包括完整的年份范围。) |

**注意:**以上细节适用于 Transact-SQL 和 SQL Server 中的 datetime 类型。

所以，这就是 SQL 中的 **datetime** 。但是，如果您有其他日期& 时间类型，并且您必须将它们转换成**日期时间**类型，您会怎么做呢？

## **将其他日期和时间类型转换为日期时间数据类型**

SQL 中的 **datetime** 数据类型包括日期和时间，有 3 位小数秒部分。其精度四舍五入到 0.000 秒、0.003 秒或 0.007 秒的增量。因此，当您将一个**日期**或**时间**值转换为**日期时间**时，额外的信息会添加到该值中。这是因为**日期时间**数据类型包含日期和时间。文章的这一部分解释了当其他**日期和时间**数据类型转换为**日期时间**数据类型时会发生什么。

### **示例 1:日期和日期时间之间的隐式转换**

```
DECLARE @date date = '2020-12-01';  
DECLARE @datetime datetime = @date;
```

**结果**

```

@datetime               @date  
------------------------- ----------  
2016-12-21 00:00:00.000 2016-12-21  

```

### **示例 2:使用 CAST()** 在日期和日期时间之间进行隐式转换

```
DECLARE @thedate date = '2020-12-01'
SELECT 
  @thedate AS 'date',
  CAST(@thedate AS datetime) AS 'datetime';
```

**结果**

```

@datetime               @date  
------------------------- ----------  
2016-12-21 00:00:00.000 2016-12-21  

```

### **示例 3:从 smalldatetime 到 datetime 的隐式转换**

从 s **malldatetime** 类型转换时，会复制小时和分钟。秒和小数秒被设置为值 0。以下代码显示了将 **smalldatetime** 值转换为 **datetime** 值的结果。

```
DECLARE @smalldatetime smalldatetime = '2020-12-01 12:32';  
DECLARE @datetime datetime = @smalldatetime;  

SELECT @datetime AS '@datetime', @smalldatetime AS '@smalldatetime'; 
```

**结果**

```
@datetime               @smalldatetime  
------------------------- -----------------------  
2016-12-01 12:32:00.000 2016-12-01 12:32:00 
```

同样，您可以隐式地或者使用 **cast()** 和 **convert()** 方法将其他**日期&时间**类型转换为**数据时间**类型。作为参考，请查看下表以熟悉所有日期和时间类型的格式。

| **数据类型** | **例子** |
| **时间** | 12:35:29\. 1234567 |
| **日期** | 2007-05-08 |
| **小型日期时间** | 2007-05-08 12:35:00 |
| **datetime** | 2007-05-08 12:35:29.123 |
| **datetime2** | 2007-05-08 12:35:29\. 1234567 |
| **datetimeoffset** | 2007-05-08 12:35:29.1234567 +12:15 |

说到这里，我们来到了本文的结尾。我希望你清楚这里讨论的内容。 ***确保你尽可能多的练习，恢复你的经验。***

*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本“SQL 中的过程”的注释部分提及它；文章，我们会回来找你。