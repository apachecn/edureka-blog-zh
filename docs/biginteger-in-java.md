# 如何用 Java 实现 BigInteger？

> 原文：<https://www.edureka.co/blog/biginteger-in-java/>

当原始数据类型帮不了你的时候，Java 有一些特殊的类来拯救你。当您处理无法包含在原始数据类型(如 int 和 long)中的大数时，就会出现这种情况。可以使用字符串数据类型来解决这个问题。但是，如果我们想对给定的数字进行算术运算，这种方法是不够的。在本帖中，我们将讨论如何借助[Java](https://www.edureka.co/blog/java-tutorial/)中的 BigInteger 来克服这个问题

本文将涉及以下几点:

*   [类和对象](#ClassesandObjects)
*   [BigInteger 类](#BigIntegerClass)
*   [构造者](#Constructors)
*   [big integer 类的方法](#MethodsofBigIntegerclass)

让我们从这篇文章开始吧，

## **Java 中的 big integer**

## **类和对象**

在开始使用 BigInteger 类之前，理解 [面向对象编程](https://www.edureka.co/blog/object-oriented-programming/) 的基础是很重要的。类和对象构成了 OOPs 的核心。这些是在处理支持 OOPs 的语言时经常使用的强大概念。所以。让我们浏览一下这些概念，并对它们的工作原理有一个简单的了解。

OOPs 背后的主要思想是代码模块化和代码可重用性。这些想法都是借助类和对象实现的。类是用户可以设置其实例的行为和属性的地方。您也可以将一个类视为属于该汽车的对象的原型。

**例如**

让我们考虑一个名为“Dog”的类。现在，如果我们想到一只狗，我们可以说所有的狗都有一些共同的属性，如颜色、腿、尾巴、耳朵等。以及走路、摇尾巴、吠叫等行为。在我们的类‘Dog’中，我们可以将所有这些公共属性写成属性，将行为写成方法。现在，这个类的每个实例都有相同的属性和行为。现在，我们可以创建任意多的对象，并使用类中提到的功能。这使得代码模块化和可重用。

类也被称为用户定义的数据类型，当我们试图实现的功能不能通过使用原始数据类型来实现时，就会用到类。BigInteger 类就是一个例子。让我们仔细研究一下这个例子。

让我们看看 Java 中这个 BigInteger 的下一点

## **大整数类**

至此，我们已经有了足够的类和对象的知识，可以开始使用 Java 提供的 BigInteger 类了。BigInteger 类是 Java.math 包的一部分，附带各种 [构造函数](https://www.edureka.co/blog/constructor-in-java/) 。当创建这个类的对象来存储大数字时，可以存储的数字没有上限。唯一的限制是可用的内存。

只有在不可避免的情况下才应该使用 BigInteger 类。因为与原始数据类型相比，它占用更多的内存，并且您不能使用各自的算术运算符进行算术运算，因为 Java 不支持运算符重载。

**申报**

```
BigInteger Big;
```

**初始化**

```
BigInteger Big2 = new BigInteger("124321098456719538751253254");
```

在下一节，我们将讨论这个类的构造函数和方法。

现在我们应该明白什么是构造函数，

## **Java 中的 BigInteger:构造函数**

让我们来看看 BigInteger 类提供的各种构造函数。可用的构造函数越多，创建 BigInteger 类对象的方法就越多。要记住的重要一点是，构造函数没有返回类型，它们不返回任何东西。

| **Sr 号** | **构造函数和参数** | **描述** |
| 1 | **大整数** (字节[] val) | 这个构造函数帮助将一个包含 BigInteger 的二进制补码二进制表示的字节数组转换成 BigInteger。 |
| 2 | **大整数**(int sign，byte[] magnitude) | 帮助将 大整数的符号-幅度表示转换成大整数。 |
| 3 | **big integer**(int bit length，int 确定性，[Random](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html)rnd) | 帮助构造一个随机生成的可能是质数的正整数，具有指定的位长。 |
| 4 | **大整数** ( [【字符串】【val】](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html) | 帮助将 BigInteger 的十进制字符串表示转换成 BigInteger。 |
| 5 | **大整数** ( [字符串【val，int radix】](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html) | 将指定基数的 BigInteger 的字符串表示形式转换为 BigInteger。 |

总共有 5 种类型的构造器，根据我们可用的情况和参数来使用。为了理解这个概念，我们将使用表中的第四个构造函数。

Java 文章中 BigInteger 的下一位是:

## **big integer 类的方法**

正如我们之前所讨论的，每个类都有不同的属性和方法，这些属性和方法是该类的所有实例所共有的。在 BigInteger 类的帮助下进行算术运算时，使用算术运算符是没有用的。因此，为了进行算术运算，我们需要使用 BigInteger 类方法。

| **方法** | **返回类型和值** | **描述** |
| abs( ) | 这个函数返回一个 BigInteger，其值是这个 BigInteger 的绝对值。 | 该函数有助于找到给定大整数的绝对值 |
| add(BigInteger val) | 此函数返回一个值为(this + val)的 BigInteger。val-要加到这个大整数上的值 | 帮助执行加法运算 |
| compareTo(BigInteger val) | 如果 BigInteger 在数值上小于 val，则返回-1，如果相等，则返回 0，如果大于 val，则返回 1。val- BigInteger，此 BigInteger 要与之进行比较。 | 将该大整数与指定的大整数进行比较 |
| divide(BigInteger val) | 此函数返回一个值为(this / val)的 BigInteger。val-big integer 要被除的值。 | 帮助用给定的 BigInteger 进行除法运算，如果除以 0 则抛出异常 |
| 等于( [)对象](https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html) x) | 当且仅当指定的对象是一个数值等于这个 BigInteger 的 BigInteger 时，这个函数返回 true 。x——与这个大整数进行比较的对象。 | 返回一个布尔值。如果指定对象是一个 BigInteger，其值在数值上等于此 BigInteger，则为 True。 |
| intValue( ) | 这个 BigInteger 转换成了 int 类型。 | 将这个 BigInteger 转换成 int。 |
| 多重(大整数 val) | 此函数返回一个值为(this * val)的 BigInteger。val-要与这个大整数相乘的值 | 帮助执行乘法运算 |
| 减去(BigInteger val) | 此函数返回一个值为(This–val)的 BigInteger。val-要从这个大整数中减去的值 | 帮助执行减法运算 |

上表中提到的方法是在处理 BigInteger 类时使用最多的方法。要查看 BigInteger 类提供的完整列表，请查看 Oracle 提供的官方 BigInteger 类[【docs】](https://docs.oracle.com/javase/7/docs/api/java/math/BigInteger.html#abs())。

**例子**

在理解了 OOPs 概念、BigInteger 类、它的构造函数和方法之后，现在让我们考虑一个例子并演示 BigInteger 类的用法。

让我们找出光到达离地球最近的星系所用的时间，即 2.4011019公里。

```

import java.math.BigInteger;
public class BiggInteger {
public static void main(String[] args) {
BigInteger Distance = new BigInteger("2401000000000000000000");
BigInteger SpeedofLight = new BigInteger("1080000000");
BigInteger Time = Distance.divide(SpeedofLight);
System.out.println("Time taken by light to reach the Andromeda Galaxy is " + Time + " hours");
}
}

```

**输出:**

过程结束，退出代码= 0

注意——上述案例仅作为示例。事实上，答案可能不同。 尝试不同的星系或恒星，并相应地编辑代码。

这样，我们就结束了这篇关于“Java 中的 BigInteger”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。