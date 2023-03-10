# 什么是 Java 中的虚函数？

> 原文：<https://www.edureka.co/blog/virtual-function-in-java/>

Java 是一种面向对象的编程语言，它支持多态、继承、抽象等概念。这些 OOPs 概念围绕着[类](https://www.edureka.co/blog/java-objects-and-classes/)、[对象](https://www.edureka.co/blog/java-object/)和成员函数。虚函数就是这样一个有助于运行时多态性的概念。在这个博客中，我们将学习 [java](https://www.edureka.co/java-j2ee-training-course) 中的虚函数。本文讨论了以下主题。

*   [什么是 Java 中的虚函数？](#virtual)
*   [虚拟功能示例](#example)
*   [带接口的虚函数](#interface)
*   [纯虚函数](#pure)
*   [运行时多态性](#polymorphism)
*   [点记](#ptr)

## **什么是 Java 中的虚函数？**

虚拟函数的行为可以用同名的继承类函数覆盖。它基本上是在基类中定义的，并在继承的类中被重写。

Java 中的虚函数应该在[派生类](https://www.edureka.co/blog/inheritance-in-java/)中定义。我们可以通过使用基类的引用或指针引用派生类的对象来调用虚函数。

默认情况下，Java 中的每个非静态方法都是虚方法。Java 没有类似于 [C++](https://www.edureka.co/blog/object-oriented-programming-in-cpp/) 的虚拟关键字，但是我们可以定义它们，并将其用于运行时多态性等概念。

## **虚函数示例**

让我们看一个例子来理解如何在 Java 中使用虚函数。

```
class Vehicle{
void make(){
System.out.println("heavy duty");
}
}
public class Trucks extends Vehicle{
void make(){
System.out.println("Transport vehicle for heavy duty");
}
public static void main(String args[]){
Vehicle ob1 = new Trucks();
ob1.make();
}
}

```

```
Output: Transport vehicle for heavy duty
```

除了 [final](https://www.edureka.co/blog/final-finally-and-finalize-in-java/) 和 [private methods](https://www.edureka.co/blog/access-modifiers-in-java/) 之外，Java 中的每一个非静态方法都是虚函数。不能用于多态性的方法不被认为是虚函数。

静态函数不被认为是虚函数，因为静态方法被绑定到类本身。所以我们不能从对象名或类中为[多态](https://www.edureka.co/blog/polymorphism-in-java/)调用静态方法。即使我们覆盖了静态方法，它也不会与多态的概念产生共鸣。

### **带接口的虚函数**

所有的 Java 接口都是虚拟的，它们依赖于实现类来提供方法实现。执行的代码是在运行时选择的。为了更好地理解，这里有一个简单的例子。

```
interface Car{
void applyBrakes();
}
interface Audi implements Car{
void applyBrakes(){
System.out.println("breaks Applied");
}
}

```

这里 applyBreaks()是虚拟的，因为接口中的函数被设计为被重写。

### **纯虚函数**

纯虚函数是我们没有实现的虚函数。Java 中的一个抽象方法可以认为是一个纯虚函数。让我们举个例子来更好地理解这一点。

```
abstract class Dog{
final void bark(){
System.out.println("woof");
}
abstract void jump(); //this is a pure virtual function
}
class MyDog extends Dog{
void jump(){
System.out.println("Jumps in the air");
}
}
public class Runner{
public static void main(String args[]){
Dog ob1 = new MyDog();
ob1.jump();
}
}

```

```
Output: Jumps in the air
```

这就是虚函数如何与抽象类一起使用。

## **运行期多态性**

运行时多态性是指对被覆盖方法的调用在运行时被解析，而不是在编译时被解析。重写的方法通过基类的引用变量调用。

```
class Edureka{
public void show(){
System.out.println("welcome to edureka");
}
}
class Course extends Edureka{
public void show(){
System.out.println("Java Certification Program");
}
public static void main(String args[]){
Edureka ob1 = new Course();
ob1.show();
}
}

```

```
Output: Java Certification Course
```

## **点记**

*   对于 Java 中的虚函数，不需要显式声明。它是我们在基类中拥有的任何一个[函数](https://www.edureka.co/blog/java-methods/)，并在派生类中用相同的名字重新定义。

*   基类指针可以用来引用派生类的对象。

*   在程序执行期间，基类指针用于调用派生类函数。

这就把我们带到了本文的结尾，我们已经了解了 Java 中的虚函数。我希望你清楚本教程中与你分享的所有内容。

*如果你发现这篇文章与“Java 中的虚函数”相关，请查看一下  Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训，这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

我们在这里帮助你踏上旅程的每一步，并为想成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种  [Java 框架](https://www.edureka.co/blog/java-frameworks/) ，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。

如果您遇到任何问题，请在“Java 中的虚函数”的评论区提出您的所有问题，我们的团队将很乐意回答。