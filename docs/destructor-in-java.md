# Java 中析构函数有什么用？

> 原文：<https://www.edureka.co/blog/destructor-in-java/>

在 Java 中使用[类时，构造函数用于初始化类的实例。使用](https://www.edureka.co/blog/java-objects-and-classes/)[构造器](https://www.edureka.co/blog/constructor-in-java/)为对象分配内存，但是在对象生命周期结束并且不再使用该对象后，必须释放内存。这就是 [Java](https://www.edureka.co/java-j2ee-training-course) 中析构函数的用武之地。在本文中，我们将按照以下顺序学习 Java 中的析构函数:

*   什么是析构函数？
    *   [垃圾收集器](#garbage)
*   [构造函数和析构函数的区别](#difference)
*   [Java finalize()方法](#finalize)
*   [例子](#ex)

## **什么是析构函数？**

析构函数是一种特殊的[方法](https://www.edureka.co/blog/java-methods/)，一旦对象的生命周期结束，它就会被自动调用。调用析构函数来释放内存。调用析构函数时，将执行以下任务。

*   松开释放锁
*   关闭所有数据库连接或文件
*   释放所有网络资源
*   其他家务工作
*   恢复在对象生存期内分配的堆空间

Java 中的析构函数也称为终结器，是不确定的。内存的分配和释放由 Java 中的[垃圾收集器隐式处理。](https://www.edureka.co/blog/garbage-collection-in-java/)

Java 中的终结器必须隐式调用，因为它们的调用没有保证，不像 C#终结器那样在。净运行时间。

让我们来看看析构函数的关键属性:

*   不允许重载或继承
*   没有指定访问修饰符或参数
*   自动调用，没有来自用户的显式调用
*   用于类中，但不用于结构中
*   从最大派生类到最小派生类，类的顺序各不相同
*   当对象实例不再适合访问时也调用
*   用于释放非托管资源，而不是对象持有的托管资源

### **拾荒者**

垃圾收集器是一个运行在 [Java 虚拟机](https://www.edureka.co/blog/java-virtual-machine/)上的程序，通过删除不再使用或已经结束生命周期的对象来回收内存。当且仅当一个对象不可达时，称该对象有资格进行垃圾收集。

让我们试着理解 Java 中垃圾收集的工作原理:

垃圾收集主要是标记或识别不可达对象并删除它们以释放内存的过程。实现存在于 JVM 中，唯一的要求是它应该符合 JVM 规范。以下是 Java 中不同类型的垃圾收集器:

*   串行垃圾收集器
*   并行/吞吐量垃圾收集器
*   CMS 收集器
*   G1 收藏家

让我们来看看 Java 中垃圾收集的几个优点:

*   它会自动删除无法访问的未使用对象，以释放内存
*   垃圾收集使 Java 内存高效
*   不需要显式调用它，因为实现存在于 JVM 中
*   垃圾收集已经成为许多编程语言的重要和标准组件

让我们试着理解一下为什么 Java 中不使用析构函数。

## **构造函数 vs 析构函数:构造函数和析构函数的区别**

| **构造器** | **析构函数** |
| 构造函数用于初始化类的实例 | 析构函数用于删除或销毁不再使用的对象 |
| 当创建一个类的实例时，调用构造函数 | 当一个对象被销毁或释放时，析构函数被调用 |
| 存储器分配 | 释放内存 |
| 超载是可能的 | 不允许超载 |
| 他们被允许有争论 | 析构函数中不能传递任何参数 |

## **Java Finalize()方法**

对于任何开发人员来说，强制执行垃圾收集器都变得相当困难，但是有一个替代方法。我们可以用这个物体。finalize() 方法的工作方式与 Java 中的析构函数完全一样。

Object.finalize()方法在所有的 [Java 对象](https://www.edureka.co/blog/java-object/)中被继承。它不是一个析构函数，但用于确保或提供额外的安全性，以确保在程序关闭前关闭文件等外部资源的使用。您可以使用方法本身或 system . runfinalizersonexit(true)来呼叫它。

强烈建议不要使用 finalize()方法，因为它可能非常不安全，并且在某些情况下使用不当。

让我们举一个简单的例子来说明如何使用 finalize()来调用垃圾收集器。

```
public class A {
public void finalize() throws Throwable{
System.out.println("Object is destroyed by the Garbage Collector");
}
public static void main(String[] args) {

A test = new A();
test = null;
System.gc();
}
}

```

至此，我们已经了解了 Java 中的析构函数。我希望你清楚本教程中与你分享的所有内容。

*如果你发现这篇文章与“Java 中的析构函数”相关，请查看一下  Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训，这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

我们在这里帮助你踏上旅程的每一步，并为想成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种  [Java 框架](https://www.edureka.co/blog/java-frameworks/) ，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。

如果你遇到任何问题，请在“Java 析构函数”的评论区自由提问，我们的团队会很乐意回答。