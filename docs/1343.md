# 如何在 Java 中最好地实现构造函数重载？

> 原文：<https://www.edureka.co/blog/constructor-overloading-in-java/>

Java 的出现席卷了编程界，主要原因是它带来了大量的特性。在本文中，我们将讨论在 [Java](https://www.edureka.co/blog/java-tutorial/) 中的构造函数重载。本文将讨论以下几点:

*   [什么是构造函数？](#WhatisaConstructors?)
*   [需要其他施工人员](#NeedforotherConstructors)
*   [本()引用](#this()reference)

那么让我们开始吧，

## **Java 中的构造函数重载**

## **什么是构造函数？**

构造函数是用来创建一个类的对象的代码块。每个类都有一个构造函数，不管是普通类还是抽象类。构造函数就像一个方法，但是没有返回类型。当一个类没有定义任何构造函数时，编译器会创建一个默认的构造函数。

**例题**

```
public class Student{
//no constructor
private String name;
private int age;
private String std;
// getters and setters
public void display(){
System.out.println(this.getName() + " " + this.getAge() + " " + this.getStd());
}
public static void main(String args[]){
// to use display method of Student class, create object of Student
Student student = new Student(); // as we have not defined any constructor, compiler creates default constructor. so that
student.display();
}
}

```

在上面的程序中，默认的构造函数是由编译器创建的，这样就创建了对象。有构造函数是必须的。

这就把我们带到了这篇文章的下一部分，关于 Java 中的构造函数重载。

## **需要其他施工人员**

在上面的例子中，学生对象只能用默认的构造函数来创建。其中 student 的所有其他属性都没有初始化。但是可以有某些其他的构造函数，用来初始化对象的状态。例如-T2

```
public class Student{
//attributes
String name;
int age;
String std;
//Constructors
public Student(String name){ // Constructor 1
this.name = name;
}
public Student(String name, String std){ // Constructor 2
this.name = name;
this.std = std;
}
public Student(String name, String std, int age){ // Constructor 3
this.name = name;
this.std = std;
this.age = age;
}
public void display(){
System.out.println(this.getName() + " " + this.getAge() + " " + this.getStd());
}
public static void main(String args[]){
Student stu1 = new Student("ABC");
stu1.display();
Student stu2 = new Student("DEF", "5-C");
stu2.display();
Student stu3 = new Student("GHI", "6-C", 12);
stu3.display();
}
}

```

这就把我们带到了本文的下一个 it 部分，关于 Java 中的构造函数重载。

## **本()引用**

这个()引用可以在参数化的构造函数中使用，隐式地调用默认的构造函数。请注意，这个()应该是构造函数中的第一条语句。

**例子**

```
public Student(){} // Constructor 4
public Student(String name, String std, int age){ // Constructor 3
this(); // will call the default constructor. *If it is not the first statement of constructor, ERROR will occur*
this.name = name;
this.std = std;
this.age = age;

```

**注**

*   递归构造函数调用在 java 中无效
*   如果我们已经定义了任何参数化的构造函数，那么编译器将不会创建默认的构造函数。反之亦然，如果我们不定义任何构造函数，编译器在编译期间默认创建默认构造函数(也称为无参数构造函数)
*   Java 中构造函数调用必须是构造函数的第一条语句

这样，我们就结束了这篇关于“Java 中的构造函数重载”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。