# 怎么写 C 程序求一个二次方程的根？

> 原文：<https://www.edureka.co/blog/c-program-quadratic-equation/>

计算二次方程的根是我们小时候学过的东西。然而，二次方程的复杂性随着时间的推移而增加。处理这个问题的方法也发生了变化。在这篇文章中，我们将看看如何写一个 C 程序来寻找一个二次方程的根。

以下是本文将涉及的要点:

我们开始吧。

## **什么是二次方程？**

在深入本帖的编码部分之前，我们先来了解一下到底什么是二次方程？这一节将让你很好地理解二次方程，这将有助于理解算法。所以，让我们回到解决方案。二次方程被称为二次方程。如果你不熟悉术语“度”，它是一个方程的阶，它的值等于方程中的最大指数。

| 程度 | 等式 |
| one | 线性的 |
| Two | 二次的 |
| three | 立方体的 |

### **标准形式**

让我们看看什么是二次方程的标准形式，这将有助于你快速识别它们。

***ax******2******+bx+c = 0***是已知变量 a、b、c 的值的二次方程的标准形式。x 的值未知，a 不等于 0。

当你在图上画二次方程时，你会得到一条曲线(抛物线)。这个方程与轴相交的点就是它的**根**。通常，一个二次方程有 2 个根。让我们讨论一个二次方程的根的细节。

## **根的种类**

有几种不同的方法可以找到给定的二次方程的根。如，f 对给定的二次方程进行运算，使用完全平方公式，最后一种方法涉及到使用二次公式求根。我将坚持最后一种方法，因为与其他方法相比，它的缺点较少。

让我们假设我们的二次方程是标准形式的***ax******2******+bx+c = 0，*** 那么我们可以使用的公式是——![Quadratic Equation - Edureka](img/7b2032eb36d7d762c0d3aab90e0995ae.png)

现在，我们来谈谈根。基本上，分子中平方根(b2–4ac)内的项也称为判别式。它能告诉你更多关于二次方程根的性质。让我们来看看

1.  如果判别式的值是正的，这意味着我们有两个根，它们在本质上是真正的 T2。
2.  如果它的值是负的，你有一对本质上复杂的根(例如- 5i，8i)。
3.  如果是 0，你会得到 2 个具有相等值和实数的根。

现在，你已经对二次方程及其根有了深刻的理解，我们可以从算法开始，当你在现实世界的问题中实现你所学到的东西时，你会感觉很神奇。

## **理解算法**

让我们一步一步地了解如何编写一个可以用来求二次方程根的程序。

现在让我们看看 C 程序，寻找一个二次方程的根。

## **C 程序求一个二次方程的根**

```
#include<stdio.h> 
#include<math.h> 
#include<conio.h>
#include<stdlib.h> 

/*Function to know the nature of roots and calculate the roots of given quadratic equation*/
void RootsofQuadratic(int a, int b, int c) 
{ 

    if (a == 0)  /*Checking for value of a*/
    { 
        printf("The value of a cannot be 0"); 
        return; 
    } 

    int d = b*b - 4*a*c; 
    double SquarerootDescriminant = sqrt(abs(d)); 

    if (d > 0) 
    { 
        printf("The Roots are Real in Nature n"); 
        printf("%fn%f",(double)(-b + SquarerootDescriminant)/(2*a) 
            , (double)(-b - SquarerootDescriminant)/(2*a)); 
    } 
    else if (d == 0) 
    { 
        printf("The roots are equal and Real in Nature n"); 
        printf("%f",-(double)b / (2*a)); 
    } 
    else // d < 0 
    { 
        printf("The Roots are Complex in Nature n"); 
        printf("%f + i%fn%f - i%f", -(double)b / (2*a),SquarerootDescriminant 
            ,-(double)b / (2*a), SquarerootDescriminant); 
    } 
}  
int main() 
{ 
    int a;
	int b;
	int c;
   printf("For a quadratic equation of form ax2 + bx + c = 0 enter values of a, b, cn");
   scanf("%d%d%d", &a, &b, &c);	 /*Asking for input*/
    RootsofQuadratic(a, b, c); 
    return 0; 
}
```

**输出:**

**![output- quadratic equation in c - Edureka](img/7fb9603c89e395406c41cc6aac070aa8.png)**

对于输入的值，我们收到了 2 个复数根。下次如果你有一个复杂的二次方程要解，这个程序一定会节省你一些时间。

本文到此为止。希望你已经理解了一个二次方程求根的概念和 C 程序。

如果您遇到任何问题，请在“C 中的二次方程”的评论区提出您的所有问题，我们的团队将很乐意回答。