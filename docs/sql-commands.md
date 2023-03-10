# SQL 命令——SQL 初学者指南

> 原文：<https://www.edureka.co/blog/sql-commands>

在这个数据海量生成的时代，人们一直需要处理数据库中的数据。关系数据库是最流行的数据库之一，而 SQL 是关系数据库的基础。因此 [**SQL 技能**](https://www.edureka.co/mysql-dba) 在大多数工作角色中都是不可或缺的。在这篇关于 SQL 命令的文章中，我将讨论您在 SQL 中需要理解的主要命令和语句。

本博客涉及的主题主要分为 4 类:

*   **[【DDL】](#DDL)**–由用于定义数据库的命令组成。
*   **[数据操作语言(DML)](#DML)**–由用于操作数据库中数据的命令组成。
*   **[数据控制语言(DCL)](#DCL)**——由处理用户权限和控制数据库系统的命令组成。
*   **[【TCL】](#TCL)**——由处理数据库事务的命令组成。

除了上述命令之外，本文还将讨论以下主题:

*   [SQL 中的注释](#Comments)
*   [数据库中不同类型的密钥](#Keys%20In%20Database)
*   [数据库中使用的约束](#Constraints)
*   [嵌套查询](#Nested%20Queries)
*   [归附](#Joins)
*   [设定操作](#Set%20Operations)
*   [日期&自动增量](#Dates%20and%20Auto%20Increment)
*   [视图](#Views)
*   [存储过程](#Stored%20Procedures)
*   [触发器](#Triggers)

在这篇关于 SQL 命令的文章中，我将以下面的数据库为例，向您展示如何编写命令。

| **员工 ID** | **EmployeeName** | **紧急联系人姓名** | **电话号码** | **地址** | **城市** | **国家** |
| 01 | 莎娜雅 | ABC 中国 | Nine billion eight hundred and ninety-eight million seven hundred and sixty-five thousand six hundred and twelve | 奥贝罗伊街 23 号 | 孟买 | 印度 |
| 02 | 阿奈 | Soumya | Nine billion four hundred and thirty-two million one hundred and fifty-six thousand seven hundred and eighty-three | 马拉塔利 23 号屋 | 德里 | 印度 |
| 03 | Preeti | 罗汉 | Nine billion seven hundred and sixty-four million two hundred and thirty-four thousand five hundred and nineteen | 皇后大道 45 号 | 班加罗尔 | 印度 |
| 04 | 我恨你 | 阿克里提 | Nine billion nine hundred and sixty-six million four hundred and forty-two thousand two hundred and eleven | 旅道第 4 座 | 海得拉巴 | 印度 |
| 05 | 马纳萨 | 舒尔亚 | Nine billion five hundred and forty-three million one hundred and seventy-six thousand two hundred and forty-six | 梅奥路 23 号 | 加尔各答 | 印度 |

那么，让我们现在就开始吧！

## **SQL 中的注释**

在 SQL 中有两种注释方式，即[单行注释](#Single-Line%20Comments)或[多行注释](#Multi-Line%20Comments)。

### **单行注释**

单行注释以两个连字符(–)开始。因此，编译器将忽略任何在(–)后面直到一行末尾的文本。

#### **例如:**

```
--Select all:
SELECT * FROM Employee_Info;

```

### **多行评论**

多行评论以 **/*** 开头，以 ***/** 结尾。因此，编译器将忽略/*和*/之间提到的任何文本。

#### **例如:**

```
/*Select all the columns
of all the records
from the Employee_Info table:*/
SELECT * FROM Students;

```

## **SQL 命令:数据定义语言命令(DDL)**

本文的这一部分将让您深入了解定义数据库的命令。这些命令如下:

### **创建**

该语句用于创建表或数据库。

#### **【创建数据库】语句**

顾名思义，该语句用于创建数据库。

##### **语法**

```
CREATE DATABASE DatabaseName;
```

##### **例如**

```
CREATE DATABASE Employee;

```

#### **【创建表】语句**

该语句用于创建表。

##### **语法**

```
CREATE TABLE TableName (
Column1 datatype,
Column2 datatype,
Column3 datatype,
....

ColumnN datatype
);
```

##### **例如**

```
CREATE TABLE Employee_Info
(
EmployeeID int,
EmployeeName varchar(255),
Emergency ContactName varchar(255),
PhoneNumber int,
Address varchar(255),
City varchar(255),
Country varchar(255)
);

```

您也可以使用另一个表格来创建表格。参考下面的系统和示例:

#### **【创建表为】语句**

##### **语法**

```
CREATE TABLE NewTableName AS
SELECT Column1, column2,..., ColumnN
FROM ExistingTableName
WHERE ....;
```

##### **例如**

```
CREATE TABLE ExampleTable AS
SELECT EmployeeName, PhoneNumber
FROM Employee_Info;

```

### **降**

该语句用于删除现有的表或数据库。

#### **‘删除数据库’语句**

此语句用于删除现有数据库。使用此语句时，数据库中的所有信息都将丢失。

##### **语法**

```
DROP DATABASE DatabaseName;
```

##### **例如**

```
DROP DATABASE Employee;

```

#### **‘删除表’语句**

该语句用于删除现有的表。使用此语句时，表中的完整信息将会丢失。

##### **语法**

```
DROP TABLE TableName;
```

##### **例如**

```
DROP Table Employee_Info;

```

### **截断**

此命令用于删除表格中的信息，但不会删除表格。因此，一旦使用这个命令，您的信息将会丢失，但表不会。

##### **语法**

```
TRUNCATE TABLE TableName;
```

##### **例如**

```
TRUNCATE Table Employee_Info;

```

### **涂改**

该命令用于删除、修改或添加现有表中的约束或列。

#### **‘ALTER TABLE’语句**

该语句用于添加、删除、修改现有表中的列。

#### **带有添加/删除列的‘ALTER TABLE’语句**

您可以根据需要将 ALTER TABLE 语句与 ADD/DROP Column 命令结合使用。如果您希望添加一列，那么您将使用 add 命令，如果您希望删除一列，那么您将使用 DROP COLUMN 命令。

##### **语法**

```
ALTER TABLE TableName
ADD ColumnName Datatype;

ALTER TABLE TableName
DROP COLUMN ColumnName;
```

##### **例如**

```

--ADD Column BloodGroup:

ALTER TABLE Employee_Info
ADD BloodGroup varchar(255);

--DROP Column BloodGroup:

ALTER TABLE Employee_Info
DROP COLUMN BloodGroup ;

```

#### **带有更改/修改列的“更改表”语句**

此语句用于更改表中现有列的数据类型。

##### **语法**

```
ALTER TABLE TableName
ALTER COLUMN ColumnName Datatype;
```

##### **例如**

```

--Add a column DOB and change the data type to Date.

ALTER TABLE Employee_Info
ADD DOB year;

ALTER TABLE Employee_Info
ALTER DOB date;

```

### **备份数据库**

此语句用于创建现有数据库的完整备份。

##### **语法**

```
BACKUP DATABASE DatabaseName
TO DISK = 'filepath';
```

##### **例如**

```
BACKUP DATABASE Employee
TO DISK = 'C:UsersSahitiDesktop';

```

你也可以用 ***差分备份。*** 这种类型的备份仅备份自上次数据库完整备份以来发生更改的数据库部分。

##### **语法**

```
BACKUP DATABASE DatabaseName
TO DISK = 'filepath'
WITH DIFFERENTIAL;
```

##### **例如**

```
BACKUP DATABASE Employee
TO DISK = 'C:UsersSahitiDesktop'
WITH DIFFERENTIAL;

```

现在您已经知道了数据定义命令，让我带您了解在学习如何操作数据库之前您需要理解的各种类型的键和约束。

## **SQL 命令:数据库中不同类型的关键字**

数据库中主要有 7 种类型的关键字。我将考虑下面的表格，向您解释各种密钥。

![Different Types of Keys - SQL Commands - Edureka](img/efae26ee60a9970ec66a30d753c53c37.png)

*   **候选关键字—**可以唯一标识一个表的一组属性可以称为候选关键字。一个表可以有多个候选键，在选择的候选键中，可以选择一个键作为主键。在上面的示例中，由于 EmployeeID、InsuranceNumber 和 PanNumber 可以唯一地标识每个元组，因此它们将被视为候选键。
*   **超级键——**能够唯一标识一个元组的属性集合称为超级键。因此，候选键、主键和唯一键是超级键，但反之亦然。
*   **主键—**用来唯一标识每个元组的一组属性也是主键。在上面的示例中，由于 EmployeeID、InsuranceNumber 和 PanNumber 是候选键，因此它们中的任何一个都可以被选为主键。这里选择 EmployeeID 作为主键。
*   **备用键—**备用键是候选键，不会被选为主键。从上面的例子来看，备选键是 PanNumber 和 Insurance Number。
*   **唯一键【T1—**唯一键类似于主键，但在列中允许有一个空值。在这里，保险号和 Pan 号可以被认为是唯一的关键字。
*   **外键—**只能将当前值作为其他属性的值的属性，是它所引用的属性的外键。在上面的示例中，Employee_Information 表中的 Employee_ID 被引用到 Employee_Salary 表中的 Employee_ID。
*   **组合键【T1—**组合键是两列或更多列的组合，唯一标识每个元组。在这里，Employee_ID 和 Month-Year_Of_Salary 可以组合在一起，以唯一地标识表中的每个元组。

## **SQL 命令:数据库中使用的约束**

约束在数据库中用于指定表中数据的规则。以下是不同类型的约束:

*   [不为空](#NOT%20NULL)
*   [独特的](#UNIQUE)
*   [检查](#CHECK)
*   [默认](#DEFAULT)
*   [索引](#INDEX)

### **不为空**

此约束确保列不能有空值。

#### **例题**

```

--NOT NULL on Create Table

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL,
EmployeeName varchar(255) NOT NULL,
Emergency ContactName varchar(255),
PhoneNumber int NOT NULL,
Address varchar(255),
City varchar(255),
Country varchar(255)
);

--NOT NULL on ALTER TABLE

ALTER TABLE Employee_Info
MODIFY PhoneNumber int NOT NULL;

```

### **独特的**

此约束确保一列中的所有值都是唯一的。

#### **例子**

```

--UNIQUE on Create Table

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL UNIQUE,
EmployeeName varchar(255) NOT NULL,
Emergency ContactName varchar(255),
PhoneNumber int NOT NULL,
Address varchar(255),
City varchar(255),
Country varchar(255)
);

--UNIQUE on Multiple Columns

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL,
EmployeeName varchar(255) NOT NULL,
Emergency ContactName varchar(255),
PhoneNumber int NOT NULL,
Address varchar(255),
City varchar(255),
Country varchar(255),
CONSTRAINT UC_Employee_Info UNIQUE(Employee_ID, PhoneNumber)
);

--UNIQUE on ALTER TABLE

ALTER TABLE Employee_Info
ADD UNIQUE (Employee_ID);

--To drop a UNIQUE constraint

ALTER TABLE  Employee_Info
DROP CONSTRAINT UC_Employee_Info;

```

### **检查**

此约束确保列中的所有值都满足特定条件。

#### **例题**

```

--CHECK Constraint on CREATE TABLE

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL,
EmployeeName varchar(255),
Emergency ContactName varchar(255),
PhoneNumber int,
Address varchar(255),
City varchar(255),
Country varchar(255) CHECK (Country=='India')
);

--CHECK Constraint on multiple columns

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL,
EmployeeName varchar(255),
Emergency ContactName varchar(255),
PhoneNumber int,
Address varchar(255),
City varchar(255),
Country varchar(255) CHECK (Country = 'India' AND Cite = 'Hyderabad')
);

--CHECK Constraint on ALTER TABLE

ALTER TABLE Employee_Info
ADD CHECK (Country=='India');

--To give a name to the CHECK Constraint

ALTER TABLE Employee_Info
ADD CONSTRAINT CheckConstraintName CHECK (Country=='India');

--To drop a CHECK Constraint

ALTER TABLE Employee_Info
DROP CONSTRAINT CheckConstraintName;

```

### **默认**

当没有指定值时，此约束由一组列的默认值组成。

#### **例题**

```

--DEFAULT Constraint on CREATE TABLE

CREATE TABLE Employee_Info
(
EmployeeID int NOT NULL,
EmployeeName varchar(255),
Emergency ContactName varchar(255),
PhoneNumber int,
Address varchar(255),
City varchar(255),
Country varchar(255) DEFAULT 'India'
);

--DEFAULT Constraint on ALTER TABLE

ALTER TABLE Employee_Info
ADD CONSTRAINT defau_Country
DEFAULT 'India' FOR Country;

--To drop the Default Constraint

ALTER TABLE Employee_Info
ALTER COLUMN Country DROP DEFAULT;

```

### **指标**

该约束用于在表中创建索引，通过索引，您可以非常快速地创建和检索数据库中的数据。

#### **语法**

```
--Create an Index where duplicate values are allowed
CREATE INDEX IndexName
ON TableName (Column1, Column2, ...ColumnN);

--Create an Index where duplicate values are not allowed
CREATE UNIQUE INDEX IndexName
ON TableName (Column1, Column2, ...ColumnN);
```

#### **例题**

```

CREATE INDEX idex_EmployeeName
ON Persons (EmployeeName);

--To delete an index in a table

DROP INDEX Employee_Info.idex_EmployeeName;

```

现在，让我们看看本文的下一部分，即 DML 命令。

## **SQL 命令:数据操作语言命令(DML)**

本文的这一部分将让您深入了解可以用来操作数据库的命令。这些命令如下:

除了这些命令，还有其他操作符/功能，如:

### **使用**

USE 语句用于选择要对其执行操作的数据库。

#### **语法**

```
USE DatabaseName;
```

#### **例子**

```
USE Employee;

```

### **插入到**

该语句用于向表中插入新记录。

#### **语法**

```
INSERT INTO TableName (Column1, Column2, Column3, ...,ColumnN)
VALUES (value1, value2, value3, ...);

--If you don't want to mention the column names then use the below syntax

INSERT INTO TableName
VALUES (Value1, Value2, Value3, ...);
```

**例子**

```

INSERT INTO Employee_Info(EmployeeID, EmployeeName, Emergency ContactName, PhoneNumber, Address, City, Country)
VALUES ('06', 'Sanjana','Jagannath', '9921321141', 'Camel Street House No 12', 'Chennai', 'India');

INSERT INTO Employee_Info
VALUES ('07', 'Sayantini','Praveen', '9934567654', 'Nice Road 21', 'Pune', 'India');

```

### **更新**

该语句用于修改表中已经存在的记录。

#### **语法**

```
UPDATE TableName
SET Column1 = Value1, Column2 = Value2, ...
WHERE Condition;
```

#### **例子**

```
UPDATE Employee_Info
SET EmployeeName = 'Aahana', City= 'Ahmedabad'
WHERE EmployeeID = 1;

```

### **删除**

该语句用于删除表中已有的记录。

#### **语法**

```
DELETE FROM TableName WHERE Condition;
```

#### **例子**

```
DELETE FROM Employee_Info
WHERE EmployeeName='Preeti';

```

### **选择**

该语句用于从数据库中选择数据，返回的数据存储在结果表中，称为 **结果集** 。

#### **语法**

```
SELECT Column1, Column2, ...ColumN
FROM TableName;

--(*) is used to select all from the table
SELECT * FROM table_name;

-- To select the number of records to return use:
SELECT TOP 3 * FROM TableName;
```

#### **例子**

```

SELECT EmployeeID, EmployeeName
FROM Employee_Info;

--(*) is used to select all from the table
SELECT * FROM Employee_Info;

-- To select the number of records to return use:
SELECT TOP 3 * FROM Employee_Info;

```

除了单独使用 SELECT 关键字之外，您还可以在 SELECT 语句中使用以下关键字:

#### **“SELECT DISTINCT”语句**

该语句仅用于返回不同的值。

##### **语法**

```
SELECT DISTINCT Column1, Column2, ...ColumnN
FROM TableName;
```

##### **例如**

```
SELECT DISTINCT PhoneNumber FROM Employee_Info;

```

#### **‘ORDER BY’语句**

“ORDER BY”语句用于按升序或降序对所需结果进行排序。默认情况下，结果按升序排序。然而，如果你希望以降序得到所需的结果，你必须使用 **DESC** 关键字。

##### **语法**

```
SELECT Column1, Column2, ...ColumnN
FROM TableName
ORDER BY Column1, Column2, ... ASC|DESC;
```

##### **例如**

```

-- Select all employees from the 'Employee_Info' table sorted by EmergencyContactName:
SELECT * FROM Employee_Info
ORDER BY EmergencyContactName;

-- Select all employees from the 'Employee_Info' table sorted by EmergencyContactName in Descending order:
SELECT * FROM Employee_Info
ORDER BY EmergencyContactName DESC;

-- Select all employees from the 'Employee_Info' table sorted by EmergencyContactName and EmployeeName:
SELECT * FROM Employee_Info
ORDER BY EmergencyContactName, EmployeeName;

/* Select all employees from the 'Employee_Info' table sorted by EmergencyContactName in Descending order and EmployeeName in Ascending order: */
SELECT * FROM Employee_Info
ORDER BY EmergencyContactName ASC, EmployeeName DESC;

```

#### **“分组依据”语句**

此“GROUP BY”语句与聚合函数一起使用，按一列或多列对结果集进行分组。

##### **语法**

```
SELECT Column1, Column2,..., ColumnN
FROM TableName
WHERE Condition
GROUP BY ColumnName(s)
ORDER BY ColumnName(s);
```

##### **例如**

```

-- To list the number of employees from each city.

SELECT COUNT(EmployeeID), City
FROM Employee_Info
GROUP BY City;

```

#### 的‘HAVING’从句

在 SQL 中使用“HAVING”子句是因为不能在任何地方使用关键字的**。**

##### **语法**

```
SELECT ColumnName(s)
FROM TableName
WHERE Condition
GROUP BY ColumnName(s)
HAVING Condition
ORDER BY ColumnName(s);
```

##### **例如**

```

/*&nbsp;&nbsp;To list the number of employees in each city. The employees should be sorted high to low and only those cities must be included who have more than 5 employees:*/

SELECT COUNT(EmployeeID), City
FROM Employee_Info
GROUP BY City
HAVING COUNT(EmployeeID) > 2
ORDER BY COUNT(EmployeeID) DESC;

```

#### **‘SELECT INTO’语句**

“SELECT INTO”语句用于将数据从一个表复制到另一个表。

##### **语法**

```
SELECT *
INTO NewTable [IN ExternalDB]
FROM OldTable
WHERE Condition;
```

##### **例如**

```

-- To create a backup of database 'Employee'
SELECT * INTO EmployeeBackup
FROM Employee;

--To select only few columns from Employee
SELECT EmployeeName, PhoneNumber INTO EmployeeContactDetails
FROM Employee;

SELECT * INTO BlrEmployee
FROM Employee
WHERE City = 'Bangalore';

```

现在，正如我之前提到的，让我们进入本文中关于 SQL 命令的下一部分，即操作符。

### **SQL 中的运算符**

SQL 中可用的不同运算符集如下:

![Operators in SQL - SQL Commands - Edureka](img/3bd74d5edb8887bbaf163b3132c5c3c5.png)

让我们一个一个地研究它们。

#### **算术运算符**

| **操作员** | **描述** |
| % | 模[A % B] |
| / | 分区[甲/乙] |
| * | 乘法[A * B] |
| – | 减法[A–B] |
| + | 加法[A + B] |

#### **按位运算符**

| **操作员** | **描述** |
| ^ | 按位异或(XOR) [A ^ B] |
| &#124; | 按位 OR [A &#124; B] |
| & | 按位与[A & B] |

#### **比较运算符**

| **操作员** | **描述** |
| < > | 不等于[A < > B] |
| <= | 小于或等于[A <= B] |
| >= | 大于或等于[A >= B] |
| < | 小于[A < B] |
| > | 大于[A > B] |
| = | 等于[A = B] |

#### **复合运算符**

| **操作员** | **描述** |
| &#124;*= | 按位或等于 [A &#124;*= B] |
| ^-= | 按位异或等于【a ^-= b】 |
| &= | 按位与等于【A&= B】 |
| %= | 模等于 [A %= B] |
| /= | 除等于 [A /= B] |
| *= | 乘等于 [A*= B] |
| -= | 减去等于[A-= B] |
| += | 相加等于[A+= B] |

#### **逻辑运算符**

SQL 中的逻辑运算符如下:

##### **和**

该运算符用于过滤依赖于多个条件的记录。该操作符显示满足由 AND 分隔的所有条件的记录，并给出 TRUE 输出。

###### **语法**

```
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE Condition1 AND Condition2 AND Condition3 ...;
```

###### **例如**

```
SELECT * FROM Employee_Info
WHERE City='Mumbai' AND City='Hyderabad';</pre>

```

##### **或**操作员

该操作符显示满足由 or 分隔的任何条件的所有记录，并给出输出 TRUE。

###### **语法**

```
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE Condition1 OR Condition2 OR Condition3 ...;
```

###### **例如**

```
SELECT * FROM Employee_Info
WHERE City='Mumbai' OR City='Hyderabad';

```

##### **不算符**

当您想要显示不满足条件的记录时，可以使用 NOT 运算符。

###### **语法**

```
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE NOT Condition;
```

###### **例如**

```
SELECT * FROM Employee_Info
WHERE NOT City='Mumbai';

```

*NOTE: You can also combine the above three operators and write a query as follows:*

```
**SELECT * FROM Employee_Info
WHERE NOT Country='India' AND (City='Bangalore' OR City='Hyderabad');** 
```

***NOTE: You can also combine the above three operators and write a query as follows:***

```
****SELECT * FROM Employee_Info
WHERE NOT Country='India' AND (City='Bangalore' OR City='Hyderabad');**** 
```

##### ******间符******

****当您希望选择给定范围内的值时，可以使用 BETWEEN 运算符。因为这是一个包含运算符，所以起始值和结束值都要考虑。****

###### ******语法******

```
****SELECT ColumnName(s)
FROM TableName
WHERE ColumnName BETWEEN Value1 AND Value2;****
```

###### ******例如******

```
****SELECT * FROM Employee_Salary
WHERE Salary BETWEEN 40000 AND 50000;**** 
```

##### ******像符******

****在 WHERE 子句中使用 LIKE 运算符来搜索表中某一列的指定模式。与 LIKE 操作符结合使用的通配符主要有两个:****

*****   **%**–匹配 0 个或更多字符。*   **_**–它只匹配一个字符。****

###### ******语法******

```
****SELECT ColumnName(s)
FROM TableName
WHERE ColumnName LIKE pattern;****
```

****请参考下表，了解您可以使用 LIKE 运算符提及的各种模式。****

| **像符条件** | **描述** |
| 其中 CustomerName 喜欢“v %” | 查找任何以“v”开头的值 |
| 其中 CustomerName 喜欢“% v” | 查找任何以“v”结尾的值 |
| 其中 CustomerName 喜欢“%和%” | 查找任何位置有“and”的值 |
| 其中 CustomerName 喜欢' _q%' | 查找第二个位置有“q”的任何值。 |
| 其中 CustomerName 喜欢“u _ % _ %” | 查找任何以“u”开头且长度至少为 3 个字符的值 |
| 其中联系人姓名如“m % a” | 查找以“m”开头、以“a”结尾的任何值 |

###### ******例如******

```
****SELECT * FROM Employee_Info
WHERE EmployeeName LIKE 'S%';**** 
```

##### ******中的**符****

****该运算符用于多个 or 条件的。这允许您在 WHERE 子句中指定多个值。****

###### ******语法******

```
****SELECT ColumnName(s)
FROM TableName
WHERE ColumnName IN (Value1,Value2...);****
```

###### ******例如******

```
****SELECT * FROM Employee_Info
WHERE City IN ('Mumbai', 'Bangalore', 'Hyderabad');**** 
```

*****NOTE: You can also use IN while writing Nested Queries.*****

##### ********存在操作符********

******EXISTS 运算符用于测试记录是否存在。******

###### ********语法********

```
******SELECT ColumnName(s)
FROM TableName
WHERE EXISTS
(SELECT ColumnName FROM TableName WHERE condition);******
```

###### ********例如********

```
******SELECT EmergencyContactName
FROM Employee_Info
WHERE EXISTS (SELECT EmergencyContactName FROM Employee_Info WHERE EmployeeId = 05 AND City = 'Kolkata');****** 
```

##### ********所有操作员********

******ALL 运算符与 WHERE 或 [HAVING 子句](#HAVING%20Clause)一起使用，如果所有子查询值都满足条件，则返回 TRUE。******

###### ********语法********

```
******SELECT ColumnName(s)
FROM TableName
WHERE ColumnName operator ALL
(SELECT ColumnName FROM TableName WHERE condition);******
```

###### ********例如********

```
******SELECT EmployeeName
FROM Employee_Info
WHERE EmployeeID = ALL (SELECT EmployeeID FROM Employee_Info WHERE City = 'Hyderabad');****** 
```

##### ********任意操作员********

******与 ALL 运算符类似，ANY 运算符也与 WHERE 或 [HAVING 子句](#HAVING%20Clause)一起使用，如果任何子查询值满足条件，则返回 true。******

###### ********语法********

```
******SELECT ColumnName(s)
FROM TableName
WHERE ColumnName operator ANY
(SELECT ColumnName FROM TableName WHERE condition);******
```

###### ********例如********

```
******SELECT EmployeeName
FROM Employee_Info
WHERE EmployeeID = ANY (SELECT EmployeeID FROM Employee_Info WHERE City = 'Hyderabad' OR City = 'Kolkata');****** 
```

******接下来，在这篇关于 SQL 命令的文章中，让我们看看 SQL 中提供的各种聚合函数。******

### ********聚合函数********

******这部分文章将包括以下功能:******

#### ********MIN()函数********

******MIN 函数返回表格中选定列的最小值。******

##### ********语法********

```
******SELECT MIN(ColumnName)
FROM TableName
WHERE Condition;******
```

##### ********例如********

```
******SELECT MIN(EmployeeID) AS SmallestID
FROM Employee_Info;****** 
```

#### ********MAX()函数********

******MAX 函数返回表格中选定列的最大值。******

##### ********语法********

```
******SELECT MAX(ColumnName)
FROM TableName
WHERE Condition;******
```

##### ********例如********

```
******SELECT MAX(Salary) AS LargestFees
FROM Employee_Salary;****** 
```

#### ********计数()函数********

******COUNT 函数返回符合指定条件的行数。******

##### ********语法********

```
******SELECT COUNT(ColumnName)
FROM TableName
WHERE Condition;******
```

##### ********例如********

```
******SELECT COUNT(EmployeeID)
FROM Employee_Info;****** 
```

#### ********SUM()函数********

******SUM 函数返回所选数值列的总和。******

##### ********语法********

```
******SELECT SUM(ColumnName)
FROM TableName
WHERE Condition;******
```

##### ********例如********

```
******SELECT SUM(Salary)
FROM Employee_Salary;****** 
```

#### ********AVG()函数********

******AVG 函数返回所选数值列的平均值。******

##### ********语法********

```
******SELECT AVG(ColumnName)
FROM TableName
WHERE Condition;******
```

##### ********例如********

```
******SELECT AVG(Salary)
FROM Employee_Salary;****** 
```

### ********空函数********

******空函数是那些让你在表达式为空时返回可选值的函数。在 SQL Server 中，函数是 **ISNULL()** 。******

#### ********例如********

```
******SELECT EmployeeID * (Month_Year_of_Salary + ISNULL(Salary, 0))
FROM Employee_Salary;****** 
```

### ********化名&案情陈述********

******在本文关于 SQL 命令的这一部分中，您将一个接一个地浏览[别名](#Aliases)和 [Case 语句](#Case%20statement)。******

#### ********别名********

******别名用于给列/表一个临时名称，并且只在查询期间存在。******

##### ********语法********

```
******--Alias Column Syntax

SELECT ColumnName AS AliasName
FROM TableName;

--Alias Table Syntax

SELECT ColumnName(s)
FROM TableName AS AliasName;******
```

##### ********例如********

```
 ******SELECT EmployeeID AS ID, EmployeeName AS EmpName
FROM Employee_Info;

SELECT EmployeeName AS EmpName, EmergencyContactName AS [Contact Name]
FROM Employee_Info;****** 
```

#### ********病例报告********

******该语句遍历所有条件，并在满足第一个条件时返回值。因此，如果没有条件为真，它将返回 ELSE 子句中的值。此外，如果没有条件为真并且没有 ELSE 部分，则它返回 NULL。******

##### ********语法********

```
******CASE
WHEN Condition1 THEN Result1
WHEN Condition2 THEN Result2
WHEN ConditionN THEN ResultN
ELSE Result
END;******
```

##### ********例如********

```
******SELECT EmployeeName, City
FROM Employee_Info
ORDER BY
(CASE
    WHEN City IS NULL THEN 'Country is India by default'
    ELSE City
END);****** 
```

******现在，我已经在这篇关于 SQL 命令的文章中告诉了你很多关于 DML 命令的内容，让我简单地告诉你关于[嵌套查询、](#Nested%20Queries) [连接](#Joins) 、 [集合操作](#Set%20Operations)和[日期&自动递增](#Dates%20and%20Auto%20Increment) 。******

## ********SQL 命令:嵌套查询********

********嵌套查询** 是那些有外部查询和内部子查询的查询。因此，基本上，子查询是嵌套在另一个查询中的查询，例如 [SELECT](#SELECT) 、 [INSERT](#INSERT%20INTO) 、 [UPDATE](#UPDATE) 或 [DELETE](#DELETE) 。参考下图:******

## ********![Nested Queries - SQL Commands - Edureka](img/53e776d292741c934ea9e84df2fade24.png) SQL 命令:加入********

******联接用于根据两个或多个表之间的相关列来组合这些表中的行。以下是连接的类型:******

*******   **[内部连接:](#INNER%20JOIN:)** 该连接返回那些在两个表中都有匹配值的记录。*   **[完全连接:](#FULL%20JOIN:)** 该连接返回在左表或右表中匹配的所有记录。*   **[左连接:](#LEFT%20JOIN:)** 该连接返回左表中的记录，以及右表中满足条件的记录。*   **[右连接:](#RIGHT%20JOIN:)** 该连接返回右表中的记录，以及左表中满足条件的记录。******

******参考下图。******

## ********![Joins in SQL - SQL Commands - Edureka](img/6c917e075d4b4e7a84294c127a9ce2ca.png)********

******除了 Employee_Info 表之外，让我们考虑下面的表，以理解连接的语法。******

| **TechID** | **【empid】** | **【技术名称】** | **项目开始日期** |
| 1 | 10 | DevOps | 2019 年 04 月 01 日 |
| 2 | 11 | 区块链 | 2019 年 06 月 07 日 |
| 3 | 12 | Python | 2019 年 01 月 03 日 |

********内部连接********

#### ********语法********

```
******SELECT ColumnName(s)
FROM Table1
INNER JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;******
```

#### ********例子********

```
******SELECT Technologies.TechID, Employee_Info.EmployeeName
FROM Technologies
INNER JOIN Employee_Info ON Technologies.EmpID = Employee_Info.EmpID;****** 
```

### ********完全加入********

#### ********语法********

```
******SELECT ColumnName(s)
FROM Table1
FULL OUTER JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;******
```

#### ********例子********

```
******SELECT Employee_Info.EmployeeName, Technologies.TechID
FROM Employee_Info
FULL OUTER JOIN Orders ON Employee_Info.EmpID=Employee_Salary.EmpID
ORDER BY Employee_Info.EmployeeName;****** 
```

### ********左加入********

#### ********语法********

```
******SELECT ColumnName(s)
FROM Table1
LEFT JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;******
```

#### ********例子********

```
******SELECT Employee_Info.EmployeeName, Technologies.TechID
FROM Employee_Info
LEFT JOIN Technologies ON Employee_Info.EmployeeID = Technologies.EmpIDID
ORDER BY Employee_Info.EmployeeName;****** 
```

### ********右加入********

#### ********语法********

```
******SELECT ColumnName(s)
FROM Table1
RIGHT JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;******
```

#### ********例子********

```
******SELECT Technologies.TechID
FROM Technologies
RIGHT JOIN Employee_Info ON Technologies.EmpID = Employee_Info.EmployeeID
ORDER BY Technologies.TechID;****** 
```

## ********SQL 命令:设置操作********

******主要有三种集合运算:[联合](#UNION)、[相交](#INTERSECT)、[除](#EXCEPT)。可以参考下图来理解 SQL 中的 set 操作。******

******![Set Operations - SQL Commands - Edureka](img/cd5c9788f381c4cf7069dc19cf230896.png)******

### ********联盟********

******该操作符用于合并两个或多个 [SELECT](#SELECT) 语句的结果集。******

#### ********语法********

```
******SELECT ColumnName(s) FROM Table1
UNION
SELECT ColumnName(s) FROM Table2;******
```

### ********相交********

******该子句用于组合两个 [选择](#SELECT) 语句，并返回两个选择语句的数据集的交集。******

#### ********语法********

```
******SELECT Column1 , Column2 ....
FROM TableName
WHERE Condition

INTERSECT

SELECT Column1 , Column2 ....
FROM TableName
WHERE Condition******
```

### ********除了********

******该操作符返回第一个[选择](#SELECT)操作返回的元组，而不是第二个选择操作返回的元组。******

#### ********语法********

```
******SELECT ColumnName
FROM TableName

EXCEPT

SELECT ColumnName
FROM TableName;******
```

******接下来，在本文中，让我们看看日期函数和自动递增字段。******

## ********SQL 命令:日期&自动递增********

******在本文的这一部分，我将向您解释如何使用[日期函数](#Dates)以及[自动递增](#Auto-Increment)字段。******

### ********日期********

******SQL Server 中存在以下数据类型，用于在数据库中存储日期或日期/时间值。******

| **数据类型** | **格式** |
| 日期 | 年-月-日 |
| 日期时间 | YYYY-MM-DD HH:MI:SS |
| SMALLDATETIME | YYYY-MM-DD HH:MI:SS |
| 时间戳 | 唯一的号码 |

#### ********例子********

```
******SELECT * FROM Technologies WHERE ProjectStartDate='2019-04-01'****** 
```

### ********自动增量********

******当一条新记录被插入表格时，该字段自动生成一个唯一的编号。MS SQL Server 使用**标识**关键字来实现这个特性。******

#### ********例子********

```
 ******<span>/* To define the "EmployeeID" column to be an auto-increment primary key field in the "Employee_Info" table */</span>

<span>CREATE TABLE Employee_Info (</span>
<span>EmployeeID INT IDENTITY(1,1) PRIMARY KEY,</span>
<span>EmployeeName VARCHAR(255) NOT NULL</span>
<span>EmergencyContactName VARCHAR(255) NOT NULL,</span>
<span>);</span>****** 
```

******现在，你们已经知道了 DML 命令，让我们进入本文的下一部分SQL 命令，即 DCL 命令。******

## ********SQL 命令:数据控制语言命令********

******本文的这一部分将让您深入了解用于在多用户数据库环境中加强数据库安全性的命令。命令如下:******

### ********授********

******该命令用于向用户提供对数据库及其对象的访问或权限。******

#### ********语法********

```
******GRANT PrivilegeName
ON ObjectName
TO {UserName |PUBLIC |RoleName}
[WITH GRANT OPTION];******
```

******其中，******

*******   **特权名称**–授予用户的特权/权利/访问权。*   **object Name**–数据库对象的名称，如表/视图/存储过程。*   **用户名**–被授予访问/权限/特权的用户的名称。*   **PUBLIC**–授予所有用户访问权限。*   **RoleName**–一组特权的名称。*   **WITH GRANT OPTION**–给予用户访问权限，授予其他用户权限。******

#### ********例子********

```
******-- To grant SELECT permission to Employee_Info table to user1
GRANT SELECT ON Employee_Info TO user1;****** 
```

### ********撤销********

******该命令用于撤销使用[授予](#GRANT)命令授予的用户访问权限。******

#### ********语法********

```
******REVOKE PrivilegeName 
ON ObjectName 
FROM {UserName |PUBLIC |RoleName}******
```

#### ********例题********

```
******-- To revoke the granted permission from user1
REVOKE SELECT ON Employee_Info TO user1;****** 
```

******现在，在这篇关于 SQL 命令的文章中，我将讨论[视图](#Views)、[存储过程](#Stored%20Procedures)和[触发器](#Triggers)。******

## ********SQL 命令:视图********

******SQL 中的视图是从其他表派生的单个表。因此，视图包含类似于真实表的行和列，并且具有来自一个或多个表的字段。******

******![Views - SQL Commands - Edureka](img/cc16869efc494f91d67aece7b8d92008.png)******

### ********【创建视图】语句********

******该语句用于从表中创建视图。******

#### ********语法********

```
******CREATE VIEW ViewName AS
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE Condition;******
```

#### ********例子********

```
******CREATE VIEW [Kolkata Employees] AS
SELECT EmployeeName, PhoneNumber
FROM Employee_Info
WHERE City = "Kolkata";****** 
```

### ********【创建或替换视图】语句********

******该语句用于更新视图。******

#### ********语法********

```
******CREATE VIEW OR REPLACE ViewName AS
SELECT Column1, Column2, ..., ColumnN
FROM TableName
WHERE Condition;******
```

#### ********例子********

```
******CREATE VIEW OR REPLACE [Kolkata Employees] AS
SELECT EmployeeName, PhoneNumber
FROM Employee_Info
WHERE City = "Kolkata";****** 
```

### ********【降视图】语句********

******该语句用于删除视图。******

#### ********语法********

```
******DROP VIEW ViewName;******
```

#### ********例子********

```
******DROP VIEW [Kolkata Employees];****** 
```

## ********SQL 命令:存储过程********

******可以保存并再次使用的代码被称为存储过程。******

#### ********语法********

```
******CREATE PROCEDURE ProcedureName
AS
SQLStatement
GO;******
```

#### ********例子********

```
******EXEC ProcedureName;****** 
```

## ********SQL 命令:触发********

******触发器是存储在数据库目录中的一组 SQL 语句。每当与表相关联的事件发生时，就会执行这些语句。因此，通过**插入**、**更新**或**删除**语句，可以在之前的**或**之后的**调用**触发器**。参考下图。********

******![Triggers in SQL - SQL Commands - Edureka](img/4beac631c2f40bbf315541081983a116.png)******

### ********语法********

```
******CREATE TRIGGER [TriggerName]
[BEFORE | AFTER]
{INSERT | UPDATE | DELETE}
on [TableName]
[FOR EACH ROW]
[TriggerBody]******
```

******现在，让我们转到本文的最后一节 SQL 命令，即事务控制语言命令。******

## ********SQL 命令:事务控制语言命令(TCL)********

******本文的这一部分将让您深入了解用于管理数据库中事务的命令。命令如下:******

### ********提交********

******该命令用于将事务保存到数据库中。******

#### ********语法********

```
******COMMIT;******
```

### ********回滚********

******该命令用于将数据库恢复到上次提交的状态。******

#### ********语法********

```
******ROLLBACK;******
```

*******NOTE: When you use ROLLBACK with SAVEPOINT, then you can directly jump to a savepoint in an ongoing transaction. Syntax: ROLLBACK TO SavepointName;*******

### ********保存点**T3]******

******该命令用于临时保存交易。因此，如果您希望回滚到任一点，那么您可以将该点保存为“保存点”。******

#### ********语法********

```
******SAVEPOINT SAVEPOINTNAME;******
```

******考虑下面的例子来理解数据库中事务的工作。******

| **员工 ID** | **EmployeeName** |
|  01 | 鲁哈安 |
| 02 | 苏哈纳 |
| 03 | 哦，天啊 |
| 04 | 阿拉希 |

******现在，使用下面的 SQL 查询来理解数据库中的事务。******

```
******INSERT INTO Employee_Table VALUES(05, 'Avinash');
COMMIT;
UPDATE Employee_Table SET name = 'Akash' WHERE id = '05';
SAVEPOINT S1;
INSERT INTO Employee_Table VALUES(06, 'Sanjana');
SAVEPOINT S2;
INSERT INTO Employee_Table VALUES(07, 'Sanjay');
SAVEPOINT S3;
INSERT INTO Employee_Table VALUES(08, 'Veena');
SAVEPOINT S4;
SELECT * FROM Employee_Table;****** 
```

*********上面这组查询的输出如下:*********

| **员工 ID** | **EmployeeName** |
|  01 | 鲁哈安 |
| 02 | 苏哈纳 |
| 03 | 哦，天啊 |
| 04 | 阿拉希 |
| 05 | 阿卡什 |
| 06 | 桑吉娜 |
| 07 | 桑杰（男子名） |
| 08 | 印度的七弦琴 |

*********现在，如果使用下面的查询回滚到 S2，输出会在下表中列出。*********

```
******ROLLBACK TO S2;
SELECT * FROM Employee_Table;****** 
```

| **员工 ID** | **EmployeeName** |
|  01 | 鲁哈安 |
| 02 | 苏哈纳 |
| 03 | 哦，天啊 |
| 04 | 阿拉希 |
| 05 | 阿卡什 |
| 06 | 桑吉娜 |

******至此，我结束了这篇关于 SQL 命令的文章。我希望您喜欢阅读这篇关于 SQL 命令的文章。我们已经看到了帮助您编写查询和处理数据库的不同命令。 *如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*******

*******有问题吗？请在“ **SQL 命令**的评论部分提出来，我会回复你。*******