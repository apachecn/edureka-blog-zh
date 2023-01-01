# 关于 Java 中的包装类，你需要知道的就是:自动装箱和取消装箱

> 原文：<https://www.edureka.co/blog/wrapper-class-in-java/>

Java 编程语言是当今最流行的编程语言之一。随着[变量、数据类型](https://www.edureka.co/blog/data-types-in-java/)、[类和对象](https://www.edureka.co/blog/java-tutorial/#obj)等概念的出现，java 中的另一个重要概念是包装类，它对于[多线程](https://www.edureka.co/blog/java-thread/)、[集合框架](https://www.edureka.co/blog/java-collections/)等中的[同步](https://www.edureka.co/blog/synchronization-in-java/)是必不可少的。在本文中，我们将通过各种例子来讨论 java 中对包装类的需求。以下是本博客中讨论的概念:

*   [什么是 Java 包装类？](#wrapperclass)
*   [需要 Java 中的包装类](#need)
*   [自动装箱](#autoboxing)
*   [拆箱](#unboxing)

## **什么是 Java 包装类？**

包装类提供了一种将原始数据类型转换为包装类对象的机制。下面是基本数据类型的等价包装类对象。

| **原始数据类型** | **包装类** |
| （同 Internationalorganizations）国际组织 | 整数 |
| 茶 | 性格；角色；字母 |
| 漂浮物 | 浮动 |
| 布尔型 | 布尔代数学体系的 |
| 两倍 | 两倍 |
| 短的 | 短的 |
| 长的 | 长的 |
| 字节 | 字节 |

下面的例子展示了如何创建 java 包装类对象。

```
class wrapperClass{
public static void main(String args[]){
Integer myInt = 5;
Character myChar = "Edureka";
System.out.println(myInt);
System.out.println(myChar);
}
}

```

```
Output : 5
Edureka
```

在上面的程序中，我们使用了包装类而不是原始数据类型。

下面是从包装对象获取相关值的[方法](https://www.edureka.co/blog/methods-and-method-overloading-in-java/)。

1.  intValue()
2.  byteValue()
3.  shortValue()
4.  longValue()
5.  doubleValue()
6.  charValue()
7.  floatValue()
8.  booleanValue()

下面是在程序中使用这些方法的示例:

```
class wrapperClass{
public static void main(String args[]){

Integer myInt = 10;
Character myChar = "edureka";
Float myFloat = 10.25;
System.out.println(myInt.intValue());
System.out.println(myChar.charValue());
System.out.println(myFloat.floatValue());
}
}

```

```
Output : 10
edureka
10.25
```

类似地，您可以使用其他方法，如 doubleValue()、shortValue()、longValue()、byteValue()来获取包装类对象的相应值。

## **需要 Java 包装类**

*   它们将原始数据类型转换成对象。
*   修改方法中的参数需要对象。
*   java.util [包](https://www.edureka.co/blog/packages-in-java/)中的类只适用于对象。
*   [集合框架](https://www.edureka.co/blog/java-collections/)中的数据结构只存储对象。
*   对象在[多线程](https://www.edureka.co/blog/java-thread/#multithreading)中帮助同步。

## **自动装箱**

自动装箱是将原始数据类型自动转换成其相应包装类的对象。

```
import java.util.ArrayList;
class Autoboxing {
public static void main(String args[]){
char ch = 'e';
Character e = ch;
ArrayList<Integer> arraylist = new ArrayList<Integer>();
arraylist.add(10);
System.out.println(arraylist.get(0));
}
}

```

```
Output : 10
```

## **拆箱**

这与自动装箱相反，其中包装类[对象](https://www.edureka.co/blog/java-tutorial/#obj)被转换成它们相应的原始数据类型。

```
import java.util.ArrayList;
class Unboxing{
public static void main(String args[])
{
Character ch = 'e';
char 'e' = ch;

ArrayList<Integer> arraylist = new ArrayList<Integer> ();
arraylist.add(10);
int number = arraylist.get(0);
System.out.println(number);
}
}

```

```
Output: 10
```

在本文中，我们讨论了 java 中的包装类，它有助于将原始数据类型转换成它们各自的对象。它有助于多线程和各种其他应用程序中的同步。Java 是一种多功能语言，具有丰富的高效和革命性的概念。业界要求现代开发人员事先彻底了解编程语言的基本概念，通过 Edureka 的 [Java 认证项目](https://www.edureka.co/java-j2ee-training-course)掌握 Java 技能，并开始学习成为一名 Java 开发人员。

有问题要问我们吗？请在“Java 中的包装类”文章的评论部分提到这一点，我们会尽快回复您。