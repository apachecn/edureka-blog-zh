# 通过例子了解 Java 中的参数化构造函数

> 原文：<https://www.edureka.co/blog/parameterized-constructor-in-java/>

Java 是众多遵循 [面向对象方法](https://www.edureka.co/blog/object-oriented-programming/) 的编程语言之一。这意味着用 Java 编程时，我们拥有数据抽象、多态、继承等所有强大的特性。所有 OOP 特性的核心是类和对象的实现以及它们之间的交互。在本文中，我们将特别关注如何在 [Java](https://www.edureka.co/java-j2ee-training-course) 中使用参数化构造函数初始化对象。请注意，在继续学习构造函数之前，需要对[类和对象](https://www.edureka.co/blog/java-tutorial/#obj)有一个基本的了解。

*   [什么是构造函数？](#whatisconstructor)
*   [默认构造函数 vs 参数化构造函数](#defaultvsparameterized)
*   [传递对象作为参数](#objasarg)
*   [从参数化构造函数中调用默认构造函数](#call)
*   [构造函数重载](#overloading)

## **什么是构造函数？**

构造函数基本上是一种方法，当创建该类的对象(实例)时，会自动调用它。它用于初始化对象的数据成员。

```
public class Edureka{
Edureka(){ System.out.println("constructor is made");}
}

```

**构造函数的一些特性包括:**

1.  它与类名同名
2.  它没有返回类型

### **建造者类型**

1.  默认构造函数
2.  参数化构造函数

![types of constructors-parameterized constructor in java-edureka](img/7d083ed7677384773ef428728ddba5cb.png)

## **默认构造函数 vs 参数化构造函数**

**默认构造函数**——不接受任何参数的构造函数称为默认构造函数。没有必要在类定义中包含构造函数块。如果您没有显式地编写构造函数，编译器会自动为您插入一个。

Java 默认构造函数示例:

```
public class Edureka{
Edureka()
{ System.out.println("I am a constructor");}
public static void main(String args[]){
Edureka obj = new Edureka();
}
}

```

```
Output: I am a constructor
```

**参数化构造函数**–当一个构造函数接受特定数量的参数时，就称为参数化构造函数。用不同的值初始化类的数据成员。

举例说明参数化构造函数:

```
public class Edureka{
String studentName;
int studentAge;
//constructor
Edureka(String name, int age){
studentName = name;
studentAge = age;
}
void display(){
System.out.println(studentName+ " "+studentAge);
}
public static void main(String args[])
{
Edureka myObj = new Edureka("Manan" , 19);
myObj.display();
}
}

```

```
Output: Manan-19
```

在上面的例子中，我们向对象传递一个字符串和一个整数。然后，构造函数使用传递的值初始化 studentName 和 studentAge。显示方法然后给出所需的输出。

对于一个类的参数化构造函数，必须提供初始值作为参数，否则，编译器会报告一个错误。

![error-parameterized constructor in java- edureka](img/da0554888ba89728f91d404b409d3f45.png)

## **传递宾语作为论元**

我们也可以在创建一个类的其他实例时传递参数。这样，参数化构造函数满足了将一个对象的值复制到另一个对象的需要。

说明将对象作为参数传递的示例:

```
public class Edureka{
String studentName;
Edureka(String name){
studentName = name;
}
Edureka(Edureka myObj){
this.studentName = myObj.studentName;
}
void display(){
System.out.println("Student:" + studentName);
}
public static void main(String args[])
{
Edureka obj1 = new Edureka("Manan");
/* passing the object as an argument for the constructor 
* this will invoke the copy constructor
*/
Edureka obj2 = new Edureka(obj1);
System.out.println("Printing obj1 - ");
obj1.display();
System.out.println("Printing obj2 - ");
obj2.display();
}
}

```

```
Output:
```

```
Printing object 1 - Manan Printing object 2 - Manan
```

在上面的例子中，我们用一个字符串初始化 obj1。然后，我们在创建 obj2 时将 obj1 作为参数传递。最后，当我们使用 display 函数打印两个对象的 studentName 变量时，我们得到“Manan”。

## **从 Java 中的参数化构造函数调用默认构造函数**

有时需要从同一个类的另一个构造函数中调用默认的构造函数。[这个关键词](https://www.edureka.co/blog/this-keyword-in-java/)满足了这个目的。

说明从参数化构造函数调用默认构造函数的示例:

```
public class Edureka{
String studentName;
int studentAge;
String member;
Edureka(){
member = "YES";
}
Edureka(String name , int age){
this();
/* this is used for calling the default constructor
*from parameterized constructor
*/
studentName = name;
studentAge = age;
}
void display(){
System.out.println(studentName + " -" + studentAge+ "-"+ "Member" + member);
}
public static void main(String args[])
{
Edureka obj = new Edureka("Manan" , 21);
obj.display();
}
}

```

**输出:**Manan–21–成员是

在上面的例子中，当参数化的构造函数被调用时，它首先借助 this()关键字调用默认的构造函数。默认构造函数将“成员”变量初始化为“是”，然后继续执行参数化的构造函数。

## **构造函数重载**

构造函数像其他类一样支持方法重载。基于不同类型或数量的参数，将调用不同的构造函数。

举例说明构造函数重载:

```
public class Rectangle{
int length;
int breadth;
String color;
//constructor 1
Rectangle( int l , int b){
length = l;
breadth = b;
color = "Green";
}
//constructor 2
Rectangle(int l, int b, String c){
length = l;
breadth = b;
color = c;
}
void display(){
System.out.println("Length-" + length + "Breadth-" + breadth+ "Color" + color);
}
public static void main(String args[]){
Rectangle obj1 = new Rectangle(2,4);
Rectangle obj2 = new Rectangle(2,4,"Green");
obj1.display();
obj2.display();
}
}

```

```
Output: Length - 2 Breadth - 4 Color - Green Length - 2 Breadth - 4 Color - Red
```

现在你已经掌握了什么是构造函数以及如何使用它们，你离学习 Java 又近了一步。像构造函数这样的概念很简单，但是非常重要，因为它们涉及到类和对象。

**什么是 Java 中的构造函数| Java 构造函数的类型| Java 教程| Java 培训| Edureka**

[https://www.youtube.com/embed/XQ5NRKg8lXI](https://www.youtube.com/embed/XQ5NRKg8lXI)

要了解更多深入的话题和有趣的读物，请注册 Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)项目。欢迎访问我们的 [Java 教程博客](https://www.edureka.co/blog/what-is-java/)来开始你的学习。

*有问题吗？请在这篇“Java 中的参数化构造函数”文章的评论部分提到这一点，我们会尽快回复您，或者您也可以参加在 Amravati 举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-amravati)*