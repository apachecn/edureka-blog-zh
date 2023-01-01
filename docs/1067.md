# Java 中的这个关键字——你所需要知道的

> 原文：<https://www.edureka.co/blog/this-keyword-in-java/>

**这个**是一个关键字，表示方法或构造函数中的一个对象。它基本上是用来消除同名类属性和参数之间的混淆。在这篇文章中，我会告诉你 ***这个*** 关键字*在 [Java](https://www.edureka.co/blog/java-tutorial/)* 中的各个方面和用途。

以下是我将在本文中涉及的主题:

*   [Java 中的**这个**关键字是什么？](#WhatisthiskeywordinJava?)
*   [为什么在 Java 中使用**这个**关键字？](#WhyusethiskeywordinJava?)
*   **该关键字在 Java 中的使用**
    *   [与字段](#Usedwithafield)一起使用
    *   [用于调用一个构造函数](#Usedtoinvokeaconstructor)
    *   [用于返回当前类的实例](#Usedtoreturnthecurrentclassinstance)
    *   [用作方法参数](#Usedasamethodparameter)
    *   [用于调用当前类的方法](#Usedtoinvokeacurrentclassmethod)
    *   [用作构造函数调用中的参数](#Usedasanargumentintheconstructorcall)
*   [重要因素**本**关键词](#Importantfactorsofthiskeyword)

那么，我们开始吧！

## **这个关键字在 Java 里是什么？**

**这个**关键字在 [Java](https://www.edureka.co/blog/what-is-java/) 中表示一个类的当前[实例。它主要用于访问同一个类的其他成员。借助 ***这个*** 关键字，可以访问类内同一类的方法、字段和](https://www.edureka.co/blog/java-tutorial/#obj)[构造函数](https://www.edureka.co/blog/constructor-in-java/)。

现在，我们再进一步，了解一下 ***这个*** 关键字在 Java 中的需求是什么。

## **为什么在 Java 中使用这个关键字？**

**使用这个关键字** 的主要目的是区分类的形参[和数据成员](https://www.edureka.co/blog/java-tutorial/#variables)。如果在这种情况下，类的形参和数据成员是相同的，那么就会导致歧义。所以，为了区分形参和类的数据成员，类的数据成员前面必须有" **this** "关键字。

基本上，这个关键词可以有两种用法。

1.  `*this. *`
2.  `*this()*`

### **1。这个。**

它可以用来区分类的[变量和方法或构造函数的形参。不仅如此，它总是指向当前的类对象。**这个**关键字的语法如下所示:](https://www.edureka.co/blog/java-tutorial/#variables)

**语法**

```
this.data member of the current class
```

**注意:** *如果有任何变量前面有**“this”、**，那么 JVM 会将该变量视为类变量*。

### **2。本()**

它可以用来调用一个[构造函数](https://www.edureka.co/blog/constructor-in-java/)到另一个构造函数中，而不需要为同一个类多次创建对象。

**语法**

```
this(); // call no parametrized or default constructor
this(value1,value2,.....) //call parametrized constructor
```

既然你已经知道了什么是 ***这个*** 关键字以及为什么需要它，那就让我们深入到这篇文章中，了解一下 ***这个*** 关键字可以用在 [Java](https://docs.oracle.com/javase/tutorial/) 中的各个方面。

## **该关键字的用途**

关键字在 Java 中有 6 种用法。它们如下:

1.  [与字段](#Usedwithafield)一起使用
2.  [用于调用一个构造函数](#Usedtoinvokeaconstructor)
3.  [用于返回当前的类实例](#Usedtoreturnthecurrentclassinstance)
4.  [用作方法参数](#Usedasamethodparameter)
5.  [用于调用当前类的方法](#Usedtoinvokeacurrentclassmethod)
6.  [在构造函数调用中用作参数](#Usedasanargumentintheconstructorcall)

现在，让我们深入了解每种方法的细节。

**1。该关键字可用于字段/变量隐藏**

***这个**关键词*在**变量隐藏**中可以很有帮助。这里，您不能创建两个同名的 i [实例/局部变量](https://www.edureka.co/blog/java-tutorial/#variables)。但是，可以创建一个同名的实例变量和一个同名的局部变量。在这种情况下，局部变量将能够隐藏实例变量。这叫做**变量隐藏**。现在，让我们借助一个例子来更详细地理解这一点。

```
package Edureka;
import java.util.*;
public class field {
int j, n;
// Parameterized constructor
Test(int j, int n)
{
this.j = j;
this.n = n;
}
void display()
{
//Displaying value of variables j and n
System.out.println("j = " + j + " n = " + n);
}
public static void main(String[] args) {
field obj = new field(27, 01);
obj.display();
}
}
```

**输出:**

```
j = 27 n = 01 
```

在上面的例子中，形式参数和实例变量是相同的。因此，为了区分这些变量，我使用了 ***t** **his*** 关键字来输出局部变量。所以这都是关于隐藏变量的。

现在让我们看看如何使用 Java 中的关键字来调用构造函数。

## **2。这个关键字可以用来调用一个构造函数**

***这个()构造函数调用*** 可以用来调用当前类的构造函数。它还可以用来重用构造函数。您也可以将这种技术称为**构造函数链接**。我们举个小例子，了解一下 *this()* 是怎么用的。

```
package Edureka;
import java.util.*;
public class Example {
{
int j, n;

//Default constructor
Example()
{
this(27, 01);
System.out.println("Inside default constructor n");
}

//Parameterized constructor
Example(int j, int n)
{
this.j = j;
this.n = n;
System.out.println("Inside parameterized constructor");
}

public static void main(String[] args)
{
Example obj = new Example();
}
}
```

**输出:**

```
Inside parameterized constructor
Inside  default constructor
```

在上面的例子中，你可以看到“ **this** 关键字用于调用同一个[类](https://www.edureka.co/blog/object-oriented-programming/)中的一个重载构造函数。

## **3。这个关键字可以用来返回当前的类实例**

在这里，你可以返回 ***这个*** 关键字作为语句的从方法。在这种情况下，方法的返回类型必须是类类型。让我们借助一个例子来理解这一点。

```
public class Edureka {
int j, int n;
//Default constructor
Edureka(){
j = 100;
n = 200;
}
//Method that returns current class instance
Edureka get() {
return this;
}
//Displaying value of variables j and n
void display() {
System.out.println("j = " + j + " n = " + n);
}
public static void main(String[] args) {
Edureka obj = new Edureka();
obj.get().display();
}
}
```

**输出:**

```
j = 100, n = 200 
```

## **4。该关键字可用作方法参数**

***这个*** 关键字可以在方法内部使用，以便从同一个类中调用另一个方法。下面的例子演示了同样的情况。

```
public class Edureka {
int j, n;
// Default constructor
Edureka()
{
j = 100;
n = 200;
}
// Method that receives 'this' keyword as parameter
void display(Edureka obj) {
System.out.println("j = " + j + " n = " + n);
}
// Method that returns current class instance
void get()
{
display(this);
}
public static void main(String[] args) {
Edureka obj = new Edureka();
obj.get();
}
}
```

**输出:**

```
 j = 100, n = 200 
```

**5。这个关键字用作当前类的方法**

***这个*** 关键字可以用来调用当前类的方法。让我们借助一个例子来理解这一点。

```
pubic class Edureka {
void display(){
//calling fuction show()
this.show();
System.out.println("Inside display function");
}
void show() {
System.out.println("Inside show funcion");
}
public static void main(String args[]) {
Edureka j = new Edureka();
j.display();
}
}
```

**输出:**

```
Inside show funcion
Inside display function
```

## **6。该关键字在构造函数调用**中用作参数

你也可以在构造函数中传递 ***这个*** 关键字。如果你不得不在多个类中使用一个[对象](https://www.edureka.co/blog/java-tutorial/#obj)，这是很有用的。现在我们借助一个例子来理解同样的道理。

```
public class Y{
X obj;

// Parameterized constructor with object of X
// as a parameter
Y(X obj) {
this.obj = obj;
// calling display method of class X
obj.display();
}
}
class X{
int x = 45;
// Default Contructor that create a object of Y
// with passing this as an argument in the
// constructor
X(){
Y obj = new Y(this);
}
// method to show value of x
void display(){
System.out.println("Value of x in Class X : " + x);
}

public static void main(String[] args) {
X obj = new X();
}
}
```

**输出** :

```
Value of x in Class X : 45
```

所以，这就是你如何在构造函数调用中使用 ***这个*** 关键字作为参数。以上就是关于 ***这个*** 关键字在 Java 中的各种用法。现在我们来看看使用*这个关键词*的一些重要因素。

## **该关键字的重要因素:**

1.  你不能在[静态方法](https://www.edureka.co/blog/constructor-in-java/#methodvsconstructor)和静态初始化块中使用 super 和 ***这个*** 关键字，即使你引用的是静态成员。

2.  只能在构造函数内部调用 ***super()*** 和 ***this()*** 调用语句，并且必须是构造函数中的第一条语句。

这就把我们带到了文章的最后，关于 ***这个 Java 中的*** 关键词。我希望你发现它信息丰富。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的这个关键字”文章的评论部分提到它，我们会尽快回复您。