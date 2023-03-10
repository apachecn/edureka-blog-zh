# C 语言中的 Switch Case:你需要知道的一切

> 原文：<https://www.edureka.co/blog/switch-case-in-c/>

switch case 是 c 语言中非常重要的工具，它是编程中的一个循环语句。当有许多条件时，它帮助我们减少 if/else 的使用。在本文中，我们将了解 [C](https://www.edureka.co/blog/bubble-sort-in-c/) 中的开关情况。以下是本文将要讨论的指针，

*   [C 中的开关箱](#SwitchCaseInC)
*   [C 中开关的执行](#ExecutionOfSwitchInC)

那么让我们开始吧，

## **C 中的开关箱**

在 switch 语句中，我们传递一个变量，该变量包含语句中的一个值。如果条件与值匹配，则执行条件下的代码。条件由关键字 case 表示，后跟可以是字符或整数的值。在这之后，有一个冒号。每种情况都有一个 break 语句，使控制离开循环。如果找不到匹配的案例，则执行默认语句。

**语法:**

```
</p>
switch (n)
{
case 1 : //execute if n=1
break;
case 2 : //execute if n=2
break;
case 3 : //execute if n=3
break;
default: // execute this code if none of the cases match
}
<p style="text-align: justify;">
```

这是开关盒的使用方式。

记住，传递给开关的变量必须包含一个字符或整数值，不能是复杂值，只能是简单值。

## **C 中开关情况的执行**

如果 n 的值是 1，那么情况 1 下的代码将被执行，并使用 break 语句从循环中断开。类似地，如果值为 2，它将首先检查情况 1，如果不匹配，控制将转到情况 2。如果有匹配，它将被执行，然后是一个 break 语句。如果检查所有案例后，没有匹配的条件，则执行默认条件。

使用 break 是为了防止其他案例被执行，即使在找到匹配项并执行其下的语句之后。如果没有 break 语句，那么它下面的 case 语句也会被执行。除了默认情况之外，每个案例都应该有 break 语句。违约是可选的。

默认案例是可选的，但是拥有一个默认案例是一个好习惯。

**示例开关代码:**

```

#include <stdio.h>
int main()
{
int m=0;
printf("enter your choice:n 1.book a car:n 2.book a bus:n 3.book a flight:n");
//accepting user choice
scanf(" %d",&m);
//passing choice in switch case
switch (m)
{
case 1:
printf("Car is booked");
break;
case 2:
printf("Bus is booked");
break;
case 3:
printf("Flight is booked");
break;
default:
printf("Invalid input");
break;
}
return 0;
}

```

**输出:**

如果找到匹配的案例。

![Feature Image - Switch Case In C - Edureka](img/a9ce904d6b8d5f468ac43bb66f1e2b09.png)

如果没有找到匹配的案例:

![Feature Image - Switch Case In C - Edureka](img/029cbeb983f38e86f47e44b7b35fe4f1.png)

上面的程序是一个用 c 语言编写的 switch case 的基本演示。我们根据用户的选择接受用户的输入。用户选择在 switch 语句中发送。switch 语句检查是否有匹配的大小写。在上面的代码中，用户首先选择 3，因此执行该块下的语句，即“预订航班”。如果用户输入的值超出该范围，则执行默认情况。在上面的示例中，用户输入 7，然后执行 default 下的语句。

至此，我们结束了这篇关于“C 语言中的 Switch Case”的文章。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这篇文章的评论部分提到它们，我们会给你回复。