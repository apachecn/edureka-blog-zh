# Java 抽象——用 Java 中的抽象掌握 OOP

> 原文：<https://www.edureka.co/blog/java-abstraction/>

在之前的博客中，你学习了 Java 中的[继承](https://www.edureka.co/blog/inheritance-in-java/)。现在在这篇博客中，我们将了解[的另一个重要支柱，也就是 Java 抽象，它的主要功能是隐藏内部实现细节。](https://www.edureka.co/blog/object-oriented-programming/)

我将在本文中讨论以下主题:

*   [面向对象程序设计中的抽象](#Abstraction)
*   [什么是 Java 抽象？](#What-is-Java-Abstraction)
*   [抽象类](#AbstractClass)
*   [界面](#Interface)
*   [Java 中抽象的真实例子](#Reallifeexample)
*   [抽象 vs 封装](#AbstractionvsEncapsulation)

*你也可以浏览一下 [OOPs Concepts](https://www.edureka.co/blog/cheatsheets/java-oop-cheat-sheet/) 的录音，在录音中你可以通过例子详细理解主题。*

[//www.youtube.com/embed/7GwptabrYyk](//www.youtube.com/embed/7GwptabrYyk)

## 面向对象中的抽象

当我们谈论抽象时，软件语言就是抽象的一个例子。让我们举个例子，写一个声明如下-

*x = y+z；*

在上面的语句中，我们添加了存储在两个不同位置的两个变量，然后将结果存储在一个新的位置。那么，接下来会发生什么？你可能知道，有寄存器、指令集、程序计数器、存储单元等。，参与其中。当我们提到 Java 中的抽象时，我们谈论的是[面向对象编程(OOP)](https://www.edureka.co/blog/object-oriented-programming/) 中的抽象以及它是如何实现的。OOP 中抽象的概念始于类被构思的那一刻。抽象在软件和 OOP 中无处不在。

## 什么是 Java 抽象？

抽象不过是处理想法而不是事件的品质。它基本上处理的是隐藏内部细节，向用户展示本质的东西。

![Calling - Java Abstraction -Edureka](img/6654e6ce561b841fa4ec344fef917699.png)

如果你看看上面的 gif，你可以看到当你接到一个电话，我们得到一个选项，要么接电话，要么拒绝它。但实际上，有很多代码在后台运行。所以在这里，你不知道调用是如何产生的内部处理，这就是抽象的美妙之处。您可以通过两种方式实现抽象:

a)抽象类

b)接口

让我们更详细地理解这些概念。

## 抽象类

抽象类包含“Abstract”关键字。但这到底意味着什么呢？如果你将类抽象，它就不能被实例化，也就是说，你不能创建一个抽象类的对象。此外，抽象类可以包含抽象和具体的方法。

***注意:**使用一个抽象类可以实现 0-100%的抽象。*

要使用抽象类，你必须从基类继承它。这里，你必须为抽象方法提供实现，否则它将成为一个抽象类。

让我们看看抽象类的语法:

```
Abstract class Sports {   // abstract class sports
Abstract void jump();    // abstract method
}

```

## 连接

Java 中的接口是抽象方法和静态常量的集合。正如您可能知道的，在接口中，每个方法都是公共的和抽象的，但是它不包含任何构造函数。除了抽象，接口还有助于实现 Java 中的多重继承。 ***注意:**使用接口可以实现 100%的抽象。*

基本上，接口是一组具有空体的相关方法。让我们以一个形状的接口及其相关方法为例来理解接口。

```
public interface shape{
public void draw();
public double getArea();
}

```

这些方法需要出现在每个“形状”中，对吗？但是他们的工作会有所不同。

让我们假设你想画一个形状，比如圆形、正方形、长方形等等。你已经知道，每个形状都有自己的尺寸，如半径、高度和宽度。说我要画一个圆，计算它的面积。出于同样的考虑，我在上面的代码中创建了两个方法，即 draw()和 getArea()。现在，使用这些方法，我可以绘制任何形状，并通过实现其接口来计算面积。

现在，让我们看看如何实现这个接口的功能。为了实现这个接口，你的类的名字会改变为任何形状，比如说“圆形”。因此，为了实现类接口，我将使用' implement '关键字:

```
public class Circle implements Shape{ 
private double radius; 
public Circle(double r){ 
this.radius = r; 
} 
void draw(){ 
System.out.println("Drawing Circle"); 
} 
public double getArea(){ 
return Math.PI*this.radius*this.radius; 
} 
public double getRadius(){
 return this.radius; 
} 
}
public class Test{ 
public static void main (String args[]){
Shape c = new Circle(8);
c.draw(); 
System.out.println("Area="+c.getArea());
}
}

```

在上面的例子中，我为不同的方法指定了功能，并计算了圆的面积。这里，在实现一个接口时，它允许一个类对它提供的行为变得更加正式。你也可以创建另一个类，比如“Rectangle”类，它可以继承具有不同功能的相同接口“shape”。

## java 中抽象的实时例子

假设我们把运动作为一个界面。这里，实现将由名为“羽毛球”和“足球”的类提供。在真实的场景中，最终用户不会意识到实现类。因此，实现类的对象可以由工厂方法提供。工厂方法可用于根据某种标准创建实现类的对象。让我们实现同样的方法，创建一个名为 Sport.java 的接口。

```
public Interface Sport{
void play();
}
//Now, we will create class named "Badminton"
public class Badminton implements Sport {
@Override
public void play() {
System.out.println("Playing badminton");
}
}
//Next let's create our last class “Football”
public class Football implements Sport { 
@Override
public void play() {
System.out.println("Playing football");
}

```

最后一步是创建一个名为“SportInterface”的主类。

```
public SportInterface{
public static void main(String args[]){
// your code here
}
}

```

当您执行上述程序时，输出将如下所示:

```
Playing badminton
-------------------
Playing football

```

我希望你们清楚这个接口，以及如何使用它实现抽象。现在，让我们通过比较抽象和封装来结束本文。

## 抽象与封装

| **抽象** | **封装** |
| 解决设计层面的问题 | 解决实现层面的问题 |
| 用于隐藏不需要的数据并给出相关结果 | 封装意味着将代码和数据隐藏在一个单元中，以保护数据不受外界影响 |
| 外部布局–用于设计方面 | 内部布局–用于实施方面 |

我希望你理解了抽象和封装之间的区别。到此，我们的 Java 抽象博客就告一段落了。希望，你发现它信息丰富，有助于增加你的知识价值。如果你希望了解更多关于 Java 的知识，可以参考 [**Java 教程。**](https://www.edureka.co/blog/java-tutorial/)

*既然你已经理解了“什么是 Java 抽象”，那就来看看 Edureka 的 [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在“Java 抽象”博客的评论部分提到它，我们会尽快回复您。*