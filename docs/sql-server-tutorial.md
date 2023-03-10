# SQL Server 教程-掌握 Transact-SQL 所需的一切

> 原文：<https://www.edureka.co/blog/sql-server-tutorial>

在当今市场中，每天都会产生海量数据，了解如何处理数据非常重要。SQL Server 是微软为处理数据而开发的集成环境。 在这篇关于 SQL Server 教程的文章中，您将学习到探索数据库所需的所有操作和命令。

为了让你更好的理解，我把博客分成了以下几类:

| **命令** | **描述** |
| **数据定义语言命令(DDL)** | 这组命令用来定义一个数据库。 |
| **数据操纵语言命令(DML)** | 操作命令用于操作数据库中的数据。 |
| **数据控制语言命令(DCL)** | 这组命令处理数据库系统的许可、权利和其他控制。 |
| **事务控制语言命令(TCL)** | 这些命令用来  处理数据库的事务。 |

除了命令之外，本文还介绍了以下主题:

![MS SQL Server - SQL Server Tutorial - Edureka](img/b993af6a2b9b0b0f13f9b6f7c3811810.png)

1.  [什么是 SQL Server？](#whatissqlserver)
2.  [安装 SQL Server](#install)
3.  [使用 SSMS 连接到 SQL Server](#connectusingssms)
4.  [访问数据库引擎](#accessdatabaseengine)
5.  [SQL Server 架构](#sqlserverarchitecture)
6.  [SQL 中的注释](#comments)
7.  [SQL Server 数据类型](#datatypes)
8.  [数据库中的密钥](#keysindatabase)
9.  [数据库中的约束](#constraints)
10.  [操作员](#operators)
11.  [聚合函数](#aggregatefunctions)
12.  [用户自定义函数](#userdefinedfunctions)
13.  [嵌套查询](#nestedqueries)
14.  [归附](#joins)
15.  [循环](#loops)
16.  [存储过程](#storedprocedures)
17.  [异常处理](#exceptionhandling)

*** * *注意***** 在本 SQL Server 教程中，我打算以下面的数据库为 为例，向大家展示如何学习和编写 命令。

| **StudentID** | **学名** | **父母名** | **电话号码** | **地址** | **城市** | **国家** |
| 1 | 我恨你 | 阿克里提·梅赫拉 | Nine billion nine hundred and fifty-five million three hundred and thirty-nine thousand nine hundred and sixty-six | 旅道 9 座 | 海得拉巴 | 印度 |
| 2 | 马纳萨 | 舒尔亚·夏尔马 | Nine billion two hundred and thirty-four million five hundred and sixty-eight thousand seven hundred and sixty-two | 梅奥路 15 号 | 加尔各答 | 印度 |
| 3 | 阿奈 | 苏米亚·米什拉 | Nine billion eight hundred and seventy-six million nine hundred and fourteen thousand two hundred and sixty-one | 马拉塔里 101 号 | 本加卢鲁 | 印度 |
| 4 | Preeti | 罗汉·西纳 | Nine billion seven hundred and sixty-five million four hundred and thirty-two thousand two hundred and thirty-four | 皇后大道 40 号 | 德里 | 印度 |
| 5 | 莎娜雅 | 阿比奈·阿加瓦尔 | Nine billion eight hundred and seventy-eight million nine hundred and sixty-nine thousand and sixty-eight | 奥贝罗伊街 21 号 | 孟买 | 印度 |

在我们开始了解 SQL Server 中使用的不同命令之前，让我们了解一下什么是 SQL Server，它的架构以及如何安装它。

## **什么是 SQL Server？**

微软 SQL Server 是关系型[数据库管理系统](https://www.edureka.co/blog/what-is-dbms)。它支持[结构化查询语言](https://www.edureka.co/blog/what-is-sql/)，并自带 SQL 语言的实现 **Transact-SQL(T-SQL)** 。它有一个处理 SQL 数据库的集成环境，这就是[SQL Server Management Studio](https://www.edureka.co/blog/sql-server-management-studio/)。

SQL Server 的关键组件如下:

*   **数据库引擎:** 该组件负责存储、快速事务处理和保护数据。
*   **SQL Server—**此服务用于启动、停止、暂停和继续 MS SQL Server 的实例。
*   **SQL Server 代理–**服务器代理服务扮演任务调度器的角色，由任何事件或根据需求触发。
*   **SQL Server 浏览器**–该服务用于将传入的请求连接到所需的 SQL Server 实例。
*   **SQL Server 全文搜索—**用于让用户对 SQL 表中的字符数据运行全文查询。
*   **SQL Server VSS 编写器******–****允许在 SQL Server 不运行时备份和恢复数据文件。
*   **SQL Server Analysis Services(SSAS)–**该服务用于提供数据分析、数据挖掘和[机器学习](https://www.edureka.co/blog/what-is-machine-learning/)功能。SQL Server 还集成了 [Python](https://www.edureka.co/blog/python-tutorial/) 和 [R](https://www.edureka.co/blog/r-tutorial/) 用于高级数据分析。
*   **SQL Server Reporting Services(SSRS)—**顾名思义，该服务用于提供特性和决策能力，包括与 [Hadoop](https://www.edureka.co/blog/hadoop-tutorial/) 的集成。
*   **[SQL Server Integration Services(SSIS)](https://www.edureka.co/blog/ssis-tutorial/)–**该服务用于对来自多个数据源的不同类型的数据执行 ETL 操作。

现在，您已经知道了什么是 MS SQL Server，让我们在这篇文章中继续学习 SQL Server 教程，并了解如何安装和设置 SQL Server。

## **安装 SQL Server**

按照以下步骤安装 SQL Server:

**第一步:**进入 **[微软 SQL Server 下载](https://www.microsoft.com/en-au/sql-server/sql-server-downloads)** 的官方页面，在这里你会发现可以选择在本地或者云端安装 SQL Server。

**![Install SQL Server - SQL Server Tutorial - Edureka](img/c9d7e276be2e42a7cdd38de6bca280a0.png)**

**第二步:**现在向下滚动，你会看到两个选项:**开发者&企业版**。在这里，我将下载**开发者版**。要下载，您只需点击**立即下载**选项。参考下文。

**![Download SQL Server - SQL Server Tutorial - Edureka](img/7b876f398b8dc6cbfeb7767e9445a407.png)**

**第三步:**应用下载完成后，双击文件，会看到以下窗口。

**![Installation Type - SQL Server Tutorial - Edureka](img/055208a758f960b9a7fffa569ddd09d3.png)**

**步骤 4:** 现在，您可以选择 3 个选项中的任何一个来设置 SQL Server。在这里，我将只选择**基本选项**。在选择安装类型选项时，下一个屏幕将是接受许可协议。为此，点击以下窗口中的**接受**。

**![License Agreement - SQL Server Tutorial - Edureka](img/6ac5bab73738708137ae92a61b328262.png)**

第五步:接下来，您必须指定 SQL Server 的安装位置。然后，你必须点击安装。

![Choose Installation Path - SQL Server Tutorial - Edureka](img/3c7656d756cd483ab99d0c59f1aa40ba.png)

一旦你点击 **Install** ，你会看到所需的软件包正在下载。现在，安装完成后，您将看到以下屏幕:

![Choose Instance Name - SQL Server Tutorial - Edureka](img/46b61996f678567144d87787c9f59b7d.png)

在这里，您可以点击“立即连接”,也可以自定义安装。为了让您更好地理解，我将选择**定制。**

**第六步:**点击上面窗口中的**定制**，会看到下面的向导打开。在以下窗口中，点击**下一步。**

**![Update - SQL Server Tutorial - Edureka](img/940de904a153619d96e88b08dcda2349.png)**

**第七步:**规则自动安装后，点击**下一步**。参考下文。

**![Install Rules - SQL Server Tutorial - Edureka](img/62cd8ebcf2e659eb0a51e38ef15d48ad.png)**

**第八步:**接下来，你要选择安装类型。因此，选择**执行一个****SQL Server 2017 新安装**选项，然后点击**下一步。**

**![Install Types - SQL Server Tutorial - Edureka](img/ffac87dd54f28033057b6d0f5642b90b.png)**

**第 9 步:**在打开的向导中，选择版本:**开发者。**然后，点击**下一步**。参考下文。

**![Product Key - SQL Server Tutorial - Edureka](img/aa0953766026295ca64bbd7507fe3643.png)**

**步骤 10:** 现在，通过勾选单选按钮阅读并接受许可协议，然后点击**下一步**。参考下文。

**![Accept License Agreement - SQL Server Tutorial - Edureka](img/1da234c3b1878bad024016c9da77274f.png)**

**步骤 11:** 在下面的向导中，您可以选择想要安装的功能。同样，你可以选择实例根目录，然后点击**下一个**。在这里，我将选择**数据库引擎服务**。

**![Feature Selection - SQL Server Tutorial - Edureka](img/53a4bac1e2213012b0aab2a25144d046.png)**

**第 12 步:**接下来您必须命名实例，实例 ID 将自动创建。在这里，我将把实例命名为“edureka”。然后，点击**下一步。**

**![Instance Configuration - SQL Server Tutorial - Edureka](img/ee153f1c88e590122970be784ffcc081.png)**

**第十三步:**在服务器配置向导中，点击**下一步**。

**![Server Configuration - SQL Server Tutorial - Edureka](img/2dd922d2ee5fd7c530f2ce4d5ccb1259.png)**

**步骤 14:** 现在，您必须启用认证模式。在这里，你会看到 **Windows 认证模式**和**混合模式**。我会选择混合模式。然后，提及密码，然后我将通过选择**添加当前用户**选项，将当前用户添加为**管理员**。

**![Database Engine Configuration - SQL Server Tutorial - Edureka](img/cc4fe944d9abc82f676caa386d5e7653.png)**

**第十五步:**然后，选择配置文件路径，点击**安装**。

## **![Install - SQL Server Tutorial - Edureka](img/3937ccc148565357ba549ec603d842e7.png)**

安装完成后，您将看到以下屏幕:

## **![Complete Installation - SQL Server Tutorial - Edureka](img/4f38cf09f37f244a5676603200fbc903.png)**

## **使用 SSMS 连接到 SQL Server**

安装 SQL Server 后，下一步是将 SQL Server 连接到 SQL Server Management Studio。为此，请遵循以下步骤:

**步骤 1:** 返回，到以下窗口，点击**安装 SSMS** 选项。

**![Install SSMS - SQL Server Tutorial - Edureka](img/1b9bd29a51269e512e13d1cb15990f8f.png)**

**第二步:**一旦你点击那个选项，你将被重定向到[的下一页](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?redirectedfrom=MSDN&view=sql-server-ver15)，在那里你必须选择**下载 SSMS。**

**![Download SSMS - SQL Server Tutorial - Edureka](img/c3486bba6c6b86acb46a39c2495866e0.png)**

**步骤 3:** 下载完设置后，双击应用程序，您将看到以下向导打开。

**![SSMS - SQL Server Tutorial - Edureka](img/a84402cf8cb8a937b34d442093f7d10c.png)**

**第四步:**在上面的窗口中点击**安装选项**，你会看到安装将开始。

**![Installation in Progress - SQL Server Tutorial - Edureka](img/541f56299d24248339db3faf99d7984f.png)**

**第五步:** 安装完成后你会得到如下所示的对话框。

![Setup Complete - SQL Server Tutorial - Edureka](img/c7c7650bbbcd2053855a1a7875609079.png)

安装 SSMS 后，下一步是访问**数据库引擎** 。

## **访问数据库引擎**

当你从**开始菜单**打开**SQL server management studio**时，会打开一个类似下图所示的窗口。

![Connect - SQL Server Tutorial - Edureka](img/794afd5096ea265304db27ca92401a52.png)

在这里，提及服务器名称、认证模式并点击**连接。**

点击**连接**后，会看到以下画面。

![SQL Server Management Studio - SQL Server Tutorial - Edureka](img/0291a380ca8de7dc165faa7bbe501a56.png)

伙计们，这就是安装和设置 SQL Server 的方法。现在，继续学习 SQL Server 教程，让我们了解 SQL Server 体系结构的不同组件。

**SQL Server 架构**

SQL Server 的体系结构如下:

![SQL Server Architecture - SQL Server Tutorial - Edureka-min](img/28056a69160a17632b9c12d83563dadf.png)

*   **服务器**——这是安装 SQL 服务和数据库的地方
*   **关系引擎**——包含查询解析器、优化器和执行器；并且执行发生在关系引擎中。
*   **命令解析器**——检查查询的语法，并将查询转换成机器语言。
*   **优化器**—通过将统计数据、查询和代数树作为输入，准备执行计划作为输出。
*   **查询执行器**——这是逐步执行查询的地方
*   **存储引擎**—负责存储系统上的数据存储和检索、数据操作、事务管理和锁定。

现在，您已经知道如何设置和安装 SQL Server 及其各种组件，让我们开始在 SQL Server 中编写[命令。但是，在此之前，让我介绍一下如何在 SQL Server 中编写注释。](https://www.edureka.co/blog/sql-commands)

## **SQL Server 中的注释**

在 SQL 中有两种方式可以进行注释，即使用 **s** **单行注释** 或 **m** **多行注释** 。

### **单行注释**

单行注释以两个连字符(–)开始。因此，编译器将忽略(–)后面的文本，直到一行结束。

#### **例如:**

```
--Example of single line comments

```

### **多行评论**

多行评论以/*开头，以 ***/** 结尾。因此，编译器将忽略 **/*** 和 ***/** 之间提到的文本。

#### **例如:**

```
/* Example for 
multi-line comments */

```

在这篇关于 SQL Server 教程的文章中，让我们从第一组命令开始，即数据定义语言命令。

## **数据定义语言命令**

本文的这一部分将向您介绍一些命令，在这些命令的帮助下，您可以定义您的数据库。命令如下:

*   [创建](#create)
*   [降](#drop)
*   [改变](#alter)
*   [截断](#truncate)
*   [重命名](#rename)

### **创建**

该语句用于创建表、数据库或视图。

#### **【创建数据库】语句**

该语句用于创建数据库。

***语法***

```
CREATE DATABASE DatabaseName;
```

***举例***

```
CREATE DATABASE Students;

```

#### **[创建表](https://www.edureka.co/blog/create-table-in-sql/)**报表

顾名思义，该语句用于创建表。

***语法***

```
CREATE TABLE TableName (
Column1 datatype,
Column2 datatype,
Column3 datatype,
....

ColumnN datatype
);
```

***举例***

```
CREATE TABLE StudentInfo
(
StudentID int,
StudentName varchar(8000),
ParentName varchar(8000),
PhoneNumber int,
AddressofStudent varchar(8000),
City varchar(8000),
Country varchar(8000)
);

```

### **降**

此语句用于删除现有的表、数据库或视图。

#### **‘删除数据库’语句**

此语句用于删除现有数据库。一旦执行以下命令，数据库中的完整信息将会丢失。

***语法***

```
DROP DATABASE DatabaseName;
```

***举例***

```
DROP DATABASE Students;

```

#### **【降表】声明**

该语句用于删除现有的表。一旦执行以下命令，表中的完整信息将会丢失。

***语法***

```
DROP TABLE TableName;
```

***举例***

```
DROP TABLE StudentInfo;

```

### **涂改**

ALTER 命令用于添加、删除或修改现有表中的列或约束。

#### **[变更表](https://www.edureka.co/blog/alter-table/)声明**

该语句用于添加、删除、修改预先存在的表中的列。

#### **带有添加/删除列的‘ALTER TABLE’语句**

ALTER TABLE 语句与 ADD/DROP Column 命令一起用于添加和删除列。

***语法***

```
ALTER TABLE TableName
ADD ColumnName Datatype;

ALTER TABLE TableName
DROP COLUMN ColumnName;
```

***举例***

```
--ADD Column BloodGroup:
ALTER TABLE StudentInfo
ADD BloodGroup varchar(8000);

--DROP Column BloodGroup:
ALTER TABLE StudentInfo
DROP COLUMN BloodGroup ;

```

#### **具有 ALTER 列的‘ALTER TABLE’语句**

ALTER TABLE 语句可以与 ALTER column 一起使用，以更改表中现有列的数据类型。

***语法***

```
ALTER TABLE TableName
ALTER COLUMN ColumnName Datatype;
```

***举例***

```
--Add a column DOB and change the data type from date to datetime.
ALTER TABLE StudentInfo
ADD DOB date;
ALTER TABLE StudentInfo
ALTER COLUMN DOB datetime;

```

### **截断**

这个 SQL 命令用于删除表中的信息，但不会删除表本身。因此，如果您想删除表中的信息，而不是删除表本身，您必须使用 TRUNCATE 命令。否则，使用 DROP 命令。

***语法***

```
TRUNCATE TABLE TableName;
```

***举例***

```
TRUNCATE TABLE StudentInfo;

```

### **改名**

该语句用于重命名一个或多个表。

***语法***

```
sp_rename 'OldTableName', 'NewTableName';
```

***举例***

```
sp_rename 'StudentInfo', 'Infostudents';

```

在这篇关于 SQL Server 教程的文章中，让我们了解 SQL Server 支持的不同数据类型。

## **SQL Server 数据类型**

| **数据类型类别** | **数据类型名称** | **描述** | **范围/语法** |
| **精确的数字** | 数字的 | 用于存储数值，并具有固定的精度和小数位数 | 从 10^38 +1 到 10^38-1。 |
| tinyint | 用于存储整数值 | 0 到 255 |
| 斯莫列特 | 用于存储整数值 | -2^15(-32768)对 2^15-1(32767) |
| 比吉斯本 | 用于存储整数值 | -2^63 (-9，223，372，036，854，775，808)对 2^63-1 (9，223，372，036，854，775，807) |
| （同 Internationalorganizations）国际组织 | 用于存储整数值 | -2^31(-2147483648)对 2^31-1(2147483647) |
| 少量 | 存储值为 0、1 或 NULL 的整数数据类型 | 0、1 或 NULL |
| 小数 | 用于存储数值，并具有固定的精度和小数位数 | 从 10^38 +1 到 10^38-1。 |
| 小额资金 | 用于存储货币或货币值。 | –214748.3648 至 214748.3647 |
| 钱 | 用于存储货币或货币值。 | -922，337，203，685，477.5808 到 922，337，203，685，477.5807 (-922，337，203，685，477.58 到 922，337，203，685，477.58 为 Informatica。 |
| **近似数字** | 漂浮物 | 用于存储浮点数值数据 | –1.79 e+308 至-2.23E-308，0 和 2.23E-308 至 1.79E+308 |
| 真实的 | 用于存储浮点数值数据 | –3.40E + 38 至-1.18 e–38，0 和 1.18 e–38 至 3.40 e+38 |
| **日期和时间** | 日期 | 用于在 SQL Server 中定义日期。 | 语法:日期 |
| smalldatetime | 用于定义与一天中的时间相结合的日期；其中时间基于一天 24 小时，秒始终为零(:00)，没有小数秒。 | 语法:smalldatetime |
| 日期时间 | 用于定义一个日期，该日期与一天中基于 24 小时制的带小数秒的时间相结合。 | Syntax: datetime |
| 日期时间 2 | **datetime2** 是对现有 **datetime** 类型的扩展，具有更大的默认小数精度，更大的日期范围。 | Syntax: datetime2 |
| 日期时间偏移量 | 用于定义与一天中具有时区意识的时间相结合的日期。它基于 24 小时制。 | Syntax: datetimeoffset |
| 时间 | 用来定义一天的时间。 | 语法:时间 |
| **字符串** | 茶 | 用于存储固定大小的字符。 | char [ ( *n* ) ]，其中 n 值从 1 到 8000 不等 |
| 可变长字符串 | 用于存储变长字符。 | varchar [ ( *n* &#124; max ) ]，其中 n 值在 1-8000 之间变化，允许的最大存储为 2GB。 |
| 文本 | 用于存储 v 变长非 Unicode 数据 | 允许的最大字符串长度–2^31-1(2，147，483，647) |
| **Unicode 字符串** | nchar | 用于存储固定大小的字符。 | nchar [ ( n ) ]其中 n 值在 1-4000 之间变化 |
| nvarchar | 用于存储变长字符。 | varchar [ ( *n* &#124; max ) ]，其中 n 值从 1-4000 不等，允许的最大存储为 2GB。 |
| ntext | 用于存储变长 Unicode 数据 | 允许的最大字符串长度–2^30-1(2，147，483，647) |
| **二进制字符串** | 二进制的 | 用于存储固定长度的二进制数据类型 | 二进制 [ ( *n* ) ]，其中 n 值从 1 到 8000 不等 |
| varbinary | 用于存储固定长度的二进制数据类型 | varbinary[(*n*)]，其中 n 值从 1-8000 不等，允许的最大存储为 2^31-1 字节。 |
| 图像 | 用于存储变长二进制数据 | 0–2^31-1(2147483647)字节 |
| **其他数据类型** | [cursor](https://www.edureka.co/blog/cursor-in-sql/) | 它是存储过程或变量输出参数的数据类型，包含对游标的引用。 | – |
| romversion | 用于暴露数据库内自动生成的、唯一的二进制数。 | – |
| hierarchyid | 用来表示在等级制度中的地位。 | – |
| 唯一标识符 | 是 16 字节的 GUID。 | 语法:唯一标识符 |
| sql _ 变量 | 用于存储 SQL Server 支持的各种数据类型的值 | 语法:sql_variant |
| xml | 用于存储 XML 数据类型。 | xml ( [内容&#124;文档] xml_schemacollection) |
| 空间几何类型 | 用于在欧几里德(平面)坐标系中表示数据。 | – |
| 空间地理类型 | 用于存储椭球体(圆形地球)数据，如 GPS 经纬度坐标。 | – |
| 桌子 | 用于存储结果集，以便以后处理 | – |

接下来，在本文中，让我们了解数据库中不同类型的键和约束。

## **数据库中不同类型的密钥**

以下是数据库中使用的不同类型的密钥:

*   **候选键—**候选键是一组可以唯一标识一个表的属性。一个表可以有多个候选键，在选择的候选键中，有一个键被选为主键。
*   **超级键——**属性的集合可以唯一地标识一个元组。因此，候选键、唯一键和主键都是超级键，但反之亦然。
*   **主键—**[主键](https://www.edureka.co/blog/primary-key-in-sql/)用于唯一标识每个元组。
*   **备用键—**备用键是那些没有被选为主键的候选键。
*   **唯一键–**唯一键类似于主键，但允许列中有一个空值。
*   **外键——**一个只能将当前值作为其他属性的值的属性，是它所引用的属性的[外键](https://www.edureka.co/blog/foreign-key-sql/)。
*   **组合键–**组合键是两个或多个列的组合，唯一地标识每个元组。

## **数据库中使用的约束**

约束在数据库中用于指定存储在表中的数据的规则。SQL 中不同类型的[约束如下:](https://www.edureka.co/blog/sql-constraints/)

*   [不为空](#notnull)
*   [独特的](#unique)
*   [检查](#check)
*   [默认](#default)
*   [索引](#index)

### **不为空**

NOT NULL 约束确保列不能有空值。

#### ***举例***

```
CREATE TABLE StudentsInfo
(
StudentID int NOT NULL,
StudentName varchar(8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000)
);

--NOT NULL on ALTER TABLE
ALTER TABLE StudentsInfo
ALTER COLUMN PhoneNumber int NOT NULL;

```

### **独特的**

此约束确保一列中的所有值都是唯一的。

***举例***

```
--UNIQUE on Create Table

CREATE TABLE StudentsInfo
(
StudentID int NOT NULL UNIQUE,
StudentName varchar(8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000)
);

--UNIQUE on Multiple Columns

CREATE TABLE StudentsInfo
(
StudentID int NOT NULL,
StudentName varchar(8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000)
CONSTRAINT UC_Student_Info UNIQUE(StudentID, PhoneNumber)
);

--UNIQUE on ALTER TABLE

ALTER TABLE StudentsInfo
ADD UNIQUE (StudentID);

--To drop a UNIQUE constraint

ALTER TABLE  StudentsInfo
DROP CONSTRAINT UC_Student_Info;

```

### **检查**

CHECK 约束确保列中的所有值都满足特定条件。

#### ***举例***

```
--CHECK Constraint on CREATE TABLE

CREATE TABLE StudentsInfo
(
StudentID int NOT NULL,
StudentName varchar(8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000) CHECK (Country ='India')
);

--CHECK Constraint on multiple columns

CREATE TABLE StudentsInfo
(
StudentID int NOT NULL,
StudentName varchar8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000) CHECK (Country ='India'  AND City = 'Hyderabad')
);

--CHECK Constraint on ALTER TABLE

ALTER TABLE StudentsInfo
ADD CHECK (Country ='India');

--To give a name to the CHECK Constraint

ALTER TABLE StudentsInfo
ADD CONSTRAINT CheckConstraintName CHECK (Country ='India');

--To drop a CHECK Constraint

ALTER TABLE StudentsInfo
DROP CONSTRAINT CheckConstraintName;

```

### **默认**

当没有指定值时，DEFAULT 约束由一组列的默认值组成。

#### ***举例***

```
--DEFAULT Constraint on CREATE TABLE

CREATE TABLE StudentsInfo
(
StudentID int,
StudentName varchar(8000) NOT NULL,
ParentName varchar(8000),
PhoneNumber int ,
AddressofStudent varchar(8000) NOT NULL,
City varchar(8000),
Country varchar(8000) DEFAULT 'India'
);

--DEFAULT Constraint on ALTER TABLE

ALTER TABLE StudentsInfo
ADD CONSTRAINT defau_Country
DEFAULT 'India' FOR Country;

--To drop the Default Constraint

ALTER TABLE StudentsInfo
ALTER COLUMN Country DROP defau_Country;

```

### **指标**

[索引约束](https://www.edureka.co/blog/index-in-sql/)用于在表中创建索引，通过它您可以非常快速地创建和检索数据库中的数据。

***语法***

```
--Create an Index where duplicate values are allowed
CREATE INDEX IndexName
ON TableName (Column1, Column2, ...ColumnN);

--Create an Index where duplicate values are not allowed
CREATE UNIQUE INDEX IndexName
ON TableName (Column1, Column2, ...ColumnN);
```

***举例***

```
CREATE INDEX idex_StudentName
ON StudentsInfo (StudentName);

--To delete an index in a table
 DROP INDEX StudentsInfo.idex_StudentName;

```

在这篇关于 SQL Server 教程的文章中，我们现在来了解一下在 Microsoft SQL Server 中使用的不同数据操作语言命令。

## **数据操作语言命令**

文章的这一部分将涵盖所有那些可以用来操作数据库的命令。命令如下:

*   [使用](#use)
*   [插入](#insert)
*   [更新](#update)
*   [删除](#delete)
*   [合并](#merge)
*   [选择](#select)
*   [立方体](#cube)
*   [ROLLUP](#rollup)
*   [偏移](#offset)
*   [获取](#fetch)
*   [榜首](#top)
*   [枢轴](#pivot)

除了这些命令，还有其他操作符/功能，如:

*   [操作员](#operators)
    *   [算术运算符](#artithmeticoperators)
    *   [赋值运算符](#assignmentoperators)
    *   [按位运算符](#bitwiseoperators)
    *   [比较运算符](#comparisonoperators)
    *   [复合运算符](#compoundoperators)
    *   [逻辑运算符](#logicaloperators)
    *   [范围解析运算符](#scoperesolutionoperators)
    *   [设置操作符](#setoperators)
    *   [字符串串联运算符](#stringconcatenationoperators)
    *   [聚合函数](#aggregatefunctions)
*   [用户自定义函数](#userdefinedfunctions)

### **使用**

该语句用于选择数据库，开始对其执行各种操作。

***语法***

```
USE DatabaseName;
```

***举例***

```
USE Students;

```

### **插入到**

[INSERT INTO 语句](https://www.edureka.co/blog/insert-query-sql/)用于向现有表中插入新记录。

#### ***语法***

```
INSERT INTO TableName (Column1, Column2, Column3, ...,ColumnN)
VALUES (value1, value2, value3, ...);

--If you don't want to mention the column names then use the below syntax

INSERT INTO TableName
VALUES (Value1, Value2, Value3, ...);
```

***举例***

```
INSERT INTO StudentsInfo(StudentID, StudentName, ParentName, PhoneNumber, AddressofStudent, City, Country)
VALUES ('06', 'Sanjana','Kapoor', '9977331199', 'Buffalo Street House No 10', 'Kolkata', 'India');

INSERT INTO StudentsInfo
VALUES ('07', 'Vishal','Mishra', '9876509712', 'Nice Road 15', 'Pune', 'India');

```

### **更新**

UPDATE 语句用于修改或更新表中已经存在的记录。

#### ***语法***

```
UPDATE TableName
SET Column1 = Value1, Column2 = Value2, ...
WHERE Condition;
```

***举例***

```
UPDATE StudentsInfo
SET StudentName = 'Aahana', City= 'Ahmedabad'
WHERE StudentID = 1;

```

### **删除**

DELETE 语句用来删除表中已有的记录。

#### ***语法***

```
DELETE FROM TableName WHERE Condition;
```

***举例***

```
DELETE FROM StudentsInfo
WHERE StudentName='Aahana';

```

### **合并**

MERGE 语句用于在提供源表的特定表上执行插入、更新和删除操作。参考下文。

#### ***![Merge Statement - SQL Server Tutorial - Edureka](img/71bc39c4b99db77e1b35f1a591c5fd5e.png)***

#### ***语法***

```
MERGE TagretTableName USING SourceTableName
ON MergeCondition
WHEN MATCHED
THEN Update_Statement
WHEN NOT MATCHED
THEN Insert_Statement
WHEN NOT MATCHED BY SOURCE
THEN DELETE;
```

***举例***

为了理解 MERGE 语句，请将下面的表视为源表和目标表。

**来源表:**

| **StudentID** | **学生名称** | **标记** |
| one | 我恨你 | Eighty-seven |
| Two | 马纳萨 | Ninety-two |
| four | 阿奈 | Seventy-four |

**目标表:**

| **StudentID** | **学生名称** | **标记** |
| one | 我恨你 | Eighty-seven |
| Two | 马纳萨 | Sixty-seven |
| three | 索拉博 | Fifty-five |

```
MERGE SampleTargetTable TARGET USING SampleSourceTable SOURCE ON (TARGET.StudentID = SOURCE.StudentID)                                                                                       
WHEN MATCHED AND TARGET.StudentName <> SOURCE.StudentName OR TARGET.Marks <> SOURCE.Marks 
THEN UPDATE SET TARGET.StudentName = SOURCE.StudentName, TARGET.Marks = SOURCE.Marks         
WHEN NOT MATCHED BY TARGET THEN  
INSERT (StudentID,StudentName,Marks) VALUES (SOURCE.StudentID,SOURCE.StudentName,SOURCE.Marks)
WHEN NOT MATCHED BY SOURCE THEN         
DELETE;    

```

***输出***

| **StudentID** | **学生名称** | **标记** |
| one | 我恨你 | Eighty-seven |
| Two | 马纳萨 | Ninety-two |
| four | 阿奈 | Seventy-four |

### **选择**

[选择语句](https://www.edureka.co/blog/sql-select)用于从数据库、表格或视图中选择数据。返回的数据存储在一个结果表中，称为 **结果集** 。

#### ***语法***

```
SELECT Column1, Column2, ...ColumN
FROM TableName;

--(*) is used to select all from the table
SELECT * FROM table_name;

-- To select the number of records to return use:
SELECT TOP 3 * FROM TableName;
```

***举例***

```
-- To select few columns
SELECT StudentID, StudentName
FROM StudentsInfo;

--(*) is used to select all from the table
SELECT * FROM StudentsInfo;

-- To select the number of records to return use:
SELECT TOP 3 * FROM StudentsInfo;

```

我们也可以在 SELECT 语句中使用以下关键字:

*   [泾渭分明](#distinct)
*   [顺序由](#orderby)
*   [分组通过](#groupby)
*   [分组集合](#groupinngsets)
*   [HAVING 子句](#havingclause)
*   [变成](#into)

#### **截然不同的**

DISTINCT 关键字与 SELECT 语句一起使用，只返回不同的值。

#### ***语法***

```
SELECT DISTINCT Column1, Column2, ...ColumnN
FROM TableName;
```

***举例***

```
SELECT DISTINCT PhoneNumber FROM StudentsInfo;

```

#### **排序依据**

该语句用于按升序或降序对所需结果进行排序。默认情况下，结果按升序存储。然而，如果你希望得到降序排列的结果，你必须使用关键字。

#### ***语法***

```
SELECT Column1, Column2, ...ColumnN
FROM TableName
ORDER BY Column1, Column2, ... ASC|DESC;
```

***举例***

```
-- Select all students from the 'StudentsInfo' table sorted by ParentName:
SELECT * FROM StudentsInfo
ORDER BY ParentName;

-- Select all students from the 'StudentsInfo' table sorted by ParentName in Descending order:
SELECT * FROM StudentsInfo
ORDER BY ParentName DESC;

-- Select all students from the 'StudentsInfo' table sorted by ParentName and StudentName:
SELECT * FROM StudentsInfo
ORDER BY ParentName, StudentName;

/* Select all students from the 'StudentsInfo' table sorted by ParentName 
in Descending order and StudentName in Ascending order: */
SELECT * FROM StudentsInfo
ORDER BY ParentName ASC, StudentName DESC;

```

#### **分组依据**

该语句与[聚合函数](https://www.edureka.co/blog/sql-functions)一起使用，按一列或多列对结果集进行分组。

#### ***语法***

```
SELECT Column1, Column2,..., ColumnN
FROM TableName
WHERE Condition
GROUP BY ColumnName(s)
ORDER BY ColumnName(s);
```

***举例***

```
-- To list the number of students from each city.
SELECT COUNT(StudentID), City
FROM StudentsInfo
GROUP BY City;

```

#### **分组集合**

SQL Server 2008 中引入了分组集，用于生成由多个简单 GROUP BY 子句的 UNION ALL 生成的结果集。

#### ***语法***

```
SELECT ColumnNames(s)
FROM TableName
GROUP BY GROUPING SETS(ColumnName(s));
```

#### ***举例***

```
SELECT StudentID, StudentName, COUNT(City)
from StudentsInfo
Group BY
GROUPING SETS
((StudentID, StudentName, City),(StudentID),(StudentName),(City));

```

该子句用于不能使用关键字的场景。

#### ***语法***

```
SELECT ColumnName(s)
FROM TableName
WHERE Condition
GROUP BY ColumnName(s)
HAVING Condition
ORDER BY ColumnName(s);
```

***举例***

```
SELECT COUNT(StudentID), City
FROM StudentsInfo
GROUP BY City
HAVING COUNT(StudentID) > 2
ORDER BY COUNT(StudentID) DESC;

```

#### **变成**

INTO 关键字可以与 [SELECT 语句](https://www.edureka.co/blog/sql-select)一起使用，将数据从一个表复制到另一个表。嗯，你可以理解这些表是临时表。临时表通常用于对表中存在的数据执行操作，而不干扰原始表。

#### ***语法***

```
SELECT *
INTO NewTable [IN ExternalDB]
FROM OldTable
WHERE Condition;
```

***举例***

```
-- To create a backup of table 'StudentsInfo'
SELECT * INTO StudentsBackup
FROM StudentsInfo;

--To select only few columns from StudentsInfo
SELECT StudentName, PhoneNumber INTO StudentsDetails
FROM StudentsInfo;

SELECT * INTO PuneStudents
FROM StudentsInfo
WHERE City = 'Pune';

```

### **立方体**

CUBE 是 GROUP BY 子句的扩展。它允许您为 GROUP BY 子句中指定的分组列的所有组合生成小计。

#### ***语法***

```
SELECT ColumnName(s)
FROM TableName
GROUP BY CUBE(ColumnName1, ColumnName2, ....., ColumnNameN);
```

***举例***

```
SELECT StudentID, COUNT(City)
FROM StudentsInfo
GROUP BY CUBE(StudentID)
ORDER BY StudentID;  

```

### **ROLLUP**

ROLLUP 是 GROUP BY 子句的扩展。这允许您包含代表小计的额外行。这些行与总计行一起被称为超级聚合行。

#### ***语法***

```
SELECT ColumnName(s)
FROM TableName
GROUP BY ROLLUP(ColumnName1, ColumnName2, ....., ColumnNameN);
```

***举例***

```
SELECT StudentID, COUNT(City)
FROM StudentsInfo
GROUP BY ROLLUP(StudentID);

```

### **偏移**

OFFSET 子句与 SELECT 和 [ORDER BY 语句](https://www.edureka.co/blog/order-by-in-sql)一起使用，以检索一系列记录。它必须与 ORDER BY 子句一起使用，因为它不能单独使用。此外，您提到的范围必须等于或大于 0。如果你提到一个负值，那么它显示一个错误。

#### ***语法***

```
SELECT ColumnNames)
FROM TableName
WHERE Condition
ORDER BY ColumnName(s)
OFFSET RowsToSkip ROWS;
```

***举例***

考虑在*学生信息*表中的一个新列**标记**。

```
SELECT StudentName, ParentName
FROM StudentsInfo
ORDER BY Marks
OFFSET 1 ROWS;

```

### **获取**

FETCH 子句用于返回包含许多行的集合。它必须与 OFFSET 子句一起使用。

#### ***语法***

```
SELECT ColumnNames)
FROM TableName
WHERE Condition
ORDER BY ColumnName(s)
OFFSET RowsToSkip 
FETCH NEXT NumberOfRows ROWS ONLY;
```

***举例***

```
SELECT StudentName, ParentName
FROM StudentsInfo
ORDER BY Marks
OFFSET 1 ROWS
FETCH  NEXT 1 ROWS ONLY;

```

### **榜首**

TOP 子句与 SELECT 语句一起使用，表示要返回的记录数。

#### ***语法***

```
SELECT TOP Number ColumnName(s)
FROM TableName
WHERE Condition;
```

***举例***

```
SELECT TOP 3 * FROM StudentsInfo;

```

### **枢轴**

PIVOT 用于将行旋转为列值，并在需要时对剩余的列值运行聚合。

#### ***语法***

```
SELECT NonPivoted ColumnName,  
    [First Pivoted ColumnName] AS ColumnName,  
    [Second Pivoted ColumnName] AS ColumnName, 
    [Third Pivoted ColumnName] AS ColumnName,   
    ...  
    [Last Pivoted ColumnName] AS ColumnName  
FROM 
    (SELECT query which produces the data)   
    AS [alias for the initial query]  
PIVOT  
(  
    [AggregationFunction](ColumName)  
FOR  
[ColumnName of the column whose values will become column headers]   
    IN ( [First Pivoted ColumnName], [Second Pivoted ColumnName],  [Third Pivoted ColumnName]
    ... [last pivoted column])  
) AS [alias for the Pivot Table];
```

***举例***

要得到详细的例子，可以参考[我关于 SQL PIVOT 和 UNPIVOT 的文章](https://www.edureka.co/blog/sql-pivot-and-unpivot/)。接下来，在本 SQL Server 教程中，我们来看看 Microsoft SQL Server 支持的不同运算符。

## **操作员**

SQL Server 支持的[不同类型的运算符](https://www.edureka.co/blog/sql-operators/)如下:

*   [算术运算符](#artithmeticoperators)
*   [赋值运算符](#assignmentoperators)
*   [按位运算符](#bitwiseoperators)
*   [比较运算符](#comparisonoperators)
*   [复合运算符](#compoundoperators)
*   [逻辑运算符](#logicaloperators)
*   [范围解析运算符](#scoperesolutionoperators)
*   [设置操作符](#setoperators)
*   [字符串串联运算符](#stringconcatenationoperators)

让我们逐一讨论它们中的每一个。

### **算术运算符**

| **操作员** | **意为** | **语法** |
| **+** | 添加 | 表情+表情 |
| **–** | 减法 | 表情–表情 |
| ***** | 乘法运算 | 表情*表情 |
| **/** | 分开 | 表情/表情 |
| **%** | 系数 | 表达式%表达式 |

### **赋值运算符**

| **操作员** | **意为** | **语法** |
| **=** | 给变量赋值 | 变量= '值' |

### **按位运算符**

| **操作员** | **意为** | **语法** |
| **&(按位与)** | 用于执行两个整数值之间的按位逻辑与运算。 | 表情&表情 |
| **& =(按位 AND 赋值)** | 用于执行两个整数值之间的按位逻辑与运算。它还为操作的输出设置一个值。 | 表情& =表情 |
| **&#124;(按位或)** | 用于在 Transact-SQL 语句中转换为二进制表达式的两个整数值之间执行按位逻辑“或”运算。 | 表情&#124;表情 |
| **&#124;=(按位或赋值)** | 用于在 Transact-SQL 语句中转换为二进制表达式的两个整数值之间执行按位逻辑“或”运算。它还为操作的输出设置一个值。 | 表达式&#124;=表达式 |
| **^(按位异或)** | 用于执行两个整数值之间的按位异或运算。 | 表情^表情 |
| **^=(按位异或赋值)** | 用于执行两个整数值之间的按位异或运算。它还为操作的输出设置一个值。 | 表情^=表情 |
| **~(按位非)** | 用于对整数值执行按位逻辑非运算。 | ~表情 |

### **比较运算符**

| **操作员** | **Meaning** | **语法** |
| **=** | 等于 | 表达式=表达式 |
| **>** | 大于 | 表情>表情 |
| **<** | 不到 | 表情<表情 |
| **> =** | 大于或等于 | 表情> =表情 |
| **< =** | 小于或等于 | 表情< =表情 |
| **<>** | 不等于 | 表情<表情 |
| **！=** | 不等于 | 表情！=表达式 |
| **！<** | 不少于 | 表情！<表情 |
| **！>** | 不大于 | 表情！>表情 |

### **复合运算符**

| **操作员** | **意为** | **语法** |
| **+ =** | 用于给原值加值，并将原值设置为结果。 | 表达式+=表达式 |
| **-=** | 用于从原始值中减去一个值，并将原始值设置为结果。 | 表达式-=表达式 |
| ***=** | 用于将值乘以原始值，并将原始值设置为结果。 | 表达式*=表达式 |
| **/=** | 用于从原始值中除以一个值，并将原始值设置为结果。 | 表达式/=表达式 |
| **%=** | 用于从原始值中除以一个值，并将原始值设置为结果。 | 表达式%=表达式 |
| **&=** | 用于执行按位 AND 运算，并将原始值设置为结果。 | 表情& =表情 |
| **^=** | 用于执行按位异或运算，并将原始值设置为结果。 | 表情^=表情 |
| **&#124;=** | 用于执行按位“或”运算，并将原始值设置为结果。 | 表达式&#124;=表达式 |

### **逻辑运算符**

| **操作员** | **意为** | **语法** |
| **全部** | 如果所有的比较都为真，则返回真。 | scalar_expression { = &#124; <> &#124;！= &#124; > &#124; >= &#124; !> &#124; < &#124; <= &#124; !< }全部(子查询) |
| **和** | 如果两个表达式都为真，则返回 TRUE。 | 布尔表达式和布尔表达式 |
| **任何** | 如果一组比较中的任何一个为真，则返回 TRUE。 | scalar_expression { = &#124; < > &#124;！= &#124; > &#124; > = &#124; !> &#124; < &#124; < = &#124; !< } { ANY }(子查询) |
| **之间** | 如果操作数在某个范围内，则返回 TRUE。 | beginexpression 和 endexpression 之间的 sampleexpression [ NOT ] |
| **存在** | 如果子查询包含任何行，则返回 TRUE。 | 存在(子查询) |
| 中的 | 如果操作数等于表达式列表中的一个，则返回 TRUE。 | test_expression [ NOT ] IN(子查询&#124;表达式[，…n ]) |
| [**如同**](https://www.edureka.co/blog/like-in-sql/) | 如果操作数与模式匹配，则返回 TRUE。 | match_expression [ NOT ] LIKE 模式[ ESCAPE escape_character ] |
| **不是** | 反转任何布尔运算符的值。 | [ NOT ]布尔表达式 |
| **或** | 如果任一布尔表达式为真，则返回真。 | 布尔表达式或布尔表达式 |
| **有的** | 如果一组比较中的一些为真，则返回真。 | scalar_expression { = &#124; < > &#124;！= &#124; > &#124; > = &#124; !> &#124; < &#124; < = &#124; !< } {一些}(子查询) |

### **范围解析运算符**

| **操作员** | **意为** | **例子** |
| **::** | 提供对复合数据类型的静态成员的访问。复合数据类型是那些包含多种方法和简单数据类型的数据类型。复合数据类型，包括内置 CLR 类型和自定义 SQLCLR 用户定义类型(udt)。 | 声明@ hid hierarchyidSELECT @ hid = hierarchy id::GetRoot()；打印@hid。ToString()； |

### **设置操作符**

主要有三种集合运算:联合、相交、减去。可以参考下图来理解 SQL 中的 set 操作。参考下图:

### **![SET Operators - SQL Server Tutorial - Edureka](img/92362f35a0a7c35830a2f2fa8c340eb2.png)**

| **操作员** | **意为** | **语法** |
| **工会** | UNION 运算符用于组合两个或多个 SELECT 语句的结果集。 | 从表 1 中选择列名 UNION 从表 2 中选择列名； |
| **相交** | INTERSECT 子句用于组合两个 SELECT 语句，并返回两个 SELECT 语句数据集的交集。 | 选择列 1、列 2 …FROM TableName；条件相交的地方选择列 1，列 2 …从表名；何处条件 |
| **除了** | EXCEPT 运算符返回第一次选择操作返回的元组，而第二次选择操作没有返回这些元组。 | 从 TableName 中选择 column name；除了从 TableName 中选择 column name； |

### **字符串运算符**

| **操作员** | **意为** | **语法/示例** |
| **+(字符串串联)** | 将两个或多个二进制或字符串、列或字符串和列名的组合连接成一个表达式 | 表情+表情 |
| **+=(字符串串联)** | 用于连接两个字符串并将字符串设置为运算的结果。 | 表达式+=表达式 |
| **%(要匹配的通配符)** | 用来匹配任何零个或多个字符的字符串。 | 示例:“样本%” |
| **[](通配符匹配)** | 用于匹配在方括号[]中指定的指定范围或集合内的单个字符。 | 例:m[n-z]%' |
| **【^】(通配符匹配)** | 用于匹配不在方括号内指定的范围或集合内的单个字符。 | 举例:'Al[^a]%' |
| **_(要匹配的通配符)** | 用于在字符串比较操作中匹配单个字符 | test_expression [ NOT ] IN(子查询&#124;表达式[，…n ]) |

## **聚合** **功能**

SQL Server 支持的不同[聚合函数](https://www.edureka.co/blog/sql-functions)如下:

| **功能** | **描述** | **语法** | **例子** |
| **SUM()** | 用于返回一组数值的总和。 | 从 TableName 中选择 SUM(ColumnName ); | 从 StudentsInfo 中选择 SUM(Marks ); |
| **COUNT()** | 根据条件或不根据条件返回行数。 | SELECT COUNT(column name)FROM TableName WHERE 条件； | 从学生信息中选择计数(学生 ID ); |
| **AVG()** | 用于计算一个数值列的平均值。 | 从表名中选择 AVG(列名)； | 从学生信息中选择 AVG(马克)； |
| **MIN()** | 这个函数返回一列的最小值。 | 从 TableName 中选择 MIN(ColumnName ); | 从 StudentsInfo 中选择 MIN(Marks ); |
| **MAX()** | 返回一列的最大值。 | 从 TableName 中选择 MAX(ColumnName ); | 从学生信息中选择最大分数； |
| **FIRST()** | 用于返回列的第一个值。 | 从 TableName 中选择 FIRST(ColumnName ); | 从学生信息中选择第一个(标记); |
| **LAST()** | 该函数返回该列的最后一个值。 | 从 TableName 中选择 LAST(ColumnName ); | 从学生信息中选择最后一个(标记); |

## **用户自定义函数**

Microsoft SQL Server 允许用户创建用户定义的例行函数。这些例程接受参数，可以执行简单到复杂的操作，并将特定操作的结果作为值返回。这里，返回值可以是单个标量值，也可以是完整的结果集。

您可以使用用户定义的函数来:

*   允许模块化编程
*   减少网络流量
*   允许更快地执行查询

此外，您可以创建不同类型的用户定义函数。它们是:

*   **标量函数:**用于返回在 RETURNS 子句中定义的类型的单个数据值。
*   **表值函数:**用于返回一个表的数据类型。
*   **系统功能:**SQL Server 提供了各种系统功能来执行不同的操作。

嗯，除了用户自定义函数，SQL Server 还有一堆内置函数；其可用于执行各种任务。继续这篇关于 SQL Server 教程的文章，现在让我们了解什么是嵌套查询。

## **嵌套查询**

**嵌套查询** 是那些具有外部查询和内部子查询的查询。因此，基本上，子查询是嵌套在另一个查询(如 SELECT、INSERT、UPDATE 或 DELETE)中的查询。参考下图:

![Nested Queries - SQL Server Tutorial - Edureka](img/d5eb78d1c2a330dc7664f4c96b1e00f0.png)

接下来，在本 SQL Server 教程中，让我们了解 SQL 中不同类型的联接。

## **归附**

[连接](https://www.edureka.co/blog/sql-joins-types)用于根据表之间的相关列，组合两个或多个表中的元组。有四种类型的连接:

*   **[内部连接:](#innerjoin)** 返回在两个表中都有匹配值的记录。
*   **[左连接:](#leftjoin)** 返回左表中的记录，以及右表中满足条件的记录。
*   **[右连接:](#rightjoin)** 返回右表中的记录，以及左表中满足条件的记录。
*   **[全联接:](#fulljoin)** 返回在左表或右表中有匹配项的记录。

![Joins - SQL Server Tutorial - Edureka](img/4fc33e757bc513b1076b72dd86b3e421.png)

考虑下表和 StudentsInfo 表，以理解连接的语法。

| **主题 ID** | **StudentID** | **主语名称** |
| 10 | Ten | 数学 |
| 2 | 11 | 物理 |
| 3 | 12 | 化学 |

### **内部加入**

***语法***

```
SELECT ColumnName(s)
FROM Table1
INNER JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;
```

***举例***

```
SELECT Subjects.SubjectID, StudentsInfo.StudentName
FROM Subjects
INNER JOIN StudentsInfo ON Subjects.StudentID = StudentsInfo.StudentID;

```

### **左加入**

***语法***

```
SELECT ColumnName(s)
FROM Table1
LEFT JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;
```

***举例***

```
SELECT StudentsInfo.StudentName, Subjects.SubjectID
FROM StudentsInfo
LEFT JOIN Subjects ON StudentsInfo.SubjectID = Subjects.SubjectID
ORDER BY StudentsInfo.StudentName;

```

### **右加入**

***语法***

```
SELECT ColumnName(s)
FROM Table1
RIGHT JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;
```

***举例***

```
SELECT StudentsInfo.StudentName, Subjects.SubjectID
FROM StudentsInfo
RIGHT JOIN Subjects ON StudentsInfo.SubjectID = Subjects.SubjectID
ORDER BY StudentsInfo.StudentName;

```

### **完全加入**

***语法***

```
SELECT ColumnName(s)
FROM Table1
FULL OUTER JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;
```

***举例***

```
SELECT StudentsInfo.StudentName, Subjects.SubjectID
FROM StudentsInfo
FULL OUTER JOIN Subjects ON StudentsInfo.SubjectID = Subjects.SubjectID
ORDER BY StudentsInfo.StudentName;

```

接下来，在这篇关于 SQL Server 教程的文章中，让我们了解 SQL Server 支持的不同类型的循环。

## **循环**

不同的流量控制命令如下:

*   [开始..结束](#beginend)
*   [突破](#break)
*   [继续](#continue)
*   [转到](#goto)
*   [如果..否则](#ifelse)
*   [返回](#return)
*   [等待](#waitfor)
*   [而](#while)

让我们逐一讨论它们中的每一个。

### **开始..END**

这些关键字用于括起一系列 SQL 语句。然后，可以执行这组 SQL 语句。

***语法***

```
BEGIN   
     { SQLStatement | StatementBlock }   
END

```

### **突破**

该语句用于退出当前的 WHILE 循环。如果当前的 WHILE 循环嵌套在另一个循环中，则 BREAK 语句只退出当前循环，并将控制权传递给当前循环中的下一条语句。BREAK 语句通常用在 IF 语句中。

***语法***

```
BREAK;

```

### **继续**

CONTINUE 语句用于重启 WHILE 循环。因此，CONTINUE 关键字之后的任何语句都将被忽略。

***语法***

```
CONTINUE;
```

这里，标签是一个点，如果 GOTO 的目标是该特定的标签，则处理在该点之后开始。

### **前往**

用于改变标签的执行流程。跳过 GOTO 关键字之后编写的语句，并在标签处继续处理。

***语法***

```
Define Label:   
Label:   
Alter Execution:  
GOTO Label
```

这里，标签是一个点，如果 GOTO 的目标是该特定的标签，则处理在该点之后开始。

### **如果..否则**

与任何其他编程语言一样，SQL Server 中的 If-else 语句测试条件，如果条件为假，则执行‘else’语句。

***语法***

```
IF BooleanExpression      
     { SQLStatement | StatementBlock }   
[ ELSE   
     { SQLStatement | StatementBlock } ]

```

### **返回**

用于无条件退出查询或程序。因此，在 RETURN 子句之后编写的语句不会被执行。

***语法***

```
RETURN [ IntegerExpression ]
```

这里，返回一个整数值。

### **等待**

wait for 控制流用于阻止存储过程、事务或批处理的执行，直到特定语句修改、返回至少一行或经过指定时间或时间间隔。

***语法***

```
WAITFOR   
{  
    DELAY 'TimeToPass'   
  | TIME 'TimeToExecute'   
  | [ ( RecieveStatement ) | ( GetConversionGroupStatement ) ]   
    [ , TIMEOUT timeout ]  
}
```

在哪里，

*   **延迟**–必须经过的一段时间
*   **时间表**–P等待的时间
*   **TIME**–存储过程、事务或批处理运行的时间。
*   **time to execute**–wait for 语句结束的时间。
*   **接收语句**–一个有效的接收语句。
*   **getconversiongroup statement**–一个有效的 GET CONVERSATION GROUP 语句。
*   **超时超时***–*指定等待消息到达队列的时间，以毫秒为单位。

### **而**

此循环用于设置重复执行特定 SQL 语句或 SQL 语句块的条件。只要用户提到的条件为真，就会执行这些语句。一旦条件失败，循环就停止执行。

***语法***

```
WHILE BooleanExpression 
{ SQLStatement | StatementBlock | BREAK | CONTINUE }
```

现在，你们已经知道了 DML 命令，让我们进入 SQL 教程的下一部分 ，也就是 DCL 命令。

## **【数据控制语言命令(DCL)**

SQL Server 教程的这一部分将向您介绍在多用户数据库环境中用于加强数据库安全性的命令。命令如下:

*   [授予](#grant)
*   [撤销](#revoke)

### **授**

GRANT 命令用于向用户提供对数据库及其对象的访问或权限。

***语法***

```
GRANT PrivilegeName
ON ObjectName
TO {UserName |PUBLIC |RoleName}
[WITH GRANT OPTION];
```

其中，

*   **特权名称**–授予用户的特权/权利/访问权。
*   **object Name**–表/视图/存储过程等数据库对象的名称。
*   **用户名**–被授予访问/权限/特权的用户的名称。
*   **公共**–授予所有用户访问权限。
*   **RoleName**–一组特权的名称。
*   **带授予选项**–赋予用户访问权限，授予其他用户权限。

***举例***

```
-- To grant SELECT permission to StudentsInfo table to user1
GRANT SELECT ON StudentsInfo TO user1;

```

### **撤销**

REVOKE 命令用于撤销使用 GRANT 命令授予的用户访问权限。

***语法***

```
REVOKE PrivilegeName 
ON ObjectName 
FROM {UserName |PUBLIC |RoleName}
```

***举例***

```
-- To revoke the granted permission from user1
REVOKE SELECT ON StudentsInfo TO user1;

```

继续学习 SQL Server 教程，让我们了解如何创建和使用存储过程。

## **存储过程**

[存储过程](https://www.edureka.co/blog/procedures-in-sql/)是封装了应用程序特定业务逻辑的可重用单元。因此，它是一组 SQL 语句和逻辑，被编译和存储在一起以执行特定的任务。

***语法***

```
CREATE [ OR REPLACE] PROCEDURE procedure_name [
(parameter_name [IN | OUT | IN OUT] type [ ])]
{IS | AS }
BEGIN [declaration_section]
executable_section 
//SQL statement used in the stored procedure
END
GO
```

## ***举例***

```
--Create a procedure that will return a student name when the StudentId is given as the input parameter to the stored procedure
Create  PROCEDURE GetStudentName 
(
@StudentId INT, --Input parameter ,  
@StudName VARCHAR(50)  OUT  --Output parameter, 
AS
BEGIN
SELECT @StudName = StudentName FROM StudentsInfo WHERE StudentID=@StudentId
END

```

要执行的步骤:

上面的过程返回一个特定学生的名字， 给出那个学生的 id 作为输入。接下来，在本 SQL Server 教程中，让我们了解事务控制语言命令。

## 事务控制语言命令(TCL)

SQL Server 教程的这一部分将让您深入了解用于管理数据库中事务的命令。 命令如下:

*   [提交](#commit)
*   [回滚](#rollback)
*   [保存点](#savepoint)

### **提交**

COMMIT 命令用于将事务保存到数据库中。

***语法***

```
COMMIT;

```

### **回滚**

roll back 命令用于将数据库恢复到上次提交的状态。

***语法***

```
ROLLBACK;
```

**注意:**当您使用 ROLLBACK with SAVEPOINT 时，您可以直接跳转到正在进行的事务中的保存点。语法:ROLLBACK TO SavepointName

### **保存点**T3]

保存点命令用于临时保存事务。因此，如果您希望回滚到任一点，那么您可以将该点保存为“保存点”。

***语法***

```
SAVEPOINT SAVEPOINTNAME;
```

考虑下表以理解数据库中事务的工作方式。

| **StudentID** | **学生名称** |
| one | rohit！rohit |
| Two | 苏哈纳 |
| three | 阿希什 |
| four | 普莱尔 |

现在，使用下面的 [SQL 查询](https://www.edureka.co/blog/interview-questions/sql-query-interview-questions)来理解数据库中的事务。

```
INSERT INTO StudentTable VALUES(5, 'Avinash');
COMMIT;
UPDATE StudentTable SET name = 'Akash' WHERE id = '5';
SAVEPOINT S1;
INSERT INTO StudentTable VALUES(6, 'Sanjana');
SAVEPOINT S2;
INSERT INTO StudentTable VALUES(7, 'Sanjay');
SAVEPOINT S3;
INSERT INTO StudentTable VALUES(8, 'Veena');
SAVEPOINT S4;
SELECT * FROM StudentTable;

```

本文的下一篇 SQL Server 教程将让我们了解如何在 Transact-SQL 中处理异常。

## **异常处理**

有两种类型的异常，即系统定义的异常和用户定义的异常。顾名思义，异常处理是一个用户可以处理生成的异常的过程。要处理异常，您必须理解以下控制流语句:

*   [投掷](#throw)
*   [试一下……接住](#trycatch)

### **扔**

此子句用于引发异常，并将执行转移到 TRY…CATCH 构造的 CATCH 块。

***语法***

```
THROW [ { ErrorNumber | @localvariable },  
        { Message | @localvariable },  
        { State | @localvariable } ]   
[ ; ]
```

其中，

*   **error number**–代表异常的常量或变量。
*   **消息**–描述异常的变量或字符串。
*   **状态**–0 到 255 之间的常量或变量，表示与消息相关的状态。

```
THROW 51000, 'Record does not exist.', 1;  

```

### **试试..抓住**

用于在 Transact-SQL 中实现异常处理。TRY 块中可以包含一组语句。如果 TRY 块中出现错误，控制将传递给 CATCH 块中包含的另一组语句。

***语法***

```
BEGIN TRY  
     { SQLStatement | StatementBlock}  
END TRY  
BEGIN CATCH  
     [ { SQLStatement | StatementBlock } ]  
END CATCH  
[ ; ]
```

```
BEGIN TRY  
    SELECT * FROM StudentsInfo;  
END TRY  
BEGIN CATCH  
    SELECT   
        ERROR_NUMBER() AS ErNum , ERROR_MESSAGE() AS ErMsg;  
END CATCH

```

*W* *带着这些，我们来结束这篇关于 SQL Server 的教程。我希望您喜欢阅读这篇关于 SQL Server 初学者教程的文章。如果您希望获得有关 MySQL 的结构化培训，请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。* *有问题吗？请在“ **SQL Server 教程**”的评论区提及，我会回复你。*