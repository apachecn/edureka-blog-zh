# 2023 年安卓面试新手问答

> 原文：<https://www.edureka.co/blog/interview-questions/android-interview-questions-answers-for-beginners/>

在我们的 [上一篇文章](https://edureka.co/blog/top-5-android-interview-questions-for-freshers/ "Android Interview Questions") 中，我们讨论了一个初学者在参加 Android 开发者面试时可能遇到的最常见的面试问题。这篇 Android 初学者教程涵盖了对这些问题的回答。这些问题及其答案都是在 ***[Android 认证](https://www.edureka.co/android-development-certification-course)*** 专家的监督和指导下严格策划的，这些专家也是具有多年开发、培训和招聘经验的工作专业人士。读了上一篇文章，你现在知道面试官对你的期望了，包括技术上和行为上的。所以，你可以做好相应的准备！

## 安卓面试问答

**I)Android 有哪些组件？**

 <caption>#### **安卓组件**</caption> 
| **分量** | **描述** |
|  | 

*   Activity provides an interface for users to interact with the application and take actions.
*   An application generally has multiple activities.

 |
|  | 

*   Use intention to allow applications to request actions from other application components.
*   For example, viewing, calling, playing, etc.

 |
| ***[服役](https://edureka.co/blog/android-tutorials-beginners-service-component/ "Android Services")*** | 

*   Services are components without user interface; They run in the background.
*   They will continue to run even if you switch to another activity or application.

 |
| ***[广播接收器](https://edureka.co/blog/android-tutorials-broadcast-receivers/ "Broadcast Receivers")*** | 

*   Content provider is a data repository that supports data sharing between different applications.
*   Content providers provide a unified interface to access data such as call records.

 |
|  | 

*   The broadcast receiver will only work under certain circumstances.
*   Assuming that there is an intention that a specific broadcast receiver has registered, the broadcast receiver is triggered and the user gets the same notification.
*   For example, a low battery notification.

 |

在 Edureka 的 Android 初学者培训中，您将通过示例了解整个过程。

**II)给你一些 C 编程题**

**1)不使用分号(；)?**

在看解决方案之前稍微想一想。

**解决方法** 这个问题可以用不止一种方法来解决: a)

```
 #include<stdio.h>
  void main()
  {
  if(printf("Hello World")) { }
  }
```

b)

```
  {
  while(printf("Hello World")){}
  }
```

c)

```
 { do{} while(printf("Hello World")){} }
```

初学面试有时候可以在安卓问选择题编程问题。看看这个例子:

**2)下面的 C 代码会输出什么？**

```
#include<stdio.h>
int main()
{
int *a1;
char **a2;
float ***a3;
double ****a4;
printf("%d %d %d %d ",sizeof(a1),sizeof(a2),sizeof(a3),sizeof(a4));
return 0;
}
Options 
```

a) 1 2 4 8

b) 2 4 4 8

c) 2 4 2 4

d) 2 2 2 2

答案:d.

指针的大小是相同的，不管它是什么类型(2 字节)

注意–这是假设我们在 32 位机器上。在 64 位上，它将是 4 字节。

**III) Java 编码问题**

**1)能不能写个 java 代码把两个数互换？**

解决办法

```
public class Swap {
public static void main(String[ ] args)  {
int x = 5;
int y = 6;
//store 'x' in a temp variable
int temp = x;
x  =  y;
y  =  temp;
System.out.println("x=" + x+ "y=" + y);
}
}
```

2)编写 Java 代码来交换两个数字，而不使用第三个变量，即上面例子中的 temp。 强悍..？？

不尽然；事实上你已经知道了:)

**解决方案**

```
public class Swap {
public static void main(String[ ] args)  {
int x = 5;
int y = 6;
//Add both the variables and store them in x  i.e x = 11 (x=5 + y=6).
x = x + y;
//Now subtract y from x and store in y i.e y = 5 (x=11 - y=8) . Hence initial value of x is assigned to y.
y = x - y;
//Now subtract y from x and store in x i.e x = 6 (x=11 - y=5) . Hence initial value of y is assigned to x.
x = x - y;
// Both the values are swapped successfully without using the third variable
System.out.println("x=" + x+ "y=" + y);
}
}
```

知识渊博的候选人应该回答比这些更难的问题。然而这篇文章讨论的是 Android 初学者的基础知识，所以我们将在后面的文章中为一个有经验的 Android 开发者处理面试问题。敬请关注。

快乐学习！

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[安卓入门培训](https://www.edureka.co/android-development-certification-course "get started with Android Development")

[大一新生 5 大安卓面试题](https://www.edureka.co/blog/interview-questions/top-5-android-interview-questions-for-freshers/ "Top 5 Android Interview Questions for freshers")

[安卓初学者教程:活动组件](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/ "Android Tutorials for Beginners Part-1: Activity component")

[安卓项目:二十一点游戏](https://www.edureka.co/blog/android-tutorial-on-blackjack/ "Android Project : BlackJack Game")

[【Android 初学者指南:Android 架构](https://www.edureka.co/blog/beginners-guide-android-architecture/ "The Beginner’s Guide to Android: Android Architecture")