# 如何用 C 实现闰年程序？

> 原文：<https://www.edureka.co/blog/leap-year-program-in-c/>

如果你是一名程序员，并且参加过面试，你会知道有很多编程面试可能会有一个问题，就是编写一个代码来找出闰年。这个看似简单的棘手问题困扰着许多人。在本文中，我们将讨论如何用 c 语言实现闰年[程序](https://www.edureka.co/blog/c-data-structures)

让我们从理解什么是闰年开始这篇文章

## 什么是闰年？

闰年每四年出现一次。这一年有 366 天，而不是 365 天。我们可以编写一个简单的 if else 代码来确定这一年是否是闰年。

**C 代码:在 C 语言中寻找闰年**

```
#include <stdio.h>
int main()
{
int year;
printf("Enter a year to check if it is a leap yearn");
scanf("%d", &year);
if(year%400 == 0)
printf("%d is a leap year.n", year);
else if(year%100 == 0)
printf("%d isn't a leap year.n", year);
else if (year%4 == 0)
printf("%d is a leap year.n", year);
else
printf("%d isn't a leap year.n", year);
return 0;
}

```

**输出:**

如果是闰年:

![Output - Leap Year Program In C - Edureka](img/19963aad1c49d3b3adabf2a81d376bb7.png)

如果不是闰年，

**![Output - leap year in c - Edureka](img/87e52612650595f536ed47476e4bd83f.png)**

**解释**

在上面的代码中，我们接受用户的输入。然后我们检查一系列条件。我们首先检查用户输入的年份是否能被 400 整除。这样做是为了检查年份是否能被 400 整除，例如 1600、2000、4000、2400 等。

接下来，如果年份不能被 400 整除，那么检查年份是否能被 100 整除。如果它不能被 400 整除，但能被 100 整除，那么它就不是闰年，例如 1900、2100、2200、1800、1300。

如果一年不能被 400 或 100 整除，那么检查它是否能被 4 整除，如果能，那就是闰年。比如 2016，2020，2024，2032，2048 等等。 最后，如果不能被 4400 或 100 整除，就不是闰年。比如 2021，2018，2019，2022，2015 等等。这正是上面的条件语句所做的。

**这是检查是否是闰年的 4 个条件。**

至此，我们结束了这篇关于“C 语言闰年程序”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。