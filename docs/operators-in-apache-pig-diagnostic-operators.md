# Apache Pig 中的操作符:第 2 部分-诊断操作符

> 原文：<https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/>

这是阿帕奇清管器操作员系列的第 2 个<sup>和第 1 个</sup>帖子。这篇文章是关于阿帕奇猪中的**诊断操作符**。你也可以参考我们之前关于关系运算符 的 [帖子了解更多信息。](https://www.edureka.co/blog/operators-in-apache-pig/)

让我们创建两个文件来运行这些命令。我们有两个名为“第一”和“第二”的文件第一个文件包含三个字段:用户、url 和 id。

[![Apache pig - 2](img/89551944b20f928f7143b2e540e82cec.png "Operators in Apache Pig - 2")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

第二个文件包含两个字段:url 和 rating。这两个文件是 CSV 文件。

[![Apache Pig - 3](img/da05fd2b12a3b74a3815c748e7d02c57.png "Operators in Apache Pig - 3")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

## **诊断符:**

#### **转储:**

DUMP 运算符用于运行 Pig Latin 语句，并在屏幕上显示结果。*在本例中，*操作员将“加载 1”打印到屏幕上。

[![Apache Pig - 4](img/a677de463d3f68b03350743e891babd9.png "Operators in Apache Pig - 4")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

#### **转储结果:**

[![Apache Pig - 5](img/43b423841aeaff9968be9f7ca2c085bb.png "Operators in Apache Pig - 5")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

#### **描述:**

使用 DESCRIBE 运算符查看特定关系的模式。DESCRIBE 运算符最适合用于调试脚本。

[![Apache Pig - 6](img/6f80c60c7b7567e3a7d39c7a8f20a5e5.png "Operators in Apache Pig - 6")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

#### **举例说明:**

说明运算符用于查看数据如何通过一系列 Pig Latin 语句进行转换。在调试脚本时，ILLUSTRATE command 是您最好的朋友。这个命令本身可能就是选择 Pig 而不是其他东西的一个很好的理由。

[![Apache pig - 7](img/cffa49d3aeb05953a075e11a0b031952.png "Operators in Apache pig - 7")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

#### **解释:**

解释操作符打印逻辑和物理平面。

[![Apache pig - 7](img/44799170b19bce646dd5cef125709d83.png "Operators in Apache pig - 7")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

[![Apache pig - 8](img/a2168a2c79da9cc9e6db1e4669fd8914.png "Operators in Apache pig - 8")](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/)

## **阿帕奇猪 0.12.0 的改进**

0.12.0 是当前可用的 Apache Pig 版本。这个版本包括几个新特性，比如断言操作符、IN 操作符、CASE 操作符。

#### **断言运算符:**

断言操作符可用于数据验证。*例如，*如果任何值为负整数，以下脚本将失败:

a = load 'something' as (a0: int，a1:int)；

通过 a0 > 0 断言 a，‘a 不能为负的原因’；

#### **在操作员:**

以前，Pig 不支持 IN 操作符。为了模仿 IN 操作，用户必须连接几个 OR 操作符，如下面的*示例*所示:

a =使用 PigStorage('，')作为(i:int)加载' 1 . txt '；

b =通过以下方式过滤 a

(i == 1)或

(i == 22)或

(i == 333)或

(i == 4444)或

(i == 55555)

现在，可以使用 in 运算符以更压缩的方式重写这种类型的表达式:

a =使用 PigStorage('，')作为(i:int)加载' 1 . txt '；

b =在(1，22，333，4444，55555)中用 I 过滤 a；

#### **案例表达式:**

早些时候，Pig 不支持 CASE 语句。为了模仿它，用户经常使用嵌套的 bincond 操作符。当有多层嵌套时，这些可能变得不可读。以下是 Pig 当前支持的 CASE 表达式类型的*示例*:

case _ operator = FOREACH foo GENERATE(

案例一% 3

当 0 时，则为“3n”

当 1 时，则“3n+1”

ELSE '3n+2 '

结束

);

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[阿帕奇猪中的运算符——关系运算符](https://www.edureka.co/blog/operators-in-apache-pig/ "Operators in Apache Pig: Part 1- Relational Operators")

[阿帕奇猪](https://www.edureka.co/blog/creating-udf-in-apache-pig/ "Steps to Create UDF in Apache Pig")创造 UDF 的步骤

[猪简介](https://www.edureka.co/blog/introduction-to-pig/ "Introduction to Pig")