# C 语言中的斐波那契数列:C 编程快速入门

> 原文：<https://www.edureka.co/blog/fibonacci-series-in-c/>

如果你作为一名程序员参加过面试，你会知道有很多关于 C 编程的面试可能会问一个为斐波那契数列创建程序的问题。这个看似简单的棘手问题困扰着许多人。在这篇文章中，我们将讨论如何在 c 中实现斐波那契数列。下面的指针将在这里讨论，

*   [斐波那契数列](#FibonacciSeries)
*   [斐波那契数列，直到用户输入数字](#FibonacciSeriesUsingRecursion)
*   [使用递归的斐波那契数列](#FibonacciSeriesUsingRecursion)

让我们开始吧，

## **C 中的斐波那契数列**

斐波那契数列是数列中前面两个数相加形成的数列。前两项分别为 0 和 1。这之后的项是通过简单地将前两项相加而生成的。

有两种方法可以编写斐波那契数列程序:

*   无递归的斐波那契数列
*   使用递归的斐波那契数列

## **如何计算斐波那契？**

斐波纳契数列是一系列数字:0，1，1，2，3，5，8，13，21，34，…

下一个数字是通过将它前面的两个数字相加得到的:

*   2 的计算方法是将它前面的两个数相加(1+1)，
*   3 是通过将它前面的两个数相加(1+2)来计算的，
*   5 是(2+3)，以此类推..

这是一个斐波那契数列的例子:0，1，1，2，3，5，8，13 等等。

在上面的例子中，0 和 1 是数列的前两项。这两个术语是直接打印的。第三项是由前两项相加而成的。在这种情况下是 0 和 1。所以，我们得到 0+1=1。因此，1 被打印为第三项。通过使用第二和第三项而不使用第一项来生成下一项。这样做，直到你想要的或用户要求的条款的数量。在上面的例子中，我们使用了八个术语。

这里有一个 c 程序:

```

#include<stdio.h>
int main()
{
int first=0, second=1, i, n, sum=0;
printf("Enter the number of terms: ");
scanf("%d",&n);
//accepting the terms
printf("Fibonacci Series:");
for(i=0 ; i<n ; i++)
{
if(i <= 1)
{
sum=i;
}
//to print 0 and 1
else
{
sum=first + second;
first=second;
second=sum;
//to calculate the remaining terms.
//value of first and second changes as new term is printed.
}
printf(" %d",sum)
}
return 0;
}

```

**输出:**

![Output - Fibonacci Series in C - Edureka](img/79587eaa3bce8487a89d8a8a2b2dfbbb.png)

在上面的程序中，我们首先声明所有的变量。首先，我们设置 First 和 second 的值，这些将是我们用来生成更多项的变量。接下来，我们声明 n 项，它将保存项数。我们有一个术语来表示两位数的和，叫做 sum。最后一项是 I，用于 for 循环中的迭代。

我们接受来自用户的术语数，并将其存储在 n 中。然后我们有一个 for 循环，从 0 一直运行到用户请求的术语数，即 n。

在 for 循环中，我们首先有一个 if 语句，条件是检查 I 的值是否小于 1。如果是零，则打印一个，这取决于术语的数量。当有两个以上的术语时，它用于打印首字母 0 和 1。

如果项数大于 1，则执行循环的 else 部分。在这部分中，变量 first 和 second 的相加被赋给变量 sum。下一项是和变量。例如，将值为 0 和 1 的 first 和 second 相加，得到的和值为 1。

在下一部分中，我们将第二项的值赋给第一项，然后将 sum 的值赋给第二项。这样做是因为对于下一个术语，随着新值的打印，前面的两个值被改变。这是总值。如果我们考虑将 0 和 1 分配给第一个和第二个，在这个步骤之后，第一个的值将是 1，第二个的值也将是 1，因为 sum 的值是 1。

退出 else 部分后，我们打印 sum 值。这一直执行到 I 的值等于 n，循环中断，我们退出程序。

让我们继续 C 语言文章中的斐波那契数列，看看还能做些什么，

## **斐波那契数列，直到用户输入数字**

**代码:**

```

#include <stdio.h>
int main()
{
int first = 0, second = 1, sum = 0, n;
printf("Enter the end term for the series: ");
scanf("%d", &n);
printf("Fibonacci Series: %d, %d, ", first, second);
sum = first + second;
while(sum <= n)
{
printf("%d, ",sum);
first = second;
second = sum;
sum = first + second;
}
return 0;
}

```

**输出:**

![Output - Fibonacci Series in C - Edureka](img/5cc6f007fa16d4cb548526a8adda9e4b.png)

在这个程序中，我们从用户那里得到最终术语。我们必须显示一个斐波纳契数列直到这个数字。这是通过使用 while 循环来完成的。我们接受用户的输入，这是最后一项。然后打印第一项和第二项。在此之后，将第一个和第二个相加，存储在 sum 中。然后，有一个 while 循环。它一直运行到总和的值小于用户输入的数字的值。在 while 循环中，首先打印出总和。

在下一部分中，我们将第二项的值赋给第一项，然后将 sum 的值赋给第二项。我们再次执行加法，将第一项和第二项相加，并将其赋值为总和。循环运行，直到总值大于用户输入的数字。

## **10 的斐波那契是什么？**

斐波纳契数列是通过将前两个数字相加得到下一个数字来实现的，从 0 和 1 开始:

`#include <iostream>``using namespace std;``int main ()``{``int a = 0, b = 1;``cout << a << ", " << b;``for (int i = 0; i < 8; i++)``{``cout << ", " << a + b;``b = a + b; // b is the sum of the 2 numbers``a= b - a; // a is the old y``}``}`

## **0 是斐波那契数吗？**

没错，斐波那契数列就是数列: 0，1，1，2，3，5，8，13，21，34，…

让我们继续讨论 C 语言文章中斐波纳契数列的最后一点。

## **使用递归的斐波那契数列**

另一种编程斐波那契数列生成的方法是使用递归。递归是以自相似的方式重复项目的过程。在编程语言中，如果一个程序允许你在同一个函数中调用一个函数，那么它就被称为该函数的递归调用。

**代码:**

```

#include<stdio.h>
int f(int);
int main()
{
int n, m= 0, i;
printf("Enter Total terms:n");
scanf("%d", &n);
printf("Fibonacci series terms are:n");
for(i = 1; i <= n; i++)
{
printf("%dn", fibonacci(m));
m++;
}
return 0;
}
int fibonacci(int n)
{
if(n == 0 || n == 1)
return n;
else
return(fibonacci(n-1) + fibonacci(n-2));
}

```

**输出:**

![Output - Fibonacci Series in C - Edureka](img/e50bcfb70a6fb7db54a334d46f1c285d.png)

在这个程序中，我们使用递归来生成斐波那契数列。函数 fibonacci 被递归调用，直到我们得到输出。在函数中，我们首先检查数字 n 是零还是一。如果是，我们返回 n 的值。如果不是，我们用值 n-1 和 n-2 递归调用 fibonacci。

**这些是在 c 中生成斐波那契数列的方法。**

至此，我们结束了这篇关于“C 语言闰年程序”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这篇文章的评论部分提到它们，我们会给你回复。