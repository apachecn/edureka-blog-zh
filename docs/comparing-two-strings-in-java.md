# 在 Java 中比较两个字符串的 5 种方法

> 原文：<https://www.edureka.co/blog/comparing-two-strings-in-java/>

字符串操作在不同的领域有很大的帮助。它可能在文本分析、数据匹配、数据挖掘等方面有所帮助。在这篇文章中，我们将重点比较 Java 中的两个字符串，这两个字符串的操作目的又是不同的。以下是将在此讨论的要点

*   [字符串等于方法](#StringEqualsMethod)
*   [字符串等于忽略大小写](#StringEqualsIgnoreCase)
*   [对象等于方法](#ObjectEqualsMethod)
*   [字符串比较方法](#StringCompareToMethod)
*   [使用双等运算符](#UsingDoubleEqualToOperator)

那么让我们开始吧，

## **在 Java 中比较两个字符串**

一个字符序列可以定义为一个字符串。它们是不可变的，即一旦创建就不能修改。在 java 中有各种方法来比较两个字符串，如下所示。

## **字符串等于方法**

基于字符串中存在的值来比较字符串。如果两个字符串的值相同，则该方法返回 true，如果不匹配，则返回 false。

```

public class Main {
public static void main(String args[])
{
String str1 = new String("Rock");
String str2 = new String("Roll");
String str3 = new String("rock");
String str4 = new String("Rock");
String str5 = new String("Roll");
//comparing the strings
System.out.println("Comparing " + str1 + " and " + str2
+ " : " + str1.equals(str2));
System.out.println("Comparing " + str3 + " and " + str4
+ " : " + str3.equals(str4));
System.out.println("Comparing " + str4 + " and " + str5
+ " : " + str4.equals(str5));
System.out.println("Comparing " + str1 + " and " + str4
+ " : " + str1.equals(str4));
}
}

```

**输出:**

比较摇滚:错误

比较摇滚和摇滚:错

比较摇滚:错误

比较摇滚和摇滚:真的

让我们继续这篇文章的第二部分，

## **字符串等于忽略大小写**

此方法比较两个字符串，不考虑字符串的大小写(小写或大写)。如果值相等且不为空，则返回 true。

```
</p>
public class Main {
public static void main(String args[])
{
String str1 = new String("Rock");
String str2 = new String("Roll");
String str3 = new String("rock");
String str4 = new String("Rock");
String str5 = new String("Roll");
//Comparing Strings
System.out.println("Comparing " + str1 + " and " + str2
+ " : " + str1.equalsIgnoreCase(str2));
System.out.println("Comparing " + str3 + " and " + str4
+ " : " + str3.equalsIgnoreCase(str4));
System.out.println("Comparing " + str4 + " and " + str5
+ " : " + str4.equalsIgnoreCase(str5));
System.out.println("Comparing " + str1 + " and " + str4
+ " : " + str1.equalsIgnoreCase(str4));
}
}

```

**输出:**

比较摇滚:错误

比较摇滚和摇滚:真的

比较摇滚:错误

比较摇滚和摇滚:真的

让我们继续下一步，比较 Java 文章中的两个字符串，

## **对象等于方法**

如果参数彼此相等，则该方法返回 true，否则返回 false。如果存在的两个参数都为 null，则返回的输出为 true。如果单个参数为空值，则返回的输出为 false。

```

import java.util.*;
public class Main {
public static void main(String args[])
{
String str1 = new String("Rock");
String str2 = new String("Roll");
String str3 = new String("Roll");
String str4 = null;
String str5 = null;
System.out.println("Comparing " + str1 + " and " + str2
+ " : " + Objects.equals(str1, str2));
System.out.println("Comparing " + str2 + " and " + str3
+ " : " + Objects.equals(str2, str3));
System.out.println("Comparing " + str1 + " and " + str4
+ " : " + Objects.equals(str1, str4));
System.out.println("Comparing " + str4 + " and " + str5
+ " : " + Objects.equals(str4, str5));
}
}

```

**输出:**

比较摇滚:错误

比较滚动和滚动:正确

比较 Rock 和 null :false

比较 null 和 null :true

现在让我们继续前进

## **字符串比较方法**

在这种方法中，输入字符串相互比较。比较后返回的值如下:

*   如果(str1>str2)，则返回一个正值。
*   如果(str1==str2)，则返回 0。
*   如果(str1

**代码**

```

import java.util.*;
public class Main {
public static void main(String args[])
{
String str1 = new String("Rock");
String str2 = new String("Pop");
String str3 = new String("Roll");
String str4 = new String("Roll");
System.out.println("Comparing " + str1 + " and " + str2
+ " : " + str1.compareTo(str2));
//Comparing String 3 = String 4
System.out.println("Comparing " + str3 + " and " + str4
+ " : " + str3.compareTo(str4));
System.out.println("Comparing " + str2 + " and " + str4
+ " : " + str2.compareTo(str4));
}
}

```

**输出:**

比较摇滚和流行音乐:2

比较滚动和滚动:0

比较 Pop 和 Roll :-2

这就把我们带到了 Java 文章中比较两个字符串的最后一点，

## **使用双等运算符**

在比较两个字符串值时，应该避免使用此方法。equals()和==运算符之间的主要区别如下:

*   equals()是方法，==是运算符。

*   ==运算符用于引用比较，另一方面，equals()方法用于内容比较。

避免使用 ***==*** 运算符，因为它检查引用是否相等，即字符串是否指向同一个对象。

**代码**

```

import java.util.*;
public class Main {
public static void main(String[] args)
{
String str1 = new String("Rock");
String str2 = new String("Rock");
System.out.println(str1 == str2);
System.out.println(str1.equals(str2));
}
}

```

**输出:**

错误的

真实的

文章中提到的方法提供了一种细致的方式来比较 java 编程语言中的两个字符串。

至此，我们已经结束了这篇关于“Java 中的对象数组”的文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。