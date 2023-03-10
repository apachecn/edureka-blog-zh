# 关于 PHP 中的特征，您需要知道的是

> 原文：<https://www.edureka.co/blog/traits-in-php/>

在我们理解 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中的特征之前。我们已经了解了继承意味着一个类可以扩展另一个类。假设，类 B 扩展了类 A，类 C 也扩展了类 A，这意味着类 A 中定义的函数可以被类 B 和类 C 访问，但是假设类 B 和类 C 覆盖了函数 X，假设类 D 扩展了这两个类。

![traits-in-php](img/9be97150ca64e511481c0474a2523697.png)

虽然 PHP 不支持多重继承，但是假设这是一种情况，那么 D 类将运行哪个函数呢？是 B 班的还是 C 班的？所以这实际上是多重继承的问题，这就是 PHP 不支持它的原因，但是在很多情况下，为了代码的可重用性，你需要扩展不止一个类。

![traits-in-php-2](img/054432c15ba500ab324e36d45358b127.png)

当我们谈到单一继承问题时，D 类扩展了 C 类，但如果我们想在 D 类中拥有 B 类的一些功能，我们可以使用 PHP 5.4 中引入的特征。它简单且易于创建。它就像一个类，但只是针对一组方法，就像抽象类一样，你不能实例化离散的方法。

*   [特质](#traits)
*   [优点特质](#advantage)
*   [特质 Vs 界面](#interface)

## **PHP 中的特性**

一般来说，他们可以定义静态成员和静态方法，这有助于开发人员在不同类层次的几个独立类中自由地重用方法。性状避免了与多重遗传、混合相关的问题，也降低了复杂性。

**语法:**

```
<?php
// syntax for trait in PHP
Trait sample
{
function ReturnType()
{
}
function ReturnDescription()
{
}
}
?>

```

特征可以以这种方式包含在其他类中。

```
class Post
{
use Sharable;
}
class Comment
{
use Sharable;
}

```

由于 PHP 不允许多重继承，Trait 通过允许我们在多个类中重用相同的功能来克服这个问题。下面的例子演示了 PHP 中特征的工作方式。

```

<?php
trait Sample
{
public function func()
{
echo "trait";
}
}

class myClass
{
use sample;
public function func()
{
echo "class";
}
}

$obj = new myClass();
$obj->func();
?>

```

**输出:**

## **![Output-traits](img/18c2840110ba99f279aabeca19adb1d3.png)**

## **特质优势**

特征减少了代码的重复，同时防止了复杂的类继承，这在你的应用环境中可能是没有意义的。

![advantages-traits](img/a62d7a9a790be1477793a7c522902277.png)

这有助于定义简洁明了简单特征，然后在适当的时候混合这些功能。

## **PHP 中的特征与接口**

一般来说，PHP 中的接口和 trait 的主要区别在于，trait 基本上定义了每个类中每个方法的实际实现，所以同一个接口由许多类实现但具有不同的行为，而 trait 只是 PHP 中注入到一个类中的代码块。

```
<?php
interface SampleInterface
{
// function...
}
?>

```

至此，我们结束了 python 文章中的这些特征。我希望你已经了解了特征、特征的优势以及特征和界面的区别。

*如果您发现这个 PHP 博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在“PHP 的特性”的评论部分提到它，我会回复你。*