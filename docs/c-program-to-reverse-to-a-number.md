# C 语言中如何反数？

> 原文：<https://www.edureka.co/blog/c-program-to-reverse-to-a-number/>

学习 C 语言时，你将会学到编程领域的所有基本概念。为了学习这些基本概念，有一些标准程序，当它们被执行时，以一种实用的方式给我们一个所有概念的简要理解。 [C 程序](https://www.edureka.co/blog/how-to-compile-c-program-in-command-prompt/)倒数就是其中之一，它让学习者对 While 循环和算术运算符有了深刻的理解。

本文将涉及以下几点

*   [理解算法](#UnderstandingtheAlgorithm)
*   [样品](#Sample)
*   [使用 While 循环](#ImplementingtheprogramusingWhileLoop) 实现程序

让我们把 C 中的一个数字倒过来

## **C 程序求逆数:理解算法**

首先，让我们看一下算法，之后我们将考虑一个例子，并深入探讨这个主题。 在开始有趣的部分之前，当你想到倒一个数的时候，你首先想到的是什么？也许，只是翻转数字的位置或其他一些复杂的方式。让我们看看它是否如我们所想的那样工作。

那么，我们先来看看算法。

*   首先，我们考虑一个由要反转的数字组成的变量“Number ”,然后我们将声明一个名为“Reverse_Number”的变量。
*   我们将使用下面的公式，Reverse_Number = Reverse _ Number * 10+Number % 10，因为 Reverse _ Number 最初是 0，而“Number”由要反转的数字组成。Reverse_Number 的值将等于“Number”除以 10 后得到的余数。
*   应用此公式后，我们将“数字”除以 10，并用除法运算后得到的值对其进行更新。应该是这样的，Number = Number / 10。
*   我们将重复步骤 2 和 3，直到“数字”变量的更新值为> 0。
*   最后，变量‘反向编号’将由我们的反向编号 组成

## **样品**

让我们转到第二部分，考虑一个例子 87342。我们将使用上面讨论的算法来获得 87342 的逆运算

*   让我们考虑用‘Number’和‘Reverse _ Number’来存储原数和反数。
*   Reverse_Number = 0 + 2，即 Reverse_Number = 2，Number = 87342 / 10 等于 8734
*   正如我们前面讨论过的，我们需要重复这个过程，直到‘T2 号’为 0。因此，Reverse_Number = 20 + 4，因此 Reverse_Number = 24，在将数字变量除以 10 之后，我们得到新的“数字”值 873
*   Reverse_Number = 243，Number = 87
*   Reverse _ Number = 2437 Number = 8
*   Reverse _ Number = 24378 Number = 0
*   这就是我们如何得到反数的。

## **使用 While 循环执行程序**

我们讨论了求一个数的倒数的算法。我们还通过考虑一个例子来手动评估结果。现在，让我们编写一个程序，它可以帮助我们理解一些关键的编程概念，并节省我们一些时间。

```

#include <stdio.h>
#include <conio.h>
/* The Function we defined to reverse the given number*/
int ReverseTheNumber(int Number)
{
int Reverse_Number = 0;
while(Number > 0) /* loops untill the number is > 0*/
{
Reverse_Number = Reverse_Number*10 + Number%10;
Number = Number/10;
}
return Reverse_Number; /*Returning our reversed number*/
}
int main()
{
int Number;
printf("Enter the number to be reversed:n");
scanf("%d", &Number);
printf("Reverse of no. is %d", ReverseTheNumber(Number)); /*Using the Function*/
getchar();
return 0;
}

```

**输出**

我们收到的输出与我们从手动实现中获得的结果相同。使用上面的代码以更少的代码行实现类似的结果。

说到这里，我们就结束这篇关于“用 C 程序来反转一个数”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。