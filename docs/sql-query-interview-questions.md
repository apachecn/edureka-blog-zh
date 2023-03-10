# 2023 年必练的 30 大 SQL 查询面试题

> 原文：<https://www.edureka.co/blog/interview-questions/sql-query-interview-questions>

SQL 或[结构化查询语言](https://www.edureka.co/blog/sql-tutorial/)是处理关系数据库的标准语言。面对海量的数据，理解如何使用查询来检索所需的数据对我们来说非常重要。在这篇关于 SQL 查询面试问题的文章中，我将讨论几个成为数据库管理员必须练习的查询，也将帮助你赢得面试。

**热门 SQL 查询面试问题**

![SQL Logo - SQL Query Interview Questions - Edureka](img/0cc226c3ea862bb392cebea8ab602d5c.png)

为了让您更好地理解，我将考虑使用下面的表来编写查询。

### **员工信息表:**

| **EmpID** | **EmpFname** | **雇员名** | **部门** | **项目** | **地址** | **出生日期** | **性别** |
| one | 桑杰（男子名） | 梅赫拉 | 人力资源（部） | 第一亲代 | Hyderabad(HYD) | 01/12/1976 | M |
| Two | 安纳亚 | 米什拉 | 管理 | P2 | 德里 | 02/05/1968 | F |
| three | 罗汉 | 地万 | 账户 | P3 | 孟买(BOM) | 01/01/1980 | M |
| four | 索尼亚（女子名） | Kulkarni | 人力资源（部） | 第一亲代 | Hyderabad(HYD) | 02/05/1992 | F |
| five | 鸭子！鸭子 | 卡普尔 | 管理 | P2 | 德里 | 03/07/1994 | M |

### **员工职位表:**

| **EmpID** | **空位置** | **加入日期** | **工资** |
| one | 经理 | 01/05/2022 | Five hundred thousand |
| Two | 执行的 | 02/05/2022 | Seventy-five thousand |
| three | 经理 | 01/05/2022 | Ninety thousand |
| Two | 铅 | 02/05/2022 | Eighty-five thousand |
| one | 执行的 | 01/05/2022 | Three hundred thousand |

让我们从一些最常见的 SQL 查询面试问题开始，

*   [编写一个查询，从 EmployeeInfo 表中获取 EmpFname，并使用别名作为 EmpName。](#fetchname)
*   编写一个查询来获取在“HR”部门工作的雇员人数。
*   编写一个查询来获取当前日期。
*   [编写一个查询，从 EmployeeInfo 表中检索 EmpLname 的前四个字符。](#retrievecharacters)
*   [编写一个查询，只从 EmployeeInfo 表的地址列中获取地名(括号前的字符串)。](#fetchaddressname)
*   编写一个查询来创建一个新表，该表包含从另一个表中复制的数据和结构。
*   编写 q 查询来查找所有工资在 50000 到 100000 之间的雇员。
*   [编写一个查询，查找以“S”开头的雇员姓名](#beginwithalphabet)
*   编写一个查询来获取前 N 条记录。
*   [编写一个查询，以“FullName”的形式检索单个列中的 EmpFname 和 EmpLname。名字和姓氏必须用空格隔开。](#retrievecolumns)

### **Q1。编写一个查询以从 EmployeeInfo 表中获取 EmpFname(大写),并将别名用作 EmpName。**

```
SELECT UPPER(EmpFname) AS EmpName FROM EmployeeInfo;

```

### **Q2。编写一个查询来获取在部门“HR”中工作的雇员人数。**

```
SELECT COUNT(*) FROM EmployeeInfo WHERE Department = 'HR';

```

### **Q3。编写一个查询来获取当前日期。**

您可以在 SQL Server 中编写如下查询:

```
SELECT GETDATE();

```

您可以在 [MySQL](https://www.edureka.co/blog/mysql-tutorial/) 中编写如下查询:

```
SELECT SYSTDATE();

```

### **Q4。编写一个查询，从 EmployeeInfo 表中检索 EmpLname 的前四个字符。**

```
SELECT SUBSTRING(EmpLname, 1, 4) FROM EmployeeInfo;

```

### **Q5。编写一个查询，仅从 EmployeeInfo 表的地址列中提取地名(括号前的字符串)。**

使用 MySQL 中的 MID 函数

```
SELECT MID(Address, 0, LOCATE('(',Address)) FROM EmployeeInfo;

```

```
Using SUBSTRING
```

```
SELECT SUBSTRING(Address, 1, CHARINDEX('(',Address)) FROM EmployeeInfo;

```

### **Q6。编写一个查询来创建一个新表，该表包含从另一个表中复制的数据和结构。**

使用 SELECT INTO 命令:

```
SELECT * INTO NewTable FROM EmployeeInfo WHERE 1 = 0;

```

使用 MySQL 中的[创建命令](https://www.edureka.co/blog/create-table-in-sql/):

```
CREATE TABLE NewTable AS SELECT * FROM EmployeeInfo;

```

### **Q7。编写 q 查询，查找工资在 50000 到 100000 之间的所有雇员。**

```
SELECT * FROM EmployeePosition WHERE Salary BETWEEN '50000' AND '100000';

```

### **Q8。编写一个查询来查找以“S”**开头的雇员姓名

```
SELECT * FROM EmployeeInfo WHERE EmpFname LIKE 'S%';

```

### **Q9。** **编写一个查询来获取前 N 条记录。**

通过在 SQL Server 中使用 TOP 命令:

```
SELECT TOP N * FROM EmployeePosition ORDER BY Salary DESC;

```

通过在 MySQL 中使用 LIMIT 命令:

```
SELECT * FROM EmpPosition ORDER BY Salary DESC LIMIT N;

```

### **Q10。编写一个查询，以“FullName”的形式在单个列中检索 EmpFname 和 EmpLname。名字和姓氏必须用空格隔开。**

```
SELECT CONCAT(EmpFname, ' ', EmpLname) AS 'FullName' FROM EmployeeInfo;

```

### **Q11。编写一个查询，查找出生日期在 02/05/1970 到 31/12/1975 之间的雇员人数，并根据性别进行分组**

```
SELECT COUNT(*), Gender FROM EmployeeInfo WHERE DOB BETWEEN '02/05/1970 ' AND '31/12/1975' GROUP BY Gender;

```

### **Q12。编写一个查询，从 EmployeeInfo 表中提取所有记录，这些记录按雇员名称降序排列，按部门升序排列。**

要按升序和降序对记录进行排序，您必须使用 SQL 中的 [ORDER BY 语句。](https://www.edureka.co/blog/order-by-in-sql)

```
SELECT * FROM EmployeeInfo ORDER BY EmpFname desc, Department asc;

```

### **Q13。编写一个查询来获取 EmpLname 以字母“A”结尾并包含五个字母的雇员的详细信息。**

要获取与某个值匹配的细节，您必须在 SQL 中使用 [LIKE 操作符。](https://www.edureka.co/blog/like-in-sql/)

```

SELECT * FROM EmployeeInfo WHERE EmpLname LIKE '____a';

```

### **Q14。编写一个查询，从 EmployeeInfo 表中获取所有雇员的详细信息，不包括名为“Sanjay”和“Sonia”的雇员。**

```

SELECT * FROM EmployeeInfo WHERE EmpFname NOT IN ('Sanjay','Sonia');

```

Want to upskill yourself to get ahead in your career? Check out this video

## **2022 年要学的十大技术| Edureka**



[https://www.youtube.com/embed/M2NyXKxyUGc](https://www.youtube.com/embed/M2NyXKxyUGc)

### **Q15。编写一个查询来获取地址为“DELHI(DEL)”的雇员的详细信息。**

```

SELECT * FROM EmployeeInfo WHERE Address LIKE 'DELHI(DEL)%';

```

### **Q16。编写一个查询来获取所有担任管理职位的雇员。**

```

SELECT E.EmpFname, E.EmpLname, P.EmpPosition 
FROM EmployeeInfo E INNER JOIN EmployeePosition P ON 
E.EmpID = P.EmpID AND P.EmpPosition IN ('Manager');

```

### **Q17。** **编写一个查询来获取部门****-按部门计数升序排序的雇员计数。**

```

SELECT Department, count(EmpID) AS EmpDeptCount 
FROM EmployeeInfo GROUP BY Department 
ORDER BY EmpDeptCount ASC;

```

### **Q18。编写一个查询来计算表中的偶数和奇数记录。**

要从表中检索偶数记录，必须使用 MOD()函数，如下所示:

```

SELECT EmpID FROM (SELECT rowno, EmpID from EmployeeInfo) WHERE MOD(rowno,2)=0;

```

类似地，要从表中检索奇数记录，可以编写如下查询:

```

SELECT EmpID FROM (SELECT rowno, EmpID from EmployeeInfo) WHERE MOD(rowno,2)=1;

```

### **Q19。** **编写一个 SQL 查询，从 EmployeeInfo 表中检索在 EmployeePosition 表中有加入日期的雇员的详细信息。**

```

SELECT * FROM EmployeeInfo E 
WHERE EXISTS 
(SELECT * FROM EmployeePosition P WHERE E.EmpId = P.EmpId);

```

### **Q20。编写一个查询，从 EmployeePosition 表中检索两个最低和最高工资。**

要检索两个最低工资，您可以编写如下查询:

```

SELECT DISTINCT Salary FROM EmployeePosition E1 
 WHERE 2 >= (SELECTCOUNT(DISTINCT Salary)FROM EmployeePosition E2 
  WHERE E1.Salary >= E2.Salary) ORDER BY E1.Salary DESC;

```

```
To retrieve two maximum salaries, you can write a query as below: 
```

```

SELECT DISTINCT Salary FROM EmployeePosition E1 
 WHERE 2 >= (SELECTCOUNT(DISTINCT Salary) FROM EmployeePosition E2 
  WHERE E1.Salary <= E2.Salary) ORDER BY E1.Salary DESC;

```

### **Q21。** **编写一个查询，在不使用 TOP/limit 关键字的情况下从表中查找第 n 个最高工资。**

```

SELECT Salary 
FROM EmployeePosition E1 
WHERE N-1 = ( 
      SELECT COUNT( DISTINCT ( E2.Salary ) ) 
	  FROM EmployeePosition E2 
	  WHERE E2.Salary >  E1.Salary );

```

### **Q22。编写查询从表中检索重复记录。**

```

SELECT EmpID, EmpFname, Department COUNT(*) 
FROM EmployeeInfo GROUP BY EmpID, EmpFname, Department 
HAVING COUNT(*) > 1;

```

### **Q23。编写一个查询来检索在同一部门工作的雇员列表。**

```

Select DISTINCT E.EmpID, E.EmpFname, E.Department 
FROM EmployeeInfo E, Employee E1 
WHERE E.Department = E1.Department AND E.EmpID != E1.EmpID;

```

### **Q24。编写一个查询，从 EmployeeInfo 表中检索最后 3 条记录。**

```
SELECT * FROM EmployeeInfo WHERE 
EmpID <=3 UNION SELECT * FROM 
(SELECT * FROM EmployeeInfo E ORDER BY E.EmpID DESC) 
AS E1 WHERE E1.EmpID <=3;

```

### **Q25。编写一个查询，从 EmpPosition 表中查找第三高的薪金。**

```
SELECT TOP 1 salary
FROM(
SELECT TOP 3 salary
FROM employee_table
ORDER BY salary DESC) AS emp
ORDER BY salary ASC;

```

### **Q26。编写一个查询来显示 EmployeeInfo 表中的第一条和最后一条记录。**

若要显示 EmployeeInfo 表中的第一条记录，可以编写如下查询:

```
SELECT * FROM EmployeeInfo WHERE EmpID = (SELECT MIN(EmpID) FROM EmployeeInfo);

```

若要显示 EmployeeInfo 表中的最后一条记录，可以编写如下查询:

```
SELECT * FROM EmployeeInfo WHERE EmpID = (SELECT MAX(EmpID) FROM EmployeeInfo);

```

### **Q27。编写一个查询，将电子邮件验证添加到您的数据库**

```
SELECT Email FROM EmployeeInfo WHERE NOT REGEXP_LIKE(Email, ‘[A-Z0-9._%+-]+@[A-Z0-9.-]+.[A-Z]{2,4}’, ‘i’);

```

### **Q28。编写一个查询来检索雇员少于 2 人的部门。**

```
SELECT DEPARTMENT, COUNT(EmpID) as 'EmpNo' FROM EmployeeInfo GROUP BY DEPARTMENT HAVING COUNT(EmpD) < 2;

```

### **Q29。编写一个查询来检索 EmpPostion 以及为每个职位支付的总工资。**

```
SELECT EmpPosition, SUM(Salary) from EmployeePosition GROUP BY EmpPosition;

```

### **Q30。编写一个查询，从 EmployeeInfo 表中提取 50%的记录。**

```
SELECT * 
FROM EmployeeInfo WHERE 
EmpID <= (SELECT COUNT(EmpID)/2 from EmployeeInfo);

```

这就把我们带到了 SQL 查询面试问题文章的结尾。我希望这一套 SQL 查询面试问题能帮助你在求职面试中胜出。**祝你面试顺利！**

*查看 Edureka 提供的 [MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)，edu reka 是一家值得信赖的在线学习公司，其网络* o *f 超过 250，000 名满意的学习者遍布全球。* *本课程培训您掌握管理数据和 MySQL 数据库的核心概念&高级工具和技术。它包括对 MySQL 工作台、MySQL 服务器、数据建模、MySQL 连接器、数据库设计、MySQL 命令行、MySQL 函数等概念的实践学习。培训结束后，您将能够创建和管理自己的 MySQL 数据库并管理数据。*

*有问题吗？请在这篇“SQL 查询*面试问题*”文章的评论部分提到它，我们会尽快回复您。*