# Java 中的泛型是什么？–初学者指南

> 原文：<https://www.edureka.co/blog/generics-in-java/>

考虑一个例子，你必须列出一个地方的生物清单。不管是人，动物还是植物。重要的是有生命的东西。在这种情况下，你会把它们都归为“生物”，而不是归类。类似地，当你必须存储一些数据时，对你来说重要的是内容而不是数据类型，这就是你使用泛型的地方。Java 中的泛型是一种允许使用泛型类型和方法的语言特性。

下面是我将在本文中涉及的主题列表:

*   [Java 中什么是泛型？](#WhatisJavaGenerics?)
*   [为什么是 Java 泛型？](#WhyJavaGenerics?)
*   [Java 泛型的类型](#TypesofJavaGenerics)
*   [Java 中泛型的优势](#AdvantagesofJavaGenerics)

## **Java 中什么是泛型？**

***泛型*** 是一个术语，表示与泛型类型和方法的定义和使用相关的一组语言特性。Java 泛型方法不同于常规的数据类型和方法。在泛型之前，我们使用 [*集合*](https://www.edureka.co/blog/java-collections/) 来存储任何类型的对象，即*非泛型*。现在，泛型迫使 Java 程序员存储特定类型的对象。

现在你知道什么是 Java 中的泛型了，让我们进一步理解你为什么需要 Java 泛型。

## **为什么是 Java 泛型？**

如果你看一下 [Java 集合框架](https://www.edureka.co/blog/java-collections/)类，你会发现大多数类都采用 Object 类型的参数。基本上，在这种形式中，它们可以将任何 Java 类型作为参数，并返回相同的对象或参数。他们本质上是*异类*，即不是一个相似的类型。

![FrameworkHierarchy - Generics in Java - Edureka](img/c99f5f18969dc58bf69c593b1fbff596.png)

在 Java 应用中，有时输入的数据类型并不固定。输入可以是一个*整数*，一个*浮点*或者 *[Java 字符串](https://www.edureka.co/blog/java-string/)* 。为了将输入分配给正确数据类型的[变量](https://www.edureka.co/blog/java-tutorial/)，必须进行预先检查。在传统的方法中，在获取输入之后，检查输入的数据类型，然后将其分配给正确数据类型的变量。当使用这种逻辑时，代码长度和执行时间都增加了。为了避免这一点， ***泛型被引入*** 。当您使用泛型时，在编译时会自动检查代码中的参数，并在默认情况下设置数据类型。所以这就是你在 Java 中需要泛型概念的地方。

现在你已经对泛型有了一些了解，让我们继续前进，看看如何将泛型应用于源代码 的各种方式。

## **Java 泛型的类型**

在 Java 中，有 4 种不同的方法可以应用泛型，如下所示:

1.  泛型类型类
2.  通用接口
3.  通用方法
4.  通用构造函数

现在让我们深入了解泛型如何应用于类型类。

#### **1。通用类型类**

如果一个类声明了一个或多个类型变量，那么这个类就是泛型。这些变量类型被称为 [Java 类](https://www.edureka.co/blog/java-tutorial/#obj)的类型参数。让我们借助一个例子来理解这一点。在下面的例子中，我将创建一个具有一个属性 ***x*** 的类，属性的类型是一个对象。

```
class Genericclass{
private Object x;
public void set(Object x) { this.x = x; }
public Object get() { return x; }
}
```

这里，一旦用某个类型初始化了类，这个类就应该只用于那个特定的类型。例如，如果您希望该类的一个实例保存类型为“**字符串**”的值 ***x*** ，那么程序员应该设置并获取唯一的[字符串](https://www.edureka.co/blog/java-string/)类型。因为我已经将属性类型声明为 Object，所以没有办法实施这种限制。程序员可以设置任何对象，并可以从 ***get 方法*** 获得任何返回值类型，因为所有 Java 类型都是[对象](https://www.edureka.co/blog/java-tutorial/#obj)类的子类型。

为了实施这种类型的限制，我们可以使用如下的泛型:

```
class Genericclass<X> {
//T stands for "Type"
private T x;
public void set(T x) { this.x = x; }
public T get() { return x; }
}
```

现在你可以确信类不会被错误的类型误用。一个简单的例子*generic class*看起来如下所示:

```
Genericclass<String> instance = new Genericclass<String>();
instance.set("Edureka");
instance.set(10); //This will raise compile time error
```

这就是它的工作原理。这个类比对于界面来说也是正确的。让我们快速看一个例子来理解，泛型类型信息是如何在 java 的接口中使用的。

#### **2。通用接口**

Java 中的[接口](https://www.edureka.co/blog/java-collections/#interface)是指抽象数据类型。它们允许 [Java 集合](https://www.edureka.co/blog/java-collections/)独立于它们表示的细节被操纵。同样，它们在 [*面向对象编程*](https://www.edureka.co/blog/object-oriented-programming/) 语言中形成一个层级。让我们来理解如何将泛型应用于 Java 中的接口。

```
//Generic interface definition
interface GenericInterface<T1, T2>
{
T2 PerformExecution(T1 x);
T1 ReverseExecution(T2 x);
}

//A class implementing generic interface
class Genericclass implements GenericInterface<String, Integer>
{
public Integer PerformExecution(String x)
{
//execution code
}
public String ReverseExecution(Integer x)
{
//execution code
}
}
```

我希望您能够理解泛型是如何应用于类型类和接口的。现在让我们更深入地研究这篇文章，理解它对方法和构造函数有什么帮助。

#### **3。通用方法**

泛型方法与泛型类非常相似。它们之间的区别仅在于,*范围或类型信息仅在方法内部。*泛型方法引入了自己的类型参数。

我们用一个例子来理解这个。下面是一个通用方法的例子，它可以用来查找变量列表中所有类型参数的出现。

```
public static <T> int countAllOccurrences(T[] list, T element) {
int count = 0;
if (element == null) {
for ( T listElement : list )
if (listElement == null)
count++;
}
else {
for ( T listElement : list )
if (element.equals(listElement))
count++;
}
return count;
}
```

如果您在这个方法中传递一个由  字符串组成的列表进行搜索，它会很好地工作。但是如果你试图在字符串列表中寻找一个数字，就会给出编译时错误。

这个类比也类似于构造函数。让我们以泛型构造函数为例，了解它是如何工作的。

#### **4。通用构造函数**

**构造函数**是初始化新创建的对象的代码块。一个**构造函数**类似于 J **ava** 中的一个实例方法，但是它不是一个方法，因为它没有返回类型。在 J **ava** 代码中，构造函数与类同名，如下所示。现在我们举个例子，了解一下它的工作原理。

```
class Dimension<T>
{
private T length;
private T width;
private T height;

//Generic constructor
public Dimension(T length, T width, T height)
{
super();
this.length = length;
this.width = width;
this.height = height;
}
}
```

在上面的示例中，Dimension 类的构造函数具有类型信息。因此，您可以拥有一个仅包含单一类型所有属性的 dimension 实例。这就是你如何使用泛型类型构造函数。我希望你理解了 Java 中泛型的类型。

现在让我们更进一步，看看 Java 中泛型的优势。

## **Java 中泛型的优势**

**1。代码可重用性**

你可以一次编写一个策略或一个类或一个接口，并用于你需要的任何类型或任何方式。

**2。不需要个体类型铸造**

基本上，你每次都从 [ArrayList](https://www.edureka.co/blog/java-arraylist/) 中恢复信息，你需要对它进行类型转换。每次恢复任务中的类型转换是一个主要的头痛问题。为了根除这种方法，引入了泛型。

**3。实施非通用算法**

它还可以计算对各种类型安全的项起作用的算法。

这就是 Java 泛型的所有优点。至此，我们结束了这篇关于 Java 中泛型的文章。我希望您发现它提供了丰富的信息，并有助于您理解 Java 泛型。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。该课程旨在为您提供 Java 编程的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 中的泛型*”文章*的评论部分提到它，我们会尽快回复您。*