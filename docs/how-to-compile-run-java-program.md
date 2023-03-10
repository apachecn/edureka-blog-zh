# 如何编译运行你的第一个 Java 程序？

> 原文：<https://www.edureka.co/blog/how-to-compile-run-java-program/>

高级语言如 [Java](https://www.edureka.co/blog/java-tutorial/) 、 [C](https://www.edureka.co/blog/how-to-compile-c-program-in-command-prompt/) 、 [C++](https://www.edureka.co/blog/difference-between-c-c-and-java) 等。将程序编译成机器能够理解和执行的等价低级代码。在这个博客中，我们将讨论如何编写、编译和运行 java 程序。

第一步，创建一个文件夹，创建一个 [Java 类](https://www.edureka.co/blog/java-objects-and-classes/)，编写一个 Java 程序。当我们编写 Java 程序时，***javac***([Java 编译器](https://www.edureka.co/blog/just-in-time-compiler/))将 Java 源代码翻译成字节码即 ***。*** *类文件*。字节码是 Java 虚拟机(JVM)的机器语言。字节码也被称为 Java 的神奇代码，它是独立于平台的。

将 Java 安装到系统中后的一个重要步骤就是设置路径。可以参考这个 [' **如何在 Java 中设置路径？'**](https://www.edureka.co/blog/how-to-set-path-in-java) 知道文章的确切程序。

让我们创建一个简单的 java 程序。

创建一个 java 文件为 HelloWorld.java

```
public class HelloWorld {
	public static void main(String args[]) {
		System.out.println("Hello World");
	}
}

```

要编译这个程序，在你的命令提示符下输入下面的命令，然后按回车键。

```
javac HelloWorld.java
```

本运行【javac.exe】，编译器。编译任何 [Java 程序](https://www.edureka.co/blog/java-programs/)的通用命令。

```
**javac <Java_file_name>.java

![helloworld- how to compile java program - Edureka](img/e915b98ad32ac00dd8fecc9934a75f52.png)** 
```

一旦你按下回车键，HelloWorld。将生成类文件。你会在工作目录的文件中找到**HelloTesters.java**和 **HelloTesters.class** 。

![helloworld file- how to compile java program - Edureka](img/855afba64ad4267a8b67aa5b622589b2.png)

当我们使用 ***javac*** 工具编译 java 程序时，一般 java 编译器会执行以下步骤:

*   语法检查

*   添加额外代码

*   将源代码转换成字节码，即从*开始。java 文件*到*。*类文件

所以，当我说编译器在编译时添加额外的代码时，例如，如果你没有在你的程序中写入任何[构造函数](https://www.edureka.co/blog/constructor-in-java/)，那么编译器将会在你的程序中添加一个[默认构造函数](https://www.edureka.co/blog/constructor-in-java/#defaultconstructor)。

![java code- how to compile java program - Edureka](img/0ca0493bb244f656454b9a83ff343dac.png)

![compilation process - how to compile java program - Edureka](img/7370dad654c43fbd3f9401bd056f8179.png)

所以 java 编译的主要目的是产生 ***。机器理解的程序的类文件*** 。

***注意:Java 要求放在自己源文件中的每个[类](https://www.edureka.co/blog/java-objects-and-classes/)必须与扩展名为 Java 的类名相同。***

当我们开始编译源代码时，每个类都被放在自己的*中。包含字节码*的类文件。 假设，如果你想一次编译多个 [Java](https://www.edureka.co/blog/java-tutorial/) 文件，那么你可以使用下面的命令:

```
javac *.java
```

这个命令会将所有的 java 文件转换成。类文件。

至此，我们结束了这篇关于 Java 编译过程的文章。我希望你理解了如何编译一个 java 程序，并且清楚我上面讨论的每一个方面。

查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。

有问题吗？请在这篇“如何编译 java 程序”文章的评论部分提到它，我们会尽快回复您。