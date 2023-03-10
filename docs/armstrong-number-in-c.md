# 如何用 C 实现阿姆斯特朗数？

> 原文：<https://www.edureka.co/blog/armstrong-number-in-c/>

使用查找阿姆斯特朗数字可能是一项棘手的任务。因此，许多面试或考试都有这个问题。在这篇文章中，我们将看到如何在 c 中实现阿姆斯特朗数。

本文将关注以下几点:

*   [C 中的阿姆斯特朗数](#ArmstrongNumberinC)
*   来自阿姆斯特朗号的程序
*   [N 位数的阿姆斯特朗数](#ArmstrongNumberforNdigits)
*   [阿姆斯特朗数使用函数](#ArmstrongNumberusingFunctions)

让我们从本文的第一个主题开始，

## **C 中的阿姆斯特朗数**

三位数的阿姆斯壮数是这样一个数，其中数字的立方之和等于该数本身。

**考虑这个例子:**

153 是阿姆斯特朗的号码

所以，1*1*1+5*5*5+3*3*3=1+125+27=153

因此 153 是阿姆斯特朗的数字。

现在让我们继续这篇关于 C 语言中阿姆斯特朗数的文章，看看如何实现一个同样的程序，

## **程序来自阿姆斯壮** **号**

```

#include <stdio.h>
int main()
{
int num, original, rem, sum = 0;
//rem is remainder and original is the original number
printf("Enter a three-digit Number: ");
scanf("%d", &num);
original = num;
while(original != 0)
{
rem = original%10;
sum =sum + rem*rem*rem;
original=original/ 10;
}
if(sum == num)
printf("%d is an Armstrong number.",num);
else
printf("%d is not an Armstrong number.",num);
return 0;
}

```

**输出:**

如果是阿姆斯特朗号。

![Output - Armstrong Number In C - Edureka](img/d0a2e4443080fe1a1dff6010c9aa64b6.png)

如果不是阿姆斯特朗编号:

![Output - Armstrong Number In C - Edureka](img/24d86ed5a136c2632bb3bcaa48938b18.png)

在上面显示的程序中，我们首先声明程序中将要使用的所有变量。我们使用一个 num 来保存用户输入的数字。原始变量用于保存原始数字。“rem”用于保存计算所需的余数。最后我们有 sum 变量，它被赋值为零。

我们首先从用户那里接受一个 3 位数的数字，并将其存储在 num 中。然后，我们将它分配给原件。我们这样做是为了在上面的代码中对原始数据进行修改，并保证用户输入的数字的安全，以便用它与计算后得到的数字进行比较。

接下来，我们有 while 循环。这一直运行到原始值为零。在 while 循环中，要执行三个步骤。首先，我们得到数字的最后一位，并将其存储在 rem 中。这是通过在原件上使用 mod 运算符来完成的。Mod 运算符在使用时给出余数。如果我们考虑这个例子，153% 10 会给我们 3，它将存储在 rem 变量中。

在下一步中，我们将 rem 变量的立方添加到 sum 中，并将其赋给 sum 变量。在最后一步中，我们将原始值除以 10。这样做是因为我们不再需要最后一位数字，因为它已经被使用了。因为它是一个整数值，小数点后的数字将不被考虑。如此重复，直到原始值等于零。然后退出 while 循环。

之后，我们将总和与包含用户在 if 语句中输入的数字的 num 变量进行比较。如果和等于 num，那么它就是一个阿姆斯特朗数，If 部分将被执行。否则，将执行 else 部分。

让我们来看看实施这一计划的其他方式，

**N 位数的阿姆斯特朗数**

我们可以写同样的代码来寻找 n 位数的阿姆斯特朗数，只需稍作修改。

**代码:**

```

#include <stdio.h>
#include <math.h>
int main()
{
int num, original, rem, sum = 0, n = 0 ;
printf("Enter a Number: ");
scanf("%d", &num);
original = num;
while (original != 0)
{
original /= 10;
++n;
}
original = num;
while (original != 0)
{
rem = original%10;
sum += pow(rem, n);
original /= 10;
}
if(sum == num)
printf("%d is an Armstrong number.", num);
else
printf("%d is not an Armstrong number.", num);
return 0;
}

```

**输出:**

![Output - Armstrong Number In C - Edureka](img/a41892bf14f37f9a751d8f4b4e3dd0f5.png)

在这个程序中，与 3 位数的阿姆斯特朗数检测程序相比，有一个微小的变化。第一个变化是:

```

while (original != 0)
{
original /= 10;
++n;
}

```

这样做是为了计算输入的位数。这样做直到原始值为零。n 递增，直到原始值为零。这是我们得到总位数的方法。

在此之后，我们在 original 进入第二个循环之前，再次将其编号赋给 original。在第二个循环中，我们对数字进行了立方运算，并将其添加到 3 位数代码的 sum 中。但是，对于 n 位数，我们必须使用名为 pow 的 math.h 函数来执行此练习。

```
sum += pow(rem, n);
```

在这个语句中，我们将余数 rem 提升到 n 的，并将其添加到 sum 变量中。这些都是我们需要在这个程序中进行的更改。

让我们从 C 语言中阿姆斯特朗数的最后一位开始，

## **阿姆斯特朗数使用函数**

使用函数可以执行相同的程序。

```

#include <stdio.h>
#include <math.h>
int armstrongNumberFinder(int n);
int main()
{
int n, flag;
printf("Enter a positive integer: ");
scanf("%d", &n);
flag = armstrongNumberFinder(n);
if (flag == 1)
printf("%d is an Armstrong number.", n);
else
printf("%d is not an Armstrong number.",n);
return 0;
}
int armstrongNumberFinder(int num)
{
int original, rem, sum = 0, n = 0, flag;
original = num;
while(original != 0)
{
original /= 10;
++n;
}
original = num;
while(original != 0)
{
rem = original%10;
sum += pow(rem, n);
original /= 10;
}
if(sum == num)
flag = 1;
else
flag = 0;
return flag;
}

```

**输出:**

![Output - Armstrong Number In C - Edureka](img/8b48383984df68c0ce87054943b9eaf3.png)

输出完全相同，但是程序的结构发生了变化。这里调用一个函数来计算阿姆斯特朗数，并将结果返回给主程序。这增加了功能的可用性。

这些是寻找阿姆斯特朗数的各种类型的程序。

至此，我们结束了这篇关于“阿姆斯特朗 C 数”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。