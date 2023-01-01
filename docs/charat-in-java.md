# 如何用 Java 实现 charAt？

> 原文：<https://www.edureka.co/blog/charat-in-java/>

[Java](https://www.edureka.co/blog/java-tutorial/) 中的 charAt()是一个方法，专门用来返回字符串中指定索引处的字符。在本文中，我们将详细了解这个主题。本文将涉及以下内容，

*   [Java 中的 charAt](#charAtinJava)
*   [StringIndexOutOfBoundsException 的示例](#ExampleforStringIndexOutOfBoundsException)
*   [使用 charAt()](#PrintingallcharactersofastringusingcharAt()) 打印一个字符串的所有字符
*   [使用 charAt()](#CountingthefrequencyofacharacterusingcharAt()) 统计字符出现的频率
*   [打印字符串的第一个和最后一个字符](#Printingthefirstandlastcharacterofastring)

让我们开始吧

## **Java 中的 charAt**

对于 charAt()方法，传递的索引值必须介于 0 和(字符串长度–1)之间。如果索引值大于、等于或为负数，则返回一个**StringIndexOutOfBoundsException**。

**签名**

```
public char charAt(int index)
```

**参数**

索引:要返回的字符的索引

**返回**

返回指定位置的字符。

**异常**

**StringIndexOutOfBoundException**:如果索引的值为负，大于或等于字符串的长度，则返回。

继续 Java 文章中的这个特性

**例子**

```

public class Main
{
public static void main(String args[])
{
String str = "We must save the planet from climate change";
//This returns the first character of the string
char c1 = str.charAt(0);
char c2 = str.charAt(5);
char c3 = str.charAt(9);
char c4 = str.charAt(15);
System.out.println("Character at 0 index : "+c1);
System.out.println("Character at 5th index : "+c2);
System.out.println("Character at 9th index : "+c3);
System.out.println("Character at 15th index : "+c4);
}
}

```

**输出**

索引为 0 的字符为:W

第 5 个索引处的字符为:s

第 11 个索引处的字符是:a

第 20 个索引处的字符为:e

继续 Java 文章中的这个特性

## **StringIndexOutOfBoundsException 的示例**

在传递负索引或大于 length()–1 的索引时，会抛出 StringIndexOutOfBoundsException。

在下面的例子中，传递了一个负索引:

```

public class Main
{
public static void main(String args[])
{
String str = "ClimateChange";
//negative index
char c = str.charAt(-1);
System.out.println(c);
}
}

```

**输出**

线程“main”Java . lang . stringindexoutofboundsexception 中的异常:字符串索引超出范围:-1

at Java . base/Java . lang . string Latin 1 . charat(tring Latin 1 . Java:44)

at Java . base/Java . lang . string . charat(string . Java:692)

at Main.main(Main.java:5)

命令以非零状态 1 退出

代码因异常而终止。

继续 Java 文章中的这个特性

## **使用 charAt()** 打印一个字符串的所有字符

使用 for 循环从 0 到字符串长度()-1，打印一个字符串的所有字符。

```
</p>
public class Main
{
public static void main(String args[])
{
String s = "ClimateChange";
for(int i=0; i<=s.length()-1; i++) {
System.out.println(s.charAt(i));
}
}
}
<p style="text-align: justify;">
```

**输出**

C

l

我

m

答

t

e

C

h

答

n

g

e

继续 Java 文章中的这个特性

## **使用 charAt()** 统计字符出现的频率

```

public class Main
{
public static void main(String[] args)
{
String s = "ClimateChangeIsReal";
int count = 0;
for (int i=0; i<=s.length()-1; i++)
{
if(s.charAt(i) == 'C'){
count++;
}
}
System.out.println("Frequency of C is: "+count);
}
}

```

使用 charAt(): 可以确定字符的频率

**输出**

C 的频率为:2

继续 Java 文章中的这个特性

## **打印字符串的第一个和最后一个字符**

字符串的第一个和最后一个字符可以用 charAt(): 打印出来

```

public class Main
{
public static void main(String[] args)
{
String s = "Climate Change Is Real";
int strLength = s.length();
//first character
System.out.println("Character at 0 index : "+ s.charAt(0));
//Fetching last Character present at the string length-1 index
System.out.println("Character at last index : "+ s.charAt(strLength-1));
}
}

```

**输出**

索引为 0 的字符:C

最后一个索引的字符:l

***charAt()方法为用户提供了无数种方法来访问任意指定索引处的元素，只要索引在适当的范围内。***

这样，我们就结束了这篇关于“Java 中的 charAt”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。