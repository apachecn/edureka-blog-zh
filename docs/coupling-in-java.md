# Java 中的耦合是什么及其不同类型？

> 原文：<https://www.edureka.co/blog/coupling-in-java/>

Java 是一种面向对象的编程语言。当你使用 Java [类](https://www.edureka.co/blog/java-objects-and-classes/)和[对象](https://www.edureka.co/blog/java-object/)时，Java 中的耦合起着重要的作用。它基本上是指一个阶级对另一个阶级的了解程度。因此，在本文中，您将了解 java 中耦合的所有内容，它的各种类型以及示例。

本教程涵盖以下主题:

*   [Java 中的耦合](#coupling)
*   [联轴器类型](#types)
    *   [紧耦合](#tightcoupling)
    *   [松耦合](#loosecoupling)
*   [紧耦合和松耦合的区别](#tightcouplingvsloosecoupling)

我们开始吧。

## **![Java Logo](img/ba2e139ba09d4bcd6574457af0fe6049.png)Java 中的耦合**

一个对象可以被另一个对象使用的情况称为耦合。这是一个合作的过程，也是为彼此工作的过程。它仅仅意味着一个对象需要另一个对象来完成分配给它的任务。它基本上是一个对象被另一个对象使用，从而减少了模块之间的依赖性。如果一个类调用另一个类的逻辑，这就叫做协作。

## **联轴器类型**

Java 中的 Couling 进一步分为两种类型，即:

*   *   [紧耦合](#tight)
    *   [松耦合](#loose)

让我们来了解他们每一个人。

紧耦合:是指一组类高度依赖于彼此。当一个类承担了太多的责任，或者一个问题分散在许多类中而没有自己的类时，就会出现这种情况。 一个对象创建另一个对象供其使用的情况，称为**紧耦合**。父对象将知道更多关于子对象的信息，因此这两个对象被称为紧密耦合的。依赖因素和对象不能被其他任何人更改的事实帮助它实现了术语“紧密耦合”。

现在，让我用一个例子来解释这个概念。

**举例:** 假设你做了两个类。第一个类是一个叫做 Volume 的类，另一个类计算盒子的体积。在 Volume 类中进行的任何更改都会反映在 Box 类中。因此，这两个类是相互依赖的。这种情况特别被称为紧耦合。

下面显示的代码将帮助你理解紧耦合的实现过程。

**例 1:**

```
package tightcoupling;

class Volume {
      public static void main(String args[]) {
           Box b = new Box(15, 15, 15);
           System.out.println(b.volume);
      }
}

class Box {
      public int volume;
      Box(int length, int width, int height) {
           this.volume = length * width * height;
      }
}

```

**输出:**

`3375`

在上面的例子中，你可以看到这两个类是如何绑定在一起并作为一个团队工作的。这是 Java 中紧密耦合的一个简单例子。 描绘这个过程的另一个例子！

**例 2:**

```
package tightcoupling;

public class Edureka {
      public static void main(String args[]) {
           A a = new A();
           a.display();
      }
}

class A {
      B b;
      public A() {
            b = new B();
      }
      public void display() {
            System.out.println("A");
            b.display();
      }
}

class B {
       public B() {
       }
       public void display() {
             System.out.println("B");
        }
}

```

**输出:**

`A`

**松耦合:**当一个对象从外部获得要使用的对象时，我们称之为松耦合。换句话说，松散耦合意味着对象是独立的。松散耦合的代码减少了维护和工作量。这是紧耦合代码的缺点，而松耦合代码消除了这一缺点。让我们看看 Java 中松耦合的一些例子。

**例 1:**

```
package lc;

class Volume {
      public static void main(String args[]) {
           Box b = new Box(25, 25, 25);
           System.out.println(b.getVolume());
      }
}

final class Box {
       private int volume;
       Box(int length, int width, int height) {
             this.volume = length * width * height;
       }
       public int getVolume() {
             return volume;
       }
}

```

**输出:**

`15625`

**例二:**

```
package losecoupling;

import java.io.IOException;

public class Edureka {
      public static void main(String args[]) throws IOException {
           Show b = new B();
           Show c = new C();
           A a = new A(b);
           a.display();
           A a1 = new A(c);
           a1.display();
      }
}

interface Show {
      public void display();
}

class A {
      Show s;
      public A(Show s) {
           this.s = s;
      }
      public void display() {
           System.out.println("A");
           s.display();
       }
}

class B implements Show {
       public B() {
       }
       public void display() {
            System.out.println("B");
       }
}

class C implements Show {
       public C() {
       }
       public void display() {
            System.out.println("C");
       }
}

```

**输出:**

`A` `B` `A`

## **紧耦合和松耦合的区别**

| 紧密结合 | 松耦合 |
| 更加相互依赖 | 依赖性更小，测试能力更强 |
| 遵循程序的 GOF 原理与接口 | 不提供接口的概念 |
| 同步通信 | 异步通信 |
| 更多的协调，在两个对象之间交换一段代码/对象很容易 | 协调性差，不容易 |

至此，我们结束了这篇“Java 中的耦合”文章。我 希望你发现它内容丰富。如果你想了解更多，你也可以看看我们的其他 **[Java 博客](https://www.edureka.co/blog/what-is-java/) [s](https://www.edureka.co/blog/java-tutorial/)** 。

*现在您已经了解了 Java 的基础知识，请查看 Edureka 提供的  [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 中的耦合”博客的评论部分提到它，我们会尽快回复您。