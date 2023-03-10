# 如何在 PHP 中实现多态性？

> 原文：<https://www.edureka.co/blog/polymorphism-in-php/>

Poly 表示许多，Morphism 表示形式或类型。以多种方式使用一个对象被称为[多态性](https://www.edureka.co/blog/polymorphism-in-java/)。换句话说，一个功能在不同的情况下扮演不同的角色。在这篇文章中，我们将探索 PHP 中的多态性

本文将涉及以下几点

*   使用接口的多态性
*   使用抽象类的多态性

所以让我们从这篇文章开始，

## PHP 中的多态性

## **多态性使用接口**

接口类似于类，但是在接口内部只声明了函数。它在界面中没有任何主体或功能。接口需要由一个具体的类来实现。实现类必须覆盖接口中定义的所有函数

```

<?php
interface vehicle
{
public function choose();
}
class MyBike implements vehicle
{
public function choose()
{
echo "Bike choosed". "<br>";
}
}
class MyCar implements vehicle
{
public function choose()
{
echo "Car choosed" ;
}
}
$obj=new MyBike();
$obj->choose();
$obj1=new MyCar();
$obj1->choose();
?>

```

**输出**

选择的自行车

选择的汽车

继续 PHP 文章中的多态性

## **使用抽象类的多态性**

抽象类是一个类，只是用来继承它的一个类。它只能用作父类。换句话说，你不能声明一个被声明为抽象的类的对象

```

<?php
abstract class shape
{
abstract protected function area();
}
class rectangle extends shape
{
var $l,$b;
public function __construct($x , $y)
{
$this->l=$x;
$this->b=$y;
}
public function area()
{
$a=$this->l*$this->b;
return $a;
}
}
class circle extends shape
{
var $r;
public function __construct($x)
{
$this->r=$x;
}
public function area()
{
$pi=3.142;
$a=pow($this->r,2)*$pi;
return $a;
}
}
$r1=new rectangle(10,20);
$area=$r1->area();
echo "rectangle area= $area <br>";
$c1=new circle(10);
$area=$c1->area();
echo "cirlce area=$area<br>";
?>

```

**输出**

矩形面积= 200

圆面积=314.2

至此我们结束了这篇文章，我希望你理解了多态性的概念，以及如何使用接口和抽象类来获得多态性。

*如果你发现这个博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“**PHP 中的多态性**”的评论部分提到它，我会回复你。*