# Java 中的包:如何在 Java 中创建和使用包？

> 原文：<https://www.edureka.co/blog/packages-in-java/>

Java 最具创新性的[特性之一是包的概念。Java 中的包是封装一组类、接口、枚举、注释和子包的一种方式。从概念上讲，您可以将 java 包想象成类似于您计算机上的不同文件夹。在本教程中，我们将介绍](https://www.edureka.co/blog/object-oriented-programming/) [Java 中软件包的基础知识。](https://www.edureka.co/blog/java-tutorial/)

下面列出了本文涉及的主题:

*   [Java 中的 Package 是什么？](#javapackages)
*   [内置包](#predefinedpackages)
*   [用户自定义包](#userdefinedpackages)
    *   [用 Java 创建包](#creatingpackages)
    *   [在 Java 包中包含一个类](#classinpackage)
    *   [在导入另一个包时在包内创建一个类](#importingpackages)
    *   [导入类时使用完全限定名](#fullyqualifiedname)
*   [Java 中的静态导入](#staticimport)
*   [Java 包中的访问保护](#accesscontrol)
*   [点记](#points)

## **Java 中的 Package 是什么？**

Java 包是一种基于功能将相似类型的类、接口和子类组合在一起的机制。当软件用 [Java 编程语言](https://www.edureka.co/blog/what-is-java/)编写时，它可以由数百甚至数千个单独的类组成。通过将相关的类和接口放入包中来组织事物是有意义的。

编码时使用包有很多好处，比如:

用 Java 编码时使用包是一个好习惯。作为一名程序员，你可以轻松地找出相关的[类](https://www.edureka.co/blog/java-tutorial/#obj)、接口、枚举和注释。在 java 中我们有两种类型的包。

## **Java 中的包类型**

根据包是否由用户定义，包分为两类:

1.  内置软件包
2.  用户定义的包

## **内置包**

内置包或预定义包是那些作为 [JDK](https://www.edureka.co/blog/what-is-java/#ComponentsinJava) (Java 开发工具包)的一部分来简化 Java 程序员任务的包。它们由大量预定义的类和接口组成，是 Java API 的一部分。常用的内置包有 java.lang、java.io、java.util、java.applet 等。下面是一个使用内置包的简单程序。

```
package Edureka;
import java.util.ArrayList;

class BuiltInPackage {

    public static void main(String[] args) {

        ArrayList<Integer> myList = new ArrayList<>(3);

        myList.add(3);
        myList.add(2);
        myList.add(1);

        System.out.println("The elements of list are: " + myList);
    }
}
```

**输出:**

```
The elements of list are: [3, 2, 1]

```

ArrayList 类属于 java.util 包。要使用它，我们必须使用 import 语句导入包。代码的第一行*导入 java.util.ArrayList* 导入 java.util 包，并使用子包 util 中的 [ArrayList 类](https://www.edureka.co/blog/java-collections/#list)。

## **用户自定义包**

用户定义的包是由用户开发的包，目的是将相关的类、接口和子程序包组合在一起。在一个示例程序的帮助下，让我们看看如何创建包，在包内编译 Java 程序并执行它们。

### **用 Java 创建包**

用 Java 创建一个包是一件非常容易的事情。为包选择一个名称，并在 Java 源文件中包含一个*包* 命令作为第一条语句。java 源文件可以包含您想要包含在包中的类、接口、枚举和注释类型。例如，下面的语句创建了一个名为 ***MyPackage 的包。***

```
package MyPackage;
```

package 语句只是指定定义的类属于哪个包..

***注意:**如果省略 package 语句，类名会放入缺省包中，缺省包没有名字。尽管缺省包对于短程序来说很好，但是对于实际的应用程序来说是不够的。*

### **在 Java 包中包含一个类**

为了在一个包中创建一个类，你应该 声明包名作为你程序的第一条语句。然后将该类作为包的一部分包含进来。但是，请记住，一个类只能有一个包声明。这里有一个简单的程序来理解这个概念。

```
package MyPackage;

public class Compare {
  int num1, num2;

  Compare(int n, int m) {
     num1 = n;
     num2 = m;
}
public void getmax(){
    if ( num1 > num2 ) {
    	System.out.println("Maximum value of two numbers is " + num1);
  }
    else {
    	System.out.println("Maximum value of two numbers is " + num2);
    }
}

public static void main(String args[]) {
		Compare current[] = new Compare[3];

		current[1] = new Compare(5, 10);
	    current[2] = new Compare(123, 120);

	      for(int i=1; i < 3 ; i++)
	    	  {
	    	  current[i].getmax();
	    	  }
	   }
}

```

**输出:**

```
Maximum value of two numbers is 10
Maximum value of two numbers is 123

```

如您所见，我已经声明了一个名为 MyPackage 的包，并在该包中创建了一个类 Compare。Java 使用文件系统目录来存储包。因此，这个程序将被保存在一个名为*Compare.java*T3 的文件中，并被保存在名为 MyPackage 的目录中。当文件被编译时，Java 会创建一个**。类**文件并将其存储在同一个目录中。请记住，包的名称必须与保存该文件的目录相同。

您可能想知道如何从另一个包的类中使用这个比较类？

### **在导入另一个包时在包内创建一个类**

嗯，很简单。你只需要导入它。导入后，您可以通过它的名称来访问它。这里有一个演示这个概念的示例程序。

```
package Edureka;
import MyPackage.Compare;

public class Demo{
	public static void main(String args[]) {
		int n=10, m=10;
        Compare current = new Compare(n, m);
        if(n != m) {
        	 current.getmax();
        }
        else {
        	System.out.println("Both the values are same");
        }   
}
}

```

**输出:**

```
Both the values are same
```

我首先声明了包 *Edureka* ，然后从包 MyPackage 中导入了类 *Compare* 。因此，当我们在一个包中创建一个类，同时导入另一个包时，的顺序是，

*   包装声明
*   包导入

如果您不想使用 import 语句，还有另一种方法可以从另一个包中访问这个包的类文件。在导入一个[类](https://www.edureka.co/blog/java-tutorial/#obj)时，你可以只使用完全限定名。

### **导入类时使用完全限定名**

这里有一个例子来理解这个概念。我将使用我之前在博客中声明的同一个包， *MyPackage* 。

```
package Edureka;
public class Demo{
	public static void main(String args[]) {
		int n=10, m=11;
		//Using fully qualified name instead of import
        MyPackage.Compare current = new MyPackage.Compare(n, m);
        if(n != m) {
        	 current.getmax();
        }
        else {
        	System.out.println("Both the values are same");
        }   
}
}

```

**输出:**

```
Maximum value of two numbers is 11

```

在演示类中，我没有导入包，而是使用了全限定名，比如 *MyPackage。比较*和来创造它的对象。既然我们在讨论导入包，那么你也可以看看 Java 中静态导入的概念。

## **Java 中的静态导入**

静态导入特性是从版本 5 开始在 [Java](https://www.edureka.co/blog/what-is-java/) 中引入的。它方便了 Java 程序员直接访问类的任何静态成员，而不用使用完全限定名。

```
package MyPackage;
import static java.lang.Math.*; //static import
import static java.lang.System.*;// static import
public class StaticImportDemo {
	   public static void main(String args[]) {
	      double val = 64.0;
	      double sqroot = sqrt(val); // Access sqrt() method directly
	      out.println("Sq. root of " + val + " is " + sqroot);
	      //We don't need to use 'System.out
	   }
	}

```

```
Output:
```

```
Sq. root of 64.0 is 8.0

```

虽然使用静态导入涉及较少的编码，但过度使用可能会使程序不可读和不可维护。现在让我们进入下一个主题，包中的访问控制。

## **Java 包中的访问保护**

您可能知道 Java 访问控制机制的各个方面及其[访问说明符](https://www.edureka.co/blog/access-modifiers-in-java/)。Java 中的包为访问控制增加了另一个维度。类和包都是[数据封装](https://www.edureka.co/blog/encapsulation-in-java/)的一种方式。包充当类和其他从属包的容器，而类充当数据和代码的容器。由于包和类之间的这种相互作用，Java 包解决了类成员可见性的四个类别:

*   同一包中的子类
*   同一包中的非子类
*   不同包中的子类
*   既不在同一个包中也不在子类中的类

下表给出了在 Java 中使用包时哪些类型的访问是可能的，哪些是不可能的:

|  | ***私人*** | ***不修改*** | ***被保护的*** | ***公共*** |
| **同类** | 是 | 是 | 是 | 是 |
| **相同的包子类** | 不 | 是 | 是 | 是 |
| **相同的包非子类** | 不 | 是 | 是 | 是 |
| **不同的包子类** | 不 | 不 | 是 | 是 |
| **不同的包非子类** | 不 | 不 | 不 | 是 |

我们可以将上表中的数据简化如下:

1.  任何公开的东西都可以从任何地方访问
2.  任何声明为私有的东西只能在那个类中看到
3.  如果没有提到访问说明符，那么一个元素对于子类和同一个包中的其他类都是可见的
4.  最后，任何声明的受保护元素都可以在当前包之外看到，但是只对直接继承你的类的类可见

这样，Java 包提供了对类的访问控制。好了，这总结了 Java 中的包的概念。以下是在使用 [Java](https://www.edureka.co/blog/java-tutorial/) 中的包时应该记住的几点。

## **点记**

*   每个类都是某个包的一部分。如果省略 package 语句，类名将放入缺省包中
*   一个类只能有一个 package 语句，但它可以有多个 import package 语句
*   包的名称必须与保存文件的目录相同
*   当导入另一个包时，包声明必须是第一个语句，随后是包导入

好了，这就把我们带到了这篇“Java 中的包”文章的结尾。我们学习了什么是软件包以及为什么我们应该使用它们。毫无疑问，java 包是高效 Java 程序员最重要的部分之一。它不仅升级了程序员的编码风格，还减少了许多额外的工作。

如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*如果您找到了这篇关于“Java 中的包”的文章，请查看 Edureka 的 [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。今天就加入我们在剑桥的 Java 培训吧。*