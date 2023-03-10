# Java 中的实例变量:你需要知道的一切

> 原文：<https://www.edureka.co/blog/instance-variable-in-java/>

你们都很熟悉 Java 中变量的概念，这是 Java 职业生涯或最终 [认证](https://www.edureka.co/java-j2ee-soa-training) 不可或缺的。Java 为我们提供了访问三个 [变量](https://www.edureka.co/blog/java-tutorial/#variables) 的自由，即局部变量、类变量和实例变量。在这篇文章中，我将讨论 Java 中实例变量的实现。 以下是将要讨论的要点:

我们开始吧！

## **Java 中的实例变量是什么？**

Java 中的实例变量是非静态变量，定义在任何方法、[构造函数](https://www.edureka.co/blog/constructor-in-java/)或块之外的类中。该类的每个实例化对象都有该变量的单独副本或实例。一个实例变量属于一个类。

你一定想知道*实例*到底是什么？我来帮你简化一下。

当你创建一个类的新对象时，你就创建了一个实例。考虑一下，如果你有一个学生班，那么

```
class Student
{
String studentName;
int studentScore;
}
```

如果你创建两个学生对象，比如，

```
Student student1 = new Student();
Student student2 = new Student();
```

然后将会创建两个学生类的实例。

现在每个学生都有自己的名字和分数了，对吗？因此，存储在“studentName”和“studentScore”中的值会因不同的学生而异，它们被称为“变量”。就像你看到的，这些变量在每个实例中都有自己的值，在 Java 中它们被称为实例变量。

现在你已经理解了实例变量的含义，让我们向前迈进一步。

我将列举实例变量的特性，这将有助于你轻松地在 java 代码中使用它们。

## **实例变量的特性？**

一个实例变量的寿命取决于一个[对象](https://www.edureka.co/blog/java-tutorial/#obj)的寿命，也就是说，当对象被创建时，一个实例变量也被创建，当对象被销毁时，同样的情况也会发生。

*   实例变量只能通过创建对象来使用
*   每个对象都有自己的实例变量副本
*   实例变量的初始化不是强制性的。默认值为零
*   声明是在类之外的任何方法中完成的，[构造函数](https://www.edureka.co/blog/constructor-in-java/)或 或
*   当一个类中的不同方法必须知道变量时，使用实例变量
*   [访问修饰符](https://www.edureka.co/blog/access-modifiers-in-java/)可以赋给实例变量

在获得理论知识之后，你可能正在思考如何在 Java 中实现实例变量！让我们在下一个话题中理解这一点。

## **如何在 Java 中实现实例变量？**

在 [Java](https://www.edureka.co/blog/java-tutorial/) 中实现实例变量相当容易。我写了一个简单的代码，可以帮助你掌握技术用法。

下面是详细代码:

```

package Edureka;

import java.util.Scanner;

public class Student
{

public String name;

private int marks;

public Student (String stuName) {
name = stuName;
}
public void setMarks(int stuMar) {
marks = stuMar;
}

// This method prints the student details.
public void printStu() {
System.out.println("Name: " + name );
System.out.println("Marks:" + marks);
}

public static void main(String args[]) {
Student StuOne = new Student("Ross");
Student StuTwo = new Student("Rachel");
Student StuThree = new Student("Phoebe");

StuOne.setMarks(98);
StuTwo.setMarks(89);
StuThree.setMarks(90);

StuOne.printStu();
StuTwo.printStu();
StuThree.printStu();

}
}

```

**输出:**

姓名:罗斯 分数:98 姓名:瑞秋 分数:89 姓名:菲比 分数:90

**说明:**

在上面的代码中，你可以看到我已经创建了三个实例变量，即' StuOne '，' StuTwo '，' StuThree '。 同样，你可以根据自己的需求创建任意多的[变量](https://www.edureka.co/blog/java-tutorial/#variables)。 现在，随着我们进一步积累关于实例变量的事实，让我也向你解释一下实例变量和类变量之间的区别！

## **实例变量和类变量的区别**

为了澄清差异，我记下了几点，这将有助于你消除两者之间的任何歧义。

| **实例变量** | **类变量** |
| 每个对象都有自己的实例变量副本，因此通过一个对象对这些变量所做的更改不会反映在另一个对象中。 | 类变量是一个类的所有对象所共有的，如果通过 object 对这些变量进行了任何更改，它也会在其他对象中反映出来。 |
| 实例变量声明时没有 *静态* 关键字。 | 类变量用关键字 *静态* 声明 |
| 实例变量只能通过对象引用使用。 | 类变量可以通过类名或对象引用来使用。 |

至此，我们已经到达了博客的末尾。我希望这篇文章的内容对你有益。我们将在接下来的博客中继续探索 Java 世界。敬请期待！

*既然你已经了解了**什么是 Java 中的实例变量* *，那就来看看 Edureka 的* [***Java 培训***](https://www.edureka.co/java-j2ee-training-course)*吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。*

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

*如果你希望学习更多关于 Java 的知识，可以参考* [***Java 教程。***](https://www.edureka.co/blog/java-tutorial/)

*有问题吗？请在这个*“[*Java 实例变量*](https://docs.google.com/document/d/1Vm9Gad8kMZl0rsreBFkzqUGc6bGkdzYG8d5Z6Wqgggs/edit?ts=5d136a8c#heading=h.gjdgxs) *”博客的评论区提出来，我们会尽快回复您，或者您也可以参加我们在望加锡的 [Java 培训](https://www.edureka.co/java-j2ee-training-course-makassar)..*