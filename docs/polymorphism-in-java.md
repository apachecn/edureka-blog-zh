# Java 中的多态性——如何开始 OOPs？

> 原文：<https://www.edureka.co/blog/polymorphism-in-java/>

在现实世界中，你可能见过变色龙按照自己的要求改变颜色。如果有人问，“它是怎么做到的？”，你可以简单的说“因为，它是多态的”。类似地，在编程世界中， [Java](https://www.edureka.co/blog/what-is-java/) 对象拥有相同的功能，其中每个对象可以采用多种形式。这个属性在 Java 中被称为 Poly morphism，其中 Poly 表示许多，morph 表示变化(或‘形式’)。在本文中，让我们讨论一下面向对象编程的关键概念，即 Java 中的多态性。

以下是本博客将要涉及的主题:

*   [OOP 中的多态性是什么？【T2](#WhatisPolymorphism)
*   [什么是多态 Java 例子？](#PolymorphisminJavawithExample)
*   Java 中多态性的类型
    *   [静态多态性](#StaticPolymorphism)
    *   [动态多态性](#DynamicPolymorphism)
*   [Java 中多态和继承有什么区别？](#polymorphismvsinheritance)
*   [Java 中多态性的其他特征](#OtherCharacteristicsofPolymorphisminJava)

You can go through this OOPs concepts video lecture where our [***Java Training***](https://www.edureka.co/java-j2ee-soa-training) expert is discussing each & every nitty gritties of the technology.[//www.youtube.com/embed/7GwptabrYyk](//www.youtube.com/embed/7GwptabrYyk)

## **OOP 中什么是多态性？**

**多态**在 OOP 中是一个实体 的 能力采取几种形式。换句话说，它指的是一个[对象](https://www.edureka.co/blog/java-tutorial/#obj)(或者一个对象的引用)接受不同形式的对象的能力。它允许向每个类发送一个公共的数据收集消息。多态鼓励称为“可扩展性”,这意味着一个对象或一个类可以扩展它的用途。

![Java Polymorphism example-Edureka](img/489280cad02a32da0e3c2d8ff06ddb30.png) 在上图中，你可以看到，*男子*只有一个，但他承担着多重角色，比如——他是孩子的爸爸，他是员工，销售人员等等。这就是所谓的 ***多态性*** 。

现在，让我们通过一个现实生活中的例子来理解这一点，并看看这个概念如何融入面向对象编程。

## 什么是多态 Java 例子？

让我们借助下面的问题陈述来理解这个(例子)。

*Consider a cell phone where you save your Contacts. Suppose a person has two contact numbers. For the ease of accessibility, your cellphone provides you the functionality where you can save two numbers under the same name.*

**类似地，在 [Java](https://www.edureka.co/blog/java-tutorial/) 中，一个对象只有一个，但它可以根据程序的上下文采用 多种形式。Su 假设你想写一个函数保存同一个人的两个联系号码，可以这样创建——**void create contact(String name，int number1，int number2)** 。**

**现在，你的联系人列表中没有必要每个人都有两个联系号码。他们中很少有人可能只有一个联系电话。在这种情况下，与其创建另一个不同名称的方法来保存联系人的一个号码，不如创建另一个相同名称的方法，即 **createContact()。**但是，不是取两个联系号码作为参数，而是只取一个联系号码作为参数即**void create contact(String name，int number1)** 。**

**![](img/0042c97bd18e4eacca1f8bb390df7c15.png)**

**在上图中可以看到， **createContact()** 方法有两个不同的定义。这里，要执行哪个定义取决于要传递的参数数量。如果传递了一个参数，那么在联系人下只保存一个联系人号码。但是，如果两个联系号码同时传递给这个方法，那么两个号码都将保存在同一个联系人下。*这也被称为**方法重载**。***

**现在让我们再举一个例子，深入理解多态性。**

***Suppose you went to a Shopping Centre (Allen Solly) near your home and bought a pair of jeans. A week later, while traveling to a nearby town, you spot another Shopping center. You walk into the shop and find a new variant of the same brand which you liked even more. But you decided to buy it from the shop near to your home. Once back home, you again went to the Shopping Center near your home to get those amazing pair of Jeans but couldn’t find it. Why? Because that was a specialty of the shop that was located in the neighboring town.***

****现在将这个概念与面向对象的语言如 Java 联系起来，假设你有一个名为 XJeans 的类，它包含一个名为 **jeans()** 的方法。用这种方法，你可以得到一条 Allen Solly 牛仔裤。对于邻镇的牛仔裤，还有另外一个阶层 **YJeans** 。XJeans 和 YJeans 类都扩展了父类 **ABCShoppingCenter** 。YJeans 类包含一个名为 **Jeans()** 的方法，使用该方法可以获得两种 jeans 变体。****

```
****classABCShoppingCenter {
public void jeans() {
System.out.println("Default AllenSolly Jeans");
}
}
class XJeans extends ABCShoppingCenter {
public void jeans() {
System.out.println("Default AllenSolly Jeans");
}
}
class YJeans extends ABCShoppingCenter { 
// This is overridden method
public void jeans() {
System.out.println("New variant of AllenSolly");
} 
}**** 
```

****因此，我们可以有一个单一的方法 jeans **()** ，它可以根据不同的子类来定义，而不是为每个新的变体创建不同的方法。因此，名为 **jeans()** 的方法有两个定义——一个只包含默认 jeans，另一个包含默认 jeans 和新变体。现在，调用哪个方法将取决于它所属的对象类型。如果您创建了**ABC****shopping center**类对象，那么将只有一条牛仔裤可用。但是如果你创建了 **YJeans** 类对象，扩展了 **ABCShoppingCenter** 类，那么你就可以拥有两种变体。*这也称为**方法覆盖**。* 因此，多态通过降低复杂性来增加代码的简单性和可读性。这使得 Java 中的多态性成为一个非常有用的概念，它也可以应用于现实世界的场景中。****

****我希望你对多态性的概念有所了解。现在，让我们继续这篇文章，理解 [Java](https://www.edureka.co/blog/top-10-reasons-to-learn-java/) 中不同类型的**多态性。******

## ******Java 中多态性的类型******

****Java 支持两种类型的多态性，它们如下:****

*****   静态多态性*   动态多态性****

#### ******静态多态******

****编译时解析的多态性被称为静态多态性。方法重载是编译时多态性的一个例子。****

### ******举例******

******方法重载** 是一个特性，允许一个类有两个或者更多的 **方法** 同名，但是有不同的参数列表 。在下面的例子中，你有同一个方法 add()的两个定义。因此，哪个 add()方法将被调用是由编译时的参数列表决定的。这就是这也被称为编译时多态性的原因。****

```
****class Calculator
{
int add(int x, int y)
{
return x+y;
}
int add(int x, int y, int z) 
{
return x+y+z;
}
}
public class Test
{
public static void main(String args[])
{
Calculator obj = new Calculator();
System.out.println(obj.add(100, 200));
System.out.println(obj.add(100, 200, 300));
}
}**** 
```

****静态多态就是这样工作的。现在，让我们来理解什么是 Java 中的动态[多态性。](https://www.edureka.co/blog/object-oriented-programming/#polymorphism)****

#### ******动态多态******

****动态多态性是一个调用被覆盖的方法的过程，在运行时解决，这就是为什么它被称为运行时多态性。方法重写是实现动态多态性的方法之一。在任何面向对象的编程语言中， **覆盖** 是一个特性，允许子类或子类提供一个 **方法** 的特定实现，该方法已经由它的一个超类或父类提供。****

******例子** 在下面的例子中，你有两个类 **MacBook** 和 **iPad** 。 *MacBook* 是父类 *iPad* 是子类。子类正在覆盖父类的方法 **myMethod()** 。在这里，我已经将子类对象分配给父类引用，以确定在运行时将调用哪个方法。决定调用哪个版本的方法的是对象的类型(而不是引用的类型)。****

```
****class MacBook{
public void myMethod(){
System.out.println("Overridden Method");
}
}
public class iPad extends MacBook{
public void myMethod(){
System.out.println("Overriding Method");
}
public static void main(String args[]){
MacBook obj = new iPad();
obj.myMethod();
}
}**** 
```

******输出:******

****压倒一切 方法****

****当你调用覆盖方法时，对象决定执行哪个方法。因此，这个决定是在运行时做出的。****

****我已经列出了几个更重要的例子。****

```
****MacBook obj = new MacBook();
obj.myMethod();
// This would call the myMethod() of parent class MacBook

iPad obj = new iPad();
obj.myMethod();
// This would call the myMethod() of child class iPad

MacBook obj = new iPad();
obj.myMethod();
// This would call the myMethod() of child class iPad**** 
```

****在第三个例子中，要执行子类的[方法](https://www.edureka.co/blog/java-tutorial/#obj)，因为需要执行的方法是由对象的类型决定的。因为对象属于子类，所以调用子类版本的 **myMethod()** 。****

### ******优势动态多态性******

*****   动态多态允许 Java 支持方法的覆盖，这是运行时多态的核心。*   它允许一个类指定对其所有派生方法通用的方法，同时允许子类定义一些或所有这些方法的具体实现。*   它还允许子类添加其特定的方法子类来定义相同的具体实现。****

****这都是关于不同的类型。现在让我们看看[多态性](https://www.edureka.co/blog/object-oriented-programming/#polymorphism)的其他一些重要特征。****

## ******Java 中多态和继承有什么区别？******

| **多态性** | **继承** |
| 多态性是指一个实体采取多种形式的能力 | 继承是指一个实体继承另一个实体的属性的能力 |
| Java 中的多态性是在方法级别上实现的 | Java 中的继承是在类的层次上实现的 |
| 多态支持编译时和运行时的方法调用 | 继承支持代码重用 |

## ******Java 中多态性的其他特征******

****除了 Java 中这两种主要类型的多态性，Java 编程语言中还有其他一些表现出多态性的特征，比如:****

*****   强迫*   运算符重载*   多态参数****

****让我们来讨论一下这些特征。****

*****   **威压******

****多态强制处理由编译器完成的隐式类型转换，以防止类型错误。一个典型的例子是整数和字符串的连接。****

```
****String str="string"=2;**** 
```

*****   **运算符重载******

****操作符或方法重载是指同一符号或操作符的多态特征，根据上下文有不同的含义(形式)。例如，加号(+)用于数学加法以及  字符串连接。在任一情况下，只有上下文(即参数类型)决定符号的解释。****

```
****String str = "2" + 2;
int sum = 2 + 2;
System.out.println(" str = %s
 sum = %d
", str, sum);**** 
```

******输出:******

```
****str = 22
sum = 4**** 
```

*****   **多态参数******

****参数多态性允许一个类中的参数或方法的名称与不同的类型相关联。在下面的例子中我已经将定义为一个  [*字符串*](https://www.edureka.co/blog/java-string/) 以及后来的一个  *整数* :****

```
****public class TextFile extends GenericFile{
private String content;
public String setContentDelimiter(){
int content = 100;
this.content = this.content + content;
}
}**** 
```

******注:** *D* *多态参数的声明会导致一个问题，称为变量隐藏* **。******

****这里，一个参数的局部声明总是覆盖另一个同名参数的全局声明。为了解决这个问题，通常建议使用全局引用，如关键字来指向局部上下文中的全局变量。****

****至此，我们关于 Java 文章中的多态性就告一段落了。希望，你发现它信息丰富，有助于增加你的知识价值。如果你希望学习更多关于 Java 的知识，可以参考[**Java 教程。**](https://www.edureka.co/blog/java-tutorial/)****

*****既然你已经理解了“什么是 Java 中的多态性”，那就来看看 Edureka 的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course)* *吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*****

*****有问题吗？请在“Java 中的多态性”博客的评论部分提到它，我们会尽快回复您。*****