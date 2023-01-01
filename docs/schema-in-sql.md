# 什么是 SQL 中的模式，如何创建它？

> 原文：<https://www.edureka.co/blog/schema-in-sql/>

听说过模式这个术语吗？嗯， [SQL](https://www.edureka.co/blog/sql-basics/) 中的模式是与特定的[数据库](https://www.edureka.co/blog/what-is-a-database/)用户名相链接的数据库对象的集合。我所说的用户名称为模式所有者，或者更恰当地说，相关对象组的所有者。让我们把这个话题挖深一点，详细讨论一下！本教程的日程如下:

*   [什么是 SQL？](#whatissql)
*   [什么是 SQL 中的模式？](#schema)
*   [使用模式的优势](#advantages)
*   [如何创建模式？![SQL-Exception Handling in PL/SQL-Edureka](img/9013709a3b45c1c5deda77ef3f10285d.png)](#createschema)
    *   [使用 SQL Server Management Studio](#sqlservermanagementstudio)
*   如何改变一个模式？
*   [参数](#parameter)
*   如何删除一个模式？

我们开始吧。

## **什么是 SQL？**

大家可能都知道 SQL 这个术语，它代表了结构化查询语言。SQL 是一种 ASI 标准语言，但是这种语言有许多不同的版本。SQL 是关系数据库系统的标准语言。它帮助你访问和操作数据库。可以对数据库执行几个查询。可以从数据库中检索数据。你可以[插入](https://www.edureka.co/blog/insert-query-sql/)，[更新](https://www.edureka.co/blog/sql-update/)，删除数据库中的记录。它有助于创建新的数据库。还可以创建新的表和视图。

让我们继续下一部分。

## **什么是 SQL Server 中的模式？**

[SQL](https://www.edureka.co/blog/sql-basics/) 中的模式是与[数据库](https://www.edureka.co/blog/what-is-a-database/)相关联的数据库对象的集合。数据库的用户名称为模式所有者(数据逻辑分组结构的所有者)。模式总是属于一个数据库，而一个数据库可以有一个或多个模式。此外，它也非常类似于存储数据库对象的单独的名称空间或容器。它包括各种数据库对象，包括表、视图、过程、索引等。

让我们继续，看看在 SQL 中使用模式的一些优点。

## **使用模式的优势**

*   您可以根据用户访问权限应用安全权限来分隔和保护数据库对象。
*   可以在一个数据库中管理一组逻辑数据库对象。模式在将数据库对象组织到这些逻辑组中起着重要的作用。
*   在数据库对象名称相同的情况下，该模式也有所帮助。但是这些对象属于不同的逻辑组。
*   一个模式可以在多个数据库中使用。
*   该模式还有助于增加安全性。
*   它有助于操纵和访问对象，否则这将是一个复杂的方法。
*   您还可以转移多个模式的所有权。
*   在数据库中创建的对象可以在模式间移动。

以上是一些优点，现在下一个主题是创建模式的方法。

## **如何创建模式？**

**创建 SQL 的语法:**

```
CREATE SCHEMA [schema_name] [AUTHORIZATION owner_name]
[DEFAULT CHARACTER SET char_set_name]
[PATH schema_name[, ...]]
[ ANSI CREATE statements [...] ]
[ ANSI GRANT statements [...] ];

```

您可以使用 SQL server management studio 创建架构。按照提到的步骤！

### **使用 SQL Server Management Studio**

按照步骤创建一个模式。

*   在对象资源管理器中，单击数据库文件夹。
*   在[数据库](https://www.edureka.co/blog/what-is-a-database/)下创建新的数据库模式。
*   右键单击安全文件夹，单击新建，选择架构。
*   在“模式-新建”对话框中，输入要为新模式创建的特定名称。
*   在“模式所有者”框中，输入数据库用户的名称，以便拥有该模式。单击搜索，打开搜索角色和用户对话框。
*   点击确定。

这就是模式的创建方式。现在让我们看看模式是如何改变的。

## 如何改变一个模式？

使用 alter schema 语句可以改变数据库中的模式。此语句专门用于重命名模式。新所有者必须是现有用户。

### **改变模式的语法:**

```

ALTER SCHEMA schema_name [RENAME TO new_schema_name] [ OWNER TO new_user_name]

```

## **参数**

| 名字 | 描述 |
| 新模式名称 | 模式的新名称 |
| 架构名称 | 现有模式 |
| 新所有者 | 架构的新所有者 |

理解了如何改变模式后，让我们继续下一部分。我们将学习如何删除一个模式。

## 如何删除一个模式？

为了删除模式，我们使用以下语法:

```

DROP SCHEMA <schema name>

```

如果必须删除整个数据库，请遵循上述语法:

```

DROP DATABASE databasename;

```

这都是关于 SQL 中的模式。我希望这些内容解释了上述对你的知识的附加价值。继续阅读，继续探索！

到此，我们结束这篇文章。我希望您理解了如何使用数据库中的各种约束。*如果您希望了解更多关于 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 的信息，并了解这款开源关系数据库，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，该培训包含讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

有问题要问我们吗？请在本文关于 SQL 约束的评论部分提到它，我会尽快回复您。