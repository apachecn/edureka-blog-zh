# 如何在 C++中最好地实现类型转换？

> 原文：<https://www.edureka.co/blog/type-conversion-in-cpp/>

本文将向您介绍另一个有趣的话题，即 C++ 中的类型转换，并随后进行详细的实践演示。本文将涉及以下几点:

*   [c++中的类型转换](#TypeConversionInC++)
*   [隐式类型转换](#ImplicitTypeConversion)
*   [显式类型转换](#ExplicitTypeConversion)
*   [通过赋值转换](#Convertingbyassignment)
*   [使用 Cast 运算符的转换](#ConversionusingCastoperator)

那么让我们开始吧，

## **c++中的类型转换**

类型转换是指从一种类型转换到另一种类型。类型转换背后主要思想是使一种类型的变量与另一种类型的变量兼容来执行操作。例如，求两个变量的和，一个 int 类型&另一个 float 类型。所以，你需要将整型变量转换成浮点型，使它们都是浮点型，以求得总和。在这个博客中，我们将学习如何在 C++中执行类型转换。

在 C++中，类型转换有两种类型，即隐式类型转换&显式类型转换。

## **隐式类型转换**

隐式类型转换或自动类型转换是由编译器自己完成的。用户不需要外部触发器来将变量从一种类型转换为另一种类型。

当表达式包含多种类型的变量时，会出现这种情况。因此，在这些场景中，会自动进行类型转换以避免数据丢失。 在自动类型转换中，表达式中出现的所有数据类型都转换为数据类型最大的变量的数据类型。

下面是自动类型转换的顺序。也可以说，从最小到最大的数据类型进行类型转换。

*bool->char->short int->int->unsigned int->long->unsigned->long long->float->double->long double*

隐式转换可能会丢失信息，例如当有符号类型隐式转换为无符号类型时，符号可能会丢失，当 long 隐式转换为 float 时，可能会发生溢出。

现在让我们看一个例子来理解 C++中隐式类型转换是如何工作的。

#### **例子**

```
#include <iostream>
using namespace std;
int main() 12w
{
int int1 = 100; // integer int1
char char1 = 'c'; // character char1
// char1 implicitly converted to int using ASCII value of 'c' i.e. 99
int1 = int1 + char1;
// int1 is implicitly converted to float
float flt1 = int1 + 2.7;
cout << "int1 = " << int1 << endl
<< "char1 = " << char1 << endl
<< "flt1 = " << flt1 << endl;
return 0;
}
```

**输出**

int1 = 199

char1 = c

flt1 = 201.7

接下来在这篇 C++中的类型转换文章中，

## **显式类型转换**

显式类型转换或类型转换是用户定义的类型转换。在显式类型转换中，用户将一种类型的变量转换为另一种类型。在 C++中，显式类型转换有两种方式:

*   通过赋值转换
*   使用 Cast 运算符进行转换

现在让我们看看显式类型将一种类型转换为另一种类型的每种方法。

## **通过赋值转换**

在这种类型转换中，所需的类型在括号中的表达式前明确定义。数据丢失发生在显式类型转换中。它被认为是强有力的铸造。让我们看一个例子。

**例子**

```
#include <iostream>
using namespace std;
int main()
{
double dbl1 = 8.9;
// Explicit conversion from double to int
int res = (int)dbl1 + 1;
cout << "Result = " << res;
return 0;
}
```

**输出**

结果= 9

接下来在这篇 C++中的类型转换文章中，

## **使用 Cast 运算符的转换**

强制转换运算符是一元运算符，强制将一种数据类型转换为另一种数据类型。C++中有四种类型的强制转换，即静态强制转换、动态强制转换、常量强制转换和重新解释强制转换。

*   **静态石膏**–这是可以使用的最简单的石膏类型。它不仅执行向上转换，还执行向下转换。这是一个编译时强制转换。在运行时不执行检查来保证被转换的对象是目标类型的完整对象。
*   **动态强制转换**–它确保类型转换的结果指向目标指针类型的有效、完整的对象。
*   **Const Cast**–操纵对象是否需要为常量或非常量。它确保要么需要设置常量，要么删除常量。
*   **重新解释转换**–将任何指针类型转换为任何其他指针类型，即使是不相关的类。它不检查指针类型和指针所指向的数据是否相同。

让我们看一个静态强制转换的例子，

**例子**

```
#include <iostream>
using namespace std;
int main()
{
float flt = 30.11;
// using cast operator
int int1 = static_cast<int>(flt);
cout <<int1;
}
```

**输出**

Thirty

这就把我们带到了这篇关于 C++中类型转换的文章的结尾。 我希望你能发现这些信息并有所帮助，敬请关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册参加在线实时培训，享受全天候支持和终身访问。

有问题要问我们吗？在这篇文章的评论部分提到它们，我们会给你回复。