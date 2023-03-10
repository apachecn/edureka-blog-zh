# Java 中如何把 Char 转换成 String？

> 原文：<https://www.edureka.co/blog/char-to-string-in-java/>

这篇文章将帮助你探索一个很难注意到但在编程世界中具有巨大价值的概念，我指的是在 [Java](https://www.edureka.co/blog/java-tutorial/) 中将 Char 转换成 String。本文将涉及以下几点:

*   [使用 String.valueOf(char ch)](#UsingStringvalueOf(charch))
*   [使用 Character.toString(char ch)](#UsingCharactertoString(charch))

在用 java 编写程序时，经常需要将字符转换成字符串。有多种方法可以实现它，其中一些是:

*   通过使用 String 类的 String.valueOf(char)方法
*   通过使用 Character 类的 Character.toString(char)方法

继续这篇关于 Java 中字符到字符串的文章

## **使用 String.valueOf(char ch):**

String 类的这个方法可用于将指定的字符转换为字符串。接受 Char 作为参数，并返回该参数的等效字符串。

```
public class CharToString{  
public static void main(String args[]){  
//given char
char character = 'S';
//char to string conversion
String string = String.valueOf(character);  
//displaying the string
System.out.println("String after conversion : "+string);    
}a
}

```

转换后的输出:字符串:S

继续这篇关于 Java 中字符到字符串的文章

## **使用 Character.toString(char ch):**

Character 类的这个方法也可以用来将指定的字符转换成字符串。

```

public class CharToString{  
public static void main(String args[]){  
// char charcater with the value 'Q'
char character = 'Q';
//char to String using toString() method
String string = Character.toString(character);  
//Value of the string after conversion is "Q"
System.out.println("String after conversion : "+string);    
}
}

```

**输出:** 字符串转换后:Q

Java 为用户提供了将字符转换成字符串的有效方法。

这样我们就结束了这篇文章。如果你想了解更多，可以去看看 Edureka 值得信赖的在线学习公司提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。