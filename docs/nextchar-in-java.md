# Java 中的 NextChar 是什么，如何实现？

> 原文：<https://www.edureka.co/blog/nextchar-in-java/>

在 [**Java**](https://www.edureka.co/java-j2ee-training-course) 中，NextChar()和 Next() 运算，返回输入中的后件 token/word 作为字符串， **charAt()** 第一个返回该字符串中的主字符。通过这篇文章，我们将有更多的了解。

*   [Java 中的扫描仪类](#scanner)
*   [扫描仪类声明](#declare)
*   [如何获得 Java 扫描仪](#how)

## **Java 中的扫描仪类**

Java 中的 scanner 类可以在 **java.util** 包中找到。Java 提供了各种从键盘读取输入的方法，java.util.Scanner 类就是其中之一。Java Scanner 类使用缺省情况下为空白的分隔符将输入分成标记。它给出了许多读取和解析各种原始值的方法。这个类广泛用于使用正则表达式解析字符串和基本类型的文本。这是在 Java 中获得输入的最简单的方法。在 Java 的 Scanner 的帮助下，用户可以从用户那里获得原始类型的输入，如 int、long、double、byte、float、short 等。

该类扩展了 object 类，实现了迭代器和可关闭接口。Scanner 类提供了 **nextXXX()** 方法来返回各种值，如 *nextInt()、nextByte()、nextShort()、next()、nextLine()、nextDouble()、nextFloat()、nextBoolean()、*等。为了从扫描器中导出单个字符，调用 **next()。charAt(0)** 可以调用返回单个字符的方法。

## **Java 扫描器类声明**

```
public final class Scanner
	extends Object implements Iterator<String>

```

**举例:**

```
import java.util.Scanner; 
public class ScannerDemo1 
{ 
    public static void main(String[] args) 
    { 
        Scanner sc = new Scanner(System.in); 
        char c = sc.next().charAt(0); 
        System.out.println("c = "+c); 
    } 
}

```

**//输出:**

`the input = g``The output is` 

## **如何获得 Java 扫描仪**

为了获得一个 Java 扫描器的实例，它读取用户的输入，我们必须在 Scanner 类的构造函数中传递输入流(System.in)。比如请看下面:

```
Scanner in = new Scanner(System.in);

```

对于解析字符串的 Java Scanner 实例，我们需要在 Scanner 类的构造函数中传递字符串。

**例如:**

```
Scanner in = new Scanner ("Hello Edureka");

```

让我们看看一些 Java 构造函数:

| **构造器** | **描述** |
| **扫描仪(文件源)** | 它构造一个新的扫描器，给出从指定文件扫描的值。 |
| **扫描仪(文件源，字符串字符集名)** | 它构造一个新的扫描器，给出从指定文件扫描的值。 |
| **扫描仪(输入流源)** | 它构造一个新的扫描器，该扫描器给出从指定的输入流中扫描的值 |
| **扫描仪(输入流源，字符串字符集名)** | 它构造一个新的扫描器，该扫描器给出从指定输入流中扫描的值。 |
| **扫描仪(可读源)** | 它构造一个新的扫描器，给出从指定源扫描的值。 |
| **扫描仪(字符串源)** | 它构造一个新的扫描器，给出从指定字符串扫描的值。 |
| **扫描仪(ReadableByteChannel 源)** | 它构造一个新的扫描器，给出从指定通道扫描的值。 |
| **Scanner(readable bytechannel source，String charsetName)** | 它构造一个新的扫描器，给出从指定通道扫描的值。 |
| **扫描仪(路径源)** | 它构造一个新的扫描器，给出从指定文件扫描的值。 |
| **扫描仪(路径源，字符串字符集名)** | 它构造一个新的扫描器，给出从指定文件扫描的值。 |

**举例:**

```
import java.util.*;  
public class ScannerExample {  
public static void main(String args[]){  
          Scanner in = new Scanner(System.in);  
          System.out.print("Enter your name: ");  
          String name = in.nextLine();  
          System.out.println("Name is: " + name);             
          in.close();             
          }  
} 

```

**//输出:**

`Enter your name: Arjun`

**举例:**

```
import java.util.*;  
public class ScannerClassExample1 {    
      public static void main(String args[]){                       
          String s = "Hello, This is Edureka.";  
          Scanner scan = new Scanner(s);  
          System.out.println("Boolean Result: " + scan.hasNext());  
          System.out.println("String: " +scan.nextLine());  
          scan.close();           
          System.out.println("--------Enter Your Details-------- ");  
          Scanner in = new Scanner(System.in);  
          System.out.print("Enter your name: ");    
          String name = in.next();   
          System.out.println("Name: " + name);           
          System.out.print("Enter your age: ");  
          int i = in.nextInt();  
          System.out.println("Age: " + i);  
          System.out.print("Enter your salary: ");  
          double d = in.nextDouble();  
          System.out.println("Salary: " + d);         
          in.close();         
	}
}

```

**//输出:**

`Boolean Result: true``String: Hello, This is Edureka``--------Enter Your Details--------` `Enter your name: Ramesh``Name: Ramesh``Enter your age: 25``Age: 25``Enter your salary: 25000``Salary: 25000`

至此，我们结束了这篇关于“Java 中的 NextChar”的文章。希望你已经通过一些实时的例子理解了重要性和实现。

*现在您已经了解了 Java 中 NextChar 的基础知识，请查看 Edureka 的  [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这篇“Java 中的 NextChar”博客的评论部分提到它，我们会尽快回复您。