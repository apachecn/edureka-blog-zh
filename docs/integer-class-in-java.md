# java 中的 Integer 类是什么，它是如何工作的？

> 原文：<https://www.edureka.co/blog/integer-class-in-java/>

Java 有一个全面的内置[类](https://www.edureka.co/blog/java-objects-and-classes/)和[接口](https://www.edureka.co/blog/java-interface/)的集合。其中，最常用的类之一是 Java 中的 Integer 类，它是原语类型包装类的一部分。在这篇博客中，你将按以下顺序了解整数类:

让我们开始吧。

## **Java 中的整数类是什么？**

Java 中的 Integer 类将一个原始类型 int 的值包装在一个对象中。Integer 类型的对象包含一个 int 类型的字段。Java Integer 类属于 Java.lang.Number 包。这里有一个完整的层级:

```
java.lang.Object
      java.lang.Number
           java.lang.Integer
```

Java Integer 类包含各种构造函数和方法。让我们直接研究它们。

## **Java.lang.Integer 类构造函数**

| 构造器 | 描述 |
| **整数(int 值)** | 用指定的 **Int** 构造新分配的整数对象 |
| **整数(字符串 s)** | 构造新分配的对象，该对象表示由参数**字符串**指示的 Int 值 |

## **Java.lang.Integer 类方法**

| 方法 | 修饰符和类型 | 描述 |
| bitCount(int i) | 静态 int | 返回指定 int 值的二进制补码表示形式中一位的个数。 |
| byteValue() | 字节 | 以字节形式返回该整数的值。 |
| compare(int x，int y) | 静态 int | 从数值上比较两个 int 值。 |
| compareTo(整数另一个整数) | （同 Internationalorganizations）国际组织 | 从数字上比较两个 Integer 对象。 |
| 解码(字符串 nm) | 静态整数 | 将字符串解码为整数。 |
| doubleValue() | 两倍 | 以双精度形式返回此整数的值。 |
| 等于(对象对象) | 布尔型 | 将此对象与指定的对象进行比较。 |
| floatValue() | 漂浮物 | 以浮点形式返回此整数的值。 |
| 整数(字符串 nm) | 静态整数 | 确定具有指定名称的系统属性的整数值。 |
| 哈希码() | （同 Internationalorganizations）国际组织 | 返回该整数的哈希代码。 |
| intValue() | （同 Internationalorganizations）国际组织 | 以 int 形式返回该整数的值。 |
| longValue() | 长的 | 以 long 类型返回此整数的值。 |
| lowstonebit(int I) | 静态 Int | 在指定的 int 值中的最低位(“最右边”)一位的位置，返回一个最多只有一位的 int 值。 |
| 反向(整数 I) | 静态 Int | 返回通过反转指定 int 值的二进制补码二进制表示形式中的位的顺序而获得的值。 |
| reverseBytes(int i) | 静态 Int | 返回通过反转指定 int 值的二进制补码表示形式中的字节顺序而获得的值。 |
| shortValue() | 短的 | 以短整型返回该整数的值。 |
| toString() | 线 | 返回表示该整数值的 String 对象。 |
| toString(int i) | 静态字符串 | 返回代表指定整数的 String 对象。 |
| valueOf(int i) | 静态整数 | 返回表示指定整数值的整数实例。 |
| valueOf(字符串 s) | 静态整数 | 返回保存指定字符串值的 Integer 对象。 |

你可以在这里了解更多这些方法[。现在你已经知道了 Integer 类中使用的不同方法，是时候实现它的一些主要方法了。](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html)

## **Java 整数示例**

在本节中，我已经实现了“Java 中的整数类”中使用的前五个方法。类似地，您可以实现它们的其余部分。如果你遇到任何困难，一定要让我知道。请参考下面的参考代码:

```

package Edureka;

import java.io.*; 
import java.util.*; 

public class javaIntegerExamples{    
	    public static void main(String args[])  
	    { 
	    		 int value = 161;
	    		 // Get the binary equivalent
	    		 System.out.println("Binary equivalent:"+Integer.toBinaryString(value));
	    		 System.out.println("Bit Count:"+Integer.bitCount(value));

	    		 //example for byteValue()
	    		 int Value1=123;
	    		 Integer a = new Integer(Value1);
	    			System.out.println("Byte Value is "+a.byteValue());

	    		//compare two integer values
	    			System.out.println(Integer.compare(20, 20));
	    			System.out.println(Integer.compare(20, 19));
	    			System.out.println(Integer.compare(20, 22));

	    		//compare two integers
	    			Integer value2 = new Integer(50);
	    			System.out.println(value2.compareTo(50)); 
	    			System.out.println(value2.compareTo(49));
	    			System.out.println(value2.compareTo(51));

	    		//decode the string
	    			System.out.println(Integer.decode("0124")); //base8
	    			System.out.println(Integer.decode("0x124")); //base16
	    		 }

	    }

```

**输出:**

二进制等价:10100001 位计数:3 字节值为 12301-101-184292

这就把我们带到了本文的结尾，我们已经理解了 Java 中的 *Integer 类。希望你们清楚这个话题。*

如果您发现这篇文章与“Java Integer class”相关，请查看一下 [*Edureka Java 认证培训*、](https://www.edureka.co/java-j2ee-soa-training) 这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*本课程旨在让您在  [Java 编程](https://www.edureka.co/blog/cheatsheets/java-cheat-sheet/) 方面有一个良好的开端，并训练您掌握核心和高级 Java 概念，以及各种  [Java 框架](https://www.edureka.co/blog/java-frameworks/) ，如 Hibernate & Spring。*

如果您遇到任何问题，请在本博客的评论区自由提问，我们的团队将很乐意回答。