# Java 中的对象数组:关于对象数组你需要知道的一切

> 原文：<https://www.edureka.co/blog/array-of-objects-in-java/>

当你谈到 Java 时，首先想到的是面向对象编程。Java 是一种处理对象的编程语言。本文将关注 Java 中的对象数组，并详细介绍对象数组。

本文将涉及以下主题:

*   [Java 中的对象数组](#ArrayOfObjectsInJava)
*   [在 Java 中声明对象数组](#DeclaringAnArrayOfObjectsInJava)
*   [用初始值声明一个数组对象](#DeclaringAnArrayObjectsWithInitialValues)
*   [对象数组的示例程序](#ExampleProgramForAnArrayOfObjects)

那么让我们从讨论的第一个话题开始

## **Java 中的对象数组**

对象数组，顾名思义，存储一个对象数组。一个对象代表内存中的一条记录，因此对于多条记录，必须创建一个对象数组。 必须注意，数组只能保存对对象的引用，而不能保存对象本身。让我们看看如何在 Java 中声明对象数组。确保你已经在我们的系统中安装了 [Java。](https://java.com/en/download/help/download_options.xml)

## **在 Java 中声明对象数组**

我们使用类名 Object，后跟方括号来声明一个对象数组。

```
Object[] JavaObjectArray;
```

另一个声明可以如下:

```
Object JavaObjectArray[];
```

让我们看看我们还能对这些物体做些什么，

## **用初始值声明一个数组对象**

一个数组对象的声明可以通过添加初始值来完成。 这里，我们创建一个数组，由一个值为“Women Empowerment”的字符串和一个值为 5 的整数组成。

```

public class Main {
public static void main(String[] args) {
Object[] JavaObjectArray = {"Women Empowerment", new Integer(5)};
System.out.println( JavaObjectArray[0] );
System.out.println( JavaObjectArray[1] );
}
}

```

代码产生以下输出:

赋予妇女权力

5

让我们通过看一个例子来结束这篇文章，

## **对象数组的示例程序**

```

class JavaObjectArray{
public static void main(String args[]){
Account obj[] = new Account[1] ;
obj[0] = new Account();
obj[0].setData(1,2);
System.out.println("For Array Element 0");
obj[0].showData();
}
}
class Account{
int a;
int b;
public void setData(int c,int d){
a=c;
b=d;
}
public void showData(){
System.out.println("Value of a ="+a);
System.out.println("Value of b ="+b);
}
}

```

**输出:**

为数组元素 0

a 的值:1

b 的值:2

***对象是所有类的根类。数组似乎是一种方便的数据结构，用于保存相同的多个值。***

这样，我们就结束了这篇关于“Java 中的对象数组”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的 [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论区提出来，我们会尽快回复你，或者你也可以参加我们在巴东的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-padang)