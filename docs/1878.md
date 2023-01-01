# 关于 PHP 中的非序列化，您需要知道的一切

> 原文：<https://www.edureka.co/blog/unserialize-in-php/>

本文将在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中介绍 unserialize，一个让你对对象或数组进行 unserialize 的函数，并附有详细的实践演示。本文将涉及以下几点:

*   [在 PHP 中取消序列化](#UnserializeInPHP)
*   [取消对象的序列化](#UnserializinganObject)
*   [取消数组的序列化](#UnserializeAnArray)

那么让我们开始吧，

**在 PHP 中取消序列化**

unserialize 函数将序列化数据转换为实际数据。 通过序列化数据、数组或对象，我们的意思是将数据转换成纯文本格式。通过解序列化数据，我们将其转换回 PHP 代码。 所以如果我们序列化一个对象，我们把它变成一个纯文本字符串。如果我们不序列化它，我们会得到之前的对象，在 PHP 中。 当我们完成外部应用程序时，我们可能想要将序列化的转换回其原始的非序列化形式。

现在我们对 PHP 中什么是不序列化有了一些了解，让我们理解如何去序列化一个对象，

**取消对象的序列化**

这将把对象转换成一个纯文本字符串，然后再把纯文本字符串转换回一个对象。下面是在 PHP 中序列化和反序列化一个对象并输出序列化数据和非序列化数据的 PHP 代码。

```
<?php
Class cars
{
Public $color;
}
$car1= new cars ();
$car1->color=&rdquo; black&rdquo;;
//serializes the object into a plain text string
$car1_serialized=serialize($car1);
//outputs the serialized text string
Echo &ldquo;This is the serialized data shown below:<br> &lsquo;$car1_serialized&rdquo;;
Echo&rdquo; <br><br>&rdquo;;
//unserializes the plain text string back into an object
$car1_unserialized=unserialize(($car1_serialized);
//outputs theobject and an object property
Echo &ldquo;This is the unserialized data shown below:<br>&rdquo;;
Echo var_dump($car1_unserialized);
Echo&rdquo; <br>;
Echo &ldquo;Object property:&rdquo;. $car1_unserialized->color;
?>
```

**实际 PHP 输出**

下面显示的序列化数据:

'0:4:"汽车":1: {s:5:"颜色"；s:3:“黑”；}'

下面显示的未序列化数据:

Object(cars)# 2(1){[" color "]=>string(3)" black " }

物体属性:黑色

在这篇文章的下一部分“PHP 中的 Unserialze”中，我们将学习如何将 can unserialized，

**取消数组的序列化**

数组是一种复杂的结构，可能需要序列化才能与 PHP 的外部应用程序一起工作。一旦我们处理了外部应用程序或语言，我们可能需要将其转换回数组。我们通过 unserialize 函数来实现。

PHP 代码序列化一个数组，然后将序列化的数据反序列化回一个数组。

```
<?php
$colors=array (&ldquo;red&rdquo;,&rdquo; pink&rdquo;,&rdquo; yellow&rdquo;,&rdquo; brown&rdquo;);
$colors_serialized=serialize($colors);
Echo &ldquo;This is serialized array shown below<br>:&rsquo;$colors_serialized&rdquo;;
$colors_unserialized= unserialized($colors_serialized);
Echo &ldquo;This is the unserializrd array shown below:<br>&rdquo;;
Echo&rdquo; <pre>&rdquo;;
Echo print_r($colors_unserialized);
Echo &ldquo;</pre>&rdquo;;
?>
```

这段 PHP 代码产生如下所示。

**实际 PHP 输出**

如下所示的序列化数组:

' a:4:{ I:0；s:4:“红色”；I:1；s:6:“粉色”；I:2；s:5:“黄色”；I:3；s:5:“棕色”；}'

**未序列化数组**如下图:

数组

(

【0】=>红色

【1】=>粉色

【2】=>黄色

【3】=>棕色

)

}

我们创建一个数组，序列化它，显示序列化的数组，然后取消序列化，得到原始的 PHP 数组。然后，我们通过 print_r()函数输出数组。我们使用 pre 标签只是为了让数组更易读。

这就把我们带到了本文的结尾。

*如果您发现这篇 PHP 文章相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在这篇文章的评论部分提到它，我会回复你。*