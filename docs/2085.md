# SQL 中的游标是什么，如何实现？

> 原文：<https://www.edureka.co/blog/cursor-in-sql/>

SQL 中的游标是任何数据库不可或缺的一部分，它基本上可以帮助用户轻松地遍历数据库。通过这篇关于 SQL 中的游标的文章，我将为您提供所有必要的细节，在您接触它之前，您必须需要这些细节。

以下是我将在本文中讨论的主题:

*   [SQL 中的游标是什么？](#sqlcursor)
*   [SQL 游标的类型](#cursortypes)
*   [SQL 游标的语法](#syntax)
*   [光标生命周期](#lifecycle)

## **SQL 中的游标是什么？**

SQL 中的游标是一个允许遍历任何结果集的行的对象。这样，您就可以处理查询返回的数据库中的单个行。这是一个 临时工作区或上下文区，是在执行 SQL 语句期间在内存系统中创建的，用于存储从数据库中检索到的数据，并协助其操作。 你可以把它看作是行的排列以及指向当前行的指针。游标是一个[数据库](https://www.edureka.co/blog/what-is-a-database/)对象，它可以保存多行，但在某个时间点它只能处理一行。由游标保持的行集合被称为  *活动* 集合。因此，你可以用单例技术控制一个表的记录，即在任一时间点控制一行。

既然您已经熟悉了什么是 SQL 中的游标，现在让我们继续看一下它的各种类型。

## **SQL 游标的类型**

SQL 提供了两种类型的游标，我在下面列出了它们:

1.  ### **Implicit cursor**

每当在数据库中处理插入、[更新](https://www.edureka.co/blog/sql-update/)和删除等 [DML](https://www.edureka.co/blog/what-is-sql/) 操作时，隐式游标会自动生成并由框架使用。这些类型的游标用于内部处理，不能从另一个代码区域控制或引用。SQL 中的隐式游标只保存受操作影响的行，并且只能使用下表中显示的游标属性来引用最近的游标。

| **属性** | **描述** |
| 找到了% | 如果 INSERT、UPDATE 或 DELETE 语句影响一行或多行，或者 SELECT INTO 语句返回一行或多行，它将返回 TRUE。在其他情况下，它将返回 FALSE。 |
| %未找到 | 从技术上讲，它与%FOUND 属性相反。如果 INSERT、UPDATE 或 DELETE 语句不影响任何行，或者 SELECT INTO 语句不返回任何行，则返回 TRUE。否则它只返回 FALSE。 |
| 等化器百分比 | 对于隐式游标，该属性将始终返回 FALSE，因为 SQL 游标会在相关 SQL 语句执行后立即自动关闭。 |
| %ROWCOUNT | 它返回 INSERT、UPDATE 或 DELETE 语句所影响的总行数，或者 SELECT INTO 语句所返回的行数。 |

2.  ### **Explicit cursor**

每当用户通过 SQL 块处理数据时，就会生成这种类型的游标。通常，使用 SELECT 查询会触发显式游标的创建，并且可以保存多行，但一次只能处理一行。这种类型的游标用于保存列中的记录。这允许程序员为执行 DML 操作的创建一个命名的上下文区域，以便更好地控制。此外，它需要在 SQL 块中定义，然后使用该代码为一个[选择查询](https://www.edureka.co/blog/sql-select)创建。

为了更好地理解游标，现在让我们看看 SQL 中游标的语法是什么。

## **SQL 游标的语法**

下面是创建显式光标的一般语法。

```
CURSOR cursorName IS selectStatement;
```

这里:

cursor name–这代表光标的有效名称

select statement–这表示将返回多行的选择查询

现在让我们继续这篇文章，看看 SQL 游标的生命周期。

## **光标生命周期**

在 SQL 中，游标的生命周期基本上有 5 个阶段，我在下面列出了它们:

1.  **宣告**

```
DECLARE cursorName CURSOR
FOR selectStatement;
```

这一步将帮助您指定光标的名称和数据类型，SELECT 语句将定义其结果集。

2.  **打开**

```
OPEN cursorName;
```

这一步将让您通过执行打开并填充光标。

3.  **获取**

```
FETCH NEXT FROM cursor INTO variableList;
```

这一步将从游标中检索一行，并将其存储到一个或多个变量中。

【T0【可选】检查状态

```
WHILE @@FETCH_STATUS = 0
BEGIN
FETCH NEXT FROM cursorName;
END;
```

该函数返回对游标执行的最后一条 FETCH 语句的状态。如果此函数返回 0，则意味着获取操作成功。为了从游标中获取所有行，使用了 [WHILE 子句](https://www.edureka.co/blog/sql-constraints/)。

4.  **关闭**

```
CLOSE cursorName;
```

该步骤将帮助您在操作完成后关闭光标。

5.  **解除分配**

```
DEALLOCATE cursor_name;
```

这一步将有助于释放游标并释放内存空间。

至此，我想结束这篇关于 SQL 中的游标的文章。我希望这篇文章能帮助你增加知识的价值。更多关于 SQL 或者数据库的信息，可以参考我们这里的综合阅读清单:  [**数据库 Edureka**](https://www.edureka.co/blog/category/databases/) 。

## **初学 SQL 基础|学习 SQL |初学 SQL 教程| Edureka**



[https://www.youtube.com/embed/zbMHLJ0dY4w?rel=0&controls=0&showinfo=0](https://www.youtube.com/embed/zbMHLJ0dY4w?rel=0&controls=0&showinfo=0)*This Edureka video on ‘SQL Basics for Beginners’ will help you understand the basics of SQL and also SQL queries which are very popular and essential.*

*如果您希望获得有关 MySQL 的结构化培训，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在 SQL 中的**游标的评论部分提到它，我会回复你。**