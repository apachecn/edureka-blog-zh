# 知道如何在 Java 中反转字符串——初学者指南

> 原文：<https://www.edureka.co/blog/reverse-a-string-in-java/>

字符串是一个字符序列，在 Java 中被认为是一个对象。在 **[Java](https://www.edureka.co/blog/java-tutorial/)** 中，有各种可以对字符串对象执行的操作。字符串对象上最广泛使用的操作之一是字符串反转。在本文中，我将告诉您在 Java 中反转[字符串的各种方法。](https://www.edureka.co/blog/java-string/)

在 Java 中，一个字符串有五种不同的反转方式。它们如下:

1.  [使用 CharAt 方法反转字符串](#ReverseaStringusingtheTraditionalApproach)
2.  [使用字符串缓冲器/字符串生成器方法进行字符串反向](#StringreverseusingStringBuffer/StringBuilderApproach)
3.  [使用反向迭代方法反转字符串](#ReverseaStringusingReverseIterativeApproach)
4.  [使用递归进行字符串反转](#StringreverseusingRecursion)
5.  [反转字符串中的字母](#ReversetheletterspresentintheString)

现在让我们从理解如何使用 CharAt 方法在 Java 中[反转一个字符串](https://www.edureka.co/blog/cheatsheets/java-string-cheat-sheet/)开始，深入了解每种方法的细节。

## **1。使用 CharAt 方法反转字符串**

下面给出的 Java 程序将帮助你理解如何反转用户输入的字符串。这里，我使用了 ***CharAt()*** 方法来从输入字符串中提取字符。 ***CharAt()*** 方法的主要任务是返回给定字符串中指定索引处的字符。然后，我将它们以相反的顺序追加，以反转给定的字符串。这是 Java 中反转字符串的简单方法之一。

```
package Edureka;
import java.util.*;
public class StringReverse{
public static void main(String args[]) {
String initial, rev="";
Scanner in=new Scanner(System.in);
System.out.println("Enter the string to reverse");
initial=in.nextLine();
int length=initial.length();
for(int i=length-1;i>=0;i--)
  rev=rev+initial.charAt(i);
System.out.println("Reversed string: "+rev);
}
}

```

当您执行这个程序时，输出如下所示:

```
Enter the string to reverse
HELLO EDUREKA
Reversed string: AKERUDE OLLEH

```

我希望你理解了如何用这个简单的方法反转一个给定的 Java 字符串。现在让我们进一步理解如何使用*字符串缓冲区/ StringBuilder 类反转字符串。*

## **2。使用字符串生成器/字符串缓冲类**反转字符串

StringBuffer 和 StringBuilder 由一个内置方法 ***reverse()*** 组成，用于反转 StringBuffer 中的字符。该方法以相反的顺序替换字符序列。下面是使用 StringBuffer 类的内置方法反转字符串的代码。

```
package Edureka; 
import java.util.*; 
public class StringRev{
// Function to reverse a string in Java using StringBuilder
public static String rev(String s){
return new StringBuilder(s).reverse().toString();
}
public static void main(String[] args){
String s= "Welcome to Edureka"; // Note that string is immutable in Java
s= rev(s);
System.out.println("Result after reversing a string is : "+s);
}
}
```

执行上述代码时，输出如下所示:

```
Result after reversing a string is : akerudE ot emocleW
```

这都是关于 StringBuilder 类的。或者，您也可以使用一个 **StringBuffer** 类 *reverse()* 方法，就像 **StringBuilder** 一样。让我们看看下面的代码。

```
package Edureka;
import java.util.*; 
public class StringRev{
 // Function to reverse a string in Java using StringBuffer
public static String rev(String s){ 
return new StringBufferr(s).reverse().toString(); 
} 
public static void main(String[] args){ 
String s= "Welcome to Edureka"; 
// Note that string is immutable in Java
 s= rev(s); 
System.out.println("Result after reversing a string is : "+s); 
} 
}
```

当您运行程序时，输出将与 StringBuilder 类的输出相同。

**注意:** *你可以使用上面程序中的 StringBuffer reverse()反转为 String，也可以简单地使用如下所示的代码逻辑:*

```
StringBuffer sb =new StringBuffer("JavaEdureka");
System.out.println(sb.reverse());
Output: akerudEavaJ
```

StringBuilder 和 StringBuffer 都有相同的在 [Java](https://docs.oracle.com/javase/tutorial/) 中反转字符串的方法。但是，StringBuilder 是首选，因为它不是同步的，并且比 StringBuffer 快。理解了这一点，让我们更深入地研究这篇文章，学习另一种在 Java 中反转字符串的方法。

## **3。使用反向迭代反转字符串**

在这种方法中，我首先使用 **CharArray()** 方法将给定的字符串转换为字符数组。之后，我刚刚以相反的顺序迭代了给定的数组。

```
package Edureka;
import java.util.*;
public class StringRev{
// Function to reverse a string in Java 
public static String reverseString(String s){
//Converting the string into a character array
char c[]=s.toCharArray();
String reverse="";
//For loop to reverse a string
for(int i=c.length-1;i>=0;i--){
reverse+=c[i];
}
return reverse;
}

public static void main(String[] args) {
System.out.println(reverseString("Hi All"));
System.out.println(reverseString("Welcome to Edureka Blog"));
}
}
```

输出:

```
llA iH
golB akerudE ot emocleW
```

我希望你理解了如何在 Java 中使用反向迭代的方法来反转一个字符串。现在让我们进一步理解使用递归来反转一个[字符串](https://www.edureka.co/blog/java-string/)。

## **4。使用递归进行字符串反转**

**递归**不过是一个调用自身的函数。在这种方法中，我将编写一个方法，它通过递归调用自身来反转字符串。让我们实现并检查它是如何工作的。

```
package Edureka;
import java.util.*;
public class StringRecursion{
String rev(String str) {
if(str.length() == 0)
return " ";
return str.charAt(str.length()-1) + rev(str.substring(0,str.length()-1)); }
public static void main(String[ ] args) {
StringRecursion r=new StringRecursion();
Scanner sc=new Scanner(System.in);
System.out.print("Enter the string : ");
String s=sc.nextLine();
System.out.println("Reversed String: "+r.rev(s)); }
}
```

输出:

```
Enter the string : Java is the blooming technology since its existence
Reversed String: ecnetsixe sti ecnis ygolonhcet gnimoolb eht si avaJ
```

在上面的代码中，我为类 String revision***【r .***创建了对象，然后，我使用 ***sc.nextLine()*** 读取了输入的字符串，并将其存储在字符串变量 ***s*** 中。最后，我把逆向方法称为 ***r.rev(s)*** 。理解了这一点，现在让我们来理解本文中的最后一种方法。在这里，我将告诉你如何反转给定字符串中的字母。

## **5。反转字符串**中的字母

这个 *Java* 程序反转用户输入的 S *字符串* 中的字母。它不像前面的方法那样反转整个字符串。例如: **Hello People** 将被称为 **olleH elpoeP。**让我们用 Java 实现同样的功能。

```
package Edureka;
public class stringreverse {
public static void main(String[] args) {
// TODO Auto-generated method stub
String str = "Welcome To Edureka";
String[] strArray = str.split(" ");
for (String temp: strArray){
System.out.println(temp);
}
for(int i=0; i<3; i++){ char[] s1 = strArray[i].toCharArray(); for (int j = s1.length-1; j>=0; j--)
{System.out.print(s1[j]);}
System.out.print(" ");
}
}
}
```

上述程序的输出如下所示:

```
Welcome
To
Edureka
emocleW oT akerudE
```

所以，这就是给定字符串中字母的反转。这就把我们带到了关于在 Java 中反转一个[字符串的文章的结尾。我希望你发现它信息丰富。](https://www.edureka.co/blog/cheatsheets/java-string-cheat-sheet/)

**Java 字符串教程| Java 中的字符串操作|面向初学者的 Java 教程| Edureka**

[https://www.youtube.com/embed/N63JCXwdd14](https://www.youtube.com/embed/N63JCXwdd14)

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“用 Java**反转一个字符串”文章的评论部分提到它，我们会尽快回复你，或者参加我们在巴东的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-padang)*