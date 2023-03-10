# Java 中的令牌是什么，如何实现？

> 原文：<https://www.edureka.co/blog/tokens-in-java/>

你可能经常看到有数千行代码的大型 Java 应用程序，但是你有没有想过它的核心是什么？这些是记号，最小的单个元素，也称为 Java 程序的构建块。通过这篇文章，我将阐明 Java 中的标记，这些标记经常被忽略，但却是 Java 编程语言不可或缺的一部分。

在 Java 中，程序是类和方法的集合，而方法是各种表达式和语句的集合。Java 中的标记是代码的小单元，Java 编译器用它来构造语句和表达式。Java 支持 5 种类型的令牌，它们是:

1.  [关键词](#keywords)
2.  [标识符](#identifiers)
3.  [文字量](#literals)
4.  [操作员](#operators)
5.  [特殊符号](#specialsymbols)

现在让我们逐一讨论它们。

## **关键词**

[Java 中的关键字](https://www.edureka.co/blog/java-keywords/)是对 Java 编译器有特殊意义的预定义或保留字。每个关键字都被分配了一个特殊的任务或功能，用户不能更改。不能将关键字用作变量或标识符，因为它们是 Java 语法本身的一部分。关键字应该总是用小写字母书写，因为 Java 是一种区分大小写的语言。Java 支持各种关键字，下面列出了其中一些:

| 01.摘要 | 02.布尔型 | 03.字节 | 04.破裂 | 05.班级 |
| 06.情况 | 07.捕捉 | 08.茶 | 09.继续 | 10.系统默认值 |
| 11.做 | 12.两倍 | 13.其他 | 14.延伸 | 15.最后的 |
| 16.最后 | 17.漂浮物 | 18.为 | 19.如果 | 20.工具 |
| 21.进口 | 22\. instanceof | 23.（同 Internationalorganizations）国际组织 | 24.连接 | 25.长的 |
| 26.当地的 | 27.新的 | 28.包裹 | 29.私人的 | 30.保护 |
| 31.公众的 | 32.返回 | 33.短的 | 34.静电 | 35.极好的 |
| 36.转换 | 37.同步的 | 38.这 | 39.扔 | 40.投 |
| 41.短暂的 | 42.尝试 | 43.空的 | 44.不稳定的 | 45.在…期间 |
| 46.维护 | 47.常数 | 48.列举型别 | 49.转到 | 50.strictfp |

## **标识符**

[Java 标识符](https://www.edureka.co/blog/identifiers-in-java/)是用户自定义的变量、方法、类、[数组](https://www.edureka.co/blog/java-array/)、[包](https://www.edureka.co/blog/packages-in-java/)和[接口](https://www.edureka.co/blog/java-interface/)的名称。一旦在 Java 程序中分配了标识符，就可以在后面的语句中使用它来引用与该标识符相关联的值。命名标识符时，您必须遵循一些事实上的标准，例如:

*   标识符必须以字母、美元符号或下划线开头。
*   除了第一个字符，标识符可以有任意字符组合。
*   Java 中的标识符区分大小写。
*   Java 标识符可以是任意长度。
*   标识符名称不能包含空格。
*   任何标识符名称都不能以数字开头，但可以包含数字。
*   最重要的是，**关键字**在 Java 中不能作为标识符使用。

示例:

```
//Valid Identifiers
$myvariable  //correct
_variable    //correct
variable     //correct
edu_identifier_name //correct
edu2019var   //correct

//Invalid Identifiers
edu variable    //error
Edu_identifier  //error
&variable       //error
23identifier    //error
switch          //error
var/edu 	    //error
edureka's       //error
```

## **文字量**

Java 中的文字类似于普通的[变量](https://www.edureka.co/blog/variables-in-java/)，但是它们的值一旦赋值就不能改变。换句话说，文字是具有固定值的常量变量。这些由用户定义，可以属于任何[数据类型](https://www.edureka.co/blog/data-types-in-java/)。Java 支持以下五种类型的文字:

1.  整数
2.  浮点
3.  性格；角色；字母
4.  线
5.  布尔代数学体系的

**举例:**

```
public class EduLiteral { 
    public static void main(String[] args) 
    { 
        int edu1 = 112; 	// Int literal 
        float edu2 = 31.10; 	// Float literal 
        char edu3 = 'edu' // char literal 
        String edu4 = "Edureka"; // String literal 
        boolean edu5 = true; // Boolean literal 

        System.out.println(edu1); //112
        System.out.println(edu2); //31.40
        System.out.println(edu3); //edu
        System.out.println(edu4); //Edureka
        System.out.println(edu5); //true
    } 
}
```

## **操作员**

Java 中的[运算符是一个特殊的符号，表示编译器对一个或多个操作数执行一些特定的数学或非数学运算。Java 支持 8 种类型的运算符。下面我列出了所有的操作符，以及它们的例子:](https://www.edureka.co/blog/operators-in-java/)

| **操作员** | **例题** |
| *算术* | **+，–，/，*，%** |
| *一元* | **++、–––、！** |
| *分配* | **=，+=，-=，*=，/=，%=，^=** |
| *关系型* | **==，！=，<，>，< =，> =** |
| *逻辑* | **& &，&#124;&#124;** |
| *三进制* | **(条件)？(语句 1):(语句 2)；** |
| *按位* | **&，&#124;，^，~** |
| *换挡* | **<<>>>>>** |

## **特殊符号**

特殊符号 [Java](https://docs.oracle.com/javase/tutorial/) 中的特殊符号是 Java 编译器已知的具有特殊含义的少数字符，不能用于任何其他目的。在下表中，我列出了 [Java](https://www.edureka.co/blog/java-tutorial/) 支持的特殊符号及其描述。

| 标志 | 描述 |
| ***【括号】*** | 这些用作数组元素引用，也表示单维和多维下标 |
| *括号()* | 这些表示带有函数参数的函数调用 |
| ***【括号{】*** | 左花括号和右花括号表示包含多个语句的代码块的开始和结束 |
| ***逗号(，)*** | 这有助于分隔表达式中的多个语句 |
| ***分号(；)*** | 这用于调用初始化列表 |
| ***星号(*)*** | 这用于在 Java 中创建一个指针变量 |

至此，我们结束了这篇关于 Java 中的令牌的文章。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然你已经了解了 Java 中的哪些令牌，那就来看看 Edureka 的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-training-course)*吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 中的标记”文章的评论部分提到它，我们会尽快回复您。*