# 理解 Java 输入和输出

> 原文：<https://www.edureka.co/blog/understanding-java-input-and-output/>

在进行 java 编程时，Java 输入和输出是一个基本概念。它由输入、输出和流等元素组成。输入是我们给程序的数据。输出是我们从程序得到的结果形式的数据。流表示数据流或数据序列。为了给出输入，我们使用输入流，为了给出输出，我们使用输出流。

[//www.youtube.com/embed/vd9nJK22BwU](//www.youtube.com/embed/vd9nJK22BwU)

## **如何从键盘上读取输入？**

“System.in”代表键盘。要从键盘读取数据，它应该连接到“InputStreamReader”。在“InputStreamReader”中，它从键盘读取数据，并将数据发送到“BufferedReader”。在“BufferedReader”中，它从 InputStreamReader 中读取数据，并将数据存储在缓冲区中。它有一些方法，可以方便地访问数据。

## **读取来自控制台的输入**

输入可以来自文件或关键字。在 java 中，可以通过三种方式从控制台读取输入:

*   缓冲阅读器
*   字符串标记器
*   扫描仪

## **buffered reader–Java 类**

这里，我们使用类“BufferedReader”并创建对象“bufferedreader”。我们还从用户那里获取整数值和字符串。

```
BufferedReader bufferedreader = new BufferedReader(new InputStreamReader(System.in));
```

```
int age = bufferedreader.read();
```

```
String name = bufferedreader.readLine();
```

从 eclipse 窗口中，我们还可以在下面的代码中看到相同的示例:

```
Bufferedreader bufferedreader = new BufferedReader(
```

```
New InputStreamReader(System.in));
```

```
System.out.println(“enter name”);
```

```
String name = bufferedreader.readline();
```

```
System.out.println(“enter age”);
```

```
int age = Integer.parseInt(bufferedreader.readline());
```

```
int age1= bufferedreader.read();
```

```
System.out.println(“I am” + name + “ “+age+”years old”);
```

```
}
```

```
}
```

当我们在 java ide 中运行代码时，它会提示用户输入姓名和年龄，如下所示。

![java output in eclipse](img/c5095da4ee431ab6c0e126f9c7f2c418.png)

## **字符串标记器——Java 类**

它可以用来在一行中接受来自控制台的多个输入，而 BufferedReader 只接受一行中的一个输入。它使用分隔符(空格、逗号)将输入转换成标记。

语法如下:

```
BufferedReader bufferedreader = new BufferedReader(new InputStreamReader(System.in));
```

```
String input = bufferedreader.readline();
```

```
StringTokenizer tokenizer = new StringTokenizer(input, “,”);
```

```
String name = tokenizer.nextToken();
```

```
int age=tokenizer.nextToken();
```

一旦我们进入 eclipse 并打开程序，我们就会看到代码:

```
BufferedReader bufferedreader = new BufferedReader(
```

```
New InputStreamReader(System.in);
```

```
System.out.println(“Enter your name and age separated by comma”);
```

```
String Input = bufferedreader.readLine();
```

```
StringTokenizer tokenizer = new StringTokenizer(Input, “,”);
```

```
String name = Tokenizer.newToken();
```

```
int age = Integer.parseInt(tokenizer.nextToken());
```

```
System.out.println(“I am”+name+age+”years old”);
```

```
}
```

```
}
```

输出将提示用户输入姓名和年龄，用逗号分隔。如果用户输入姓名，然后在空格后写年龄，就会显示异常错误。

## **扫描器——Java 类**

它接受来自文件或键盘的多种输入，并分成多个标记。它有 tokenizer 没有的不同类型输入(int、float、string、long、double、byte)的方法。

语法表示如下:

```
Scanner scanner = new Scanner(System.in);
```

```
int rollno = scanner.nextInt();
```

```
String name =  scanner.next();
```

```
In the Eclipse window we view the following code:
```

```
Scanner.scanner = new Scanner (System.in);
```

```
System.out.println(“Enter your name and age”);
```

```
String name = scanner.next();
```

```
int age=scanner.nextInt();
```

```
System.out.println(“ I am “ “+name” “+age+” years old”);
```

```
}
```

```
}
```

一旦我们运行代码，它会提示用户写下姓名和年龄。

## **将输出写入控制台**

输出可以通过两种方式写入控制台:

第一种方法称为 print (String)

```
System.out.print(“hello”);
```

第二种方法是 write(int)

int input = ' i

```
System.out.write(input);
```

```
System.out.write(‘/n’);
```

一旦我们进入 Eclipse 窗口，我们会看到下面的代码:

```
System.out.print(“hello”);
```

```
System.out.print(“hello”);
```

```
System.out.print(“hello”);
```

```
int Input = ‘a’;
```

```
 System.out.write(Input);
```

```
System.out.write(“In”);
```

```
}
```

```
}
```

一旦我们运行代码，我们会收到输出:

```
‘HelloHelloHello’
```

“Println”是一个接受输入并给出输出的方法。

## **Java 中 I/O 流的类型**

I/O 流可以分为“面向字节的流”和“面向 Unicode 字符的流”。当处理“面向字节的流”时，我们可以处理输入流和输出流。“面向 Unicode 字符的流”包含 Reader 和 Writer 等元素。

这样我们就结束了这篇文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)的 Java 课程。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**![edureka-logo](img/17b384eac14ae8abcfa768bc10276bbe.png)相关帖子:**

[和 Edureka 一起揭开 Java 课程的神奇！](https://www.edureka.co/blog/java-tutorial/ "Unveil the Magic of Java Course with Edureka!")

[面向 Java 专业人士的 Hadoop](https://www.edureka.co/blog/videos/free-webinar-on-hadoop-for-java-professionals/ "Hadoop for Java Professionals")

[学 Java/J2EE&SOA](https://www.edureka.co/java-j2ee-soa-training "Learn Java/J2EE & SOA")