# Java 中的枚举是什么？初学者指南

> 原文：<https://www.edureka.co/blog/enumeration-in-java/>

枚举只不过是一组命名的常量，帮助定义自己的[数据类型](https://www.edureka.co/blog/data-types-in-java/)。当你能识别程序中变量的类型时，定义它们就变得容易了。所以，当你在编译时已经知道所有的值时，使用 ***枚举*** 。在本文中，我将借助例子告诉你如何在 [Java](https://www.edureka.co/blog/java-tutorial/) 中定义枚举。

在本文中，我将涉及以下主题:

*   [Java 中什么是枚举？](#WhatisEnumerationinJava?)
*   [在 Java 中定义枚举](#DefiningEnumerationinJava)
*   [枚举使用开关的情况](#Enumusingswitchcase)
*   [Values()和 ValueOf()方法](#Values()andValueOf()method)
*   [用构造函数、实例变量和方法进行枚举](#EnumerationwithConstructor,instancevariableandMethod)

我们开始吧！

## **Java 中什么是枚举？**

**枚举** 基本上是一个命名常数的列表。在 Java 中，它定义了一个类类型。它可以有[构造函数](https://www.edureka.co/blog/constructor-in-java/)，方法和[实例变量](https://www.edureka.co/blog/instance-variable-in-java/)。它是使用**枚举** 关键字创建的。默认情况下，每个枚举常数是[*public*](https://www.edureka.co/blog/access-modifiers-in-java/#Public_Access_Modifier)，*static*和  *final* 。即使枚举定义了一个类类型并有构造函数，你也不需要使用**新**变量来实例化一个  **枚举** 。枚举变量的使用和声明方式与基元变量相同。

现在让我们进入枚举的细节，理解它的语法和声明。

## **在 Java 中定义枚举**

枚举声明既可以在[类](https://www.edureka.co/blog/java-tutorial/#obj)之外完成，也可以在类内部完成。但是，我们不能在方法中声明 Enum。我们举一个小例子来理解它的声明。首先，我将告诉你如何在类外声明 enum。

### **1。在类外用 Java 声明枚举**

```
enum Directions{ // enum keyword is used instead of class keyword
NORTH, SOUTH, EAST, WEST;
}
public class enumDeclaration {
public static void main(String[] args) {
Directions d1 = Directions.EAST; // new keyword is not required to create a new object reference
System.out.println(d1);
}
}
```

**输出:**

```
EAST
```

### **2。在类**中用 Java 声明枚举

```
public class enumDeclaration {
enum Directions{
NORTH, SOUTH, EAST, WEST;
}
public static void main(String[] args) {
Directions d1 = Directions.EAST; // new keyword is not required to create a new object reference
System.out.println(d1);
}
}
```

**输出:**

```
EAST
```

枚举类型中的第一行应该是常数列表。然后，可以使用方法、[变量](https://www.edureka.co/blog/java-tutorial/#variables)和[构造函数](https://www.edureka.co/blog/constructor-in-java/)。基本上，enum 代表一组变量和常量。

***注:***

*   枚举基本上提高了类型安全性。
*   它可以不同地用于开关情况的例子。
*   枚举可以很容易地被遍历。
*   枚举有字段、构造函数和方法。
*   Enum 基本上实现了许多[接口](https://www.edureka.co/blog/java-interface/)，但是不能扩展任何类，因为它的 ***内部扩展了 Enum 类*** 。

现在，您已经知道如何在程序中声明和使用 enum，让我们了解如何用 switch case 语句实现它。

**使用 Switch 语句枚举**

枚举值也可以用来控制一个开关语句。所有 case 语句必须使用与 switch 语句相同的枚举中的常量。下面的例子演示了同样的情况。

```
package Edureka;
import java.util.*;
enum Directions {
NORTH,
SOUTH,
EAST,
WEST
}
public class Test1{
public static void main(String[] args) {
Directions d= Directions.SOUTH;
switch(d) { //The name of the enumertion constants are used without their enumeration
case NORTH: //only constants defined under enum Directions can be used
System.out.println("North direction");
break;
case SOUTH:
System.out.println("South direction");
break;
case EAST:
System.out.println("East directiion");
break;
case WEST:
System.out.println("West directiion");
break;
}
```

**输出:**

```
South Direction
```

我希望您理解了如何使用枚举实现 switch 语句。现在让我们进一步了解什么是 *Values()和 ValueOf( )* 方法以及它们之间的区别。

## **Values()和 ValueOf()方法**

**Values():** 当你创建一个 enum 时， [Java 编译器](https://www.edureka.co/blog/just-in-time-compiler/)在内部添加了 ***values()*** 方法。这个方法返回一个包含枚举的所有值的[数组](https://www.edureka.co/blog/java-array/)。

**语法:**

```
public static enum-type[ ] values()
```

**ValueOf():** 此方法用于返回枚举常数，其值等于调用此方法时作为参数传递的[字符串](https://www.edureka.co/blog/cheatsheets/java-string-cheat-sheet/)。

**语法:**

```
public static enum-type valueOf (String str)
```

现在让我们写一个程序来更详细地理解这些方法。

```
enum Colors{
black, red blue, pink, white
}
class Test {
public static void main(String args[]) {
Colors c;
System.out.println("All constants of enum type Colors are:");
Colors cArray[] = Colors.values(); //returns an array of constants of type Colors
for(Colors a : cArray) //using foreach loop
System.out.println(a);
c = Colors.valueOf("red");
System.out.println("I Like" + c);
}
}
```

**输出:**

```
All constants of enum type Colors are:
black
red
blue
pink
white
I Like red
```

这就是如何使用 ***Values()*** 方法返回包含该方法中所有枚举的数组，并使用 ***Valueof()*** 返回枚举常数。我希望你理解这个概念。

现在让我们更进一步，用[构造函数](https://www.edureka.co/blog/constructor-in-java/)、[实例变量](https://www.edureka.co/blog/instance-variable-in-java/)和方法来理解 Java 中枚举的实现。

## **用构造函数、实例变量和方法进行枚举**

基本上，枚举可以包含构造函数，并且在加载枚举类时为每个枚举常量单独执行。不仅如此，枚举还可以创建具体的方法。我们来写个代码，用构造函数，实例变量，方法来理解枚举实现。

```
enum Student {
mack(11), Birdie(10), Son(13), Victor(9);
private int age; //variable defined in enum Student
int getage { return age; } //method defined in enum Student
public Student(int age) //constructor defined in enum
{ this.age= age; }
}
class EnumDemo {
public static void main( String args[] ) {
Student S;
System.out.println("Age of Victor is " +Student.Victor.getage()+ "years");
}
}
```

**输出:**

```
Age of Victor is 9 years
```

这里，只要我们声明一个枚举变量( *Student S* )，构造函数就被调用一次，它用括号中指定的值初始化每个枚举常数的年龄参数。这就是它的工作原理。

这就把我们带到了关于 [Java](https://docs.oracle.com/javase/tutorial/) 中枚举的文章的结尾。我希望你发现它信息丰富。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 枚举”文章的评论部分提到它，我们会尽快回复您。