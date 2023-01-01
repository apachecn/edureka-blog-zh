# 什么是 Java 静态方法？

> 原文：<https://www.edureka.co/blog/java-static-method/>

如果你曾经学过或者试图学过 Java，那么你就会知道 Java 静态方法是一个在某种程度上确实会造成混乱的概念。在本文中，我将试图揭开这个 Java 概念的神秘面纱。本文将涉及以下几点:

*   [Java 静态方法 vs 实例方法](#JavaStaticMethodvsInstanceMethod)
*   [Java 静态方法](#JavaStaticMethod)
*   [对静态方法的限制](#RestrictionsonStaticMethod)
*   [为什么 Java main 方法是静态的？](#WhyistheJavamainmethodstatic?)

那么让我们开始吧，

## **Java 静态方法 vs 实例方法**

**实例方法**

要求在调用一个类的对象之前创建它的方法被称为实例方法。要调用一个实例方法，我们必须创建一个类的对象，它在这个类中定义。

**样本:**

```
public void Sample(Str name)
{
//Execution Code....
}
// Return type should be something from the following int, float String even user defined data types will do.

```

**静态方法**

静态方法不依赖于需要创建的类的对象。你可以通过 **类名本身** 或者你所指代的类的对象来指代它们。

**样本:**

```
public static void Example(Str name) 
{ 
// code to be executed.... 
} 
//Ensure To static modifier in their declaration. 
//Return type just like the last example can be int, float, String or user defined data type.

```

让我们进入本文的下一个主题，

## **Java 静态方法**

在 Java 中，静态方法是属于一个类的方法，而不是一个类的实例。类的每个实例都可以访问该方法，但是在实例中定义的方法只能由该类成员访问。

**样品**

```
//Java Program to demonstrate the use of a static method.
class Student{
int rollno;
String name;
static String college = "ITS";
//static method to change the value of static variable
static void change(){
college = "BBDIT";
}
//constructor to initialize the variable
Student(int r, String n){
rollno = r;
name = n;
}
//method to display values
void display(){System.out.println(rollno+" "+name+" "+college);}
}
//Test class to create and display the values of object
public class TestStaticMethod{
public static void main(String args[]){
Student.change();//calling change method
//creating objects
Student s1 = new Student(111,"Karan");
Student s2 = new Student(222,"Aryan");
Student s3 = new Student(333,"Sonoo");
//calling display method
s1.display();
s2.display();
s3.display();
}
}

```

**输出**

111 Karan BBDIT

雅利安 222 号

索诺 333 号

让我们继续这篇文章的下一部分

## **限制**

有两个主要的限制。他们是:

1.  静态方法不能使用非静态数据成员或直接调用非静态方法。
2.  在静态上下文中不能使用 this 和 super。

让我们继续这篇文章的最后一点，

## **为什么 Java main 方法是静态的？**

是因为不要求对象调用静态方法。如果是非静态方法，JVM 首先创建一个对象，然后调用 main()方法，这将导致额外的内存分配问题。

我们就此结束了这篇文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论区提出来，我们会尽快回复你，或者你也可以参加我们在阿姆利则举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-amritsar)