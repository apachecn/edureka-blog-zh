# PHP 教程:PHP 中变量和字符串的数据类型和声明

> 原文：<https://www.edureka.co/blog/php-data-types-declaration>

在之前的 [PHP 教程](https://www.edureka.co/blog/php-tutorial-differentiating-php-code-in-html-script "PHP Tutorial: Differentiating PHP Code in HTML Script") 中，我们学习了各种方法来 [区分 PHP 代码和 HTML 代码](https://www.edureka.co/blog/php-tutorial-differentiating-php-code-in-html-script "PHP Tutorial: Differentiating PHP Code in HTML Script") 、，这样 PHP 解析器就很容易解释代码了。在这篇文章中，让我们学习如何在 PHP 脚本中存储信息。存储信息是必要的，以便您可以在程序中的任何地方使用该值。变量是一个名字，用来存储程序中使用的值。在 PHP 中，变量名前面带有“$”符号。

*举例:*

```
<?php
$a=10;
$b=10;
$c=$a+$b;
echo $c;
?>
```

## **变量命名:**

命名变量时，必须遵循某些规则。它们是:

*   变量用前面的美元符号($)定义

*   PHP 变量必须以字母或下划线“_”开头

*   PHP 变量应该只包含字母数字字符和下划线

*   变量名不能以数字开头

*   我们可以用下划线来分隔变量名。例如$employee_details

*   变量名区分小写字母和大写字母(Y 和$y 是两个不同的变量)

*   可以使用“=”运算符赋值

*   PHP 中另一件重要的事情是所有的语句必须以分号“；”结尾

使用变量的第一步是给它赋值。

## **分配变量:**

变量赋值很简单。只需写下名字，加上一个等号(=)，然后是我们要赋给那个变量的表达式。

*例:*$ pi = 3+0.1489；

## **重新分配变量:**

给变量赋值后，如果在程序的后期必须更改，也可以将值重新赋值给同一个变量名。

*举例:*

```
$my_num_var = “this should be a number – hope it is reassigned later”;
$my_num_var = 5;
```

## **未赋值变量:**

如果您试图在给变量赋值之前使用它们，许多编程语言都会报告错误。但是 PHP 处理这种未赋值的变量。在 PHP 中，默认的错误报告设置允许您使用未赋值的变量而不报告任何错误。如果您希望得到关于尚未赋值的变量的警告，错误报告级别将从默认的错误报告级别变为 E_ALL。

这可以通过两种方式实现:

*   通过在脚本顶部包含错误报告(E_ALL)语句。

*   通过更改 php.ini 文件来设置默认级别。

## **默认值:**

当您没有将值传递给函数中的参数时，PHP 默认分配一个值，该值称为默认值

*   PHP 中的变量没有内部类型

*   变量事先不知道它是否将被用来存储一个数字或一串字符

*   变量的类型根据其使用的上下文来解释

PHP 脚本中要存储和使用的数据可以是各种类型的。为了区分这一点，PHP 提供了各种数据类型。

## **PHP 中的数据类型**

PHP 脚本中存储和使用的值有不同的类型。数据类型定义了程序中使用的数据类型。PHP 有 8 种数据类型。它们是:

*   整数是整数，没有小数点，比如 495

*   双精度是浮点数，比如 3.1415 或 49

*   布尔只有两个可能的值:TRUE 和 FALSE

*   NULL 是一种特殊的数据类型。它只有一个值:NULL

*   字符串是一系列字符

*   数组是值的集合

*   对象是类的实例，可以访问特定类的数据和函数

*   资源是保存对 PHP 外部资源(数据库连接)的引用的特殊变量

这些数据类型分为两种主要类型:

*   **简单类型**–整数、双精度数、布尔值、空值和字符串

*   **复合类型**–字符串、数组、对象、资源

**简单数据类型:**

**整数:**

整数是最简单的类型。它们对应于简单的整数，既有正数也有负数。

*举例:*

```
$int_var = 6789;
$another_int = -1245+134 //will zero
```

**双精度和浮点数:**

实数(即包含小数点的数字)

*举例:*

```
$first_double =568.998;
$second_double = 0.444;
$even_double =6.0;
```

## **布尔:**

布尔值是 true 或 false 值，用于控制结构，如 if 语句的测试部分

**布尔常量:**

为了使用布尔值，PHP 提供了两个常量:TRUE 和 FALSE

*举例:*

```
If(TRUE)
Print();
Else
Print();
```

## **NULL:**

然而，NULL 类型将这种情况推向了逻辑的极端:NULL 类型只有一个可能的值，即值 NULL

*举例:*

$my_var = NULL;

赋给 null 的变量具有以下属性:

*   在布尔上下文中，它的计算结果为 FALSE

*   当用 IsSet()测试时，它返回 FALSE

除了声明数字，PHP 还支持“字符串”,其中字符序列被视为一个单元。

## **PHP 中字符串的声明**

字符串是被视为一个单元的字符序列。PHP 中的字符串有两种声明方式:

*   单引号

*   双引号

**单引号字符串:**

在这里，单引号中的语句将按原样显示，不做任何更改。

*举例:*

```
<?php
$string_variable = "name";
$literally = 'My $string_variable is Happy!
';
print($literally);
?>
```

*输出:*

我的$string_variable 开心了！

**双引号字符串:**

这里双引号中的语句将被解释，程序的输出将被显示。

*举例:*

```
<?php
$string_variable = "name";
$literally = “My $string_variable is Happy!
”;
print($literally);
?>
*Output:*
```

我的名字叫快乐！

当我们想重复执行一个语句块时，就要用到函数。

请继续关注我们下一篇关于如何将参数传递给函数以及 PHP 支持的各种内置函数的文章。

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[PHP 入门& MySQL](https://www.edureka.co/php-mysql-self-paced)

[PHP 教程:区分 HTML 脚本中的 PHP 代码](https://www.edureka.co/blog/php-tutorial-differentiating-php-code-in-html-script)