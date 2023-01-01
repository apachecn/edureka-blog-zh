# Java 中的文件处理——如何处理 Java 文件？

> 原文：<https://www.edureka.co/blog/file-handling-in-java/>

Java 作为最流行的编程语言之一，提供了对各种功能的广泛支持，如数据库、[套接字](https://www.edureka.co/blog/socket-programming-in-java/)等。一个这样的功能是 Java 中的文件处理。文件处理是对文件执行各种任务所必需的，例如读、写等。在这篇文章中，我将告诉你 Java 中的各种文件操作是什么。

本文涵盖了以下主题:

*   [Java 中的文件处理是什么？](#WhatisFileHandlinginJava?)
*   [什么是溪流？](#WhatisaStream?)
*   [Java 文件方法](#JavaFileMethods)
*   [Java 中的文件操作](#FileOperationsinJava)

**Java 中的文件处理是什么？**

Java 中的文件处理意味着从文件中读取数据和向文件中写入数据。来自 **java.io 包**的 File 类允许我们处理不同格式的文件。为了使用 File 类，你需要创建一个[类](https://www.edureka.co/blog/java-tutorial/#obj)的对象，并指定文件名或目录名。

**例如:**

```
// Import the File class
import java.io.File

// Specify the filename
File obj = new File("filename.txt"); 
```

Java 使用流的概念对文件进行 I/O 操作。那么现在让我们来理解 Java 中的流是什么。

**什么是溪流？**

在 Java 中，流是两种类型的数据序列。

### **1。字节流**

这主要包括字节数据。当一个输入被提供并以字节数据执行时，它被称为具有字节流的文件处理过程。

### **2。字符流**

字符流是包含字符的流。用字符处理输入数据称为用字符流处理文件。

现在您已经知道了什么是流，让我们更深入地阅读这篇关于 Java 中的文件处理的文章，并了解对文件操作有用的各种方法，如创建、读取和写入。

## **Java 文件方法**

下表描述了用于对 Java 文件执行操作的各种方法。

| 方法 | 类型 | 描述 |
| canRead() | 布尔代数学体系的 | 它测试文件是否可读 |
| canWrite() | 布尔代数学体系的 | 它测试文件是否可写 |
| createNewFile() | 布尔代数学体系的 | 该方法创建一个空文件 |
| 删除() | 布尔代数学体系的 | 删除文件 |
| 存在() | 布尔代数学体系的 | 它测试文件是否存在 |
| getName() | 线 | 返回文件的名称 |
| getAbsolutePath() | 线 | 返回文件的绝对路径名 |
| 长度() | 长的 | 以字节为单位返回文件的大小 |
| 列表() | 字符串[] | 返回目录中文件的数组 |
| mkdir() | 布尔代数学体系的 | 创建一个目录 |

现在让我们了解 Java 中的各种文件操作是什么，以及如何执行它们。

## **Java 中的文件操作**

基本上，您可以对一个文件执行四种操作。它们如下:

现在，让我们深入了解这些操作的细节

### **1。创建一个文件**

在这种情况下，要创建一个文件，您可以使用 *createNewFile()* 方法。如果文件创建成功，该方法返回 **true** ，如果文件已经存在，则返回 **false** 。

让我们看一个如何在 [Java](https://docs.oracle.com/javase/tutorial/) 中创建文件的例子。

```
package FileHandling;

 // Import the File class
import java.io.File;

// Import the IOException class to handle errors
import java.io.IOException; 

public class CreateFile {
public static void main(String[] args) {
try {
// Creating an object of a file
File myObj = new File("D:FileHandlingNewFilef1.txt"); 
if (myObj.createNewFile()) {
System.out.println("File created: " + myObj.getName());
} else {
System.out.println("File already exists.");
}
} catch (IOException e) {
System.out.println("An error occurred.");
e.printStackTrace();
}
}
}
```

在上面的代码中，在指定的位置创建了一个名为 ***NewFilef1*** 的文件。如果有错误，则在 [捕捉块](https://www.edureka.co/blog/java-exception-handling#ExceptionMethods)中处理。让我们检查执行上述代码的输出:

**输出:**

```
File created: NewFilef1.txt
```

了解了这些，我们来看看如何获取文件信息。

**2。获取文件信息**

让我们在下面的示例代码的帮助下，看看如何使用各种方法获取文件信息

```
package FileHandling;
import java.io.File; // Import the File class

public class FileInformation {
public static void main(String[] args) {
 // Creating an object of a file
File myObj = new File("NewFilef1.txt");
if (myObj.exists()) {
 // Returning the file name
System.out.println("File name: " + myObj.getName());

// Returning the path of the file 
System.out.println("Absolute path: " + myObj.getAbsolutePath());   

// Displaying whether the file is writable
System.out.println("Writeable: " + myObj.canWrite());  

// Displaying whether the file is readable or not
System.out.println("Readable " + myObj.canRead());  

// Returning the length of the file in bytes
System.out.println("File size in bytes " + myObj.length());  
} else {
System.out.println("The file does not exist.");
}
}
}
```

当您执行上述程序时，您将获得如下输出所示的文件信息:

**输出:**

```
File name: NewFilef1.txt
Absolute path: D:FileHandlingNewFilef1.txt
Writable: true
Readable true
File size in bytes 52
```

这就是你需要如何编写一个程序来获取特定文件的信息。现在，让我们进一步看看对该文件的另外两个操作。即读和写操作。

**3。写入文件**

在下面的例子中，我使用了 **FileWriter** 类及其 **write()** 方法将一些文本写入文件。让我们借助一个代码来理解这一点。

```
package FileHandling;

// Import the FileWriter class
import java.io.FileWriter; 

// Import the IOException class to handle errors
import java.io.IOException; 

public class WriteToFile {
public static void main(String[] args) {
try {
FileWriter myWriter = new FileWriter("D:FileHandlingNewFilef1.txt");
 // Writes this content into the specified file
myWriter.write(Java is the prominent programming language of the millenium!"); 

// Closing is necessary to retrieve the resources allocated
myWriter.close(); 
System.out.println("Successfully wrote to the file.");
} catch (IOException e) {
System.out.println("An error occurred.");
e.printStackTrace();
}
}
}
```

**输出:**

```
Successfully wrote to the file
```

当你运行文件时，上面的文字，“ *Java 是千禧年的杰出编程语言！*将被输入到您创建的文件中。你可以通过在指定位置打开文件来交叉检查。

现在让我们进一步理解对文件的最后一个操作，即读取文件

## **4。从文件中读取**

在下面的例子中，我使用了 Scanner 类来读取文本文件的内容。

```
package FileHandling;

// Import the File class
import java.io.File; 

// Import this class to handle errors
import java.io.FileNotFoundException; 

// Import the Scanner class to read text files
import java.util.Scanner; 

public class ReadFromFile {
public static void main(String[] args) {
try {
// Creating an object of the file for reading the data
File myObj = new File("D:FileHandlingNewFilef1.txt");  
Scanner myReader = new Scanner(myObj);
while (myReader.hasNextLine()) {
String data = myReader.nextLine();
System.out.println(data);
}
myReader.close();
} catch (FileNotFoundException e) {
System.out.println("An error occurred.");
e.printStackTrace();
}
}
}
```

当您执行上述程序时，它将显示给定文件中的内容。

**输出:**

```
Java is the prominent programming language of the millennium!
```

事情就是这样的。这就是 Java 中各种文件操作的全部内容。至此，我们结束了这篇关于 Java 文件处理的文章。我希望你发现它信息丰富。如果你想了解更多，你也可以看看我们的 **[其他 Java 博客](https://www.edureka.co/blog/java-tutorial/) [s](https://www.edureka.co/blog/java-tutorial/)** 。

*查看 Edureka 提供的 **[Java 认证培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的文件处理”文章的评论部分提到它，我们会尽快回复你，或者你也可以参加我们在谢菲尔德的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-sheffield)