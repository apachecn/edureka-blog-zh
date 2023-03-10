# SQLite 教程:您需要知道的一切

> 原文：<https://www.edureka.co/blog/sqlite-tutorial/>

如果你曾经使用过关系数据库系统，你可能听说过一些流行的数据库系统，比如 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 、 [SQL](https://www.edureka.co/blog/sql-commands) 服务器或者 [PostgreSQL](https://www.edureka.co/blog/postgresql-tutorial) 。SQLite 是另一个非常有用的 RDBMS，它的设置和操作非常简单。此外，与其他关系数据库 相比，它有许多独特的特性。本 SQLite 教程教授您需要在大量实践的帮助下了解的基本概念。

本文讨论的主题是:

*   [什么是 SQLite？](#sqlite)
    *   [SQLite 的特性](#features)
*   [在 Windows 上安装 SQLite](#installing)
*   [SQLite 命令](#commands)
    *   [数据库命令](#database)
    *   [表格命令](#table)
    *   [积垢操作](#crud)
    *   [SQLite 条款/条件](#conditions)
    *   [加入 SQLite](#joins)
*   [SQLite 的缺点](#disadvantages)

## **SQLite 教程:什么是 SQLite？**

下面是 SQLite 的行业标准定义:

*SQLite is an open-source, zero-configuration, self-contained, stand-alone, transaction relational database engine designed to be embedded into an application.*

**可以考虑将 **SQLite** 作为其他复杂 RDBMS (Oracle、 [SQL](https://www.edureka.co/blog/sql-commands) 等)的“ **打火机** ”版本。)，其数据库引擎配置为*独立处理(进程内库)* ，即 ***无服务器、自包含、零配置、事务性*** 。它以其可移植性、可靠性以及即使在低内存环境下的强大性能而闻名。此外，SQLite 是一种流行的选择，作为最终程序或应用程序中本地/客户端存储的嵌入式数据库，这与其他 RDBMS 不同，后者配置了客户端-服务器 DB 引擎。**

### ****SQLite 的特性****

**SQLite 提供了许多独特的特性，例如:**

***   **无服务器:**大多数 [SQL 数据库](https://www.edureka.co/blog/sql-basics/) 都是作为一个单独的服务器进程实现的，但是 SQLite 没有单独的服务器进程。它是一个无服务器的数据库引擎。它直接读写普通磁盘文件。*   **零配置:** It 不需要任何配置就能运行。这意味着，不需要像在客户机/服务器系统中那样启动、停止或配置服务器进程。*   **清单类型:** SQLite 使用清单类型，它允许将任意数量的任意数据类型存储到任意列中，而不管该列声明的数据类型是什么。请注意，这条规则有一些例外。*   **轻量级:**顾名思义，SQLite 库是非常轻量级的。事实是，尽管它所占用的空间因安装的系统而异，但它只占用不到 600 千磅的空间。*   **可移植:**与其他 DBMS 不同，整个 SQLite 数据库存储在一个文件中。 该文件可以通过可移动介质或文件传输协议非常轻松地共享。*   **多样选择:** 很多编程语言都为 SQLite 提供了绑定，包括 [C](https://www.edureka.co/blog/c-programming-tutorial/) 、 [C++](https://www.edureka.co/blog/cpp-tutorial/) 、 [C#](https://www.edureka.co/blog/c-sharp-tutorial/) 、 [Java](https://www.edureka.co/blog/java-tutorial/) 、 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 、 [Ruby](https://www.edureka.co/blog/ruby-on-rails-tutorial/) 、 [Python](https://www.edureka.co/blog/videos/python-tutorial/) 等等。*   **免费:** SQLite 是免费开源的。使用 SQLite 不需要商业许可。**

**如上所列，SQLite 以其零配置而闻名，这意味着实际上不需要复杂的设置或管理。在本 SQLite 教程的下一部分，让我们看看如何在您的系统上安装 SQLite。**

## ****SQLite 教程:在 Windows 上安装 SQLite****

**接下来的步骤是:**

****Step1:** 进入[官方 SQLite](https://www.sqlite.org/download.html) 网站，点击合适的链接下载预编译二进制文件。**

****第二步:**下载 SQLite 命令行 zip 文件(此处:**SQLite-tools-win32-x86-3270200 . zip)**，将这些文件展开到自己选择的文件夹中。**

**这个 SQLite 命令行工具将包含以下 SQLite 产品**

***   **SQLite 核心**:SQLite 核心包含实际的数据库引擎和公共 API。*   **SQLite3 命令行工具**:SQLite3 应用程序是一个命令行工具，构建在 SQLite 核心之上。*   **Tcl 扩展**:这个库本质上是 SQLite 核心的副本，附带了 Tcl 绑定。*   **SQLite 分析工具**:SQLite 分析工具用于分析数据库文件。**

****Step3:** 之后初始化 SQLite 命令行就像点击 sqlite3 应用一样简单，会弹出命令行。**

**如果你想进一步测试，只需输入 **。帮助 **sqlite >** 提示符下的** 命令，查看 **sqlite3** 中所有可用的命令，如下图所示。**

*****注意:**默认情况下，SQLite 会话使用内存数据库，因此，当会话结束时，所有更改都将消失。***

**够简单吧？然后，让我们从 SQLite 命令开始。**

## ****SQLite 教程:SQLite 命令****

**SQLite 教程的这一部分介绍了可用于 SQLite 的基本 SQL 语句。**

****注意:** SQLite 命令以分号(`;` ) 结尾。它告诉 SQLite 您的命令已经完成，应该运行了。此外，您可以将命令扩展到多行，并在最后一行使用分号。**

### ****数据库命令****

**这个部分由那些命令组成，通过它们你可以处理你的数据库。这些命令是:**

***   **SQLite 创建数据库****

**SQLite 不像其他关系数据库管理系统那样使用 CREATE DATABASE 语句，比如 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) ，SQL Server 等。要在 SQLite 中创建新的数据库，只需输入 sqlite3，后跟您希望用于该数据库的文件名。下面的代码创建了一个名为<samp>student details . db:</samp>T5 的数据库文件**

***例如***

```
**sqlite3 StudentDetails.db;

sqlite> .databases 
main: D:sqliteStudentDetails.db;** 
```

***   **SQLite 附加数据库****

**当您有多个数据库时，一次只能使用一个。在 SQLite 中，ATTACH DATABASE 语句用于为当前连接附加特定的数据库。一个在这个命令之后，所有的 SQLite 语句将在附加的数据库下执行。**

***例如***

```
 **sqlite> ATTACH DATABASE 'DepartmentDetails.db' AS 'Department';

sqlite> .databases
main: D:sqliteStudentDetails.db;
Department: D:sqliteDepartmentDetails.db**
```

***   **SQLite 分离数据库****

**在 SQLite 中，DETACH DATABASE 语句用于将别名数据库从先前使用 ATTACH 语句连接的数据库连接中分离出来。如果同一个数据库文件附加了多个别名，那么该命令将只断开给定名称的连接，而附件的其余部分仍将继续存在。内存或临时数据库中的数据库将被完全销毁，内容将丢失。**

***例如***

```
**sqlite> .databases
main: D:sqliteStudentDetails.db;
Department: D:sqliteDepartmentDetails.db
Student: D:sqliteStudentDetails.db
DeptInformation: D:sqliteDepartmentDetails.db

sqlite> DETACH DATABASE 'Department';

sqlite> .databases
main: D:sqliteStudentDetails.db;
Student: D:sqliteStudentDetails.db
DeptInformation: D:sqliteDepartmentDetails.db** 
```

****表格命令****

**在这里，我们将学习在使用 SQLite 时如何处理表格。**

***   **SQL 创建表****

**在 SQLite 中，CREATE TABLE 语句用于创建新表。创建表时，需要命名表并定义它的列和每列的数据类型。**

***语法:***

```
**CREATE TABLE table_name(
         Column1 column_type [constraints]
         Column2 column_type [constraints]
         [.....]
          );**
```

***例如***

```
 **CREATE TABLE StudentInfo(
ID INT PRIMARY KEY NOT NULL,
NAME TEXT NOT NULL,
AGE INT NOT NULL,
ADDRESS CHAR(50),
DEPARTMENTID INTEGER NOT NULL,
PHONE TEXT DEFAULT 'UNKNOWN',
FOREIGN KEY(DEPARTMENTID) REFERENCES DepartmentInfo(DeptID)
);** 
```

**您可以使用 ***来检查表格是否被创建。**表*命令如下所示。注意，我已经创建了一个名为 **DepartmentInfo** 的表，其中 DeptID 是主键。 Departments 表对 Students 表有一个外键约束。**

```
 **sqlite> .tables
StudentInfo Contacts Emp_Master** 
```

***   **SQLite 下拉表****

**在 SQLite 中，DROP TABLE 语句允许您从 SQLite 数据库中移除或删除表。一旦删除了该表，它包含的所有数据都将从数据库中永久删除。任何关联的索引和触发器也将被删除。如果在该表上启用了任何 foreign key 约束，那么它将等效地删除表中的每一行，并且与该表相关联的任何触发器也将被删除。**

***语法***

```
**DROP TABLE [ IF EXISTS ] table_name;**
```

***例如***

```
 **DROP TABLE Department;
Error: no such table: Department

DROP TABLE Company;
sqlite> .tables
StudentInfo**
```

****注意:**如果存在，是可选子句。如果指定，则如果其中一个表不存在，DROP TABLE 语句将不会引发错误。**

**此外，还有一个 **SQLite Alter Table 语句**，我们将在本文接下来的几节中了解它。现在我们已经创建了一个表，让我们看看如何插入、删除和修改数据。**

### ****SQLite 教程:CRUD 操作****

***   **SQLite 插入查询****

**创建表格后，可以用 SQLite Insert Into 命令在指定的表格中创建新行。SQLite insert 语句有两种有意义的形式。第一种形式使用 VALUES 子句指定要插入的值列表。**

***语法***

```
 **INSERT INTO TABLE_NAME [(column1, column2, column3,...columnN)]  
VALUES (value1, value2, value3,...valueN);** 
```

***例如***

```
**INSERT INTO StudentInfo ( ID, NAME, AGE, ADDRESS, DEPARTMENTID, PHONE)
VALUES (1,'Dean', 20, 'California', 2, '934*******');**
```

***输出***

```
**SELECT *from StudentInfo;
ID          NAME        AGE         ADDRESS     DEPARTMENTID  PHONE
----------  ----------  ----------  ----------  ----------  ----------
1           Dean        20          California  2  934*********
```

**这里，创建了一个单独的新行，每个值被记录到各自的列中。请注意，两个列表必须具有相同的项目数。这里，列的**列表是可选的。我们也可以在不指定列列表** 的情况下将数据插入到表 ***中。*****

***例如***

```
**INSERT INTO StudentInfo 
VALUES ( 2, 'SAM', 22, 'Texas', 2, '976*******');**
```

***输出***

```
 **SELECT *from StudentInfo;
ID          NAME        AGE         ADDRESS     DEPARTMENTID  PHONE
----------  ----------  ----------  ----------  ----------  ----------
1           Dean        20          California  2  934*******
2           SAM         22          Texas        2  976********* 
```

**SQLite 还提供了一个特性，可以在一条 insert 语句中 ***插入多行*** 。语法如下所示。**

***例如***

```
**INSERT INTO StudentInfo
VALUES (3,'John',23,'Norway',1,'923*******'),
(4,'Mitch',22,'Houston',3,'934*******');**
```

***输出***

```
 **Select *from StudentInfo;
1|Dean|20|California|2|934*******
2|SAM|22|Texas|2|976*******
3|John|23|Norway|1|923*******
4|Mitch|22|Houston|3|934*********
```

**如您所见，输出的格式与之前的不太相似。那么，如何在 SQLite 中改变输出的格式呢？让我们格式化输出，以便我们的结果更容易阅读。**

***   **格式化****

**你可以用。模式来改变输出模式。上面的例子用的是**。模式**列表，将结果显示为列表。同样，你可以使用**。headers** 语句来指定是否显示列标题。完成更改后，您可以使用**查看设置。显示**命令。**

***例如***

```
 **sqlite>.mode 'column'
sqlite> .headers on
sqlite> .show
echo: off
eqp: off
explain: auto
headers: on
mode: column
nullvalue: ""
output: stdout
colseparator: "|"
rowseparator: "n"
stats: off
width:
filename: StudentDetails.db**
```

***输出***

```
 **SELECT *FROM StudentInfo;

ID NAME AGE ADDRESS DEPARTMENT PHONE
---------- ---------- ---------- ---------- ---------- ----------
1 Dean 20 California 2 934*******
2 SAM 22 Texas 2 976*******
3 John 23 Norway 1 923*******
4 Mitch 22 Houston 3 934*********
```

***   **SQLite 选择查询****

**在 SQLite 中，Select 语句用于从表中获取数据，该表以结果表的形式返回数据。这些结果表也被称为结果**集合。**使用 SQLite select 语句，我们可以根据需要执行简单的计算或多个表达式。我们之前在插入数据时已经使用了 SELECT 语句。**

***语法***

```
**SELECT [ALL | DISTINCT] result [FROM table-list]
[WHERE expr]**
```

***   **DISTINCT**–当我们在 select 语句中使用 DISTINCT 关键字时，它只返回不同的数据行。*   **ALL**–如果我们在 select 语句中使用 ALL 关键字，它将返回所有数据行，即使是重复的。*   **FROM table-list**–这是您想要从中获取数据的表的列表。*   **WHERE 表达式**–WHERE 表达式用于定义我们的自定义条件，以从表中获取所需的数据。**

***例 1***

```
 **SELECT ID, NAME FROM StudentInfo WHERE AGE < 21;**
```

***输出***

```
**ID NAME
---------- ----------
1 Dean**
```

***例 2***

```
**Select NAME FROM StudentInfo WHERE DEPARTMENTID
= (SELECT DeptID FROM DepartmentInfo WHERE DeptName = 'Psychology');**
```

***<u>输出</u>***

```
**//fetches people from department whose id is 2

NAME
----------
Dean
SAM**
```

***   **SQLite 更新查询****

**在 SQLite 中，UPDATE 语句可以用来修改表中的现有记录。可以使用 SQLite 的 WHERE 子句来准确指定应该更新哪些行。根据 WHERE 子句应用的筛选条件，您可以轻松地更新所有行、某些行或不更新任何行。**

***语法***

```
**UPDATE table_name  
SET column1 = value1, column2 = value2...., columnN = valueN  
WHERE [condition];**
```

***例如***

```
**UPDATE StudentInfo SET DEPARTMENTID = 4 WHERE ID = '2';**
```

***输出***

```
 **SELECT *FROM StudentInfo;
ID          NAME        AGE         ADDRESS     DEPARTMENTID  PHONE
----------  ----------  ----------  ----------  ------------  ----------
1           Dean        20          California  2             934*******
2           SAM         22          Texas       4             976*******
3           John        23          Norway      1             923*******
4           Mitch       22          Houston     3             934*********
```

***   **SQLite 删除查询****

**在 SQLite 中，DELETE 语句可用于从表中删除记录。根据 WHERE 子句应用的筛选条件，可以很容易地删除所有行、一些行或一行都不删除。**

***<u>例如</u>***

```
 **DELETE FROM DepartmentInfo WHERE DeptName = 'Science';**
```

***输出***

```
 **SELECT *FROM DepartmentInfo;
DeptID DeptName
---------- -----------
1 Mathematics
2 Psychology
3 Sports
4 Music**
```

**如果试图删除被外键引用的记录，将会出现错误。在删除主键记录之前，您需要先删除外键记录。让我们试着删除部门科学。**

***例如***

```
**DELETE FROM DepartmentInfo WHERE DeptName = 'Music';
Error: FOREIGN KEY constraint failed**
```

**因此，我们需要在删除主键之前删除外键记录。**

```
**DELETE FROM StudentInfo WHERE DEPARTMENTID = 4;

sqlite> DELETE FROM DepartmentInfo WHERE DeptName = 'Music';

sqlite> SELECT *FROM DepartmentInfo;
DeptID      DeptName
----------  -----------
1           Mathematics
2           Psychology
3           Sports

 SELECT *FROM StudentInfo;
ID          NAME        AGE         ADDRESS     DEPARTMENTID  PHONE
----------  ----------  ----------  ----------  ------------  ----------
1           Dean        20          California  2             934*******
3           John        23          Norway      1             923*******
4           Mitch       22          Houston     3             934*********
```

**现在你知道如何编辑 SQLite 数据库表中的记录。在这篇 SQLite 教程博客中，让我们进一步讨论您在 SQLite 中最常遇到的不同子句和条件。**

### ****SQLite 条款/条件****

**在开始使用子句之前，这里是 SQLite 中 SELECT 语句的完整语法。**

***语法***

```
**SELECT [ALL | DISTINCT] result [FROM table-list]
[WHERE expr]
[GROUP BY expr-list]
[HAVING expr]
[compound-op select]*
[ORDER BY sort-expr-list]
[LIMIT integer [(OFFSET|,) integer]]**
```

**注意:我已经更新了 StudentInfo 和 DepartmentInfo 表，如下所示。**

```
**//Student 
Table ID          NAME        AGE         ADDRESS     DEPARTMENTID  PHONE
----------  ----------  ----------  ----------  ------------  ----------
1           Dean        20          California  2             934*******
3           John        23          Norway      1             923*******
4           Mitch       22          Houston     3             934*******
2           SAM         22          Texas       4             976*******
5           Johny       23          Norway      2             945*******
6           Robin       23          Norway      2             UNKNOWN

//Department Details
DeptID      DeptName
----------  -----------
1           Mathematics
2           Psychology
3           Sports
4           Music
5           Science** 
```

***   **SQLite 其中****

**在 SQLite 中，WHERE 子句用于通过定义一个或多个条件来从数据库的表中获取所需的数据，从而对 SELECT 语句施加限制。如果指定的条件满足或为真，则从表中返回特定值。如前所述，WHERE 子句不仅用于 SELECT 语句，还用于 UPDATE、DELETE 语句等。**

***例如***

```
**SELECT NAME FROM StudentInfo WHERE AGE = 23;NAME
----------
John
Johny
Robin**
```

**在 SQLite 中，有许多关系运算符可以与 WHERE 子句一起使用。**

***   **SQLite 分组依据****

**在 SQLite 中，GROUP BY 子句用于将数据聚合到单行中，其中一个或多个指定列的值是重复的。此子句在 SELECT 语句中与 WHERE 子句一起使用，位于 ORDER BY 子句之前。**

***语法***

```
**SELECT result
FROM [table-list]
GROUP BY [expr-list]**
```

```
**SELECT NAME, ADDRESS FROM StudentInfo GROUP BY NAME;

NAME ADDRESS
---------- ----------
Dean California
John Norway
Johny Norway
Mitch Houston
Robin Norway
SAM Texas**
```

**注意，分组过程有两个步骤。首先，GROUP BY 表达式用于将表行排列到不同的组中。一旦定义了组，SELECT 语句就定义了如何将这些组展开成一行。**

***   **SQLite 排序依据****

**通常，SQLite 表以未指定的顺序存储数据，当使用 SQLite select 语句提取数据时，它将以相同的未指定顺序返回记录。在这种情况下，可以使用 ORDER BY 子句按升序或降序对列记录进行排序。在下面的例子中，我根据地址对数据进行了分组和降序排列。**

***语法***

```
**SELECT expressions
FROM tables-list
[WHERE conditions]
ORDER BY column1, column2,... [ ASC | DESC ];**
```

***例如***

```
**SELECT ADDRESS, COUNT(ADDRESS) FROM StudentInfo GROUP BY ADDRESS ORDER BY ADDRESS DESC;
ADDRESS COUNT(ADDRESS)
---------- --------------
Texas 1
Norway 3
Houston 1
California 1**
```

***   **SQLite 由**拥有**

**在 SQLite 中，  **HAVING** 子句与  **WHERE** 子句相同。HAVING 子句是在 select 语句中与 group by 一起发生聚合后应用的进一步条件。通常在 SQLite 中，  **其中** 子句用于将条件应用于表中的单个元素，而具有 子句的 **用于根据 Group By 子句创建的组添加过滤条件。****

***例如***

```
**SELECT ADDRESS, COUNT(ADDRESS) FROM StudentInfo 
GROUP BY ADDRESS 
HAVING COUNT(*)>1;

ADDRESS     COUNT(ADDRESS)
----------  --------------
Norway      3**
```

***   **SQLite 限制条款****

**在 SQLite 中，LIMIT 子句用于对 select 语句返回的记录设置限制。让我们考虑一个例子来理解这个概念。**

***语法***

```
**SELECT expressions
FROM tables-list
[WHERE conditions]
LIMIT number_rows OFFSET offset_value;**
```

***例如***

```
**SELECT NAME, ADDRESS FROM StudentInfo LIMIT 4 OFFSET 2;
NAME        ADDRESS
----------  ----------
Mitch       Houston
SAM         Texas
Johny       Norway
Robin       Norway** 
```

**OFFSET 是可选的，它根据 **offset_value** 定义在结果集的开头跳过多少行。**

***   **SQLite 和&或****

**在 SQLite 中，AND 和& OR 运算符用于根据我们的需求对 select、insert、update 和 delete 语句执行多个条件。SQLite AND 运算符将返回满足使用 AND 运算符定义的条件的行或记录。**

***例 1***

```
**SELECT NAME FROM StudentInfo WHERE AGE = 22 AND ADDRESS = 'Texas';
NAME
----------
SAM**
```

**OR 条件用于在 SQLite 语句中定义多个条件，如果满足其中任何一个条件，它将从语句中返回行或记录。**

***例 2***

```
**SELECT NAME FROM StudentInfo WHERE (AGE = 22 AND ADDRESS = 'Norway') OR ADDRESS = 'Norway';
NAME
----------
John
Johny
Robin**
```

***   **SQLite 全局运算符****

**在 SQLite 中，GLOB 操作符用于检查给定的字符串值是否匹配特定的模式。如果字符串值与模式值匹配，那么它将返回  **true** ，这类似于 LIKE 运算符。另外，GLOB 是区分大小写的。**

***语法***

```
**SELECT * FROM table_name
WHERE column_name GLOB 'search-expression'**
```

***例如***

```
**SELECT *FROM StudentInfo WHERE NAME GLOB 'Joh*';
ID NAME AGE ADDRESS DEPARTMENTID PHONE
---------- ---------- ---------- ---------- ------------ ----------
3 John 23 Norway 1 923*******
5 Johny 23 Norway 2 945*********
```

***   **SQLite Distinct****

**在 SQLite 中，DISTINCT 关键字将扫描 SELECT 语句的结果集，并消除任何重复的行。同样，空值被认为是重复的，所以如果我们对包含空值的列使用 DISTINCT 子句，那么它将只保留一行空值。当您对多个列应用 DISTINCT 时，该语句将返回**列 1** 和**列 2 的每个唯一组合。****

***例如***

```
**SELECT DISTINCT AGE FROM StudentInfo;
AGE
----------
20
23
22**
```

***   **SQLite IN 运算符****

**在 SQLite 中，In 运算符用于确定给定值是否与给定值列表或子查询返回的结果相匹配。**

***例如***

```
**SELECT NAME FROM StudentInfo WHERE ADDRESS IN ('Texas', 'Houston');
NAME
----------
Mitch
SAM**
```

***   **SQLite UNION & UNION ALL****

**在 SQLite 中，UNION 运算符用于组合 **2** 或更多 SELECT 语句的结果集，并删除不同 SELECT 语句之间的重复行。请记住，我们与 UNION 操作符一起使用的 SELECT 语句在结果集中必须具有相同数量的字段，并且具有相似的数据类型。**

***语法***

```
**SELECT expression1, expression2,... expression_n
FROM tables
[WHERE conditions]

UNION / UNION ALL

SELECT expression1, expression2,... expression_n
FROM tables
[WHERE conditions];**
```

***例如***

```
 **SELECT DEPARTMENTID FROM StudentInfo 
UNION
SELECT DeptId FROM DepartmentInfo ORDER BY DEPARTMENTID ASC;

DEPARTMENTID
------------
1
2
3
4
5** 
```

**UNION ALL 运算符用于组合 2 个或更多 SELECT 语句的结果集，它将返回包括重复项在内的所有行。**

***例如***

```
**SELECT DEPARTMENTID FROM StudentInfo UNION ALL SELECT DeptId FROM DepartmentInfo ORDER BY DEPARTMENTID ASC;
DEPARTMENTID
------------
1
1
2
2
2
2
3
3
4
4
5**
```

**至此，我们已经介绍了在使用 SQLite 时可能会用到的最基本的命令。继续这个 SQLite 教程，让我们看看 SQLite 中的 join 语句。**

### ****加入 SQLite****

**在 SQLite 中，连接用于组合数据库中两个或更多表的记录，并根据我们的要求获得记录。dSQLite 中可用的不同类型的连接有:**

***   **内连接**–内连接用于根据 SQLite 语句中定义的条件，从多个表中组合并只返回匹配的记录。*   **外连接**–SQLite 外连接将从多个表中选择与**内连接**相同的匹配行以及关系之外的一些其他行。简单来说，我们可以说 SQLite 外连接是内连接**的增加。**通常，我们在 SQL 标准中有三种类型的外连接，即左外连接、右外连接和全外连接，但是 SQLite 只支持左外连接。*   **交叉连接**–它用于通过将第一个表的每一行与第二个表的每一行进行匹配来获得行的笛卡尔积。*   **Self Join**–It用于与自身连接同一个表。要使用自连接，我们需要为同一个表创建不同的别名，以便根据我们的要求执行操作。**

**这个概念类似于 SQL 等其他关系数据库系统。所以，要了解更多，你可以参考这篇关于 [SQL 连接](https://www.edureka.co/blog/sql-joins-types)的文章。**

**至此，我们已经介绍了基本的 SQLite 命令。这里不涉及高级概念。因此，请继续关注关于高级 SQLite 概念的另一篇文章。尽管 SQLite 提供了所有好的特性，但是它也有一些缺点。**

## ****SQLite 教程:SQLite 的缺点****

**下面列出了使用 SQLite 的缺点:**

***   它在客户机/服务器体系结构中不能很好地工作。*   在大多数情况下，SQLite 数据库的大小限制为 2GB。*   SQLite 没有实现右外连接和全外连接。使用 SQLite，我们只能实现左外连接。*   SQLite 中的视图是只读的。我们不能将 DML 语句(Insert、Update 和 Delete)用于视图。*   我们不能在 SQLite 中使用 GRANT 和 REVOKE 语句。**

**到此，本 SQLite 教程告一段落。**

***如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。***

**有问题要问我们吗？请在本 SQLite 教程的评论部分提到它，我会回复您。**