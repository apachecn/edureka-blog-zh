# 如何在 PHP 中实现接口？

> 原文：<https://www.edureka.co/blog/interface-in-php/>

[PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的接口一般需要在代码系统中有相同类型的命名法。假设你正在和一个团队一起工作，你已经创建了一些函数，而其他团队成员也创建了相同类型的函数，只是名字不同。显然，会有冲突。所以让我们详细讨论一下这个概念。

本文将涉及以下几点:

*   PHP 中的[接口](#InterfaceInPHP)
*   [接口示例](#ExampleforInterface)
*   [接口如何解决问题](#HowInterfaceSolvesProblem)

那么让我们开始吧，

## PHP 中的**接口**

它允许用户通过指定一个类必须实现的公共方法来创建程序，而不涉及如何实现特定方法的复杂性和细节。它通常被称为下一级抽象，将子类提交给它们应该实现的抽象方法。

下面的 代码演示了一个接口的例子。

## **接口示例**

```
<?php class Circle { public function getArea() { echo 'Circle Area'; } } class Square { public function CalculateArea() { echo 'Square Area'; } } $circ=new Circle; echo $circ->getArea();
?>

```

上面的代码得到了圆的面积。显然，如果用户想得到一个正方形的面积，他肯定也会通过调用 getArea()对 square 做同样的事情。 这会产生冲突，因为 square 没有任何名为 getArea()的函数。因此，你不得不强迫你的团队或你自己为你的整个项目创建相同的功能或相同的术语。

为此，我可以创建一个接口。接口只是强迫你在你的类中有一些函数。

继续 PHP 文章中的这个接口

## **界面如何解决问题？**

ShapeInterface.php:

```
<?php interface shapeInterface { //You don't need to give the structure of getArea public function getArea(); } ?>

```

这个接口会告诉将要实现这个接口的类，你必须实现这个函数，否则我会给你一个错误。

```

<?php
include "ShapeInterface.php";
class Circle implements ShapeInterface
{
public function getArea()
{
echo 'Circle Area';
}
}
class Square implements ShapeInterface
{
public function getArea()
{
echo 'Square Area';
}
}
$circ=new Circle;
$squ=new Square;
echo $circ->getArea();
echo "<br>";
echo $squ->getArea();
?>

```

如果你没有给出由接口决定的功能，那么你会得到一个错误。您甚至可以为单个类获得多个接口。你只需要用逗号给出接口的名称。

geometryInterface.php

```
<?php
interface geometryInterface
{
public function getCircumference($value1, $value2);
}
?>
<?php
include "ShapeInterface.php";
include "geometryInterface";
class Circle implements ShapeInterface,geometryInterface
{
public function getArea()
{
echo 'Circle Area';
}
public function getCircumference($value1, $value2)
{
echo $value1 . "<br>" . $value2\. "<br>";
}
}
class Square implements ShapeInterface
{
public function getArea()
{
echo 'Square Area';
}
}
$circ=new Circle;
$squ=new Square;
echo $circ->getArea();
echo "<br>";
echo $circ->getCircumference(21,23);
echo $squ->getArea();
?>

```

本文到此结束，我希望你通过各种场景理解了 php 中的接口。

*如果你发现这个博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在 PHP 中的“**接口** **评论区提及，我会回复你。***