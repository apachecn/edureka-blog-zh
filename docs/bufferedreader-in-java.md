# Java 中的 BufferedReader:如何从输入流中读取文本

> 原文：<https://www.edureka.co/blog/bufferedreader-in-java/>

*Java* 提供了几种机制来读取[文件](https://www.edureka.co/blog/file-handling-in-java/)。有助于执行这个操作的一个重要类是 *BufferedReader* 。所以，这篇关于 Java 中的 BufferedReader 的文章将会帮助你理解 Bufferedreader 类和例子。以下是本博客涵盖的主题:

*   [Java 中的 BufferedReader 是什么？](#reader)
*   [BufferedReader 类声明](#declaration)
*   [Java BufferedReader 构造函数](#constructors)
*   [方法&描述](#methods)
*   [扫描仪和缓冲阅读器的区别](#difference)
    *   [JDK 7 例子中的 buffered reader](#jdk7)
    *   [通过 InputStreamReader 和 BufferedReader 从控制台读取数据](#inputstreamreader)
    *   [从控制台读取数据，直到用户写入停止](#consolestop)

## **Java 中的 BufferedReader 是什么？**

BufferedReader 是一个从输入流中读取文本的 Java 类。它对字符进行缓冲，以便能够高效读取字符、[数组](https://www.edureka.co/blog/java-array/)等。它继承了 reader 类并使代码高效，因为我们可以用 readline() [方法](https://www.edureka.co/blog/java-methods/)逐行读取数据。在 Java 中使用 BufferedReader 类时，我们必须记住几个要点。

*   我们可能必须指定缓冲区大小，即使默认的大小对于任何目的都足够大。
*   随着每一个请求由一个相应的阅读器发出，一个读请求也由一个底层字符发出。
*   总是建议用 BufferedReader 类包装任何阅读器，比如 InputStreamReaders。
*   对于使用 DataInputStream 进行文本输入的程序，一个合适的 BufferedReader 会替换 data input stream 来对其进行本地化。

## **BufferedReader 类声明**

```
public class BufferedReader extends Reader

```

## **Java BufferedReader 构造函数**

| **构造器** | **描述** |
| 缓冲阅读器 | 这个构造函数创建一个缓冲字符输入流，它在默认大小的输入缓冲区上工作。 |
| BufferedReader(Reader reader，int size) | 它使用指定大小的输入缓冲区来缓冲字符输入流。 |

## **方法和描述**

下面是我们对 Java BufferedReader 类的描述。

| **方法** | **描述** |
| int read() | 读取单个字符 |
| 字符串读取线() | 它读取一行文本 |
| 无效复位() | 将流重新定位到上次调用 mark 方法的位置 |
| int read(char[] cb，int off，int len) | 读取数组的一部分中的字符 |
| 布尔标记 Supported() | 它测试输入流对重置和标记方法的支持 |
| 布尔就绪() | 它检查输入流是否准备好读取 |
| 长跳跃(长 n) | 跳过字符 |
| 无效关闭() | 它关闭输入流 |
| void 标记(int readAheadLimit) | 用于标记流中的当前位置 |

**举例:**

```
import java.io.*;
public class Example{
public static void main(String args[] throws Exception)
{
FileReader f = new FileReader("filelocation");
BufferedReader b = new BufferedReader(f);

int i ;
while((i = b.read()) != -1){
System.out.println((char) i);
}
b.close();
f.close();

```

## **扫描仪和 BufferedReader 的区别**

| 缓冲器 | **扫描仪** |
| 同步，应该与多线程一起使用 | 不同步，不用于多线程 |
| 缓冲存储器更大 | 缓冲存储器更小 |
| 比扫描仪快 | 较慢，因为它解析输入数据 |
| 没有与 nextline()方法相关的歧义 | nextline()方法有很多问题。 |
| 使用缓冲从字符输入流中读取字符 | 这是一个简单的文本扫描器，可以解析原始类型和字符串 |

## **JDK 7 例子中的 buffered reader**

```
import java.io.*;
public class Example{
public static void main(String[] args){
try( BufferedReader b = new BufferedReader(new fileReader("filename")));
{
String s;
while((s = b.readLine()) != null){
System.out.println(s);
}
}
catch(IOException e)
{
e.printStackTrace();
}
}
}

```

## **Java 中的 InputStreamReader 和 BufferedReader 从控制台读取数据**

```
import java.io.*;
public class Example{
public static void main(String args[] throws Exception){
InputStreamReader i = new InputStreamReader(system.in);
BufferedReader b = new BufferedReader(i);
System.out.println("Enter Course");
String course = b.readLine();
System.out.pritln("Edureka" + course);
}
} 

```

```
Output:Enter Course
       Java
       Edureka Java
```

## **从控制台读取数据，直到用户写入停止**

```
import java.io.*;
public class Example{
public static void main(String args[] throws Exception){
InputStreamReader i = new InputStreamReader(system.in);
BufferedReader b = new BufferedReader(i);
string course = "";
while(!name.equals("stop")){
System.out.println("enter course:");
course = b.readLine();
System.out.println("Course is:" + course);
}
b.close();
i.close();
} 
}

```

```
Output: enter course:
        Course is: Java
        enter course:
        Course is: stop
```

这就把我们带到了本文的结尾，在这里我们学习了如何使用 Java 中的 BufferedReader 类从字符输入流中读取字符。希望你清楚本教程中与你分享的所有内容。

*如果你觉得这篇关于“Java 中的 BufferedReader”的文章很有意义，那就去看看 Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训吧，这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

我们在这里帮助你踏上旅程的每一步，并为想成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念，以及各种 Java 框架，如[Hibernate](https://www.edureka.co/blog/what-is-hibernate-in-java/)&[Spring](https://www.edureka.co/blog/spring-tutorial/)。

如果您遇到任何问题，请在“Java buffered reader”的评论区提出您的所有问题，我们的团队将很乐意回答。