# Java 中的 append 方法是什么？

> 原文：<https://www.edureka.co/blog/append-method-in-java/>

Java 提供了许多方法来减轻你的工作。在本文中，我们来讨论这样一种方法，【append()】。java 中的 append 方法将指定的字符串追加到字符序列中。我来详细说明一下 Java 中的[方法](https://www.edureka.co/blog/java-methods/) append。

要讨论的要点如下:

*   [Java 中的 append 方法是什么？](#WhatisappendmethodinJava?)
*   [语法](#syntax)
*   [示例–StringBuilder 和 StringBuffer](#Example)
*   [什么时候使用追加方法？](#when)

让我们开始吧！

## **Java 中的 append 方法是什么？**

Java 中的 append 方法有助于将指定的字符串追加到字符序列中。然后附加上[字符串](https://www.edureka.co/blog/java-string/)参数的字符。

*   **申报**

append 方法的声明如下:

```
public StringBuilder append(String str)
```

*   **参数**

str:是一个字符串

*   **返回值**

返回对对象的引用

现在你已经知道了一般语法，让我们来看看 Java 中 append 方法的不同使用方式/形式。

## **在 Java 中追加:语法**

表示 ***的不同方式追加*** 的方法有:

*   **public**StringBuilder append(**布尔** b)
*   **public**StringBuilder append(int I)
*   **public**StringBuilder append(float f)
*   **public**StringBuilder append(长 l)
*   **public**StringBuilder append(双 d)
*   **公共** StringBuilder 追加( **char** c)
*   **public** StringBuilder 追加( **char** [] str)
*   **public**StringBuilder append(**char**[]str， **int** offset， **int** len)
*   **public**StringBuilder append(char sequence cs)
*   **public**StringBuilder append(char sequence cs， **int** start， **int** end)
*   **public**StringBuilder append(Object obj)
*   **public**StringBuilder append(字符串 str)
*   **public**StringBuilder append(string buffer sb)
*   **public** StringBuilder 附录代码点( **int** 代码点)

现在你已经知道了这个概念，让我们试着借助一个例子来理解这个概念。

## **例子**

下面给出的代码向你展示了 **StringBuilder** 类的用法。看一看！

**代码:**

```
import java.util.*; 
import java.util.concurrent.LinkedBlockingQueue; 

public class A { 
    public static void main(String[] argv) 
        throws Exception 
    { 

        StringBuilder str 
            = new StringBuilder(); 

        str.append("ABC"); 

        System.out.println("String = "
                           + str.toString()); 

        StringBuilder str1 
            = new StringBuilder("XYZ"); 

        System.out.println("String1 = "
                           + str1.toString()); 

        StringBuilder str2 
            = new StringBuilder(10); 

        // print string 
        System.out.println("String2 capacity = "
                           + str2.capacity()); 

        StringBuilder str3 
            = new StringBuilder(str1); 

        // print string 
        System.out.println("String3 = "
                           + str3.toString()); 
    } 
} 

```

**输出:**

String = ABC

String1 = XYZ

字符串 2 容量= 10

String3 = XYZ

另一种方法是使用 **StringBuffer** 类。

**代码:**

```
import java.io.*; 
class GFG { 
    public static void main(String[] args) 
    { 
        StringBuffer s = new StringBuffer("GeeksforGeeks"); 
        int p = s.length(); 
        int q = s.capacity(); 
        System.out.println("Length of the string Edureka =" + p); 
        System.out.println("Capacity of the string Edureka =" + q); 
    } 
} 

```

**输出:** 字符串长度 Edureka = 7 字符串容量 Edureka = 10

在上面的代码中，我提到了属于 StringBuffer 类的两个最常用的方法。让我再详细介绍一下 Java 提供的这种方法！

## **什么时候使用追加方法？**

嗯，在字符串[对象](https://www.edureka.co/blog/java-object/)上使用+运算符的情况。Java 本身通过对 StringBuffer 实例的两个类似操作来改变对 string 实例的任何修改。因此串联调用了一个 [StringBuffer](https://www.edureka.co/blog/stringbuffer-in-java/) 对象上的 append 方法。一旦执行了连接，编译器就调用 ***toString*** 方法将修改后的 StringBuffer 变回常量字符串。听起来真的很复杂，对吧？

与其这样，为什么不创建一个类似于 ***StringBuffer*** 的 string 类呢？

这里的解决方案是性能。知道 string 对象是不可变的，时间和时间可以做出很多优化。Java 隐藏了 String 和 StringBuffer 之间转换的复杂部分，更准确地说，程序员从未真正感觉到有必要使用 StringBuffer，并且将能够根据字符串变量上的+运算符解决大多数问题！

这就把我们带到了这篇关于 Java 中的方法追加的文章的结尾。我希望你发现它信息丰富。继续阅读，继续探索！

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“用 Java 追加”文章的评论部分提到它，我们会尽快回复您。