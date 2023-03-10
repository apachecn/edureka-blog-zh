# 了解如何处理 PL/SQL 中的异常

> 原文：<https://www.edureka.co/blog/exception-handling-pl-sql/>

如果你是一名程序员，你可能熟悉异常处理是任何编程语言不可或缺的一部分的概念。由于错误是不可避免的，即使是我们中最聪明的人也会在编写代码时犯错误，所以我们必须熟悉如何处理它们。在本文中，我们将特别学习 PL/SQL 中的异常处理。

下面是本文涵盖的主题:

*   什么是例外？
*   [异常处理的语法](#syntax)
*   [异常类型](#types)
    *   [系统定义的](#systemdefined)
        *   [命名系统异常](#Namedsystemexceptions)
        *   [未命名的系统异常](#Unnamedsystemexceptions)
    *   [用户自定义](#userdefined)
        *   [声明用户自定义函数的步骤](#stepstodeclareuserdefinedfunction)
        *   [用户自定义函数示例](#examplesofuserdefinedfunction)

## 什么是例外？

任何在运行时中断我们程序指令正常流程的异常情况或事件，或者简单地说一个异常，都是错误。

## **PL/SQL 中异常处理的语法**

```
DECLARE
<declarations section>
BEGIN
<executable command(s)>
EXCEPTION
<exception handling goes here >
WHEN exception1 THEN
exception1-handling-statements
WHEN exception2&nbsp; THEN
exception2-handling-statements
WHEN exception3 THEN
exception3-handling-statements
........

WHEN others THEN
exception3-handling-statements
END;

```

在这里，我们可以列出尽可能多的我们想要处理的异常。默认异常将使用“WHEN others THEN”来处理

### **PL/SQL 中的异常处理示例**

下面的程序显示给定 ID 的学生的姓名和地址。因为在我们的数据库中没有 ID 值为 8 的学生，所以程序引发运行时异常 NO_DATA_FOUND，该异常是在异常块中捕获的。

```
DECLARE 
   s_id studentS.id%type := 8; 
   s_name studentS.Name%type; 
   s_loc studentS.loc%type; 
BEGIN 
   SELECT  name, loation INTO  s_name, s_loc 
   FROM students 
   WHERE id = s_id;  
   DBMS_OUTPUT.PUT_LINE ('Name: '||  s_name); 
   DBMS_OUTPUT.PUT_LINE ('Location: ' || s_loc);
EXCEPTION 
   WHEN no_data_found THEN 
      dbms_output.put_line('No such student!'); 
   WHEN others THEN 
      dbms_output.put_line('Oops, Error!'); 
END; 

```

### **输出**

```
No such student!
PL/SQL procedure successfully completed.  

```

在这里，我们可以列出尽可能多的我们想要处理的异常。默认的异常会在别人接时用**处理**

## **PL/SQL 中的异常类型**

*   系统定义的
*   用户定义的

接下来在这篇关于 [PL/SQL](https://www.postgresql.org/) 中异常处理的文章中，让我们详细讨论这两种类型。

### **系统定义的**

这些异常由 Oracle 服务器隐式定义和维护，主要在 Oracle 标准包中定义。每当程序内部出现异常时，Oracle server 都会从 Oracle 标准包中的可用异常集中匹配并识别适当的异常。基本上，这些异常是在 [PL/SQL](https://www.edureka.co/blog/postgresql-tutorial) 中预定义的，当违反特定的数据库规则时，就会引发*。*

**系统定义的异常**进一步分为两类:

*   命名系统异常
*   未命名的系统异常

#### **命名系统异常**

命名的 PL/SQL 异常是在 PL/SQL 的标准包中命名的*，因此开发人员不需要在他们的代码中定义 PL/SQL 异常。PL/SQL 提供了许多预定义的命名异常，当程序违反任何数据库规则时，就会执行这些异常。下表列出了一些重要的预定义异常*

| **异常** | **甲骨文错误** | **SQLCODE** | **描述** |
| ACCESS_INTO_NULL | 06530 | -6530 | 当一个空对象被自动赋值时引发。 |
| 案例 _ 未找到 | 06592 | -6592 | 当 [CASE 语句](https://www.edureka.co/blog/case-in-sql)的 when 子句中的选项都没有被选中，并且没有 ELSE 子句时，引发此问题。 |
| COLLECTION_IS_NULL | 06531 | -6531 | 当程序试图将 EXISTS 之外的集合方法应用于未初始化的嵌套表或 varray，或者程序试图将值赋给未初始化的嵌套表或 varray 的元素时，会引发此问题。 |
| DUP 谷指数 | 00001 | -1 | 当试图在具有唯一索引的列中存储重复值时，会引发此问题。 |
| 无效 _ 光标 | 01001 | -1001 | 当试图进行不允许的游标操作时，如关闭未打开的游标，会引发此问题。 |
| 无效 _ 编号 | 01722 | -1722 | 当由于字符串不代表有效数字而导致字符串转换为数字失败时，会引发此问题。 |
| 登录 _ 被拒绝 | 01017 | -1017 | 当程序试图用无效的用户名或密码登录数据库时，会引发此问题。 |
| 未发现数据 | 01403 | +100 | 当 SELECT INTO 语句不返回任何行时，会引发此问题。 |
| 未登录 | 01012 | -1012 | 在没有连接到数据库的情况下发出数据库调用时引发。 |
| 程序错误 | 06501 | -6501 | 当 PL/SQL 出现内部问题时，会引发此问题。 |
| 行类型 _ 不匹配 | 06504 | -6504 | 当游标在具有不兼容数据类型的变量中取值时引发。 |
| SELF_IS_NULL | 30625 | -30625 | 当成员方法被调用，但是对象类型的实例没有被初始化时，它被引发。 |
| 存储 _ 错误 | 06500 | -6500 | 当 PL/SQL 用尽内存或内存损坏时，会引发此问题。 |
| 太多行 | 01422 | -1422 | 当 SELECT INTO 语句返回多行时会引发此问题。 |
| 值 _ 误差 | 06502 | -6502 | 当出现算术、转换、截断或大小约束错误时引发。 |
| 零 _ 除 | 01476 | 第 1476 章 | 当试图用零除一个数时会引发此问题。 |

#### **例题**

```
CREATE OR REPLACE PROCEDURE add_new_student
      (student _id_in IN NUMBER, student _name_in IN VARCHAR2)
IS
BEGIN
       INSERT INTO student (student _id, student _name )
       VALUES ( student _id_in, student _name_in );
EXCEPTION
       WHEN DUP_VAL_ON_INDEX THEN
 raise_application_error (-20001,'Duplicate student _id');
       WHEN OTHERS THEN
raise_application_error (-20002,'An error occurred.');
END;

```

在这篇关于 PL/SQL 中异常处理的文章中，让我们理解什么是未命名的系统异常。

#### **未命名的系统异常**

Oracle 没有命名的系统异常称为未命名系统异常。这些异常并不经常发生，并且用代码和相关消息来编写。

**基本上有两种处理未命名系统异常的方法:**

1.使用 WHEN OTHERS 异常处理程序

2.将异常代码与名称相关联，并将其用作命名异常。

**未命名系统异常遵循的一些步骤是:**

*   含蓄的提出来。
*   如果在“WHEN Others”中没有处理它们，那么必须显式处理它们。
*   要显式处理异常，可以使用 Pragma EXCEPTION_INIT 声明它们，并通过引用异常部分中用户定义的异常名称来处理它们。

本文后面提供了一个使用 Pragma EXCEPTION_INIT 处理未命名异常的示例。在这篇关于 PL/SQL 中异常处理的文章中，让我们理解用户定义的异常。

## **用户自定义**

像所有其他编程语言一样，Oracle 也允许您声明和实现自己的异常。与系统定义的异常不同，这些异常在 PL/SQL 块中显式引发。

#### **在 Oracle 数据库中声明用户定义的异常的步骤**

我们可以通过以下三种方式在 Oracle 数据库中定义用户定义的异常:

*   使用异常类型的变量

这里，我们可以通过在代码中声明 EXCEPTION [datatype](https://www.edureka.co/blog/sql-data-types/) 的变量来声明用户定义的异常，并在程序中使用 raise 语句显式地引发它。

*   使用 PRAGMA 异常初始化函数

我们可以用异常数据类型的变量定义一个非预定义的错误号

*   使用引发应用程序错误方法

使用这种方法，我们可以用自定义的错误号和消息来声明用户定义的异常。

到目前为止，您可能已经对在 PL/SQL 中引发用户定义的异常的方法有了大致的了解。在这篇关于 PL/SQL 中异常处理的文章中，我们将通过示例进一步了解上述每种方法。

在本文的下一步，让我们继续演示用户定义的异常处理。

### **用户定义异常的演示**

本文继续讨论 PL/SQL 中的异常处理，让我们了解如何使用异常类型的变量。

#### **使用异常类型的变量**

声明用户定义异常的过程分为三个部分，这三个部分是:

*   声明变量异常数据类型
*   引发异常
*   处理异常

让我们写一个代码来详细演示以上步骤。

```
DECLARE
       var_dividend NUMBER :=10;
       var_divisor  NUMBER :=0
       var_result NUMBER;
       ex-DivZero EXCEPTION

```

在上面的声明块中，我们有四个变量，其中前三个是正常数字数据类型变量，第四个是 ex_DivZero，是特殊异常数据类型变量。第四个是我们的用户定义的异常。

```
DECLARE
       var_dividend NUMBER :=10;
       var_divisor  NUMBER :=0
       var_result NUMBER;
       ex-DivZero EXCEPTION

```

只有当除数为 0 时，这个匿名块的上述执行部分才会起作用。如果除数是零，就像在我们的例子中一样，将会产生错误，程序的控制将会跳过所有接下来的步骤，并寻找匹配的异常处理程序。如果发现任何其他错误，它将相应地执行操作，否则它将终止程序或提示我们一个未处理的系统定义的错误。

```
EXCEPTION WHEN ex_DivZero THEN
DBMS_OUTPUT.PUT_LINE(‘ ERROR, The divisor can’t be zero’);

```

这是异常处理程序。一旦用户输入除数为 0，就会出现上述消息字符串。

**最终代码:**

```
DECLARE
       var_dividend NUMBER :=10;
       var_divisor  NUMBER :=0
       var_result NUMBER;
       ex-DivZero EXCEPTION
BEGIN
IF var_divisor =0 THEN
RAISE ex-DivZero;
END IF;
Var_result := var_dividend/var_divisor;
DBMS_OUTPUT.PUT_LINE (‘Result = ‘ || var_result);
BEGIN
IF var_divisor =0 THEN
RAISE ex-DivZero;
END IF;
Var_result := var_dividend/var_divisor;
DBMS_OUTPUT.PUT_LINE (‘Result = ‘ || var_result);
END;

```

在这篇关于 PL/SQL 异常处理的文章中，让我们了解如何使用 PRAGMA 异常初始化方法。

### **使用 PRAGMA 异常初始化函数**

在 PRAGMA EXCEPTION_INIT 函数中，一个异常名与一个 Oracle 错误号相关联。该名称可用于设计错误的异常处理程序。 对于有很多用户自定义错误的大型项目，PRAGMA EXCEPTION_INIT 是最有用最合适的方法。

#### **语法:**

```
PRAGMA EXCEPTION_INIT(exception_name, -Oracle_error_number);

```

#### **例子**

```
DECLARE
   deadlock_detected EXCEPTION;
   PRAGMA EXCEPTION_INIT(deadlock_detected, -60);
BEGIN
 NULL; -- Some operation that causes an ORA-00060 error
EXCEPTION
   WHEN deadlock_detected THEN
      NULL; -- handle the error
END;

```

PRAGMA EXCEPTION_INIT 告诉编译器将异常名与前面提到的 Oracle 错误号相关联。它允许您通过名称引用任何内部异常，并为其编写特定的处理程序。当您看到一个错误堆栈或错误消息序列时，最上面的一个是可以被捕获和处理的。

本文继续讨论 PL/SQL 中的异常处理，让我们了解如何使用 RAISE_APPLICATION_ERROR 方法。

### **使用 RAISE_APPLICATION_ERROR 方法**

这是 oracle 软件内置的一个程序。使用此过程，我们可以将错误号与自定义错误消息相关联。结合错误号和自定义错误消息，可以组成一个错误字符串，它看起来类似于 oracle 在遇到错误时显示的那些默认错误字符串。在 DBMS_STANDARD 包中找到了 RAISE_APPLICATION_ERROR 过程

#### **语法**

```
raise_application_error (error_number, message [, {TRUE | FALSE}]);

```

#### **例子**

```
/* A trigger trg_emp_detail_chk is created.*/
CREATE OR REPLACE TRIGGER trg_emp_detail_chk

/* The trigger timing is declared as BEFORE UPDATE on the EMPLOYEES table.*/
Before UPDATE ON employees

DECLARE
permission_denied EXCEPTION;
BEGIN

/*Start of the IF condition checking whether the day of the system time is either Saturday or Sunday or not.*/
IF trim(TO_CHAR(sysdate,'Day')) IN ('Saturday', 'Sunday') THEN
raise_application_error(-20000, 'You are not authorized to do any modification in the weekends!!');

/* The procedure raise_application_error is called with the first parameter value as -20000 and the second parameter
with a default text stating that the user is not authorized to do any modification in the weekends. */
END IF;
END;

```

至此，我们结束了这篇关于“PL/SQL 中的异常处理”的文章。希望这个题目理解好了，对你有帮助。尝试编写自己的代码，并结合本文中介绍的方法。

如果你想从专业人士那里获得这方面的培训，你可以选择 edureka 的结构化培训！查看 Edureka 提供的 MySQL DBA 认证培训, edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。本课程训练你掌握管理数据和 MySQL 数据库的核心概念&高级工具和技术。它包括对 MySQL 工作台、MySQL 服务器、数据建模、MySQL 连接器、数据库设计、MySQL 命令行、MySQL 函数等概念的实践学习。培训结束后，您将能够创建和管理自己的 MySQL 数据库并管理数据。

有问题吗？请在这篇“PL/SQL 中的异常处理”文章的评论部分提到它，我们会尽快回复您。