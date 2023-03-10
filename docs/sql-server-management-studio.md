# 了解如何使用 SQL Server Management Studio

> 原文：<https://www.edureka.co/blog/sql-server-management-studio/>

SQL Server 是微软开发的关系型[数据库](https://www.edureka.co/mysql-dba)管理系统。这是一个处理任何 [SQL](https://www.edureka.co/blog/sql-tutorial/) 基础设施的集成环境。在本文中，我们将了解 SQL Server management studio。本博客涵盖了以下主题:

*   [什么是 SQL Server Management Studio？](#ssms)
*   [安装](#install)
*   [访问管理工作室](#access)
*   [SQL Server Management Studio 组件](#components)
*   [SQL Server Management Studio 提示](#tips)

## **什么是 SQL Server Management Studio？**

SQL server management studio 也称为 SSMS，是处理任何 SQL 基础结构的集成环境。它是免费的，基本上提供了一个图形用户界面来使用 MSSQL server。

![SQL Server Management Studio](img/704475e6015d5ddad76a7aa8eba05b17.png)

SSMS 提供了各种工具来配置、监控和管理 SQL server 和数据库的实例。您可以使用 SQL server management studio 部署、监视您的应用程序并构建查询和脚本。

让我们看看如何安装 SSMS。

## **安装**

你可以在这里下载安装设置[。下载安装程序后，按照以下步骤安装 SQL server management studio。](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)

*   打开安装程序并选择安装。 ![setup - sql server management studio - edureka](img/4718b7963ee3d7044c3a2144bb0b7871.png)
*   安装将开始。 ![progress - sql server management studio - edureka](img/b1eba9e264d165849a1ed8c680f6e6bd.png)
*   安装完成后，您将看到一个类似下图的对话框。 ![setup complete - sql server management studio - edureka](img/b7110754ee3cd86d9a746d6f90988b4e.png)

## **访问管理工作室**

当您从“开始”菜单打开 SQL server management studio 时，将会打开一个类似于下图所示的窗口。

![](img/00a46675dec3665eebedf3a2d7e611cf.png)

让我们了解一下图像中提到的所有字段的用途。

*   **服务器类型**–这是从四种可用服务中选择一种。可用的服务有数据库引擎、分析、报告和集成。

*   **服务器名称**–这是将要建立连接的服务器的名称。

*   **身份验证**–如果我们在 SQL server 安装期间使用了“Windows 身份验证”，这将是默认的 Windows 身份验证。

*   **用户名/密码**–如果您选择“Windows 身份验证”以外的任何内容，这两个字段将是必填的。

还有一种访问 SSMS 的方法，使用命令行。要使用命令行访问 SSMS，请复制 ssms.exe 的完整路径并运行以下命令。

```
'path-ssms.exe'

```

## **SSMS 组件**

*   **对象资源管理器**–可用于查看和管理一个或多个 SQL Server 实例中的所有对象。

*   **模板浏览器**–模板浏览器可用于构建和管理文件，以加速查询和脚本的开发。

*   **Solution Explorer**–它可用于构建和管理管理项目，如脚本和查询。

*   **可视化数据库工具**–SSMS 包括可视化设计器，用于构建 transact-SQL 查询、表格和图表数据库。

*   **查询和文本编辑器**–Management studio 语言编辑器可用于交互式构建和调试脚本和查询。

## **SMSS 提示**

*   SQL server management studio 是一个独立的产品，它可以与任何版本的 SQL server 一起使用。它不需要任何特定版本的 SQL Server。

*   为了提高可读性，使用更多的注释。大代码会降低可读性。您可以在任何一行前面使用“-”来注释掉它。 ![](img/2abf6245773ba4ce75874acc55a32ba3.png)

*   始终确保您已选中工具>选项>环境>自动恢复中的自动恢复选项，以便在意外关机的情况下最大限度地减少数据丢失。 ![](img/23a28946bce655e5b06f6b1aeed38ef0.png)

*   以文本格式保存您的查询，以供将来参考。

以上就是关于 SQL Server Management Studio 的全部内容，我希望这篇文章能够帮助您增加知识的价值。更多关于 SQL 或者数据库的信息，可以参考我们这里的综合阅读清单:  [**数据库 Edureka**](https://www.edureka.co/blog/category/databases/) 。

*如果您希望获得有关 MySQL 的结构化培训，那么请查看我们的 **[MySQL DBA 认证培训](https://www.edureka.co/mysql-dba)** ，它附带有讲师指导的现场培训和真实项目体验。本培训将帮助您深入了解 MySQL，并帮助您掌握这门学科。*

*有问题吗？请在“ **SQL Server 管理服务器**的评论区提出来，我会回复你。*