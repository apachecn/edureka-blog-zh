# 如何在 Java 中实现匿名类

> 原文：<https://www.edureka.co/blog/anonymous-class-in-java/>

匿名类允许你写小代码，同时允许你声明和实例化类。这些类没有名字，当你想一次使用一个类的时候就用它。这是 Java 编程的一个重要方面。我们按以下顺序来了解一下什么是 Java 中的匿名类:

*   [声明匿名类](#declare)
*   [Java 中匿名类的语法](#syntax)
*   [在 Java 中创建匿名类的方法](#ways)
*   [普通类和匿名类的区别](#difference)

**声明匿名类**

通常我们创建一个类，即我们声明类，但是，匿名类是表达式，这意味着我们在另一个**表达式**中定义匿名类。简单来说，匿名内部类是一个没有名字的类，只创建一个对象。

![Anonymous-Class-In-Java](img/e854e7933748cd8aa9fcd30065f59e6d.png)

当我们必须用类或接口的重载方法创建对象的实例而不创建类的子类时，匿名类是有用的。

匿名可以通过两种方式创建:

*   类(也可以是抽象的)
*   连接

在匿名类中，我们可以声明如下:

*   字段
*   额外方法
*   实例初始值
*   本地类

## **Java 中匿名类的语法**

匿名类的语法就像构造函数一样，只是块中有一个类定义，如下面的代码片段所示:

```
// AnonymousClass = interface,abstract/concrete class.
AnonymousClass t = new AnonymousClass()
{
  // methods and fields
  public void someMethod()
  {
     //code goes here
   }  
}
```

我们来看看下面这个例子:

下面的例子， `HelloAnonymousClass` ，使用匿名类初始化语句中的局部变量 `greetSomeone` 但是，使用局部类初始化变量 `greetWorld` :

```
public class HelloAnonymousClass {
interface HelloWorld {
public void sayHello();
public void sayHelloTo(String someone);
}
public void sayHello() {
class GreetWorld implements HelloWorld {
String name = "world";
public void sayHello() {
sayHelloTo("world");
}
public void sayHelloTo(String someone) {
name = someone;
System.out.println("Hello " + name);
}
}
HelloWorld greetWorld = new GreetWorld();
HelloWorld greetSomeone = new HelloWorld() {
String name = "jon";
public void sayHello() {
sayHelloTo("Jon");
}
public void sayHelloTo(String someone) {
name = someone;
System.out.println("hola " + name);
}
};
greetWorld.sayHello();
greetSomeone.sayHelloTo("Doe");
}
public static void main(String... args) {
HelloAnonymousClass myApp = new HelloAnonymousClass();
myApp.sayHello();
}
}
```

正如我们已经看到的，匿名类是一个表达式，语法就像构造函数一样，只是在块中有一个类定义。考虑 greetSomeone 对象的实例化:

```
HelloWorld greetSomeone = new HelloWorld() {
String name = "jon";
public void sayHello() {
sayHelloTo("Jon");
}
public void sayHelloTo(String someone) {
name = someone;
System.out.println("hola " + name);
}
}
```

匿名类由以下内容组成:

*   新操作员。
*   它可以实现一个接口或扩展一个类。和上面的例子一样，它实现了接口。
*   它像普通类一样包含圆括号，以便将参数传递给构造函数。
*   包含方法声明的主体。不允许声明。

匿名类应该是语句的一部分。

在上面的例子中，匿名类表达式是由`greetSomeone`发起的语句的一部分。

## **在 Java 中创建匿名类的方法**

在 Java 中创建内部类有三种方法

*   **通过扩展类**

我们可以通过扩展其他类来创建一个匿名内部类，假设我们必须使用 thread 类来创建一个线程，我们可以创建一个匿名内部类，而不是创建一个单独的类。

```
//Program to illustrate Anonymous Inner class by extending other class
class AnonymousThreadClass {
public static void main(String[] args) {
//Anonymous Inner class that extends Thread class
Thread t = new Thread() {
public void run() {
System.out.println("Child!");
}
};
t.start();
System.out.println("Parent!");
}
}
```

**输出:**

`Parent!`

`Child!`

*   **通过实现接口**

我们还可以通过实现接口来创建一个匿名的内部类。现在，正如我们通过扩展 class 创建了一个内部类一样，我们也可以创建一个实现接口的类。

```
//Program to illustrate Anonymous Inner class by implementing interface
class AnonymousThreadClass
{
public static void main(String[] args)
{
//Anonymous Inner class that implements interface
Runnable r = new Runnable()
{
public void run()
{
System.out.println("Child!");
}
};
Thread t = new Thread(r);
t.start();
System.out.println("Parent!");
}
}
```

**输出:**

`Parent!`

`Child!`

*   **作为方法/构造函数的参数**

为了理解语法，让我们看看下面的例子:

```
//Program to illustrate Anonymous Inner class by argument
class AnonymousThreadClass {
public static void main(String[] args) {
//Anonymous class with constructor argument
Thread t = new Thread(new Runnable() {
public void run() {
System.out.println("Child!");
}
});
t.start();
System.out.println("Parent!");
}
}
```

**输出:**

`Parent!`

`Child!`

## **普通内部类和匿名内部类的区别**

*   通过使用普通的类，我们可以实现**多个接口**，但是使用匿名内部类，我们只能实现一个接口。

*   使用常规类，我们可以**扩展一个类**并且实现多个接口，但是使用匿名内部类，我们可以扩展一个类或者实现一个接口，但是不能同时扩展和实现两者。

*   使用匿名，我们**无法编写构造函数**,因为匿名内部类没有名字，而构造函数的名字应该与类名相同。

在本文中，我们看到了什么是匿名内部类，以及如何创建一个匿名内部类。我们学习了匿名内部类的语法，以及如何用 3 种方法创建匿名类，至此，我们结束了 Java 文章中的匿名类。查看 Edureka 的 [***Java 培训***](https://www.edureka.co/java-j2ee-training-course) 。

*有问题吗？在这篇文章的评论部分提到它，我们会尽快回复你。*