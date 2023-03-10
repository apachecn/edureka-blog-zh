# 求两个数的 LCM 的 c 程序

> 原文：<https://www.edureka.co/blog/c-program-to-find-lcm-of-two-numbers/>

我们很久以前就学会了寻找 2 个数字的 LCM，并且在我们的日常生活中仍然使用它。在这篇文章中，我们将深入理解 LCM 的基本概念，并实现一个 [C 程序](https://www.edureka.co/blog/c-data-structures)来寻找 2 个数的 LCM。

下面是本文中涉及到一些要点，

1.  [了解 LCM 的概念](#UnderstandtheconceptofLCM)
2.  [理解算法](#UnderstandingtheAlgorithm)
3.  [咱们代号](#Let%E2%80%99scode)

那么让我们开始吧，

## **C 程序求两个数的 LCM**

## **理解 LCM 的概念**

LCM 代表**L**owest**C**ommon**M**倍数。这是能被我们所考虑的两个数整除的最低可能数。让我们不要拘泥于定义，而深入挖掘概念。

让我们考虑两个数字 4 和 15，看看它们各自的倍数

| **4** | 8 | 12 | 16 | 20 | 24 | 28 | 32 | 36 | 40 | 44 | 48 | 52 | 56 | **60** |
| **十五** | 30 | 45 | **60** | 75 | 90 | 105 | 120 | 135 | 150 | 165 | 第 180 章 | 195 | 210 | 235 |

在上表中，我提到了几个 4 和 15 的倍数。现在，让我们找到 LCM。为了实现这个目标，我们需要在查看表格后找到能被这两个数字整除的最小可能数，这看起来并不是一个困难的任务，我们可以很容易地得出答案，在这种情况下是 **60。**但是，制作这样的桌子并不总是可行的。因此，创建一个程序将节省我们制作这些巨大的表格和大量的时间。

## 理解算法

在理解算法的同时，我们将研究不同的方法来降低程序的复杂性并提高效率。我们开始吧。

*   首先，我们需要考虑 LCM 的 2 个值，它是正整数。让我们考虑 a 和 b

*   现在，让我们考虑一下，对于任何 2 个数字，LCM 的最小可能值是多少，现在，我们将它视为 1，也是 LCM 的最大可能值。你会同意我先前的说法。因为 2 的乘积数是它们的倍数。因此，它可能不是 LCM，但肯定是一个公倍数。

*   现在，我们将对 1 和 a * b 之间的所有值运行一个循环，在循环中，我们将检查该数是否能被 a 和 b 整除。一旦找到该数，我们将打印其值。

*   如果我们在程序中实现了上面的 3 个步骤，它将运行良好，但是让我们更进一步，实现我们到目前为止所学的，我们认为 LCM 的最低可能值为 1，但是 LCM 的值可以小于 a 或 b 吗？不。如果仍然，你在想它怎么不能小于 a 和 b，参考上表。因此，在我们的循环中，我们不会检查小于 a 或 b 的值

*   为了进一步修改，我们可以将增量值改为两个数字中最大值的倍数，因为它们之间的数字不能是 LCM。

我们已经完成了这篇“用 C 程序寻找两个数的 LCM”文章的最后一部分

## 让我们编写代码:C 程序求两个数的 LCM

到目前为止，我们已经学习了所有的基本概念来编写一个代码，可以找到 2 个数字的 LCM。现在，我们用上面的算法，写一个程序，求 2 个数的 LCM。

```
#include <stdio.h>
#include <conio.h>int main(){
int a;
int b;
int GreatestNumber;
int PossibleLCM;printf("Enter 2 positive integers:");
scanf("%d%d", &a, &b);&nbsp; /*Asking input from the user*/
if(a>b)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; /*Checking for the greatest number*/
GreatestNumber = a;
else
GreatestNumber = b;
for(PossibleLCM = GreatestNumber; PossibleLCM<=a*b; PossibleLCM = PossibleLCM+GreatestNumber)

```

**输出**

当我们使用我们的程序找到 4 和 15 的 LCM 时，我们得到 60，这是正确的答案，摆弄代码，尝试用更少的代码行获得类似的结果。恭喜你，这个程序将会是你下一次找到 2 个数的 LCM 的救命稻草。

至此，我们就到了这篇关于“用 C 程序寻找两个数的 LCM”的文章的结尾。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？请在这篇文章的评论部分提到它们，我们会尽快回复您。