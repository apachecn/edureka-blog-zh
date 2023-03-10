# 如何在 C++中实现 Goto 语句？

> 原文：<https://www.edureka.co/blog/goto-statement-in-cpp/>

无论是哪种编程语言，程序员都很难在代码之间进行遍历。在本文中，我们将探讨“C++中的 Goto 语句”，它有助于我们简化遍历代码的过程。

以下是本文将要讨论要点:

*   [c++中 Goto 语句是什么？](#WhatisGotoStatementinC++?)
*   [Goto 语句示例](#ExamplesOfGotoStatement)
*   [为什么不使用 Goto 语句？](#WhynottouseGotoStatement?)

因此，让我们从理解第一个主题开始，

## **c++中 Goto 语句是什么？**

C++中的 goto 语句是一个无条件跳转语句，用于转移程序的控制权。它允许程序的执行流程跳转到函数中的指定位置。有两种方法可以调用 goto 语句。

| **语法 1** | **语法 2** |
| *goto 标签；**//语句块**标签:；* | *标签:；**//语句块**goto 标签；* |

标签的名称是用户定义的标识符，通过紧跟其名称的冒号来区分。紧跟在“label:”之后的语句是在 goto 语句之后执行的语句。goto 语句跳转到标有标签的语句。

## **Goto 语句示例**

让我们看几个关于如何在 C++中使用 goto 语句的例子

### **例 1:**

```

//based on syntax 1
#include<iostream>
using namespace std;
// function to check greater number
void checkGreater()
{
int i, j;
i=2;j=5;
if(i>j)
goto iGreater;
else
goto jGreater;
iGreater:
cout<<i<<" is greater";
return;
jGreater:
cout<<j<<" is greater";
}
// main method to test above function
int main()
{
checkGreater();
return 0;
}

```

**输出:**

![output - Goto Statement in C++ - Edureka](img/30d99f293f6f711d87e2bc144ca8570b.png)

“checkGreater”函数中“iGreater:”后的 return 语句。一旦控件跳转到带有“iGreater:”的标签，程序将执行它后面的每一段代码。因此，如果数量更大，返回是很重要的。否则，标签“jGreater:”之后的代码也会在它出现在“iGreater:”之后时被执行。

### **例 2:**

```

//based on Syntax 2
#include <iostream> 
using namespace std; 
// function to print numbers from 1 to 5
void printNumbers() 
{ 
int n = 1; 
print: 
cout << n << " "; 
n++; 
if (n <= 5) 
goto print; 
} 
// main method to test above function 
int main() 
{ 
printNumbers(); 
return 0; 
}

```

**输出:**

![output - Goto Statement in C++ - Edureka](img/a5b9f1cda124238f17447cfefa39b615.png)

在上面的程序中，标签被命名为“print”，goto 语句仅在变量“n”小于或等于 5 时跳转到“print”标签。

## **为什么不使用 Goto 语句？**

早期的编程语言如 FORTRAN 和 BASIC 的早期版本没有 while 这样的结构化语句，所以程序员被迫使用 goto 语句来编写循环。使用 goto 语句的问题是很容易开发出非常难以理解的程序逻辑，即使对于代码的原作者来说也是如此。

如果 goto 点在 goto 调用之上，很容易陷入无限循环。

### **如何避免 goto 语句？**

Goto 不是不可避免的，而是可以避免的。使用 break 和 continue 语句可以避免 Goto 语句。

这就把我们带到了这篇关于“C++中的 Goto 语句”的文章的结尾。我希望你喜欢这条信息。既然您已经理解了上述概念，如果您对类似的内容或培训感兴趣，请查看 Edureka 提供的[这些课程，edu reka](https://www.edureka.co/all-courses)是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

Edureka 的培训和认证课程是为希望在自己的专业领域出类拔萃的学生和专业人士设计的。该课程旨在让您在自己的首选领域有一个良好的开端，并针对您希望在各自感兴趣的领域实现的认证或专业目标对您进行培训。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。