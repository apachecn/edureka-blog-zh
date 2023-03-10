# 如何在 php 中实现抽象类？

> 原文：<https://www.edureka.co/blog/abstract-class-in-php/>

如果我们想写一个特定的类方法，但我们只知道方法的名字，而不知道应该如何写的细节，我们在 PHP 中使用抽象类。当我们希望子类被提交给它们从父类继承的某些方法，但是我们不能提交应该写在方法内部的代码时。然后我们使用抽象类和方法。

因此，让我们通过以下几点来探讨上述问题，

*   [PHP 中的抽象类](#AbstractClassinPHP)
*   [创建一个抽象类](#Createanabstractclass)
*   [抽象类内的非抽象方法](#Nonabstractmethodsinsideanabstractclass)
*   [抽象类的工作](#WorkingOfAbstractClass)

那么让我们开始吧，

## **PHP 中的抽象类**

至少有一个方法的类， 这是一个没有任何实际代码的方法，只有名称和参数，并且已经被标记为“抽象” 被称为抽象类。当我们想定义一个抽象类时，我们需要使用关键字 abstract。为了 提供一种模板来继承并强制继承类实现抽象方法，我们使用了一个抽象类。 它既可以包含抽象方法，也可以包含非抽象方法。

继续这个 PHP 中的抽象类，

## **创建一个抽象类**

```
</pre>

<?php //abstract class abstract class school { // abstract function teach abstract public function teach(); } ?>

```

在上面的例子中，我们的类 school 是一个抽象类，它有一个抽象方法。如果你想创建一个扩展我们的类 学校 的新类，那么你必须为抽象方法 教导 提供一个定义，否则子类也应该是抽象的。所有子类都必须提供方法 teach()的定义。

继续这个 PHP 中的抽象类

## **抽象类中的非抽象方法**

非抽象方法也可以和抽象方法一起或不一起出现在抽象类中。所以抽象类也被称为部分实现类。子类可以直接访问和使用它们，而无需覆盖它们。

```
<?php //abstract class abstract class school { //It is protected variable protected $subject; //It is non-abstract public function english public function english() { echo $this->subject. " English Subject
";
}        
//It is non-abstract public function computer
public function computer()
{
echo $this->subject. " Computer Science subject
";
}        
//It is non-abstract public function tenthClassa
public function tenthClass($group)		{
$this->subject = $group;
}        
//It is abstract public function teach
abstract public function teach();
}    
?>

```

在上面，我们在我们的抽象 学校 类中增加了三个非抽象方法 【英语()计算机() 和 tenthClass() 。

继续这个 PHP 中的抽象类

## **抽象类的工作**

下面的例子演示了抽象类的工作原理

```
<?php abstract class school { //abstract method only needs to define the required arguments abstract protected function subject($name); } class ConcreteClass extends school { public function subject($sub) { $sub1=$sub; return $sub; } } $obj = new ConcreteClass; echo $obj->subject("English");
echo "
";
echo $obj->subject("Computer Science");
?>

```

![feature Image - Abstract Class In PHP - Edureka](img/bf1fa000e54fa09288353b74980b57d1.png)

本文到此结束，我希望你理解 PHP 中的抽象类，创建一个抽象类，在抽象类中使用非抽象方法。如果你觉得这篇文章相关，请查看 Edureka 的[](https://www.edureka.co/php-mysql-self-paced)PHP 认证培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*