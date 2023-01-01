# JAVA 中完整性约束的介绍

> 原文：<https://www.edureka.co/blog/introduction-to-integrity-constraints-in-java/>

[//www.youtube.com/embed/_rKDgN6jvjY](//www.youtube.com/embed/_rKDgN6jvjY)

## JAVA 中完整性约束的组成:

*   该值不能为空
*   应该是独一无二的
*   它将有唯一的主键，用于查找表上的值
*   外键，以防另一个表中有相同的主键

## 不为空

它是一个约束，确保每一行都填充有该列的某个值，该值已被指定为“not null”。

## 基本语法

创建表 table_name

(column1_name 数据类型不为空，

column2_name 数据类型)；

**此处列 1 数据类型不能为空*

## 独特的

它是一个约束，用于表中的列，以便该列的行在允许空值的情况下是唯一的。

## 基本语法

创建表 table_name(

Column1_name 数据类型唯一，

Column2_name 数据类型)；

* *这里，唯一列 1 将只接受唯一值。*

## 主键

它是一个约束，用于表中的一列，以便表中的一行可以被唯一地标识。

## 基本语法

创建表 table_name(

Column1_name 数据类型主键

Column_2name 数据类型)；

在同一列中找不到任何其他具有相同值的主键。它用于引用具有相同值的表。

## 外键

它是一种约束，用于在相同或不同表中的两列之间建立关系。对于要定义为外键的列，它应该被定义为它所引用的表中的主键。可以将一列或多列定义为外键。这个约束标识引用另一个表中主键的任何列，这意味着在一个表中有主键，并且在第二个表中找到所有值。然后，第二个表中的列实际上是第二个表的外键。

## 基本语法

创建表 table_name(

Column1_name 数据类型外键，

Column_2name 数据类型)；

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[JAVA/J2EE 简介&SOA](https://www.edureka.co/blog/videos/introduction-to-javaj2ee-soa/)

[JAVA/J2EE & SOA 课程](https://www.edureka.co/java-j2ee-soa-training)