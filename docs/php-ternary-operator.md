# PHP 中三元运算符是什么，如何使用？

> 原文：<https://www.edureka.co/blog/php-ternary-operator/>

使用 if-else 和 switch case 是评估条件编程的重要部分。我们总是到处寻找捷径，不管是旅行的路线还是游戏或代码。在这个三元运算符 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中，我们将看到它是如何按照以下顺序缩短条件语句的:

*   [什么是三元运算符？](#ternaryoperator)
*   [我们什么时候使用三元运算符？](#useternaryoperator)
*   [三元运算符的优点](#advantages)
*   [三元速记](#ternaryshorthand)
*   [零合并算子](#nullcoalescing)

## **什么是三元运算符？**

三元运算符是一个条件运算符，它在执行比较和条件运算时减少了代码长度。此方法是使用 if-else 和嵌套 if-else 语句的替代方法。该运算符的执行顺序是从左到右。显然，这是节省时间的最佳选择。

当条件遇到空值时，它还会生成一个电子通知。它被称为三元运算符，因为它接受三个操作数——一个条件、一个 true 结果和一个 false 结果。

**语法:**

```

(Condition) ? (Statement1) : (Statement2);

```

*   **条件:**返回布尔值的是待求值的表达式。
*   **语句 1:** 是条件导致真状态时要执行的语句。
*   **语句 2:** 是条件导致假状态时要执行的语句。

**举例**程序判断学生是否及格:

```

<?php
$marks=40;
print ($marks>=40) ? "pass" : "Fail";
?>

```

**输出:**

```
pass
```

## **我们什么时候使用三元运算符？**

当我们需要简化用于给变量赋值的 if-else 语句时，我们使用三元运算符。此外，当我们分配 post 数据或验证表单时，通常会用到它。

比方说，我们正在为一所大学编写一个登录表单，我们希望确保用户输入了学校提供的注册号，然后我们就可以继续进行。

```

//if the registration number is not specified, notify the customer
$reg_number = (isset($_POST['reg'])) ? $_POST['reg'] : die('Please enter your registration number');

```

为了更好地理解，我们来看一个验证表单的示例:

```

<form method="post" action=”edit.php">
<label>Name<input type="text" name="name"></label><br>
<label>Email<input type="text" name="email"></label><br>
<input type="submit" name="submit" value="Submit">
</form>

```

为了获得文本字段的值，我们可以使用下面的代码:

```

<?php
if(isset($_POST['submit']))
{
$name = isset($_POST['name']) ? $_POST['name'] : null;
$email = isset($_POST['email']) ? $_POST['email'] : null;

}
?>

```

## **三元运算符的优点**

*   这将使代码更短
*   这将使代码更具可读性
*   代码变得更简单

## **三元速记**

短三元运算符语法可以通过省略三元运算符的中间部分来使用，以便快速简化计算。它也被称为猫王歌剧院(？:)

**语法:**

```

expression1 ?: expression2

```

可以使用 Elvis 运算符来减少冗余条件并缩短作业长度。它是省略了第二个操作数的三元运算符。如果操作数为真，它将返回第一个操作数，否则它将计算并返回第二个操作数。

```

$val = $_GET['user'] ?: 'default';

```

如果你像这样使用三元速记符，它会引起注意如果

```

$_GET['user']

```

不设置，而不是像这样编写一些冗长的代码:

```

$val = isset($_GET['user']) ? $_GET['user'] : 'default';

```

## **零合并算子**

它结合 isset()函数取代了三元运算，isset()函数用于检查给定变量是否为空，如果存在，则返回第一个操作数，否则返回第二个操作数。

语法:

```

(Condition)?(Statement1)?(Statement2);

```

```

$user= $_GET['user'] ?? 'nobody';

```

它将获取**$ _ GET[' user ']【T1]的值，如果不存在，则返回' nobody'。**

而不是像这样写一些冗长的代码:

```

$user= isset($_GET['user']) ? $_GET['user'] : 'nobody';

```

本文到此结束，我希望你理解了三元运算符，三元运算符的目的和优点，三元速记和零合并运算符。

*如果你发现这个三元运算符博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“php 中的三元运算符”的评论部分提及，我会回复你。*