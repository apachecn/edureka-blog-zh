# 什么是嵌入式 C 编程，有什么不同？

> 原文：<https://www.edureka.co/blog/embedded-c-programming/>

**C** 是面向系统编程的高级编程语言。 **嵌入式 C** 是 的扩展，为 **嵌入式** **设备开发高效程序提供支持。**还不是 [**C** **语言**](https://www.edureka.co/blog/c-programming-tutorial/) **的一部分。在这篇“嵌入式 C 编程”文章中，我们将讨论以下主题。**

*   [什么是嵌入式 C 编程](#WhatisEmbeddedCProgramming)
*   [C 和嵌入式 C 的区别](#DifferencebetweenCandEmbeddedC)
*   [嵌入式 C 程序的基本结构](#BasicStructureofEmbeddedCProgram)

## **什么是嵌入式 C 编程**

嵌入式 C 编程语言是传统的 **[C 编程语言](https://www.edureka.co/blog/c-programming-tutorial/)** 的扩展，用于嵌入式系统。嵌入式 C 编程语言使用与 C 编程语言相同的语法和语义。

嵌入式 C 语言对普通 C 编程语言的唯一扩展是 I/O 硬件寻址、定点算术运算、访问地址空间等。

现在我们来看一下 C 和嵌入式 C 的区别。

## **C 与嵌入式 C 的区别:**

| **C 编程语言** | **嵌入式 C 编程语言** |
| 从本质上来说，这是一种自然发展 | 在本质上，它是交叉发展的 |
| 它独立于硬件架构 | 它依赖于硬件 |
| 用于桌面应用程序 | 用于有限的资源，如 RAM 和 ROM |

现在我们来学习一下嵌入式 C 程序的基本结构。

**嵌入式 C 程序的基本结构:**

嵌入式 C 程序有一个类似 C 编程的 **[结构。](https://www.edureka.co/blog/basic-structure-of-a-c-program/)**

这五层是:

1.  评论
2.  预处理器指令
3.  全球宣言
4.  本地申报
5.  主函数()

整个代码遵循这个大纲。每个代码都有相似的轮廓。现在让我们详细了解这一层中的每一层。

```
Multiline Comments . . . . . Denoted using /*&hellip;&hellip;*/
Single Line Comments . . . . . Denoted using //
Preprocessor Directives . . . . . #include<&hellip;> or #define
Global Variables . . . . . Accessible anywhere in the program
Function Declarations . . . . . Declaring Function
Main Function . . . . . Main Function, execution begins here
{
      Local Variables . . . . . Variables confined to main function
      Function Calls . . . . . Calling other Functions
      Infinite Loop . . . . . Like while(1) or for(;;)
      Statements . . . . .
      &hellip;.
      &hellip;.
}
Function Definitions . . . . . Defining the Functions
{
      Local Variables . . . . . Local Variables confined to this Function 
      Statements . . . . .
      &hellip;.
      &hellip;.
}
```

让我们看看评论区。

### **评论部分:**

注释是简单易读的文本，用代码编写以使读者更容易理解。通常评论都是用//或者/* */写的。

**示例**://测试程序

让我们看看预处理指令部分。

### **预处理器指令段:**

预处理器指令告诉编译器在哪个文件中查找程序中没有的符号。

例如，在我们使用的 8051 Keil 编译器中，

```
#include<reg51.h>
```

让我们看看全局声明部分。

### **全局声明部分:**

这部分代码是声明全局变量的部分。此外，用户定义的函数也在这部分代码中声明。从任何地方都可以访问它们。

```
void delay (int);
```

让我们看看本地声明部分。

### **本地声明部分:**

这些变量在各自的函数中声明，不能在主函数之外使用。

让我们看看主功能部分。

### **主要功能部分:**

每个 [C 程序](https://www.edureka.co/blog/basic-structure-of-a-c-program/)都需要有 main 函数。嵌入式 C 程序也是如此。每个主要功能包含两个部分。声明部分和[执行部分](https://www.edureka.co/blog/how-to-compile-c-program-in-command-prompt/)。声明部分是声明所有变量的部分。执行部分以花括号开始，以花括号结束。声明和执行部分都在花括号内。

```
void main(void) // Main Function
{
     P1 = 0x00;
     while(1) 
     {
           P1 = 0xFF; 
           delay(1000);
           P1 = 0x00; 
           delay(1000);
       }
}

```

### 函数定义部分

在本节中，定义了函数。

*这是嵌入式 c 程序的基本结构。*

至此，我们结束了这篇“嵌入式 C 编程”的文章。希望你已经理解了基本结构。

*既然您已经了解了 C 语言编程的基础知识，那就来看看 Edureka 提供的关于 Java、[Spring](https://spring.io/)等多种技术的  培训* *吧，这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者*

有问题要问我们吗？在这个博客的评论部分提到它，我们会尽快回复你。