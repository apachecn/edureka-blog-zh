# 关于 Java 中的 StringBuffer，您需要知道的一切

> 原文：<https://www.edureka.co/blog/stringbuffer-in-java/>

Java 中的字符串是一系列不可变的字符。另一方面，StringBuffer 用于创建可变字符序列。在本文中，我们将深入探讨 Java 中 StringBuffer 的概念。本次会议将讨论以下几点:

*   [构造函数](#Constructors)
*   [方法](#Methods)

让我们开始吧，然而，重要的是我们从一些构造函数开始，

## **构造函数**

### **空字符串缓冲区**

创建一个初始容量为 16 个字符的空字符串缓冲区。

```
StringBuffer str=new StringBuffer();
```

### **参数字符串缓冲区**

创建的字符串缓冲区具有参数中指定的大小。

```
StringBuffer str=new StringBuffer(20);
```

### **Str 字串缓冲区**

指定的参数设置 StringBuffer 对象的初始内容，并在不重新分配的情况下为另外 16 个字符保留空间。

```
StringBuffer str=new StringBuffer(“Welcome”);
```

让我们继续 Java 文章中的 StringBuffer，

## **方法**

StringBuffer 中使用的方法指定如下:

### **Java 中的 string buffer:length()**

它指定了存在的元素数量。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("JohnDoe");
int q = str.length();
System.out.println("Length : " + q);
}
}

```

**输出:**

长度:7

### **容量():**

使用这个方法可以找到 StringBuffer 的容量。

```
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("JohnDoe");
int q = str.capacity();
System.out.println("Capacity :" + q);
}
}

```

**输出:**

容量:23

**Java 中的 string buffer:append():**

方法用于在 StringBuffer 的末尾添加元素。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("John");
str.append("Doe");
System.out.println(str); // appends a string
str.append(5);
System.out.println(str); // appends a number
}
}

```

**输出:**

某人

约翰多 5

### **insert():**

方法用于在指定的索引位置插入元素。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockRoll");
str.insert(4, "and");
System.out.println(str);
str.insert(0, 5);
System.out.println(str);
str.insert(5, 69.70d);
System.out.println(str);
str.insert(6, 69.42f);
System.out.println(str);
char arr[] = { 'h', 's', 'w', 'p', 'a' };
str.insert(2, arr);
System.out.println(str);
}
}

```

**输出:**

洛克德罗尔

5RockandRoll

5Rock69.7andRoll

5Rock669.429.7andRoll

5Rhswpaock669.429.7andRoll

### **Java 中的 string buffer:reverse():**

方法用于反转 StringBuffer 中存在的元素。

```

import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockandRoll");
str.reverse();
System.out.println(str);
}
}

```

**输出:**

洛尔德纳克科尔

### **delete(int startIndex，int endIndex)**

方法用于删除 StringBuffer 中存在的元素。要删除的第一个字符由第一个索引指定。startIndex 和 endIndex-1 之间的元素被删除。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockAndRoll");
str.delete(0, 4);
System.out.println(str);
}
}

```

**输出:**

AndRoll

### **Java 中的 string buffer:delete charat(int index)**

方法移除 StringBuffer 中存在的字符串内的单个字符。int 索引指定字符的位置。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockAndRoll");
str.deleteCharAt(5);
System.out.println(str);
}
}

```

**输出:**

RockAdRoll

### **替换()**

方法用于在 StringBuffer 中用一组元素或字符替换另一组元素或字符。此方法中存在参数 startIndex 和 endIndex。从 startIndex 到 endIndex -1 的子字符串被替换。

```
import java.io.*;
class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockAndRoll");
str.replace(4, 7, "nor");
System.out.println(str);
}
}

```

**输出:**

罗克诺罗尔

**ensureCapacity()**

通过这种方法可以增加 StringBuffer 的容量。新容量要么是用户指定的值，要么是当前容量的两倍加 2，具体取决于容量大小。

举例:如果 16 是当前容量:(16*2)+2。

```
class Main{
public static void main(String args[]){
StringBuffer str=new StringBuffer();
System.out.println(str.capacity()); //initial capacity
str.append("Rock");
System.out.println(str.capacity()); //now 16
str.append("My name is John Doe");
System.out.println(str.capacity()); //(oldcapacity*2)+2
str.ensureCapacity(10); //no change
System.out.println(str.capacity());
str.ensureCapacity(50); //now (34*2)+2
System.out.println(str.capacity()); //now 70
}
}

```

**输出:**

Sixteen

Sixteen

Thirty-four

Thirty-four

Seventy

**string buffer appendCodePoint(int code point)**

在这个方法中，代码点的字符串表示被添加到 StringBuffer 中的字符中。

```
import java.lang.*;
public class Main {
public static void main(String[] args)
{
StringBuffer str = new StringBuffer("RockAndRoll");
System.out.println("StringBuffer : " + str);
//Appending the CodePoint as a string
str.appendCodePoint(70);
System.out.println("StringBuffer with codePoint : " + str);
}
}

```

**输出:**

StringBuffer : RockAndRoll

带有代码点的 string buffer:rockan droll f

### **Java 中的 string buffer:****int codePointAt(int index)**

在这个方法中，在索引处返回字符的“Unicodenumber”。索引的值必须介于 0 和长度-1 之间。

```
class Main {
public static void main(String[] args)
{
//creating a StringBuffer
StringBuffer s = new StringBuffer();
s.append("RockAndRoll");
//Getting the Unicode of character at position 7
int unicode = s.codePointAt(7);
//Displaying the result
System.out.println("Unicode of Character at index 7 : " + unicode);
}
}

```

**输出:**

索引 7 : 82 处的 Unicode 字符

### **String toString()**

这个内置方法输出一个表示 StringBuffer 中数据的字符串。声明并初始化一个新的 String 对象，以从 StringBuffer 对象中获取字符序列。然后，toString()返回字符串 sis。

```
import java.lang.*;
class Main {
public static void main(String[] args)
{
StringBuffer s = new StringBuffer("RockAndRoll");
System.out.println("String : " + s.toString());
}
}

```

**输出:**

字符串:RockAndRoll

### **Java 中的 string buffer:****void trim tosize()**

trimToSize()是一个内置的方法。字符序列的容量是用这种方法修剪的。

```
import java.lang.*;
class Main {
public static void main(String[] args)
{
StringBuffer s = new StringBuffer("RockAndRoll");
//adding another element
s.append("Pop");
// isplaying initial capacity
System.out.println("Capacity before trimming : " + s.capacity());
//Trimming
s.trimToSize();
//Displaying the string
System.out.println("String = " + s.toString());
//Displaying trimmed capacity
System.out.println("Capacity after trimming : " + s.capacity());
}
}

```

**输出:**

修剪前的容量:27

字符串:rockandrollpop

修整后的容量:14

***本文中提到的各种方法都可以相应地与 java 中的 StringBuffer 类一起使用。这些方法是有效的，并且允许用户容易地修改字符串。***

这样，我们就结束了这篇关于“Java 中的 StringBuffer”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。