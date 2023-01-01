# 2023 年你必须准备的数据仓库面试问题和答案

> 原文：<https://www.edureka.co/blog/interview-questions/data-warehousing-interview-questions-and-answers/>

基于 DBMS 的系统已经过时了。组织数据处理涉及吸收、存储、检索和处理的日子已经一去不复返了。如今，需要同时处理来自各种来源的数据，并呈现和处理即时结果，以确保以客户为中心的业务运营。像 BFSI、医疗保健、公用事业甚至政府组织这样的垂直行业正在转向由商业智能驱动的数据仓库，以击败竞争对手。这种关键的业务需求已经产生了一种全新的业务动态，围绕这种业务动态，工作岗位如雨后春笋般涌现。

如果你对管理数据充满热情，数据仓库和商业智能(DWBI)是一个有利可图的职业选择。如果你想参加 DWBI 面试，我们可以帮你。我们已经创建了一个可能的数据仓库面试问题和答案的列表。如果你最近参加过 DWBI 的面试，我们鼓励你在评论栏里粘贴更多的问题。万事如意！

## 1.什么是数据仓库？列出数据仓库架构的类型。

数据仓库是组织历史数据的电子存储，用于数据分析。换句话说，数据仓库包含支持组织决策过程的各种数据。

主要有 3 种类型的数据仓库架构:

 <caption>#### **数据仓库架构的类型**</caption> 
| **单层架构** | 

*   The purpose of single layer is to minimize the amount of stored data by removing data redundancy.
*   This is not commonly used in practice.

 |
| **双层架构** | 

*   This architecture separates the physically available data source from the data warehouse.
*   This schema is not scalable & it does not support a large number of end users.
*   Because of the network limitation, this architecture faces the problem of connection.

 |
| **三层架构** | 

*   It is the most widely used architecture, consisting of top layer, middle layer and bottom layer.
*   **Bottom layer:** Usually, a relational database of the data warehouse acts as the bottom layer, where data is cleaned, converted and loaded.
*   **Middle tier:** This application tier is a OLAP server & that presents an abstract view of the database and acts as an intermediary between the end user and the database.
*   "T0" top layer: "t1", "T2" and "T3" The top layer is the front-end client layer that channels data from the data warehouse.

 |

## 2.在数据仓库环境中定义数据分析。

*   数据分析是检查原始数据的科学，目的是得出有关该数据的业务驱动的结论。
*   数据仓库的作用是支持数据分析。

## 3.什么是面向主题的数据仓库？

面向主题的数据仓库是那些围绕特定“主题”存储数据的数据仓库，例如客户、销售、产品等等。

## 4.OLAP 代表什么？

OLAP 代表联机分析处理。它是一个收集、管理和处理多维数据以进行分析和管理的系统。

## 5.OLTP 代表什么？

OLTP 代表联机事务处理。这是一个无论何时收到数据都会对大量并发用户进行修改的系统。

## 6.列出 OLAP 服务器的类型。

*   关系 OLAP
*   多维 OLAP
*   混合 OLAP
*   专用 SQL 服务器

## 7.请列出 OLAP 的一些职能。

OLAP 执行的一些主要功能包括“上滚”、“下钻”、“切片”、“掷骰子”和“旋转”。

## 8.什么是星型模式？

星型模式是数据仓库中使用的一种模式，其中一个事实表引用多个维度表。在星型模式中，来自所有维度表的“键”流入事实表。这种实体关系图类似于星形，因此被命名为星形模式。

## 9.什么是雪花模式？

就像星型模式一样，snow flake 模式中的一个事实表引用多个其他维度表。然而，在这里，这些维度表被进一步规范化为多个相关的表。随着这些表被进一步雪花化成更小的表，这种模式被称为雪花模式。

## 10.用于模式定义的语言是什么？

数据挖掘查询语言(DMQL)用于架构定义。

## 11.有哪些不同类型的“维度”？

*   确认维度
*   垃圾维度
*   退化维度
*   角色扮演维度

## 12.什么是迷你维度？

迷你维度是在将大量快速变化的属性分隔到较小的表中时使用的维度。

## 13.定义无事实的事实。

无事实事实是不包含任何值的事实表。这样的表只包含来自不同维度表的键。

## 14.ODS 是什么？

ODS 代表操作数据存储。它本质上是实时操作数据的存储库。

## 15.什么是数据立方体？

数据立方体有助于在多个方面表示数据。数据立方体是由维度和事实定义的。

## 16.你对 ER 模型的理解是什么？

ER 模型或实体关系模型是一种用于数据建模的方法，其中建模的目标是通过减少冗余来规范化数据。

## 17.你所理解的维度建模是什么？

维度模型是一种由“维度”和“事实表”组成的方法论。事实表用于存储来自“维度表”的各种事务性度量，这些维度表限定了数据。

## 18.数据仓库环境中的 VLDB 是什么？

VLDB 代表超大型数据库。VLDB 的大小预设为超过 1tb。

## 19.什么是数据集市？

数据集市是组织数据的子集。换句话说，它是特定于组织内特定组的数据集合。

## 20.什么是数据聚合？

数据汇总是对任何能够以汇总形式表达信息以进行统计分析的过程的广义定义。

## 21.什么是摘要信息？

摘要信息是数据仓库中存储预定义聚合的位置。

## 22.区分“bteqexport”和“fastexport”？

当行数少于 50 万时使用“bteqexport ”,而当行数超过 50 万时使用“fastexport”。

有问题要问我们吗？请在评论区提出来，我们会尽快回复您，或者今天就在线参加我们的[数据仓库和商业智能](https://www.edureka.co/data-warehousing-and-bi)课程。

**相关帖子:**

[数据仓库&商业智能职业道路](https://www.edureka.co/blog/data-warehousing-and-business-intelligence-career-path-bag-data-warehousing-and-data-mining)