# 如何用 SQL 创建存储过程？

> 原文：<https://www.edureka.co/blog/procedures-in-sql/>

程序是子程序，可以作为数据库对象创建并保存在[数据库](https://www.edureka.co/blog/what-is-a-database/)中。就像在其他语言中一样，您也可以在 [SQL](https://www.edureka.co/blog/what-is-mysql/) 中创建和删除过程。在本文中，让我们通过语法和示例来探索 SQL 中的过程。

本文讨论的主题是:

*   [SQL 中的过程是什么？](#procedure)
*   [SQL 过程语法](#syntax)
*   [SQL 中的示例过程](#example)
*   [SQL 程序的优点](#advantages)

## **SQL 中的过程是什么？**

[SQL](https://www.edureka.co/blog/sql-commands) 中的一个过程(通常称为存储过程)，是一个可重用的单元，封装了应用程序的特定业务逻辑。SQL 过程是一组 SQL 语句和逻辑，它们被编译和存储在一起以执行特定的任务。

![SQL Procedure - Procedures in SQL - Edureka](img/2a22cc955168acd51479fa8fa8605cc1.png)

下面列出的是 SQL 过程的主要特性:

*   易于实现，因为它们使用非常简单的高级强类型语言
*   支持三种类型的参数，即输入、输出和输入输出参数。
*   比同等的外部程序更可靠。
*   SQL 过程提高了可重用性和可维护性。
*   支持一个简单但强大的条件和错误处理模型。
*   向调用过程或批处理返回一个状态值，以指示成功或失败以及失败的原因。

现在你知道了什么是过程以及为什么需要它们，让我们来讨论 SQL 中过程的语法和例子。

## **SQL 中过程的语法**

下面说明了在 SQL 中创建过程的基本语法:

```

CREATE [ OR REPLACE] PROCEDURE procedure_name [
(parameter_name [IN | OUT | IN OUT]  type [ ])]
{IS | AS }
BEGIN [declaration_section]
executable_section 
//SQL statement used in the stored procedure
END
GO

```

### **语法术语**

**参数**

参数是一个变量，包含任何有效 SQL 数据类型的值，子程序可以通过它与主代码交换值。换句话说，p 参数用于向过程传递值。有 3 种不同类型的参数，如下所示:

*   中的**:T这是缺省参数，它总是接收来自调用程序的值。它是子程序中的只读变量，其值不能在子程序中更改。**
*   **OUT:** 是，用于获取子程序的输出。
*   **IN OUT:** 这个参数用于给定输入和从子程序获取输出。

**其他术语**

*   *程序名称* 指定程序的名称。应该是独一无二的。
*   【或替换】选项允许修改现有程序。
*   IS | AS 子句，它们设置上下文来执行存储过程。不同之处在于，当程序嵌套在其他程序块中时，使用关键字“is ”,如果程序是独立的，则使用“AS”。
*   Code_Block 声明了处理存储过程中所有处理的过程语句。code_block 的内容取决于[数据库](https://www.edureka.co/blog/sql-basics/)使用的规则和过程语言。

**SQL 中的过程:示例**

### **例 1**

下面的示例创建了一个简单的过程，该过程在执行时会在屏幕上显示欢迎消息。然后，程序将是:

```
CREATE OR REPLACE PROCEDURE welcome_msg
(para1_name IN VARCHAR2)
IS 
BEGIN 
    dbms_output.put_line (‘Hello World! '|| para1_name);
END; 
/
```

执行存储过程。可以通过两种方式调用独立过程

*   使用  **执行** 关键字
*   从 SQL 块调用过程的名称

可以使用 Execute 关键字调用上述过程，如下所示:

```
 EXEC welcome_msg (‘Welcome to Edureka!’);
```

**输出**

```
Hello World! Welcome to Edureka 
```

过程被执行，消息被打印为“Hello World！欢迎来到 Edureka”。

### **例 2**

让我们假设您有一个包含员工详细信息的表，比如，EmployeId、Firstname、Lastname 和 DepartmentDetails。

这个示例创建了一个 SQL 过程，当 EmployeId 作为存储过程的输入参数给定时，该过程将返回雇员姓名。然后，程序将是:

```
Create  PROCEDURE GetStudentName 
(
@employeeID INT,                       --Input parameter ,  employeID of the employee
@employeName VARCHAR(50)  OUT  --Output parameter, employeeName of employee
AS
BEGIN
SELECT @employeName= Firstname+' '+Lastname FROM Employee_Table WHERE EmployeId=@employeID
END
```

要执行的步骤:

*   将@ employeName 声明为 nvarchar(50)
*   EXEC GetStudentName 01，@ employeName 输出
*   选择@员工名

上面给出雇员 id 作为输入的过程返回特定雇员的名字。假设我们有一个输出参数 t ，那么我们首先需要声明变量来收集输出值。现在让我们来看看 SQL 中过程的优点。

## **SQL 中过程的优势**

SQL 中存储过程的主要目的是隐藏代码中的直接 [SQL 查询](https://www.edureka.co/blog/sql-basics/#basic)，提高数据库操作的性能，如选择、更新和删除数据。SQL 中过程的其他优点有:

*   减少发送到数据库服务器的信息量。当网络带宽较少时，这可能成为更重要的好处。
*   启用代码的可重用性
*   增强了安全性，因为您可以授予用户执行存储过程的权限，而不是授予存储过程中使用的表的权限。
*   支持对其他 SQL 过程或用其他语言实现的过程的嵌套过程调用。

总之，SQL(存储过程)中的过程不仅提高了代码重用的可能性，还提高了数据库的性能。怎么会？通过减少网络上发送的信息量来减少网络流量。就这样，我们来到了这篇文章的结尾。

*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这个开源的关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本“SQL 中的过程”的注释部分提及它；文章，我们会回来找你。