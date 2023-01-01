# Java 中如何把 Int 转换成 String？

> 原文：<https://www.edureka.co/blog/convert-int-to-string-in-java/>

在特定条件下，Java 允许你将值从一种数据类型转换成另一种数据类型。您可以将字符串变量转换为数值，也可以将数值转换为字符串变量。在本文中，让我们看看如何在 [Java](https://www.edureka.co/java-j2ee-soa-training) 中将 int 转换成 String。

下面列出了在 Java 中将 int 转换为 string 的不同方法:

*   [我们如何在 Java 中把 int 转换成 String:](#toString)[使用 Integer.toString(int)](#toString)
*   [我们如何在 Java 中将 int 转换成 String:使用 String.valueOf(int)](#valueOf)
*   [我们如何在 Java 中将 int 转换成 String:使用 String.format()](#format)
*   [我们如何在 Java 中将 int 转换成 String:使用 DecimalFormat](#DecimalFormat)
*   [我们如何在 Java 中将 int 转换成 String:使用 StringBuffer 或 StringBuilder](#StringBuilder)

对于这些方法中的每一个，我将讨论语法、涉及的参数和返回值以及 Java 中的示例程序。让我们开始吧。

## **在 Java 中我们如何把 int 转换成 String？**

### **Java 中整数到字符串的转换:使用 Integer.toString(int)**

Integer 类有一个静态方法，该方法返回一个 String 对象，该对象表示在 *Integer.toString(int)* 函数中指定的 int 参数。与其他方法不同，这种方法可以返回一个 *NullPointerException* 。

**语法**

Integer.toString()方法有两种不同的表达式:

*   公共静态字符串 toString(int i)
*   公共静态字符串 toString(int i，int radix)

**参数**

该方法的参数是:

*   ***i:*** 要转换的整数。
*   ***基数:*** 用来表示字符串的基数-数字系统。

基数值是可选参数，如果没有设置，十进制系统的默认值是 10。

**返回值**

两个表达式的返回值都是一个表示整数*“I”*参数的 [Java 字符串](https://www.edureka.co/blog/java-string/)。如果使用 radix 参数，则返回的字符串由各自的 radix 指定。

**使用 Integer.toString()将整数转换为字符串。**

```
package MyPackage;
public class Method1 
{
	public static void main(String args[]) 
	{
		  int n = Integer.MAX_VALUE;
		  String str1 = Integer.toString(n);
		  System.out.println("The output string is: " + str1);
		  int m = Integer.MIN_VALUE;
		  String str2 = Integer.toString(m);
		  System.out.println("The output string is: " + str2);
	}

}
```

**输出**

```
The output string is: 2147483647
The output string is: -2147483648
```

## **使用 String.valueOf(int)** 将 int 转换为 string

*String.valueOf()* 是字符串类的静态实用方法，可以将大多数原始的[数据类型](https://www.edureka.co/blog/data-types-in-java/)转换成它们的字符串表示。它包括整数。由于其简单性，这种方法被认为是最佳实践。

**语法**

它表示为:

*   公共静态字符串 valueOf(int i)

**参数** 参数

*   ***i:*** 需要转换的整数

**返回值**

这个方法返回 int 参数的字符串表示。

**使用 String.valueOf()将整数转换为字符串。**

```
class Method2
{ 
  public static void main(String args[]) 
  { 
    int number = 1234; 
    String str = String.valueOf(number);
    System.out.println("With valueOf method: string5 = " + str);
  } 
}  
```

**输出**

```
With valueOf method: string5 = 1234
```

## **使用 String.format()** 将 int 转换为 String

在 [Java](https://www.edureka.co/blog/what-is-java/) ， *String.format()* 是一个新的替代方法，可以用来将整数转换成字符串对象。虽然这个方法的目的是格式化一个字符串，但是它也可以用于转换。

**语法**

有两种不同的表达方式:

*   公共静态字符串格式(区域设置 l，字符串格式，对象…参数)
*   公共静态字符串格式(字符串格式，对象…参数)

**参数**

这种方法的参数是:

*   ***l:*** 格式化时要寻址的局部
*   ***格式:*** 格式字符串，包括格式说明符，有时也包括固定文本
*   ***参数:*** 参数，引用在*格式*参数中设置的格式说明符

**返回值**

该方法根据格式说明符和指定的参数返回一个带格式的字符串。

**使用 String.format()将 int 转换为 String。**

```
class Method3
{ 
  public static void main(String args[]) 
  { 
    int number = -1234; 
    String str = String.format("%d", number);
    System.out.println("With format method: string = " + str);
  } 
}
```

**输出**

```
With format method: string = -1234
```

## **使用 DecimalFormat 将 int 转换为 String**

DecimalFormat 是 NumberFormat 类的一个具体子类，用于格式化十进制数。它有很多特性用来解析和格式化数字。您可以使用它将一个数字格式化为一个遵循某种[模式](https://www.edureka.co/blog/30-pattern-programs-in-java/)的字符串表示。下面是一个示例程序。

```
import java.text.DecimalFormat;
public class Method4
{
	 public static void main(String[] args) 
	 {
	      int number = 12345;
	      DecimalFormat numberFormat = new DecimalFormat("##,###");
	      String str = numberFormat.format(12345);	      
          System.out.println("The number to be converted is: " + number);
	      System.out.println("The string version of 12345 is: " + str);
	 }

}
```

**输出**

```
The number to be converted is: 12345
The string version of 12345 is: 12,345

```

如果你知道如何使用 [DecimalFormat](https://docs.oracle.com/javase/7/docs/api/java/text/DecimalFormat.html) 方法，这是将整数转换成字符串的最佳选择，因为你可以对格式进行级别的控制。如上面的示例所示，您可以指定小数位数和逗号分隔符以提高可读性。

## **使用 StringBuffer 或 StringBuilder 将 int 转换为 String**

*StringBuilder* 和 *StringBuffer* 是用于将多个值连接成一个字符串的类。StringBuffer 是[线程安全的，但速度较慢，而 StringBuilder 不是线程安全的，但速度较快。下面我给出了一个例子来演示这些类，并解释了它是如何工作的。看一看。](https://www.edureka.co/blog/java-thread/)

**使用 StringBuilder/StringBuffer 将 int 转换成 String。**

```
class Method5
{
  public static void main(String args[]) 
  { 
    int number1 = -1234;
    StringBuilder sb = new StringBuilder(); 
    sb.append(number1); 
    String str1 = sb.toString(); 
    System.out.println("With StringBuilder method: string = " + str1); 
    StringBuffer SB = new StringBuffer(); 
    SB.append(number1); 
    String str2 = SB.toString(); 
    System.out.println("With StringBuffer method: string = " + str2); 
  } 
} 
```

**输出**

```
With StringBuilder method: string = -1234
With StringBuffer method: string = -1234
```

StringBuilder 对象表示一个[字符串](https://www.edureka.co/blog/java-string/)对象，该对象可以被修改并被视为一个带有字符序列的[数组](https://www.edureka.co/blog/java-array/)。为了在字符串末尾添加一个新参数，StringBuilder 实例实现了 *append()* 方法。最后，调用 *toString()* 方法是很重要的，以便获得数据的字符串表示。或者，您也可以使用这些类的简写版本。下面是如何在 Java 中将 int 转换成 String:

**使用 StringBuilder/StringBuffer 将 int 转换成 String 的例子。**

```
class Method6
{
  public static void main(String args[]) 
  { 
	String str1 = new StringBuilder().append(1234).toString(); 
    System.out.println("With StringBuilder method: string = " + str1); 
    String str2 = new StringBuffer().append(1234).toString(); 
    System.out.println("With StringBuffer method: string = " + str2); 
  } 
} 
```

**输出**

```
With StringBuilder method: string = -1234
With StringBuffer method: string = -1234
```

最重要的是调用 *toString()* 方法，以获得数据的字符串表示。

“如何在 Java 中将 int 转换成 String”这篇文章到此结束。我已经讲述了 Java 的一个基本主题，使用 [JDK](https://www.edureka.co/blog/what-is-java/#ComponentsinJava) 附带的工具将 int 或 Integer 转换成 String。 希望你清楚本文与你分享的一切。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 提供的 [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。*

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*有问题吗？请在这篇“如何在 Java 中把 int 转换成 String”**文章的评论部分提到它，我们会尽快回复你。*