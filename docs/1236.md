# Java 中的拆分方法:如何在 Java 中拆分一个字符串？

> 原文：<https://www.edureka.co/blog/split-string-method-in-java/>

拆分[字符串](https://www.edureka.co/blog/java-string/)是编码时非常频繁执行的操作。在 Java 中有许多方法可以拆分字符串，但最常用的方法是使用 String split()方法。本文重点介绍如何在 [Java](https://www.edureka.co/blog/java-tutorial/) 中使用 ***拆分方法*** 拆分字符串。

下面列出了本文涉及的主题:

*   [Java 中的拆分方法](#SplitMethod)
*   [使用没有限制参数](#WithoutLimit)的 split()方法
    *   [使用 omma 作为分隔符拆分字符串](#comma)
    *   [使用空格作为分隔符分割字符串](#whitespace)
    *   [使用点作为分隔符分割字符串](#dot)
    *   [使用字母作为分隔符拆分字符串](#letter)
    *   [使用多个分隔符分割字符串](#delimiters)
*   [使用带极限参数](#WithLimit)的 split()方法
    *   [演示极限参数使用的示例程序](#ExampleWithLimit)

## **Java 中的拆分方法**

Java 中的 **String 类**提供了一个 *split()* 方法，该方法可用于根据匹配正则表达式的分隔符将一个字符串拆分成一个字符串对象的[数组](https://www.edureka.co/blog/java-array/)。例如，给定以下字符串:

```
String s = "Welcome, To, Edureka!";
```

您可以使用下面这段代码将字符串分割成子字符串:

```
String[] result = s.split(",");
```

更准确地说，该表达式会将字符串分解成子字符串，其中子字符串由 *分隔符* 字符分隔。在上面的例子中，输入字符串“Welcome，To，Edureka”被分成三个字符串对象，即:

***Welcome******To******Edureka!***

在 [Java](https://www.edureka.co/blog/what-is-java/) 中，split()方法有两种变体。让我们逐一讨论一下。

## **使用没有限制参数的 split()方法**

这个 *split()* 方法的变体接受一个正则表达式作为参数，并根据正则表达式 *regex* 断开给定的字符串。这里的默认限制是 0。下面列出了语法、参数、返回值、[抛出的异常](https://www.edureka.co/blog/java-exception-handling)以及大量演示该概念的示例程序。

**语法:**public String[]split(String regex)

**参数:** regex(一个定界正则表达式)

**返回值:**一个 S *tring* 对象的数组

**异常:***PatternSyntaxException*，如果提供的正则表达式的语法无效

**例 1:** 调用字符串对象上的 ***split()*** 方法——用逗号分割

```
package MyPackage;

public class Method1 { 
    public static void main(String args[]) 
    { 
    	String str = "We're,Ridiculously,Committed!"; 
        String[] arrOfStr = str.split(","); 
         System.out.println("Number of substrings: "+arrOfStr.length);

         for(int i=0; i< arrOfStr.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr[i]);
         }

    } 
}  
```

**输出**

```
Number of substrings: 3
str[0] : We're
str[1] : Ridiculously
str[2] : Committed!

```

**例 2:** 调用字符串对象上的 ***split()*** 方法——按空格拆分

```
package MyPackage;

public class Method2 { 
    public static void main(String args[]) 
    { 
    	String str = "We're Ridiculously Committed! Welcome"; 
        String[] arrOfStr = str.split(" "); 
         System.out.println("Number of substrings: "+arrOfStr.length);

         for(int i=0; i< arrOfStr.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr[i]);
         }

    } 
}  
```

**输出**

```
Number of substrings: 4
str[0] : We're
str[1] : Ridiculously
str[2] : Committed!
str[3] : Welcome

```

**例 3:** 调用字符串对象上的 ***split()*** 方法——用点分割

```
package MyPackage;

public class Method3 { 
    public static void main(String args[]) 
    { 
    	String str = "We're.Ridiculously.Committed.Welcome"; 
        String[] arrOfStr = str.split("."); 
         System.out.println("Number of substrings: "+arrOfStr.length);

         for(int i=0; i< arrOfStr.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr[i]);
         }

    } 
}  
```

**输出**

```
Number of substrings: 4
str[0] : We're
str[1] : Ridiculously
str[2] : Committed
str[3] : Welcome

```

**例 4:** 调用字符串对象上的 ***split()*** 方法——用字母拆分

```
package MyPackage;

public class Method4 { 
    public static void main(String args[]) 
    { 
    	String str = "We're Ridiculously Committed! Welcome"; 
        String[] arrOfStr = str.split("W"); 
         System.out.println("Number of substrings: "+arrOfStr.length);

         for(int i=0; i< arrOfStr.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr[i]);
         }

    } 
}  
```

**输出**

```
Number of substrings: 3
str[0] : 
str[1] : e're Ridiculously Committed! 
str[2] : elcome

```

**例 5:** 调用字符串对象上的 ***split()*** 方法——通过多个分隔符进行拆分

```
package MyPackage;

public class Method5 { 
    public static void main(String args[]) 
    { 
    	String str = "We're, Ridiculously Committed! Welcome to Eduerka.Hello"; 
        String[] arrOfStr = str.split("[, .!]+"); 
         System.out.println("Number of substrings: "+arrOfStr.length);

         for(int i=0; i< arrOfStr.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr[i]);
         }

    } 
}  
```

**输出**

```
Number of substrings: 7
str[0] : We're
str[1] : Ridiculously
str[2] : Committed
str[3] : Welcome
str[4] : to
str[5] : Eduerka
str[6] : Hello

```

很简单，对吧？但是，如果在拆分操作之后，您只需要前 n 个元素，但希望字符串的其余部分保持原样，该怎么办呢？为此，我们有 s *plit()* 方法的另一个变体。

## **使用带*极限*参数**的 split()方法

当我们希望将字符串拆分成有限数量的字符串时，使用 split()方法的这种变体。split()方法的这个变体与其他变体之间的唯一区别是，它限制了拆分后返回的字符串数量。该限制可以作为一个输入参数提供给 *split()方法。*限制参数控制应用模式的次数，因此影响生成的数组的长度。

下面列出的是语法、参数、返回值、抛出的异常和许多演示这个概念的示例程序。

**语法:**公共 String[] split(String regex，int limit)

**参数:**

*   正则表达式–一个定界正则表达式
*   极限–产生的阈值

极限可以有 3 个值，分别是:

1.  ***极限> 0:*** 如果极限为正，那么模式最多应用极限-1 次。得到的数组的长度不会大于 n，数组的最后一个条目将包含最后一个匹配的分隔符之外的所有输入。
2.  ***限制< 0:*** 如果限制为正，那么该模式将被应用尽可能多的次数，并且结果数组可以具有任何长度。
3.  ***limit = 0:*** 如果 limit 等于 0，则该模式将被应用尽可能多的次数，得到的数组可以是任意长度，但尾部的空字符串将被丢弃。

**返回值:**根据*限制*参数拆分给定字符串计算出的*字符串*对象数组

**异常:***PatternSyntaxException*，如果提供的正则表达式的语法无效

**示例:**使用*限制*参数在字符串对象上调用 *split()* 方法

```
package MyPackage;

public class SplitMethod { 
    public static void main(String args[]) 
    { 
    	String str = "468-567-7388";
        String[] arrOfStr1 = str.split("8",2); 
        System.out.println("Output when limit is +ve");
         System.out.println("Number of substrings: "+arrOfStr1.length);

         for(int i=0; i<arrOfStr1.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr1[i]);
         }

         String[] arrOfStr2 = str.split("8",-3); 
         System.out.println("nOutput when limit is -ve");
         System.out.println("Number of substrings: "+arrOfStr2.length);

         for(int i=0; i<arrOfStr2.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr2[i]);
         }
         String[] arrOfStr3 = str.split("8",0); 
         System.out.println("nOutput when limit is 0");
         System.out.println("Number of substrings: "+arrOfStr3.length);

         for(int i=0; i<arrOfStr3.length; i++)
         {
             System.out.println("str["+i+"] : "+arrOfStr3[i]);
         }
    } 
}  
```

**输出:**

```
Output when limit is +ve
Number of substrings: 2
str[0] : 46
str[1] : -567-7388

Output when limit is -ve
Number of substrings: 4
str[0] : 46
str[1] : -567-73
str[2] : 
str[3] : 

Output when limit is 0
Number of substrings: 2
str[0] : 46
str[1] : -567-73

```

上面的程序演示了当指定了*限制*参数时，split()方法是如何工作的。正如您从输出中看到的:

1.  当限制为 2 时，结果数组中子字符串的数量为 2
2.  当限制为-3 时，输入字符串被分成 4 个子字符串，包括尾随空格
3.  当限制为 0 时，输入字符串被分成 2 个子字符串，因为尾部空格被排除在外

“Java 中的拆分方法”这篇文章到此结束。我已经讲述了 Java 的一个基本主题，即如何在 Java 中使用 *split()方法*来拆分字符串。 希望你清楚本文与你分享的一切。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“如何在 Java 中把 int 转换成 String”**文章的评论部分提到它，我们会尽快回复你。*