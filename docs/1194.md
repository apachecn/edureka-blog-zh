# Java 中的字符数组:关于字符数组你需要知道的一切

> 原文：<https://www.edureka.co/blog/character-array-in-java/>

一门好的编程语言应该擅长处理所有的数据类型。这些天处理的很多数据也有字符在里面。Java 是最好的编程语言之一，它利用 char 数组来保存数据。在这篇文章中，我们将探索关于他们的一切。

本文将讨论以下几点:

*   [声明字符数组](#DeclaringCharArray)
*   [初始化字符数组](#InitializingCharArray)
*   [字符数组中的循环](#LoopsInCharArray)
*   [字符数组长度](#LengthOfCharArray)
*   [对字符数组进行排序](#SortingAChar%20Array)
*   [将字符串数组转换成字符数组](#ConvertingAStringArrayIntoCharArray)

让我们从快速介绍 Char 数组开始，

充电阵列非常有利。值得注意的事实是，字符串是不可变的，即它们的内部状态在创建后不能改变。但是，使用 char 数组，可以操作字符缓冲区。虽然数据结构列表和集合也是可以接受的，但是数组被证明是简单而有效的。此外，Char 数组速度更快，因为可以在没有任何分配的情况下操作数据。

让我们通过理解如何在 Java 中声明数组来开始这篇关于 Java 中 Char 数组的文章。虽然从 [Java 安装](https://java.com/en/download/help/download_options.xml)开始。如果你没有。

## **声明字符数组**

可以使用方括号来声明 char 数组:

```
char[] JavaCharArray;
```

方括号也可以放在末尾。

```
char JavaCharArray[];
```

下一步是初始化这些数组

## **初始化字符数组**

char 数组可以通过赋予它一个默认大小来初始化。

```
char[] JavaCharArray = new char[4];
```

这会给它分配一个大小为 4 的实例。

我们使用下面的代码给我们的 char 数组赋值:

```

char[] JavaCharArray = new char[5];
JavaCharArray[0] = 'r';
JavaCharArray[1] = 's';
JavaCharArray[2] = 't';
JavaCharArray[3] = 'u';

```

在避免重复代码方面，循环起着非常重要的作用，这是 Java 文章中 Char 数组的下一部分，

## **字符数组中的循环**

为了遍历数组中的每个值，我们使用 for 循环。

```

char[] JavaCharArray = {'r', 's', 't', 'u', 'v'};
for (char c:JavaCharArray) {
System.out.println(c);
}

```

**输出:**

r

s

t

u

v

我们还可以实现以下方法:

```

char[] JavaCharArray = {'r', 's', 't', 'u', 'v'};
for (int i=0; i<JavaCharArray.length; i++) {
System.out.println(JavaCharArray[i]);
}

```

这产生了与先前代码相同的输出。

让我们看看如何找出字符数组的长度

## **字符数组长度**

字符数组的长度可以如下确定:

```

char[] JavaCharArray = {'r', 's', 't', 'u', 'v'};
System.out.println(JavaCharArray.length);

```

**输出:**

five

我们甚至可以对 char 数组进行排序，

## **对字符数组进行排序**

为了对数组进行排序，我们可以实现 Arrays.sort()，如下所示:

```

char[] JavaCharArray = {'r', 't', 'u', 's', 'v'};
Arrays.sort(JavaCharArray);
System.out.println(Arrays.toString(JavaCharArray));

```

**输出:**

[r、s、t、u、v]

Java 中这个 Char 数组的最后一位会讲到下面的指针，

## **将字符串数组转换成字符数组**

下面的代码将字符串转换为 char 数组。

```

public class Main {
public static void main(String[] args) {
String value = "hello";
//Convert string to a char array.
char[] array = value.toCharArray();
array[0] = 'j';
//Loop over chars in the array.
for(char c : array) {
System.out.println(c);
}
}
}

```

**输出:**

j

e

l

l

o

虽然字符串通常是首选，但 char 数组给了我们一种有效的方法。

这样，我们就结束了这篇关于“Java 中 Char 数组”的文章。如果您想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。如果你刚刚开始，那么看看这篇 Java 教程，理解基本的 Java 概念。

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

有问题要问我们吗？请在这个博客的评论区提出来，我们会尽快回复你，或者你也可以参加我们在 T2 举办的 Java 培训。