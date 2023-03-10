# 如何在 C 语言中最好地利用幂函数？

> 原文：<https://www.edureka.co/blog/power-function-in-c/>

求一个数的幂是[编程逻辑](https://www.edureka.co/programming-and-frameworks-certification-courses)中非常常见的运算。在这篇文章中，我们将了解如何使用 C 语言中的幂函数编写程序来计算一个数的幂。本文将涉及以下几点:

*   [乘方逻辑](#LogicForPowerMultiplication)
*   [编写自定义功率函数](#WritingaCustomPowerFunction)
*   [C 中的幂函数](#PowerFunctioninC)

让我们从理解如何写一个程序来计算一个数的幂开始。

## **乘方逻辑**

2 <sup>3</sup> = 2*2*2 = 8

要找到 2^3，你需要将 2 乘以 3。这可以通过使用 for 循环简单地实现。

对于上面的例子，基数= 2，指数= 3。

```
for (exponent=3; exponent>0; exponent--)
{
result = result * base;
}
```

让我们看一下实现相同功能的 C 程序。

**例子**

```
#include <stdio.h>
int main()
{
int base, exponent;
int result = 1;
printf("Enter a base number: ");
scanf("%d", &base);
printf("Enter an exponent: ");
scanf("%d", &exponent);
for (exponent; exponent>0; exponent--)
{
result = result * base;
}
printf("Answer = %lld", result);
return 0;
}
```

**输出:**

![Output - Power FUnction In C - Edureka](img/11d79b4b2354d3999e5f29a7c58a256c.png) 继续这篇关于 C 中幂函数的文章

## **编写自定义功率函数**

你也可以创建一个函数来计算幂，你可以在任何时候调用它来计算任意整数的幂。

```
int power(int base, int exponent)
{
int result=1;
for (exponent; exponent>0; exponent--)
{
result = result * base;
}
return result;
}
```

让我们看看如何使用这个函数的完整代码。

**例子**

```
#include <stdio.h>
int power(int base, int exponent){
int result=1;
for(exponent; exponent>0; exponent--){
result = result * base;
}
return result;
}
int main()
{
int base, exponent;
printf("Enter a base number: ");
scanf("%d", &base);
printf("Enter an exponent: ");
scanf("%d", &exponent);
int res = power(base, exponent);
printf("Answer = %lld", res);
return 0;
}
```

**输出:******

![Output - Power FUnction In C - Edureka](img/3cd68e49f5877b28d33ce7b619c05626.png)

只有当指数是正整数时，这种技术才有效。 ***如果想求一个指数为实数的数的幂，需要使用 pow()函数。***

继续这篇关于 C 语言中的幂函数的文章

## **C 中的幂函数**

*   函数的作用是:计算一个给定数字的幂。
*   它返回 x 的 y 次幂(即 x <sup>y</sup> )。
*   pow()函数存在于 math.h 头文件中。所以，你需要在程序中导入 math.h 头文件来使用 pow()函数。

#包括<math.h></math.h>

*   幂函数的声明如下:

***声明*** : double pow(双 ***基数*** ，双 ***指数***)；

*   pow()函数采用两个参数(即 ***底数*** & ***指数)*** &返回将 ***底数*** 提高到幂 ***指数*** 的结果。
*   调用幂函数:

***【2.4，3.2】***

其中 2.4 是基数，3.2 是指数

让我们快速看一个例子来理解如何在程序中使用 pow()函数。

**举例:**

```
#include <stdio.h>
#include <math.h>
int main()
{
double base, expo, res;
printf("Enter a base number: ");
scanf("%lf", &base);
printf("Enter an exponent: ");
scanf("%lf", &expo);
res = pow(base, expo);
printf("%.1lf^%.1lf = %.2lf", base, expo, res);
return 0;
}
```

**输出**

现在，在执行了上面的程序之后，你应该已经理解了如何在 c 语言中使用幂函数。我希望这篇文章能给你提供信息并增加价值。

请继续关注更多类似主题的教程。您也可以查看我们的培训项目 t 以获得关于 jQuery 及其各种应用程序的深入知识，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册参加实时在线培训，享受全天候支持和终身访问。 用不同的字符串和修改实现上面的代码。现在，我们已经很好地理解了与指针相关的所有关键概念。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。