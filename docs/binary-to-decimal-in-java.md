# Java 中如何把二进制转换成十进制？

> 原文：<https://www.edureka.co/blog/binary-to-decimal-in-java/>

从那时起，我们就知道计算机理解二进制语言，毫无疑问，我们每个人都想知道如何将二进制数转换成十进制、八进制和十六进制数。嗯，在一个需要将数百个数字从机器语言解码成人类解释语言的环境中，手动完成几乎是不可能的。因此，相反，我们可以写一个简单的代码[来说明如何在 Java 中将二进制转换成十进制。因此，在这篇文章中，我将按以下顺序讨论这个问题:](https://www.edureka.co/blog/hello-world-program-in-java/)

*   [二进制到十进制的数学转换](#mathematicalconversionfrombinarytodecimal)
*   [在 Java 中把二进制转换成十进制:](#convertbinarytodecimalnumbersinjava)
    1.  [使用 Interger.parseInt()](#usemethod)
    2.  [使用自定义逻辑](#usecustomlogic)

在我讨论在 [Java](https://www.edureka.co/blog/what-is-java/) 中把二进制数转换成十进制数的各种方法之前，让我们先来看看老式的转换方法。

## **二进制到十进制的数学转换**

想法很简单。你只需要从右边提取二进制数的数字，然后乘以 2 的幂。然后，您必须将所有值相加，以获得所需的十进制数。参考下图:

![Convert Binary to Decimal - How to Convert Binary to Decimal - Edureka](img/6bf5c10f6ce6768713924eec7ab5fbd9.png)

既然你已经理解了二进制数到十进制数的数学转换，那么让我们来理解如何为它写一个代码。

## **在 Java 中把二进制数转换成十进制数**

要在 Java 中将二进制数转换成十进制数，可以使用 [Integer.parseInt()](#usemethod) 方法或[自定义逻辑](#usecustomlogic)。因此，让我们一个一个地研究它们。从 Integer.parseInt() [方法](https://www.edureka.co/blog/java-methods/)开始:

### **Interger.parseInt()方法**

此方法用于将字符串转换为具有给定基数的整数。它来自 Integer [类](https://www.edureka.co/blog/java-objects-and-classes/)，该方法的语法如下:

```
public static int parseInt(String s,int radix)  

```

#### **Java 程序使用 Integer.parseInt()**

有两种方法可以使用 Integer.parseInt()编写一个 [Java 程序](https://www.edureka.co/blog/java-programs/)。第一种方式是在程序本身中提到二进制数，第二种方式是要求用户输入二进制数。

##### **在程序本身中提到二进制数**

```
package sampleprogram;
public class ConvertBinaryToDecimal {
public static void main(String args[]){
String binarynumber="10101";
int decimalnumber=Integer.parseInt(binarynumber,2);
System.out.println(decimalnumber);
}
}

```

**输出:**

![Output - How to Convert Binary to Decimal - Edureka](img/348f0e55c93f5e2106ef1398cabc5aaf.png)

如果你想在代码本身中提及多个二进制数，你可以用下面的方式提及:

```
package sampleprogram;
public class ConvertBinaryToDecimal {
public static void main(String args[]){
System.out.println(Integer.parseInt("1110",2));
System.out.println(Integer.parseInt("0010",2));
System.out.println(Integer.parseInt("1010",2));
System.out.println(Integer.parseInt("0110",2));
System.out.println(Integer.parseInt("1101",2));
}
}

```

**输出:**

##### **![Multiple Outputs - How to Convert Binary to Decimal - Edureka](img/91e09a9b09c1d51f140c0931e7bf57f4.png)要求用户输入二进制数**

为了让用户输入二进制数，你必须导入[扫描器类](https://www.edureka.co/blog/scanner-class-in-java/)。 Scanner 类主要用于获取用户输入，它属于 java.util 包。

```
package sampleprogram;
import java.util.Scanner;
public class ConvertBinaryToDecimal {
public static void main(String args[]){
Scanner BinaryInput = new Scanner( System.in );
System.out.print("Enter the Binary Number - ");
String BinaryNumber =BinaryInput.nextLine();
System.out.println("Decimal Number- "+Integer.parseInt(BinaryNumber,2));
}
}

```

**输出:**

![User Input and Output - How to Convert Binary to Decimal - Edureka](img/4b294c1511fd6e1df56828b4d564e31b.png)

好了，伙计们，这是关于使用 Integer.parseInt()方法编写 java 程序的。现在，在这篇关于用 java 将二进制转换成十进制的文章中，让我们看看如何编写一个不使用 Integer.parseInt()方法将二进制数转换成十进制数的 Java 程序。

## **使用自定义逻辑的 Java 程序**

要编写一个关于如何在不使用 Integer.parseInt()方法的情况下将二进制数转换为十进制数的 Java 程序，您可以通过在代码中提及二进制数来编写代码，也可以通过用户输入来编写代码。

### **在程序本身中提到二进制数**

```
package sampleprogram;
public class ConvertBinaryToDecimal {
public static int retrieveDecimal(int binarynumber){
int decimalnumber = 0;
int power = 0;
while(true)
{
if (binarynumber == 0)
{
break;
}
else
{
int temp = binarynumber%10;
decimalnumber += temp*Math.pow(2, power);
binarynumber = binarynumber/10;
power++;
}
}
return decimalnumber;
}
public static void main(String args[]){
System.out.println("Decimal value is: "+retrieveDecimal(1110));
System.out.println("Decimal value is: "+retrieveDecimal(0010));
System.out.println("Decimal value is: "+retrieveDecimal(1010));
System.out.println("Decimal value is: "+retrieveDecimal(0110));
System.out.println("Decimal value is: "+retrieveDecimal(1101));
}
}

```

##### **输出:**

### ![Multiple Outputs - How to Convert Binary to Decimal - Edureka](img/55427aec2cfe12fa56fee462438e011e.png)要求用户输入二进制数

```
package sampleprogram;
import java.util.Scanner;
class ConvertBinaryToDecimal
{
public static void main(String args[])
{
Scanner binaryinput=new Scanner(System.in);
System.out.println("Enter the binary number-");
int n=binaryinput.nextInt();
int decimalnumber=0,power=0;
while(n!=0)
{
decimalnumber+=((n%10)*Math.pow(2,power));
n=n/10;
power++;
}
System.out.println(decimalnumber);
}
}

```

##### **输出:**

![User Input and Output - How to Convert Binary to Decimal - Edureka](img/1647677c71a2f60cd79e473a21da97d8.png)

这就把我们带到了这个' *的结尾，Java 中如何把二进制转换成十进制？*‘文章。我们已经学习了如何通过编程将二进制数转换成十进制数。

*如果你发现这篇关于“Java 中如何将二进制转换成十进制？”，查看 Edureka 提供的 [**Java 在线培训**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“如何在 Java**中将二进制转换成十进制”的评论部分提及，我们会尽快回复您。*