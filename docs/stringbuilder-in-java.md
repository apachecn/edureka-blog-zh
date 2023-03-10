# 你需要知道的 Java StringBuilder 的一切

> 原文：<https://www.edureka.co/blog/stringbuilder-in-java/>

在编程方面，Java 给了你各种各样的特性。本文将重点讨论 Java 中的 StringBuilder。以下是本文中讨论指针:

*   [Java 中的 StringBuilder](#StringBuilderinJava)
*   [Java 中的构造函数](#ConstructorsInJava)
*   [StringBuilder 方法](#StringBuilderMethods)

那么让我们开始吧，

## **Java 中的 StringBuilder**

java 中的字符串是一系列不可变的字符。另一方面，StringBuffer 用于创建可变字符序列。StringBuilder 类似于 StringBuffer 类，但是它不提供任何同步保证。然而，在大多数实现中，它实际上要快得多。必须注意的是，StringBuilder 类被多线程使用是不安全的。

## **构造函数**

*   **StringBuilder( ):** 创建一个初始容量为 16 个字符的空字符串生成器。
*   **StringBuilder(int capacity):):**创建的字符串生成器具有参数中指定的容量。
*   **StringBuilder(CharSequence seq**):创建的字符串生成器包含与指定的 char sequence 相同的字符。
*   **StringBuilder(String str** ):构造一个字符串生成器，初始化为指定字符串的内容。

让我们继续这篇文章，看看不同的方法

**StringBuilder 方法**

StringBuilder 类中使用了以下方法:

### **追加方法**

此方法将指定的元素添加到现有字符串中。

```
class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder("Rock");
str.append("Roll");
System.out.println(str);
}
}

```

**输出:**

摇滚

### **Java 中的 StringBuilder:插入方法**

此方法在指定的索引处插入一个字符串。

```
public class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder("Rock ");
str.insert(2,"Roll");
System.out.println(str);
}
}

```

**输出:**

罗洛克

### **替换方法**

此方法将字符串从指定的 beginIndex 替换为 endIndex。

```
public class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder("Rock");
str.replace(1,3,"Roll");
System.out.println(str);
}
}

```

**输出:**

罗尔克

### **Java 中的 StringBuilder:Delete 方法**

此方法删除从 beginIndex 到 endIndex 的特定字符串。

```
public class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder("Rock");
str.delete(1,3);
System.out.println(str);
}
}

```

**输出:**

放射状角膜切开术

### **反向方法**

此方法反转 StringBuilder 中的字符串。

```
public class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder("Rock");
str.reverse();
System.out.println(str);
}
}

```

**输出:**

kcoR

### **容量法**

通过这种方法可以确定生成器的当前容量。必须注意，构建器的默认容量是 16。生成器的容量可以增加:(旧容量*2)+2。

```

public class Main{
public static void main(String args[]){
StringBuilder str=new StringBuilder();
System.out.println(str.capacity());
str.append("Rock");
System.out.println(str.capacity());
str.append("It is a good day to rock");
System.out.println(str.capacity());
}
}

```

**输出:**

Sixteen

Sixteen

Thirty-four

至此，我们已经结束了这篇关于“Java 中的 StringBuilder”的文章。如果你想了解更多， 请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。