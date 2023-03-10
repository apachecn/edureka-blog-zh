# Java 中的 Comparable:关于 Comparable & Comparator 接口您需要知道的一切

> 原文：<https://www.edureka.co/blog/comparable-in-java/>

在 [Java 编程语言](https://www.edureka.co/blog/java-tutorial/)中，接口用于指定类必须实现的行为。Java world 为我们提供了两个这样的接口 Comparable 和 Comparator！Java 中的 Comparable 用于对自然排序的对象进行排序，Comparator 用于对不同对象的属性进行排序。让我们通过本文的媒介来了解这些接口。

I have covered the following pointers which demonstrate comparable and comparator in Java:

*   [Java 有什么可比性？](#WhatiscomparableinJava?)
*   [如何使用 compareTo 方法？](#HowtousethecompareTomethod?)
*   [Java 可比示例](#Javacomparableexample)
*   [Java 中的比较器是什么？](#WhatiscomparatorinJava?)
*   [如何实现比较器？](#Howtoimplementacomparator?)
*   [Java 中的可比 v/s 比较器](#Comparablev/sComparatorinJava)

既然我们清楚了我们的议程，让我们开始吧！

## **Java 有什么可比性？**

顾名思义， **Comparable** 是一个[接口](https://www.edureka.co/blog/java-interface/)，它定义了将一个对象与同类型的其他对象进行比较的方法。它有助于对具有自我排序倾向的对象进行排序，即对象必须知道如何对自己进行排序。**例如:**卷号，年龄，工资。这个接口在 *java.lang 包*中，它只包含一个方法，即 *compareTo()。* Comparable 本身不能对[对象](https://www.edureka.co/blog/java-tutorial/#obj)进行排序，但是接口定义了一个负责排序的方法 *int compareTo()* 。

此外，你一定在想什么是 compareTo 方法？好吧，让我解释给你听！

## **什么是 compareTo 方法，如何使用？**

这个方法用来比较给定对象和当前对象。方法返回一个整数值。该值可以是正数、负数或零。所以现在我们已经熟知了 Java 中 Comparable [接口](https://www.edureka.co/blog/java-interface/)和 **compareTo** 方法的理论知识。

让我们开始理解实现过程。首先，我们来看看如何实现 Comparable。

## **Java 可比示例**

下面的代码描述了 Java 中 comparable 的用法。

```
public class Student implements Comparable {
private String name;
private int age;
public Student(String name, int age) {
this.name = name;
this.age = age;
}
public int getAge() {
return this.age;
}
public String getName() {
return this.name;
}
@Override
public String toString() {
return "";
}
@Override
public int compareTo(Student per) {
if(this.age == per.age)
return 0;
else
return this.age > per.age ? 1 : -1;
}

public static void main(String[] args) {
Person e1 = new Person("Adam", 45);
Person e2 = new Person("Steve", 60);
int retval = e1.compareTo(e2);

switch(retval) {
case -1: {
System.out.println("The " + e2.getName() + " is older!");
break;
}

case 1: {
System.out.println("The " + e1.getName() + " is older!");
break;
}

default:
System.out.println("The two persons are of the same age!");

}
}
}
```

在上面的例子中，我创建了一个包含姓名和年龄两个字段的班级学生。Class Student 正在实现 Comparable 接口并覆盖 compareTo 方法。该方法根据年龄对学生类的[实例](https://www.edureka.co/blog/instance-variable-in-java/)进行排序。

现在我已经介绍了 Java 中的 Comparable，接下来我将讨论另一个接口，即 [Java](https://www.edureka.co/blog/what-is-java/) 中的 Comparator。让我们转到理解 Java 中的比较器！

## **Java 中的比较器是什么？**

比较器接口用于对特定类的对象进行排序。这个接口可以在 java.util 包中找到。它包含两种方法；

*   比较(对象 obj1，对象 obj2)
*   等于(对象元素)。

第一个方法，`compare(Object obj1,Object obj2)`比较它的两个输入参数并显示输出。它返回负整数、零或正整数，以说明第一个参数是小于、等于还是大于第二个参数。

第二种方法，`equals(Object element),`需要一个对象作为参数，并显示输入对象是否等于比较器。只有当提到的对象也是比较器时，该方法才会返回 true。顺序与比较器的顺序相同。

简要了解了 Java 中的 Comparator 之后，是时候向前迈进一步了。让我给你看一个用 Java 描述 Comparator 的例子。

## **如何在 Java 中实现比较器**

下面是一个在 Java 中使用 Comparator 的例子:

```
import java.util.Comparator;

public class School {
private int num_of_students;
private String name;
public Company(String name, int num_of_students) {
this.name = name;
this.num_of_students = num_of_students;
}
public int getNumOfStudents() {
return this.num_of_students;
}
public String getName() {
return this.name;
}
}
public class SortSchools implements Comparator {
@Override
public int compare(School sch1, School sch2) {
if(sch1.getNumOfStudents()== sch2.getNumOfStudents())
return 0;
else
return sch1.getNumOfStudents() > sch2.getNumOfStudents() ? 1 : -1;
}
public static void main(String[] args) {
School sch1 = new School("sch1", 20);
School sch2 = new School("sch2", 15);
SortSchools sortSch = new SortSchools();
int retval = sortSch.compare(sch1, sch2);
switch(retval) {
case -1: {
System.out.println("The " + sch2.getName() + " is bigger!");
break;
}
case 1: {
System.out.println("The " + sch1.getName() + " is bigger!");
break;
}
default:
System.out.println("The two schools are of the same size!");
}
}
}

Output:
The sch1 is bigger!
```

嗯，这里没必要惊慌。上面写的代码很容易理解。我们走吧！

首先，我创建了一个由学生姓名和年龄组成的班级学校。之后，我创建了另一个类 SortSchools，以实现 Comparator 接口，该接口实现了根据学生数量在名为 School 的第一个类的实例之间施加顺序的目标。

理解了 Java 中的比较器和比较器之后，让我们进入下一个话题。

## **Java 中的可比 v/s 比较器**

| Java 中的可比性 | Java 中的比较器 |
| 可比较接口用于以自然顺序对对象进行排序。 | Java 中的比较器是用来对不同对象的属性进行排序的。 |
| Comparable 接口将“this”引用与指定的对象进行比较。 | Java 中的比较器比较两个不同的类对象。 |
| Comparable is present in java.lang package. | java.util 包中有一个比较器。 |
| Comparable 影响原始类，即实际类被修改。 | 比较器不影响原始类 |
| Comparable 提供 compareTo()方法对元素进行排序。 | 比较器提供 compare()方法，equals()方法对元素进行排序。 |

我希望上面提到的差异能够澄清这两个概念。

至此，我们已经接近了文章的结尾。希望这些内容能够给你的 [Java 世界](https://docs.oracle.com/javase/tutorial/)带来信息和知识。敬请期待！

*现在您已经了解了 Java Collections，您可以查看 Edureka 提供的* [***Java 在线课程***](https://www.edureka.co/java-j2ee-training-course)*，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为希望成为 Java 开发人员的学生和专业人士设计的。本课程旨在让您对 Java 编程有一个初步的了解，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

有问题要问我们吗？请在本 [*【堪比 Java】*](#_top)*博客的评论区提及，我们会尽快回复您。*