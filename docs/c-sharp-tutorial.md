# C#教程:掌握 C#所需的基础知识

> 原文：<https://www.edureka.co/blog/c-sharp-tutorial/>

C#是微软公司在 2000 年开发的通用且健壮的编程语言，是 Java 的致命竞争对手。就 web 开发和桌面应用程序开发而言，它是最受欢迎和占主导地位的编程语言。

在本 C#教程中，我们将学习以下概念。

*   [C#基础知识](#basics)
*   [面向对象编程](#oops)
*   [高级 C#概念](#advanced)
*   [基于 C#的面试问题](#interview)

## **C#基础知识**

*   [c#编程语言简介](#intro)
*   [c#编程语言的特点](#feature)
*   [安装](#installa)
*   [C#程序结构](#stru)
*   [数据类型](#dtype)
*   [变量](#var)
*   [操作员](#oper)
*   [循环](#loop)
*   [条件](#condition)
*   [琴弦](#string)
*   [数组](#array)
*   [收藏](#collect)
    *   [列表](#lis)
    *   [哈希集合](#hash)
    *   [已排序集合](#sort)
    *   [堆栈](#stack)
    *   [队列](#Q)
    *   [链表](#linked)
    *   [字典](#dict)
    *   [分类词典](#sortd)
    *   [排序列表](#sortl)
*   [结构](#struc)
*   [功能](#funct)

**c#编程语言简介**

早在 90 年代早期，Java 是 web 开发、桌面应用程序开发和许多其他领域的领先编程语言。微软想找一个拥有许多高级特性的竞争对手，把 Java 远远甩在后面。

![C#-Tutorial-hejlsberg_bio](img/257383bd3b278e55c2922abef01e4aa6.png)

那是在 2000 年， **安德斯·海尔斯伯格**和他的微软团队提出了 C#的想法，也就是通常所说的 C-Sharp。这一倡议得到了国际标准组织 **(ISO)** 和欧洲计算机制造商协会 **(ECMA)的批准。最后，C#进入了软件开发的世界。**

**c#编程语言的特点**

*   **面向对象的编程语言**

面向对象的编程方法使得 C# sharp 成为最友好的程序员，并且易于开发和维护编程语言。

*   **类型安全语言**

类型安全的含义是，编译器只能访问有权执行的内存位置。这个特性将代码安全性提高到了指数级。

*   **互操作性**

互操作性的特性使得 C#有足够的能力以一种比 C++本身更有效的方式做 C++固有的一切事情。

*   **富库**

C#提供了对多个内置库的访问，这些库提供了预编程的功能以减少开发过程中花费的时间。

![C# Tutorial Edureka Features](img/8e89c63f7a9d8dd57d787ada32ec364e.png)

*   **可扩展和可更新**

C#被设计成优于其他编程语言。因此，它总是对更新开放，并保持其特性的高度可伸缩性。

*   **面向组件**

微软的开发人员使用基于组件的方法来开发 C#。这是保持 C#高度可伸缩和更新的最主要的开发方法。

*   **结构化语言**

在软件开发生命周期中，结构化编程方法是首选，因为与面向过程的编程方法相比，它更容易开发、编译和部署软件。

*   **快**

与 C++和其他编程语言相比，C#编程在编译和执行上要快得多。

**安装**

实践证明，微软 Visual Studio 的 [**是 C#编程最好的类编辑器。我们将按照下面提到的步骤安装和设置 Microsoft Visual Studio 来执行我们的 C#程序:**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Professional&rel=16)

**第一步** : [**下载微软 Visual Studio**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Professional&rel=16)

谷歌一下 Visual Studio 的**最新版本，下载**安装程序**文件到你的本地系统，然后**以** **管理员的身份运行**安装程序文件**。****

![C# Tutorial Edureka Install 1](img/9506f6ec24bd16b1586c5fb3d67c8563.png)

![C# Tutorial Edureka Install 2](img/0c6ba25000d57fcab2fafef0a9a3ee8b.png)

**第二步:选择。NET 桌面开发包**

一旦你运行安装程序，Visual Studio 编辑器将被成功下载到你的本地系统中，稍后一个对话框将显示在你的桌面屏幕上，询问你在你的系统中需要一个特定的**包**。在这里，你需要选择**。NET 桌面开发**包。

![C# Tutorial Edureka Install 3](img/17f741c6b13a183948bbcc318fe2f946.png)

![C# Tutorial Edureka Install 4](img/2c4cba9092af31bbd30060bffeb5d29d.png)

**第三步:设置 C#环境**

一旦你的包裹为**。NET Development** 被下载后，屏幕上会显示另一个对话框，询问您正在寻找的开发环境。在这里，你需要**为 C#选择环境。**

![](img/05bb0ae202b115fb56e1bb3b0ad1d7a5.png)

第四步:创建你的第一个项目

一旦环境设置好了，你就可以开始了。启动 Visual Studio 并在显示的对话框中选择**创建新项目**选项。

![C# Tutorial Edureka Install 6](img/83299618276fb120569d9ffd147d7e80.png)

你将被重定向到下一个对话框，在那里你需要选择类库作为**。网标**如下图所示。

![C# Tutorial Edureka Install 7](img/2569cec908b25dcfe0e8cc9abd3f7f46.png)

在下一个对话框中，您将被要求**配置您的项目**。配置它，你现在在编辑器中。编写你的第一个程序，然后**运行**它。输出将成功显示在**命令提示符上。**

```
using System;
class Edureka
{
     static void Main(string[] args)
    {
         Console.WriteLine("Welcome to Edureka!, Happy Learning..!");
    }
}

```

![C# Tutorial Edureka Install 9](img/3a13a36b4022098d4e71a46787288132.png)

**//输出:**

![C# Tutorial Edureka Install 10](img/2dc4f2886fc4f555e8429f67cf519413.png)

让我们执行我们的第一个 C#程序。

**C#程序结构**

现在我们已经执行了我们的第一个 C#程序，让我们详细了解它的结构。一个简单的 C#程序有以下几个部分。

```
using System;  
namespace ConsoleApplication1  
{  
    public class Edureka  
    {  
        public static void Main(string[] args)  
        {  
            Console.WriteLine("Welcome to Edureka!, Happy Learning..!");  
        }  
    }  
}

```

**//输出:**

`Welcome to Edureka!, Happy Learning..!`

*   **class:** class 一般可以定义为一个**关键字**，用于在 C#程序中定义一个类。
*   **Edureka:** 它是**类的名字。**类通常被认为是存储了与类相关的成员和方法的蓝图。
*   **Main:** 基本上是整个 C#程序的**主方法**，它充当控件进入程序的网关。它在程序的任何其他方法执行之前被执行。
*   **void:** 这段代码被指定给方法的**返回类型**。它可以是除 void 之外的任何数据类型。Void 意味着该方法没有从它返回任何数据。
*   **static:** 这是一个**关键字**，表示声明的数据成员是静态的，并且为声明的成员分配了一个专用内存。
*   **String[] args:** 它类似于我们在程序中使用的命令行参数。当我们执行程序时，我们基本上传递一些**参数，**，由于这个语句，这些参数将被程序接受。
*   **系统。Console.WriteLine("欢迎来到 Edureka！，快乐学习..!");** 在这里，是 **的命名空间。**控制台就是系统命名空间中概述的类别。 **WriteLine()** 是控制台类别的静态技术，用于在控制台上写下文本。

现在，让我们学习 C#中可用的数据类型。

**数据类型**

C#中的数据类型分为三类，如下所述。

![C# Tutorial Edureka Datatypes](img/e2a543008b255755d66db649cfe22534.png)

**数值数据类型**

**值数据类型**位于**系统中。ValueType** 库，并且总是准备好被直接访问，变量可以被直接赋值给一个特定的值。值数据类型进一步分为两种类型，如下所示:

*   **预定义的数据类型**
*   **用户定义的数据类型**

**预定义的数据类型:**这些是我们在日常编程中通常使用的数据类型。这些数据类型是由语言开发人员预先定义的，随时可供程序员使用。

**举例:**

**int、float、char、short double 等**

用户定义的数据类型:有些情况下，我们可能需要将不同数据类型的值存储到一个变量中。在这些情况下，**预定义的数据类型**是不够的。**用户自定义的**数据类型就像是用户可定制的数据类型。

**示例:结构，枚举**

| **Datatype** | **分配的内存范围** | **内存大小** |
| **带符号字符** | **-128 到 127** | 1 字节 |
| **无符号字符** | **0 到 127** | 1 字节 |
| **字符** | **-128 到 127** | 1 字节 |
| **带符号短码** | **-32768 至 32767** | 2 字节 |
| **无符号短整型** | **0 到 65535** | 2 字节 |
| **短** | **-32768 至 32767** | 2 字节 |
| **带符号整数** | **-2147483648 至-2147483647** | 4 字节 |
| **无符号整数** | **0 到 4294967295** | 4 字节 |
| **int** | **-2，147，483，648 至-2，147，483，647** | 4 字节 |
| **签名长** | **-9223372036854775808 至 9223372036854775807** | 8 字节 |
| **无符号长整型** | **0 到 18，446，744，073，709，551，615** | 8 字节 |
| **龙** | **-9223372036854775808 至 9223372036854775807** | 8 字节 |
| **浮动** | **1.5 * 10-45–3.4 * 1038，(7 位精度)** | 4 字节 |
| **double** | **5.0 * 10-324–1.7 * 10308，(15 位精度)** | 8 字节 |
| ** decimal** | **-7.9 * 10-28–7.9 * 1028，(28 位精度)** | 16 字节 |

**指针数据类型**

指针类型是一种简单的数据类型。它的功能完全类似于 c 语言中的指针，它们被设计用来存储另一个指针的地址。

```
float* ptr;

```

**参考数据类型**

这个名字不言自明。**引用数据类型**实际上不存储变量，而是存储特定变量的引用值。换句话说，它们存储实际变量的地址。

参考变量分为三种不同类型，如下所述:

*   **对象类型**

对象数据类型在**系统中可用。对象**类。对象类型可以将赋值给其他类型的值，引用类型，预定义，用户自定义类型。但是，在赋值值之前，需要进行 **类型** **转换。**

```
object abc;
abc = 50;  //this is called boxing

```

*   **动态类型**

动态类型变量被设计用来存储几乎所有类型的值。它被称为动态类型，因为值的类型检查发生在运行时

```
dynamic x=10;

```

*   **字符串类型**

字符串类型在**系统中可用。字符串**类。String 类型旨在存储字符串文字。字符串以两种形式存储在的两种形式中

```
String S = "Edureka";

```

*   **@引用的**字符串看起来像

```
@"Edureka";

```

现在让我们来理解这些变量。

**变量**

变量是分配给存储用户给定的某些数据的内存位置的名称，使用变量名可以很容易地访问这些数据。C#中有五种变量

| **类型** | **例子** |
| **Null** | Null data |
| **布尔型** | 真假 |
| **整数** | Int，Char，Byte，Short，Long |
| **浮动** | 浮点和双精度 |
| **Decimal** | 小数 |

**举例:**

```
int a, b;  
double x;      
float p;      
char abc;

```

**在 C#中声明变量应遵循的规则**

*   变量可以包括字母、数字和下划线。
*   变量名只能以字母或下划线开头。
*   变量不能以数字或特殊字符开头。
*   变量名之间不允许有空格。
*   保留关键字被限制用作变量名。

**操作员**

运算符可以定义为一个特殊的符号，它解释了计算机对一组变量执行特定的数学逻辑运算。C#包括各种运算符，如下所述。

*   算术运算符
*   关系运算符
*   逻辑运算符
*   按位运算符
*   赋值运算符

**算术运算符**

| **操作员** | **例子** | **描述** |
| **+** | **A + B** | 将两个操作数相加 |
| **–** | **A–B** | 减去两个操作数 |
| ***** | **A * B** | 两个操作数的倍数 |
| **/** | **A / B** | 将两个操作数相除 |
| **%** | **A % B** | 两个操作数的余数 |
| **++** | **A++** | 增量操作 |
| **—** | **A—** | 减量操作 |

**关系运算符**

| **操作员** | **例子** | **描述** |
| **==** | **A == B** | 如果两个操作数相等，则为真，否则为假 |
| **！=** | **答！= B** | 如果两个操作数不相等，则为真，否则为假 |
| **>** | **甲>乙** | 如果 A 更大，则为真，否则为假 |
| **<** | **甲<乙** | 如果 B 更大，则为真，否则为假 |
| >= | **甲> =乙** | 如果 A 大于或等于，则为真，否则为假 |
| **< =** | **甲< =乙** | 真，id B 大于等于，否则为假 |

**逻辑运算符**

| **操作员** | **例子** | **描述** |
| **&&** | **A&B** | 如果两个操作数都为真，则为真，否则为假 |
| **&#124;&#124;** | **A &#124;&#124; B** | 如果操作数之一为真，则为真，否则为假 |
| ！ | **答！B** | 反转操作数的逻辑状态 |

**按位运算符**

| **答** | **B** | **甲&乙** | **A &#124; B** | **甲^乙** |
| **1** | **1** | **1** | **1** | **0** |
| **1** | **0** | **0** | **1** | **1** |
| **0** | **1** | **0** | **1** | **1** |
| **0** | **0** | **0** | **0** | **0** |

| **操作员** | **例子** | **描述** |
| ~ | **(~A)** | 二进制一的补码运算符是一元的，具有“翻转”位的效果。 |
| **<<** | **一<二<一** | 二元左移运算符。左操作数值左移右操作数指定的位数。 |
| >> | **一>二>一** | 二元右移位运算符。左操作数的值向右移动右操作数指定的位数。 |

**赋值运算符**

| **操作员** | **例子** | **描述** |
| **=** | **A = B+C** | A=B+C，B+C 赋给 A |
| **+=** | **A += B** | A=A+B，A+B 赋给 A |
| **-=** | **A -= B** | A=A-B，A-B 被分配到 A |
| ***=** | **A -= B** | A=A*B，A*B 赋给 A |
| **/=** | **A /= B** | A=A/B，A/B 分配给 A |
| **%=** | **A %= B** | A=A%B，A%B 被分配给 A |
| **< < =** | **一个< < = 2 个** | 左移和赋值运算符 |
| **> > =** | **一个> > = 2 个** | 右移位和赋值运算符 |
| **& =** | **一个& = 2 个** | 按位 and 赋值运算符 |
| **^=** | **一个^= 2** | 按位异或赋值运算符 |
| **&#124;=** | **答！= 2** | 按位包含和赋值运算符 |

**循环**

**循环** 语句用于重复执行一组语句，直到满足特定条件。C#语言由以下循环语句组成。

*   For 循环
*   While 循环
*   Do While 循环

**为循环**

循环的**用于多次执行一个特定的代码段，直到满足给定的条件。**

**语法**

```
for(initialization; condition; increment/decrement)
{  
	//code segment
}

```

**流程图:**

![c#-tutorial-for-loop](img/c99b5ab4e1fe8d3e7edd5873e60dc899.png)

**举例:**

```
using System;
public class ForExample
{
    public static void Main(string[] args)
    {
        for (int i = 1; i<= 5; i++)
        {
            Console.WriteLine(i);
        }
    }
}

```

**//输出:**

`1``2``3``4`

**While 循环**

**While 循环**用于多次执行一个代码段，直到满足特定条件。

**语法**

```
while(condition)
{  
	//code to be executed  
} 

```

**流程图:**

![](img/73429fb9f368e92a463a7988e7bfc1d8.png)

**举例:**

```
using System;

namespace Loops
{
    class Program
    {
           static void Main(string[] args)
           {
                  int x = 5;
                  while (x<= 10)
                  {
                        Console.WriteLine("The value of a: {0}", x);
                        x++;
                  }
                  Console.ReadLine();
           }
     }
}

```

**//输出:**

`The value of a: 5``The value of a: 6``The value of a: 7``The value of a: 8``The value of a: 9`

**Do While 循环**

Do while 循环与 while 循环完全相似，但唯一的区别是条件放在循环的末尾。因此，循环至少执行一次。

**语法**

```
do
{  
	//code to be executed  
}while(condition); 

```

**流程图:**

![](img/86379119773849571c4bb4bcd7013868.png)

**举例:**

```
using System;
namespace Edureka
{
    class DoWhileLoop
    {
        public static void Main(string[] args)
        {
            int i = 1, n = 5, product;
            do
            {
                product = n * i;
                Console.WriteLine("{0} * {1} = {2}", n, i, product);
                i++;
            } while (i<= 10);
        }
    }
}

```

**//输出:**

`5 * 1 = 5``5 * 2 = 10``5 * 3 = 15``5 * 4 = 20``5 * 5 = 25``5 * 6 = 30``5 * 7 = 35``5 * 8 = 40``5 * 9 = 45``5 * 10 = 50`

**条件**

**条件语句** 用于根据某种条件执行 **语句** 或一组 **语句** 。如果 **条件** 为真，则执行 **C#语句** ，否则执行下一条 **语句** 。

C++语言中不同类型的条件语句如下:

1.  如果语句
2.  If-Else 语句
3.  嵌套的 If-else 语句
4.  If-Else If 阶梯
5.  交换语句

**If 语句**

C#语言中的单个 **if** 语句用于在条件为真时执行代码。也称为单向选择语句。

**语法**

```
if (boolean-expression)
{
	// statements executed if boolean-expression is true
}

```

**流程图:**

![](img/6329e92a31c167d3e180daffaab0a81e.png)

**举例:**

```
using System;
namespace Conditional
{
    class IfStatement
    {
        public static void Main(string[] args)
        {
            int number = 2;
            if (number<5)
            {
                Console.WriteLine("{0} is less than 5", number);
            }
            Console.WriteLine("This statement is always executed.");
        }
    }
}

```

**//输出:**

`2 is less than 5`

**If-Else 语句**

C 语言中的  **if-else** 语句用于在条件为真或假时执行代码。也叫双向选择语句。

**语法**

```
if (boolean-expression)
{
	// statements executed if boolean-expression is true
}
else
{
	// statements executed if boolean-expression is false
}

```

**流程图:**

![](img/de2a4117b403659b6e2de63d30c87fdc.png)

**举例:**

```
using System;
namespace Conditional
{
    class IfElseStatement
    {
        public static void Main(string[] args)
        {
            int number = 12;
            if (number<5)
            {
                Console.WriteLine("{0} is less than 5", number);
            }
            else
            {
                Console.WriteLine("{0} is greater than or equal to 5", number);
            }
            Console.WriteLine("This statement is always executed.");
        }
    }
}

```

**//输出:**

`12 is greater than or equal to 5`

**嵌套的 If-else 语句**

当程序需要一个以上的测试表达式时，使用嵌套的 **if-else** 语句。它也被称为多路选择语句。当一个语句中涉及一系列决策时，我们使用嵌套形式的 **if-else** 语句。

**语法**

```
if (boolean-expression)
{
	if (nested-expression-1)
	{
		// code to be executed
	}
	else
	{
	// code to be executed
	}
}
else
{
	if (nested-expression-2)
	{
		// code to be executed
	}
	else
	{
		// code to be executed
	}
}

```

**流程图:**

![C#-Tutorial-nested-if-C-Edureka.jpg](img/c35aeb9f2c5863d282374aaebce66129.png)

**举例:**

```
using System;

namespace Conditional
{
      class Nested
      {
             public static void Main(string[] args)
             {
                   int first = 7, second = -23, third = 13;
                   if (first &gt; second)
                   {
                        if (first<third)
                        {
                              Console.WriteLine("{0} is the largest", first);
                        }
                        else
                        {
                               Console.WriteLine("{0} is the largest", third);
                        }
                   }
                   else
                   {
                        if (second<third)
                        {
                              Console.WriteLine("{0} is the largest", second);
                        }
                        else
                       {
                               Console.WriteLine("{0} is the largest", third);
                       }
                   }
             }
      }
}

```

**//输出:**

`13 is the largest`

**Else-if 阶梯**

**if-else-if**语句用于执行多个条件下的一个代码。它也被称为多路径决策语句。这是一连串的假设..else 语句，其中每个 if 语句都与 else if 语句相关联，最后一个是 else 语句。

**语法**

```
if(condition1)
{  
    // code to be executed if condition1 is true  
}
else if(condition2)
{  
    // code to be executed if condition2 is true  
}  
else if(condition3)
{  
    // code to be executed if condition3 is true  
}  
... 
else
{
    // code to be executed if all the conditions are false  
}

```

**流程图:**

**举例:**

![C++-Tutorial-else-if-ladder-C-Edureka.jpg](img/9ac474ebd84d369c09dc502cba669084.png)

```
using System;

class Edureka
{
     public static void Main(String[] args)
     {
          int i = 20;
          if (i == 10)
              Console.WriteLine("i is 10");
          else if (i == 15)
              Console.WriteLine("i is 15");
          else if (i == 20)
              Console.WriteLine("i is 20");
          else
              Console.WriteLine("i is not present");
     }
}

```

**//输出:**

`i is 20`

**开关语句**

**Switch** 语句作为一个长的 if-else-if 阶梯的替代，用于测试一系列案例。switch 语句包含一个或多个 case 标签，这些标签根据 switch 表达式进行测试。当表达式与一个事例匹配时，就会执行与该事例相关的语句。

**语法**

```
switch (variable/expression)
{
    case value1:
        // Statements executed if expression(or variable) = value1
        break;
    case value2:
        // Statements executed if expression(or variable) = value1
        break;
    ... ... ... 
    ... ... ... 
    default:
        // Statements executed if no case matches
}
```

**流程图:**

![C++-Tutorial-switch-Edureka](img/2e0b1fda3248c50fbea175f8895a6ec6.png)

**举例:**

```
using System;

namespace Conditional
{
     class SwitchCase
     {
          public static void Main(string[] args)
          {
               char ch;
               Console.WriteLine("Enter an alphabet");
               ch = Convert.ToChar(Console.ReadLine());
               switch (Char.ToLower(ch))
               {
                     case 'a':
                     Console.WriteLine("Vowel");
                     break;
                     case 'e':
                     Console.WriteLine("Vowel");
                     break;
                     case 'i':
                     Console.WriteLine("Vowel");
                     break;
                     case 'o':
                     Console.WriteLine("Vowel");
                     break;
                     case 'u':
                     Console.WriteLine("Vowel");
                     break;
                     default:
                     Console.WriteLine("Not a vowel");
                     break;
               }
          }
     }
}

```

**//输出:**

`Enter an alphabet``e`

**琴弦**

**字符串**数据类型是**系统的成员。字符串**类。它能够存储字符类型的数据。我们可以对字符串执行各种操作，比如连接、比较、获取子字符串、搜索、修剪、替换等等。

**弦与弦的类比**

在 C#中**字符串**和**字符串**是等价的。单词串是一个**关键字**，充当**系统。字符串**类。我们可以使用任何一个版本来声明字符串。

**语法:**

```
string s1 = "Edureka";//creating string using string keyword  
String s2 = "Happy Learning";//creating string using String class  

```

**举例:**

```
using System;
public class StringExample
{
    public static void Main(string[] args)
    {
        string s1 = "Edureka";
        char[] ch = { 'C', 's', 'h', 'a', 'r', 'p',' ','T','u','t','o','r','i','a','l' };
        string s2 = new string(ch);
        Console.WriteLine(s1);
        Console.WriteLine(s2);
    }
}

```

**//输出:**

`Edureka`

**c#中的字符串方法**

| **方法** | **描述** |
| **克隆()** | 用于返回对此字符串实例的引用。 |
| **比较(字符串，字符串)** | 用于比较两个指定的 String 对象。 |
| **Concat(String, String)** | 连接字符串的两个指定实例。 |
| **包含(字符串)** | 返回一个指示指定子字符串的值 |
| **复制(字符串)** | 用于创建具有相同值的字符串的新实例 |
| **CopyTo(Int，Char[]，Int，Int)** | 从指定位置复制字符 |
| **等于(字符串，字符串)** | 确定两个 String 对象具有相同的值。 |
| **格式(字符串，对象)** | 替换指定字符串中的一个或多个格式项 |
| **IndexOf(String)** | 报告第一个匹配项的从零开始的索引 |
| **插入(Int32，String)** | 返回一个新字符串，其中一个字符串被插入到索引处。 |
| **IsInterned(String)** | 指示此字符串采用 Unicode 范式 c。 |
| **IsNullOrEmpty(String)** | 指示指定的字符串为 null 或空字符串。 |
| **is nullorwhitespace(String)** | 用于指示指定的字符串是否为 null、空， |
| **Join(String，String[])** | 用于连接字符串数组的所有元素 |
| **LastIndexOf(Char)** | 报告最后一个字符的从零开始的索引位置 |
| **LastIndexOfAny(Char[])** | 报告最后一个字符的从零开始的索引位置 |
| **删除(Int32)** | 返回一个新字符串，其中所有字符 |
| **替换(字符串，字符串)** | 返回一个新字符串，其中所有出现的字符串 |
| **Split(Char[])** | 它用于将一个字符串拆分成子字符串 |
| **以(字符串)开头** | 它用于检查该字符串的开头是否 |
| **子串(Int32)** | 它用于从该实例中检索子字符串。 |
| **ToCharArray()** | 将此实例中的字符复制到 Unicode 数组中。 |
| **ToString()** | 它用于返回字符串的实例。 |
| **Trim()** | 修剪字符串 |

**阵列**

与其他编程语言类似，C#也有数组。数组是简单的数据结构，用于在连续的内存位置存储相同数据类型的元素。

C#支持以下数组类型。

*   一维数组
*   多维数组
*   锯齿状阵列

**一维数组**

一维数组以单行的形式存储元素。

**语法**

```
int[] arr = new int[5];//creating array  

```

**举例:**

```
using System;
public class ArrayExample
{
    public static void Main(string[] args)
    {
        int[] arr = new int[5];        arr[0] = 10;
        arr[1] = 20;
        arr[2] = 30;
        arr[3] = 40;
        arr[4] = 50;
        for (int i = 0; i < arr.Length; i++)
        {
            Console.WriteLine(arr[i]);
        }
    }
}

```

**//输出:**

`10``20``30``40`

![Data-Structures-in-C-One-Dimensional-Array-Edureka](img/3bcc5f22d1bc8097eab695643e154fea.png)

**多维数组**

多维数组以矩阵和立方体等多维形式存储元素。

**语法**

```
int val = a[2,3];

```

**举例:**

```
using System;

namespace ArrayApplication
{
     class MyArray
     {
           static void Main(string[] args)
           {
                  int[,] a = new int[5, 2] { { 0, 0 }, { 1, 2 }, { 2, 4 }, { 3, 6 }, { 4, 8 } };
                  int i, j;
                  for (i = 0; i < 5; i++)
                  {
                          for (j = 0; j < 2; j++)
                          {
                                 Console.WriteLine("a[{0},{1}] = {2}", i, j, a[i, j]);
                          }
                  }
                  Console.ReadKey();
           }
     }
}

```

**//输出:**

`a[0,0] = 0``a[0,1] = 0``a[1,0] = 1``a[1,1] = 2``a[2,0] = 2``a[2,1] = 4``a[3,0] = 3``a[3,1] = 6``a[4,0] = 4``a[4,1] = 8`

**![Data-Structures-in-C-Two-Dimensional-Array-Edureka](img/9fffd908780563a140643b1352835304.png)**

**交错排列**

交错数组就是数组的数组。

**举例:**

```
using System;

namespace ArrayApplication
{
     class MyArray
     {
           static void Main(string[] args)
           {
                  int[][] a = new int[][]{new int[]{0,0},new int[]{1,2},
                  new int[]{2,4},new int[]{ 3, 6 }, new int[]{ 4, 8 } };
                  int i, j;
                  for (i = 0; i < 5; i++)
                  {
                         for (j = 0; j < 2; j++)
                         {
                                Console.WriteLine("a[{0}][{1}] = {2}", i, j, a[i][j]);
                         }
                  }
                  Console.ReadKey();
           }
      }
}

```

**//输出:**

`a[0][0] = 0``a[0][1] = 0``a[1][0] = 1``a[1][1] = 2``a[2][0] = 2``a[2][1] = 4``a[3][0] = 3``a[3][1] = 6``a[4][0] = 4``a[4][1] = 8`

**收藏**

集合可以简单地认为是一组收集在一起的对象，以便对收集的数据应用一些功能。曾经可能在集合上执行的操作是，

*   存储对象
*   更新对象
*   删除对象
*   检索对象
*   搜索对象，以及
*   排序对象

**收藏类型**

使用集合有三种不同的可能性。下面提到了三个名称空间:

*   **系统。收藏.类属** 类
*   **系统。收藏** 类
*   **系统。集合.并发** 类

系统。泛型类有以下种类的类:

*   目录
*   堆
*   长队
*   链接列表
*   HashSet
*   黑色套装
*   词典
*   分类字典
*   排序列表

**系统。集合**类被认为是遗留类。它们包括以下类。

*   数组列表
*   堆
*   长队
*   散列表

**系统。collections . Concurrent**classes命名空间为线程安全操作提供类。现在，多线程将不会产生访问集合项的问题。这里可用的类别有，

*   阻塞收集
*   并发包
*   并发堆栈
*   并发队列
*   并发字典
*   瓜分者ˌ分割者
*   瓜分者ˌ分割者
*   可订购分区者

**列表**

**列表**被认为是**系统中可用的数据结构。Collection.Generics** 命名空间。它可以存储和获取元素。该列表能够存储重复的元素。

**举例:**

```
using System;
using System.Collections.Generic;

public class Edureka
{
      public static void Main(string[] args)
      {
           var names = new List<string>();
           names.Add("Sandhya");
           names.Add("Arun");
           names.Add("Prashanth");
           names.Add("Kiran");
           foreach (var name in names)
           {
                Console.WriteLine(name);
           }
      }
}

```

**//输出:**

`Sandhya` `Arun` `Prashanth`

**哈希集合**

C# HashSet 类往往是习惯了店，带走或读组件。它不存储重复的组件。如果已经让单独存储**有特色的** **组件** ，建议使用类别。 **是系统中发现的** 。集合。通用命名空间。

**举例:**

```
using System;
using System.Collections.Generic;

public class Edureka
{
     public static void Main(string[] args)
     {
          var names = new HashSet<string>();
          names.Add("Sunil");
          names.Add("Amar");
          names.Add("Pujari");
          names.Add("Imran");
          names.Add("karan");
          foreach (var name in names)
          {
              Console.WriteLine(name);
          }
     }
}

```

**//输出:**

`Sunil``Amar``Pujari``Imran`

**已排序集合**

C# SortedSet 类通常习惯于存储， **删除** 或 **元素读作****。它保持升序，并且不存储重复的元素。如果已经得到存储 **区别** **组件** 并保持升序，则提示使用已排序的集合类别。在系统中找到的是。集合。通用命名空间。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
     public static void Main(string[] args)
     {
          var names = new SortedSet<string>();
          names.Add("Sanjay");
          names.Add("Anuradha");
          names.Add("Praveen");
          names.Add("Ravi");
          names.Add("Kajol");
          foreach (var name in names)
          {
               Console.WriteLine(name);
          }
      }
} 
```

****//输出:****

**`Anuradha``Kajol``Praveen``Ravi`**

****堆栈****

****栈**是一个简单的集合，它遵循 **FILO** 或先进后出过程，同时处理存储在其中的元素。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
      public static void Main(string[] args)
      {
            Stack<string> names = new Stack<string>();
            names.Push("Chandan");
            names.Push("Pooja");
            names.Push("James");
            names.Push("Rajesh");
            names.Push("kumar");
            foreach (string name in names)
            {
                   Console.WriteLine(name);
            }
            Console.WriteLine("Peek element: " + names.Peek());
            Console.WriteLine("Pop: " + names.Pop());
            Console.WriteLine("After Pop, Peek element: " + names.Peek());
      }
} 
```

****//输出:****

**`kumar``Rajesh``James``Pooja``Chandan``Peek element: kumar``Pop: kumar``After Pop, Peek element: Rajesh`**

****队列****

**队列完全类似于堆栈，但唯一的区别是队列在处理存储在其中的元素时遵循 **FIFO** 或先进先出原则。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
      public static void Main(string[] args)
      {
            Queue<string> names = new Queue<string>();
            names.Enqueue("Srujan");
            names.Enqueue("Prajat");
            names.Enqueue("John");
            names.Enqueue("Raju");
            names.Enqueue("Hari");
            foreach (string name in names)
            {
                  Console.WriteLine(name);
            }
            Console.WriteLine("Peek element: " + names.Peek());
            Console.WriteLine("Dequeue: " + names.Dequeue());
            Console.WriteLine("After Dequeue, Peek element: " + names.Peek());
      }
} 
```

****//输出:****

**`Srujan``Prajat``John``Raju``Hari``Peek element: Srujan``Dequeue: Srujan``After Dequeue, Peek element: Prajat`**

****链表****

**链表是一个动态的内存集合。链表中的元素通过从堆中访问内存来存储，并通过链接它们的地址来以连续的顺序存储元素。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
      public static void Main(string[] args)
      {
            var names = new LinkedList<string>();
            names.AddLast("Rajat");
            names.AddLast("Arun");
            names.AddLast("Prakash");
            names.AddLast("jay");
            names.AddFirst("sai");
            foreach (var name in names)
            {
                   Console.WriteLine(name);
            }
      }
} 
```

****//输出:****

**`sai``Rajat``Arun``Prakash`**

****字典****

****字典** 类别采用散列表的创意。它在键的前提上存储值。它只包含独特的键和。通过键的辅助，我们将简单地搜索或取走元素。在系统中找到的是。集合。通用命名空间。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
      public static void Main(string[] args)
      {
            Dictionary<string, string> names = new Dictionary<string, string>();
            names.Add("1", "Shiva");
            names.Add("2", "Prasad");
            names.Add("3", "Preetam");
            names.Add("4", "Roy");
            names.Add("5", "Akash");
            foreach (KeyValuePair<string, string> kv in names)
            {
                  Console.WriteLine(kv.Key + " " + kv.Value);
             }
      }
} 
```

****//输出:****

**`1 Shiva``2 Prasad``3 Preetam``4 Roy``5 `**

****分类词典****

****sorted dictionary**category使用哈希表的概念。它将值存储在键的概念上。它包含独特的键，并在键的和上保持升序。通过键的辅助，我们将简单地搜索或取走元素。在系统中找到的是。集合。通用命名空间。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
     public static void Main(string[] args) 
     {
           SortedDictionary<string, string> names = new SortedDictionary<string, string>(); 
           names.Add("1", "Arun"); 
           names.Add("4", "Vishal");
           names.Add("5", "Ramesh");
           names.Add("3", "Vidya"); 
           names.Add("2", "Pallavi");
           foreach (KeyValuePair<string, string> kv in names)
           {
                 Console.WriteLine(kv.Key + " " + kv.Value);
           }
     }
} 
```

****//输出:****

**`1 Shiva``2 Prasad``3 Preetam``4 Roy`**

****排序列表****

****排序列表**是键/值对的数组。它在键的前提上存储值。排序列表类别包含区别性键，并在键的前提上保持升序。通过键的辅助，我们能够简单地搜索或移除元素。在**系统中找到的。Collections.Generic** 名称空间。**

****举例:****

```
using System;
using System.Collections.Generic;

public class Edureka
{
       public static void Main(string[] args)
       {
              SortedDictionary<string, string> names = new SortedDictionary<string, string>();
              names.Add("1", "Arun");
              names.Add("4", "Vishal");
              names.Add("5", "Ramesh");
              names.Add("3", "Vidya");
              names.Add("2", "Pallavi");
              foreach (KeyValuePair<string, string> kv in names)
              {
                    Console.WriteLine(kv.Key + " " + kv.Value);
              }
       }
} 
```

****//输出:****

**`1 Arun``2 Pallavi``3 Vidya``4 Vishal`**

****结构****

**该结构是用户定义的数据类型，用于存储不同数据类型的多个元素。使用关键字 **struct 声明该结构。****

****举例:****

```
using System;

struct Books
{
     public string title;
     public string author;
     public string subject;
     public int book_id;
};

public class Edureka
{
     public static void Main(string[] args)
     {
          Books Book1;
          Books Book2;
          Book1.title = "C# Programming";
          Book1.author = "Ramchandra Kumar";
          Book1.subject = "C++ Programming Tutorial";
          Book1.book_id = 95908978;
          Book2.title = "Telecom Billing";
          Book2.author = "Karan";
          Book2.subject = "Telecom Billing Tutorial";
          Book2.book_id = 18674900;
          Console.WriteLine("Book 1 title: {0}", Book1.title);
          Console.WriteLine("Book 1 Author: {0}", Book1.author);
          Console.WriteLine("Book 1 subject: {0}", Book1.subject);
          Console.WriteLine("Book 1 book_id:{0}", Book1.book_id);
          Console.WriteLine("Book 2 title: {0}", Book2.title);
          Console.WriteLine("Book 2 Author: {0}", Book2.author);
          Console.WriteLine("Book 2 subject: {0}", Book2.subject);
          Console.WriteLine("Book 2 book_id: {0}", Book2.book_id);
          Console.ReadKey();
     }
} 
```

****//输出:****

**`Book 1 title: C# Programming``Book 1 Author: Ramchandra Kumar``Book 1 subject: C++ Programming Tutorial``Book 1 book_id :95908978``Book 2 title: Telecom Billing``Book 2 Author: Karan``Book 2 subject: Telecom Billing Tutorial``Book 2 book_id: 18674900`**

****功能****

**该功能被定义为主代码的一个代码块。函数用于执行代码块中指定的语句。函数由以下组件组成。**

***   **函数名:** 这是一个与众不同的名字，用来进行函数调用。*   **返回值类型:** 指定函数返回值的数据类型。*   **正文:** 它包含可执行语句。*   **访问说明符:** 指定应用中的功能可访问性。*   **参数:** 它是我们在调用过程中可以传递给函数的参数列表。**

****语法****

```
<access-specifier><return-type>FunctionName(<parameters>)  
{  
// function body  
// return statement  
} 
```

****举例:****

```
using System;
namespace FunctionExample
{
    class Edureka
    {
        public string Show(string message)
        {
            Console.WriteLine("Inside Show Function");
            return message;
        }
        static void Main(string[] args)
        {
            Edureka program = new Edureka();
            string message = program.Show("To Edureka");
            Console.WriteLine("Welcome " + message);
        }
    }
} 
```

****//输出:****

**`Inside Show Function`**

**功能可以通过三种不同的方式执行:**

***   按值调用*   引用调用*   输出参数**

****按值调用****

**在 C#中**值****-类型**参数是，它将原始值的一个副本传递给函数而不是引用。它不修改第一个值。在已通过的值中创建的修正不会改变特定值。在下面的示例中，我们已经通过调用得到了传递值。**

****举例:****

```
using System;
namespace CallByValue
{
    class Edureka
    {
        public void Show(int val)
        {
            val *= val; 
            Console.WriteLine("The value inside the show function " + val);
        }
        static void Main(string[] args)
        {
            int val = 50;
            Edureka program = new Edureka(); 
            Console.WriteLine("Value before calling the function " + val);
            program.Show(val);        
            Console.WriteLine("Value after calling the function " + val);
        }
    }
} 
```

**//输出:**

**`Value before calling the function 50``The value inside the show function 2500`**

****引用调用****

**在通过引用方法调用时， a **ref** 关键字将参数作为引用类型进行传递。它将参数的引用传递给函数，而不是原始值的副本。传递值的变化是永久性的，而 **修改** 原始变量值。**

****举例:****

```
using System;
namespace CallByReference
{
    class Edureka
    {
        public void Show(ref int val)
        {
            val *= val; 
            Console.WriteLine("The value inside the show function " + val);
        }
        static void Main(string[] args)
        {
            int val = 50;
            Edureka program = new Edureka(); 
            Console.WriteLine("Value before calling the function " + val);
            program.Show(ref val);            
            Console.WriteLine("Value after calling the function " + val);
        }
    }
} 
```

**//输出:**

**`Value before calling the function 50``The value inside the show function 2500`**

****输出参数****

**out 参数提供了 **out** 关键字来传递 Out 类型的参数。它类似于引用类型，只是它不要求变量在传递前初始化。我们必须使用 **out** 关键字将参数作为 out-type 传递。当我们希望一个函数返回多个值时，这很有用。**

****举例:****

```
using System;
namespace OutParameter
{
    class Edureka
    {
        public void Show(out int val)
        {
            int square = 5;
            val = square;
            val *= val; 
        }
        static void Main(string[] args)
        {
            int val = 50;
            Edureka program = new Edureka(); 
            Console.WriteLine("Value before passing out variable " + val);
            program.Show(out val); 
            Console.WriteLine("Value after recieving the out variable " + val);
        }
    }
} 
```

**//输出:**

**`Value before passing out variable 50`**

**`Value` `after recieving the out variable 25`**

**现在让我们转向面向对象编程**

## ****面向对象编程****

****面向对象编程**系统 是一种基于**对象**概念的编程范例，这些对象包含**数据成员**和与之相关的**方法**。面向对象编程的主要目的是增加程序的灵活性和可维护性**

## ****面向对象编程的特点:****

***   它更强调数据而不是过程。*   这些程序被分成对象，因此很容易操作。*   数据结构是以这样一种方式设计的，即它们表征对象。*   对一个对象的数据进行  操作的函数一起放在数据结构中。*   数据是隐藏的，未经允许不能被外部函数访问。*   借助于函数，可以进行对象之间的通信。*   添加新的数据和函数变得很容易。*   在程序设计中遵循自下而上的方法。**

**C#中面向对象的范例如下**

***   [c#中的枚举](#enum)*   [面向对象的编程方法](#oopa)
    *   [封装](#enc)
    *   [抽象](#abs)
    *   [界面](#inter)
    *   [多态性](#poly)
    *   [继承](#inh)*   [超载和超越](#over)*   [命名空间](#name)*   [文件操作](#file)*   [事件](#event)*   [仿制药](#gene)*   [代表们](#del)*   [反思](#ref)**

****c#中的枚举****

**C#中的**枚举**或也被称为**枚举**用于存储常量值，而无需在整个 C#程序执行过程中更改它们。它用于存储一组命名的常量，如季节、日期、月份、大小等**

****举例:****

```
using System;
public class EnumExample
{
      public enum week { Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday }
      public static void Main()
      {
           int x = (int)week.Monday;
           int y = (int)week.Friday;
           Console.WriteLine("Monday = {0}", x);
           Console.WriteLine("Friday = {0}", y);
     }
} 
```

****//输出:****

**`Monday = 0`**

****面向对象的编程方法****

**遵循下面规定的方法可以实现面向对象风格的编程。**

****封装****

****![Encapsulation - Object Oriented Programming in Cpp - Edureka](img/c2f0960ca6de2625639980840e0bdbf0.png)****

****封装**是一种将**方法**和它们的**数据成员结合起来的方法。****

****举例:****

```
using System;

namespace Edureka
{
     class Rectangle
     {
            public double length;
            public double width;   
            public double GetArea()
            {
                  return length * width;
            }
            public void Display()
            {
                  Console.WriteLine("Length: {0}", length);
                  Console.WriteLine("Width: {0}", width);
                  Console.WriteLine("Area: {0}", GetArea());
            }
     }
     class ExecuteRectangle
     {
             static void Main(string[] args)
             {
                  Rectangle r = new Rectangle();
                  r.length = 50;
                  r.width = 35;
                  r.Display();
                  Console.ReadLine();
             }
     }
} 
```

****//输出:****

**`Length: 50``Width: 35`**

****抽象****

**![](img/3f50810aac157b10207d267457365535.png)**

****抽象**是一种向用户隐藏复杂编码部分的方法，只向用户提供他需要的信息。**

****举例:****

```
using System;
public abstract class Shape
{
    public abstract void draw();
}
public class Rectangle : Shape
{
    public override void draw()
    {
        Console.WriteLine("drawing rectangle...");
    }
}
public class Circle : Shape
{
    public override void draw()
    {
        Console.WriteLine("drawing circle...");
    }
}
public class TestAbstract
{
    public static void Main()
    {
        Shape s;
        s = new Rectangle();
        s.draw();
        s = new Circle();
        s.draw();
    }
} 
```

****//输出:****

**`drawing rectangle...`**

****界面****

****![java-interface](img/1263d22170a197aefb0640150f37da68.png)****

****接口**完全类似于抽象。界面的功能是向用户隐藏不重要的数据，只向他提供他需要的重要数据。**

****举例:****

```
using System;
public interface Drawable
{
    void draw();
}
public class Rectangle : Drawable
{
    public void draw()
    {
        Console.WriteLine("drawing rectangle...");
    }
}
public class Circle : Drawable
{
    public void draw()
    {
        Console.WriteLine("drawing circle...");
    }
}
public class TestInterface
{
    public static void Main()
    {
        Drawable d;
        d = new Rectangle();
        d.draw();
        d = new Circle();
        d.draw();
    }
} 
```

****//输出:****

**`drawing rectangle...`**

****多态性****

**![polymorphism-in-c++-real-life](img/e2d2b15fbbabf79811af12675805016b.png)**

**多态是**【多】** + **【变体】**的组合，意为多种形式。这是一个希腊词。这意味着代码段可以采用多种形式。我们有两种类型的多态性。**

***   编译时间多态性*   运行时间多态性**

****举例:****

```
using System;
public class Animal
{
      public string color = "white";
}
public class Dog : Animal
{
      public string color = "black";
}
public class TestSealed
{
      public static void Main()
      { 
            Animal d = new Dog();
            Console.WriteLine(d.color);
      }
} 
```

****//输出:****

**`white`**

****继承****

**![Inheritance-Inheritance in Java-Edureka](img/666ad255a8f36039637b6aa968918305.png)**

****继承**是一个对象自动获得其父对象所有属性和行为的过程。您可以重用、扩展或修改在其他类中定义的属性和行为。继承另一个类的成员的类被称为**派生类**，其成员被继承的类被称为**基类**。派生类是基类的专用类。**

****单级继承的例子****

```
using System;
namespace RectangleApplication
{
     class Rectangle
     {
          protected double length;
          protected double width;
          public Rectangle(double l, double w)
          {
               length = l;
               width = w;
          }
          public double GetArea()
          {
               return length * width;
          }
          public void Display()
          {
               Console.WriteLine("Length: {0}", length);
               Console.WriteLine("Width: {0}", width);
               Console.WriteLine("Area: {0}", GetArea());
          }
     }
     class Tabletop : Rectangle
     {
          private double cost;
          public Tabletop(double l, double w) : base(l, w) { }
          public double GetCost()
          {
                double cost;
                cost = GetArea() * 70;
                return cost;
          }
          public void Display()
          {
                base.Display();
                Console.WriteLine("Cost: {0}", GetCost());
          }
     }
     class ExecuteRectangle
     {
           static void Main(string[] args)
           {
                 Tabletop t = new Tabletop(4.5, 7.5);
                 t.Display();
                 Console.ReadLine();
           }
     }
} 
```

****//输出:****

**`Length: 4.5` `Width: 7.5` `Area: 33.75`**

****多级继承的例子****

```
using System;

namespace InheritanceApplication
{
      class Shape
      {
           public void setWidth(int w)
           {
                width = w;
           }
           public void setHeight(int h)
           {
                 height = h;
           }
           protected int width;
           protected int height;
      }
      public interface PaintCost
      {
           int getCost(int area);
      }
      class Rectangle : Shape, PaintCost
      {
           public int getArea()
           {
                 return (width * height);
           }
           public int getCost(int area)
           {
                 return area * 70;
           }
      }
      class RectangleTester
      {
            static void Main(string[] args)
            {
                 Rectangle Rect = new Rectangle();
                 int area;
                 Rect.setWidth(5);
                 Rect.setHeight(7);
                 area = Rect.getArea();
                 Console.WriteLine("Total area: {0}", Rect.getArea());
                 Console.WriteLine("Total paint cost: ${0}", Rect.getCost(area));
                 Console.ReadKey();
            }
      }
} 
```

****//输出:****

**`Total area: 35`**

****过载****

**重载是指我们使用相同的名称声明了两个或多个成员。当我们用相同的名字声明两个或更多的方法时，重载也是可能的。让我们来看看两者的例子。**

****成员重载****

****举例:****

```
using System;
public class Edureka
{
    public static int add(int a, int b)
    {
        return a + b;
    }
    public static int add(int a, int b, int c)
    {
        return a + b + c;
    }
}
public class TestMemberOverloading
{
    public static void Main()
    {
        Console.WriteLine(Edureka.add(12, 23));
        Console.WriteLine(Edureka.add(12, 23, 25));
    }
} 
```

****//输出:****

**`35`**

****方法重载****

****举例:****

```
using System;
public class Edureka
{
    public static int add(int a, int b)
    {
        return a + b;
    }
    public static float add(float a, float b)
    {
        return a + b;
    }
}
public class TestMemberOverloading
{
    public static void Main()
    {
        Console.WriteLine(Edureka.add(12, 23));
        Console.WriteLine(Edureka.add(12.4f, 21.3f));
    }
} 
```

****//输出:****

**`35`**

****超驰****

**覆盖是指子类定义了父类也在定义的相同方法的情况。让我们通过一个小例子来理解这一点。**

****举例:****

```
using System;
public class Edureka
{
    public virtual void eat()
    {
        Console.WriteLine("Eating ");
    }
}
public class Dog : Edureka
{
    public override void eat()
    {
        Console.WriteLine("Eating food");
    }
}
public class Overriding
{
    public static void Main()
    {
        Dog d = new Dog();
        d.eat();
    }
} 
```

****//输出:****

**`Eating food`**

****命名空间****

**名称空间主要用于处理程序中的多个类。命名空间有不同的使用方式。**

***   **系统。控制台:**在这里，**系统**成为名称空间*   要访问一个命名空间的类，我们需要使用**namespace name . class name .***   我们可以使用 **也可以使用** 关键字。**

****举例:****

```
using System;
using First;
using Second;
namespace First
{
    public class Edureka
    {
        public void sayWelcome() { Console.WriteLine("Welcome To Edureka"); }
    }
}
namespace Second
{
    public class Happy_Learning
    {
        public void sayWishes() { Console.WriteLine("Happy Learning"); }
    }
}
public class Namespace
{
    public static void Main()
    {
        Edureka h1 = new Edureka();
        Happy_Learning w1 = new Happy_Learning();
        h1.sayWelcome();
        w1.sayWishes();
    }
} 
```

****//输出:****

**`Welcome To Edureka`**

****文件操作****

**C#中可用的**文件操作**如下:**

| **操作** | **描述** |
| **二进制阅读器** | 从二进制流中读取原始数据。 |
| **BinaryWriter** | 以二进制格式写入原始数据。 |
| **BufferedStream** | 字节流的临时存储。 |
| **目录** | 帮助操作目录结构。 |
| **目录信息** | 用于对目录执行操作。 |
| **驾驶信息** | 提供驱动器的信息。 |
| **文件** | 帮助操作文件。 |
| **FileInfo** | 用于对文件执行操作。 |
| **文件流** | 用于读取和写入文件中的任何位置。 |
| **内存流** | 用于随机访问存储在内存中的流数据。 |
| **路径** | 对路径信息执行操作。 |
| **流媒体阅读器** | 用于从字节流中读取字符。 |
| **流式书写器** | 用于将字符写入流。 |
| **StringReader** | 用于从字符串缓冲区读取。 |
| **StringWriter** | 用于写入字符串缓冲区。 |

****文件模式****

****FileMode** 是定义多种文件打开方法的枚举器。FileMode 枚举器的成员描述如下:**

***   **Append:** 打开一个已有的文件，将光标放在文件的末尾，如果文件不存在，则创建该文件。*   **创建:**创建一个新文件。*   **CreateNew:** 它的设计目的是向操作系统指定，它应该创建一个新文件。*   **打开:**用于打开一个已有的文件。*   **OpenOrCreate:** 用于指定操作系统，如果文件存在就打开，否则创建一个新文件。*   **Truncate:** Truncate 打开一个现有文件，将其大小截断为零字节。**

****FileAccess****

****FileAccess** 枚举器用于获取对特定文件的访问权限。它有以下成员。**

***   **改为***   **写***   **读写****

****文件共享****

****文件共享**枚举器用于共享特定的文件。它有以下成员。**

***   **Inheritable:** Inheritable 允许文件句柄将继承传递给子进程。*   **无:**无拒绝共享当前文件*   **Read:** Read 允许打开文件进行读取。*   **读写:**读写允许打开文件进行读写。*   **Write:** Write 允许打开文件进行写入。**

****事件****

**事件通常被认为是由用户产生的动作。它可能是鼠标的一次点击，甚至是键盘上的一次击键。同样，C#程序也有事件。事件的发生者称为**发布者**，事件的接收者称为**订阅者。****

****发布者****

****发布者** 包含事件的定义和委托。在这个对象中定义了**事件委托**关联。一个**发布者**类对象调用该事件，并且它被通知给其他对象。**

****订户****

**一个 **订户** 接受事件并提供一个**事件处理程序。发布者类中的**委托**调用订阅者类的方法/事件**处理程序**。****

****举例:****

```
using System;

namespace Edureka
{
       public delegate string Del(string str);
       class EventBlock
       {
              event Del NewEvent;
              public EventBlock()
              {
                    this.NewEvent += new Del(this.WelcomeUser);
              }
              public string WelcomeUser(string username)
              {
                    return "Welcome To Edureka. " + username;
              }
              static void Main(string[] args)
              {
                    EventBlock obj1 = new EventBlock();
                    string result = obj1.NewEvent("Happy Learning");
                    Console.WriteLine(result);
              }
        }
} 
```

****//输出:****

**`Welcome To Edureka. Happy Learning`**

****仿制药****

****泛型**是一个在**运行时为类的成员和方法提供占位符的概念。**我们可以用< > **括号来定义泛型。让我们来看看下面的例子。****

****类中的泛型****

```
using System;
namespace Edureka
{
    class GenericClass<T>
    {
        public GenericClass(T msg)
        {
            Console.WriteLine(msg);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            GenericClass<string> gen = new GenericClass<string>("This message is from generic class");
            GenericClass<int> genI = new GenericClass<int>(123);
            GenericClass<char> getCh = new GenericClass<char>('E');
        }
    }
} 
```

****//输出:****

**`This message is from generic class``123`**

****方法中的泛型****

```
using System;
namespace Edureka
{
    class GenericClass
    {
        public void Show<T>(T msg)
        {
            Console.WriteLine(msg);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            GenericClass genC = new GenericClass();
            genC.Show("This message is from the generic method");
            genC.Show(321);
            genC.Show('H');
        }
    }
} 
```

****//输出:****

**`This message is from the generic method``321`**

****代表们****

****委托**充当对该方法的引用。基本上，它与 C 和 C++中的**函数指针**相同，但要好得多，而且是类型安全的。**静态方法**中的委托只封装方法。而**实例**方法中的委托封装了方法和实例。委托的最佳用途是用作**事件。****

****举例:****

```
using System;
delegate int Calculator(int n);
public class Edureka
{
      static int number = 25;
      public static int add(int n)
      {
            number = number + n;
            return number;
      }
      public static int mul(int n)
      {
           number = number * n;
           return number;
      }
      public static int getNumber()
      {
           return number;
      }
      public static void Main(string[] args)
      {
           Calculator c1 = new Calculator(add);
           Calculator c2 = new Calculator(mul);
           c1(20);
           Console.WriteLine("After calculator one delegate, the new Number is: " + getNumber());
           c2(3);
           Console.WriteLine("After calculator two delegate, the new Number is: " + getNumber());
      }
} 
```

****//输出:****

**`After calculator one delegate, the new Number is: 45`**

****倒影****

**反射是在运行时获取元数据所必需的。参考可在**系统中获得。反射**名称空间。它需要执行以下类。**

***   类型*   MemberInfo*   建筑信息*   MethodInfo*   FieldInfo*   财产信息*   TypeInfo*   事件信息*   组件*   装配*   程序集名称*   指针**

****类型类****

**C# Type class 表示类类型、接口类型、枚举类型、数组类型、值类型的类型声明**

## **类型属性**

**下面列出了类型类的重要属性。**

| **属性** | **描述** |
| **组装** | 获取此类型的程序集。 |
| **AssemblyQualifiedName** | 获取此类型的程序集限定名。 |
| **属性** | 获取与该类型关联的属性。 |
| **基本类型** | 获取基类型或父类型。 |
| **FullName** | 获取该类型的完全限定名。 |
| **IsAbstract** | 用于检查该类型是否是抽象的。 |
| **IsArray** | 用于检查类型是否为数组。 |
| 【T0 类】T1 类 | 用于检查类型是否为类。 |
| **我的心** | 用于检查类型是否为枚举。 |
| **是接口** | 用于检查类型是否为接口。 |
| **是指** | 用于检查该类型是否嵌套。 |
| ** IsPrimitive** | 用于检查该类型是否为基元类型。 |
| ** IsPointer** | 用于检查类型是否为指针。 |
| **不是公共的** | 用于检查该类型是否不是公共的。 |
| **是公共的** | 用于检查该类型是否是公共的。 |
| **已密封** | 用于检查该类型是否是密封的。 |
| **可串行化** | 用于检查该类型是否可序列化。 |
| **成员类型** | 用于检查该类型是否是嵌套类型的成员类型。 |
| **模块** | 获取该类型的模块。 |
| **名称** | 获取该类型的名称。 |
| **命名空间** | 获取该类型的命名空间。 |

| **属性** | **描述** |
| **GetConstructors()** | 返回该类型的所有公共构造函数。 |
| **get constructors(binding flags)** | 返回具有指定 BindingFlags 的类型的所有构造函数。 |
| **GetFields()** | 返回该类型的所有公共字段。 |
| **获取字段(BindingFlags)** | 返回具有指定 BindingFlags 的类型的所有公共构造函数。 |
| **GetMembers()** | 返回该类型的所有公共成员。 |
| **获取成员(BindingFlags)** | 返回具有指定 BindingFlags 的类型的所有成员。 |
| **GetMethods()** | 返回该类型的所有公共方法。 |
| **GetMethods(BindingFlags)** | 返回具有指定 BindingFlags 的类型的所有方法。 |
| **GetProperties()** | 返回该类型的所有公共属性。 |
| **get properties(binding flags)** | 返回具有指定 BindingFlags 的类型的所有属性。 |
| **GetType()** | 获取当前类型。 |
| **GetType(String)** | 获取给定名称的类型。 |

****反射示例:****

****获取类型****

****举例:****

```
using System;
public class GetType
{
    public static void Main()
    {
        int a = 10;
        Type type = a.GetType();
        Console.WriteLine(type);
    }
} 
```

****//输出:****

**`System.Int32`**

****获取装配****

****举例:****

```
using System;
using System.Reflection;
public class GetAssembly
{
    public static void Main()
    {
        Type t = typeof(System.String);
        Console.WriteLine(t.Assembly);
    }
} 
```

****//输出:****

**`System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e`**

****打印类型信息****

****举例:****

```
using System;
using System.Reflection;
public class PrintType
{
    public static void Main()
    {
        Type t = typeof(System.String);
        Console.WriteLine(t.FullName);
        Console.WriteLine(t.BaseType);
        Console.WriteLine(t.IsClass);
        Console.WriteLine(t.IsEnum);
        Console.WriteLine(t.IsInterface);
    }
} 
```

****//输出:****

**`True``False`**

****打印构造函数****

****举例:****

```
using System;
using System.Reflection;
public class PrintConstructors
{
    public static void Main()
   {
       Type t = typeof(System.String);
       Console.WriteLine("Constructors of {0} type...", t);
       ConstructorInfo[] ci = t.GetConstructors(BindingFlags.Public | BindingFlags.Instance);
       foreach (ConstructorInfo c in ci)
       {
              Console.WriteLine(c);
       }
   }
} 
```

****//输出:****

**`Constructors of System.String type...``Void .ctor(Char[])``Void .ctor(Char[], Int32, Int32)``Void .ctor(Char*)``Void .ctor(Char*, Int32, Int32)``Void .ctor(SByte*)``Void .ctor(SByte*, Int32, Int32)``Void .ctor(SByte*, Int32, Int32, System.Text.Encoding)``Void .ctor(Char, Int32)``Void .ctor(System.ReadOnlySpan`1[System.Char])`**

****打印方式****

****举例:****

```
using System;
using System.Reflection;
public class PrintMethods
{
      public static void Main()
     {
         Type t = typeof(System.String);
         Console.WriteLine("Methods of {0} type...", t);
         MethodInfo[] ci = t.GetMethods(BindingFlags.Public | BindingFlags.Instance);
         foreach (MethodInfo m in ci)
         {
              Console.WriteLine(m);
         }
     }
} 
```

****//输出:****

**`Methods of System.String type...``System.String Replace(System.String, System.String)``System.String[] Split(Char, System.StringSplitOptions)``System.String[] Split(Char, Int32, System.StringSplitOptions)``System.String[] Split(Char[])``System.String[] Split(Char[], Int32)``System.String[] Split(Char[], System.StringSplitOptions)``System.String[] Split(Char[], Int32, System.StringSplitOptions)``System.String[] Split(System.String, System.StringSplitOptions)``System.String[] Split(System.String, Int32, System.StringSplitOptions)``System.String[] Split(System.String[], System.StringSplitOptions)`**

****打印字段****

****举例:****

```
using System;
using System.Reflection;
public class PrintFields
{
     public static void Main()
     {
          Type t = typeof(System.String);
          Console.WriteLine("Fields of {0} type...", t);
          FieldInfo[] ci = t.GetFields(BindingFlags.Public | BindingFlags.Static | BindingFlags.NonPublic);
          foreach (FieldInfo f in ci)
          {
                 Console.WriteLine(f);
          }
     }
} 
```

****//输出:****

**`Fields of System.String type...`**

**现在，让我们继续学习一些高级的 C#编程概念**

## ****高级 C#概念****

***   [匿名功能](#anon)*   [多线程](#mul)*   [异常处理](#exec)*   [同步](#sync)*   [新功能](#new)**

****匿名功能****

**缺少特定名称的函数称为**匿名**函数。C#中有两种类型的匿名函数**

***   λ表达式*   匿名方法**

****举例:****

```
using System;
namespace LambdaExpressions
{
    class Edureka
    {
        delegate int Square(int num);
        static void Main(string[] args)
        {
            Square GetSquare = x => x * x;
            int j = GetSquare(25);
            Console.WriteLine("Square: " + j);
        }
    }
} 
```

****//输出:****

**`Square: 625`**

****匿名方法****

****匿名方法**提供了与 **lambda 表达式**相同的功能，除了它允许我们忽略参数列表。**

****举例:****

```
using System;
namespace AnonymousMethods
{
    class Program
    {
        public delegate void AnonymousFun();
        static void Main(string[] args)
        {
            AnonymousFun fun = delegate () {
                Console.WriteLine("This is anonymous function");
            };
            fun();
        }
    }
} 
```

****//输出:****

**`This is anonymous function`**

****多线程****

**多线程是一个创建多个线程并分配给不同任务的过程。这通过一次执行多个作业来节省时间。多线程类在**系统中可用。线程化**名称空间。**

****系统。线程命名空间****

****系统。Threading** 名称空间包含类和接口，以方便多线程处理。它提供了同步线程资源的类。下面列出了常用的类别:**

***   线*   互斥（体）…*   计时器*   班长*   旗语*   线程本地*   线程池*   不稳定的**

****进程和线程****

**该进程实际上是和**应用**并被认为是一个**重量级**组件。另一方面，线程是整个应用程序的一个单独的**模块**。与流程相比，它是轻量级的**

****线程的生命周期****

**每个线程都有一个生命周期。线程的生命周期在系统中定义。线程。线程类。以下是任何线程生命周期中的各个阶段。**

***   未启动*   可运行(准备运行)*   运转*   不可运行*   死亡的**

**Thread 类提供如下属性和方法。**

****线程属性****

| **属性** | **描述** |
| **当前线程** | 返回当前运行线程的实例。 |
| isalive | 检查当前线程是否处于活动状态。 |
| **是背景** | 获取/设置当前线程的值是否在后台。 |
| **ManagedThreadId** | 用于获取当前托管线程的唯一 id。 |
| **名称** | 用于获取或设置当前线程的名称。 |
| **优先级** | 用于获取或设置当前线程的优先级。 |
| **线程状态** | 用于返回表示线程状态的值。 |

****线程方法****

| **方法** | **描述** |
| **中止()** | 用于终止线程。它会引发 ThreadAbortException。 |
| **中断()** | 用于中断处于 WaitSleepJoin 状态的线程。 |
| **Join()** | 用于阻塞所有调用线程，直到该线程终止。 |
| **ResetAbort()** | 用于取消当前线程的中止请求。 |
| **简历()** | 用于恢复挂起的线程。它已经过时了。 |
| **睡眠(Int32)** | 用于将当前线程挂起指定的毫秒数。 |
| **开始()** | 将线程的当前状态更改为可运行。 |
| **暂停()** | 如果当前线程没有被挂起，则挂起它。它已经过时了。 |
| **收益率()** | 用于将当前线程的执行让给另一个线程。 |

****主线程示例****

```
using System;
using System.Threading;
public class Edureka
{
    public static void Main(string[] args)
    {
        Thread t = Thread.CurrentThread;
        t.Name = "MainThread";
        Console.WriteLine(t.Name);
    }
} 
```

****//输出:****

**`MainThread`**

****异常处理****

**异常是程序在运行时抛出的一个错误。我们执行异常处理是为了让我们的程序没有异常。**

| **异常** | **描述** |
| **系统。DivideByZeroException** | 用零除一个数产生的误差。**** |
| **系统。NullReferenceException** | 处理通过引用 null 对象生成的错误。**** |
| **系统。InvalidCastException** | 处理由无效类型转换生成的错误。**** |
| **系统。IO.IOException** | 处理输入/输出错误。 |
| **系统。FieldAccessException** | 无效的私有/受保护访问产生错误。 |

**在 C#中，我们使用 4 个关键字来执行**异常处理:****

***   尝试*   捕捉*   最后，还有*   扔**

****Example:****

```
using System;
public class EdurekExample
{
     public static void Main(string[] args)
     {
           try
           {
                 int a = 10;
                 int b = 0;
                 int x = a / b;
            }
            catch (Exception e) 
            { 
                 Console.WriteLine(e); 
             }
             Console.WriteLine("This message is from catch block");
       }
} 
```

****//输出:****

**`System.DivideByZeroException: Attempted to divide by zero.``at ExExaEdurekample.Main(String[] args) in F:C# TutorialC# ProgramsConsoleApp1ConsoleApp1Program.cs:line 10`**

****定制例外示例****

```
using System;
public class InvalidAgeException : Exception
{
       public InvalidAgeException(String message): base(message)
       {
       }
}
public class Customized
{
      static void validate(int age)
      {
           if (age < 18)
           {
                  throw new InvalidAgeException("Sorry, Age is expected to be greater than 18");
           }
      }
      public static void Main(string[] args)
      {
            try
            {
                  validate(12);
            }
            catch (InvalidAgeException e) 
           { 
                  Console.WriteLine(e); 
           }
           Console.WriteLine("Catch block is being executed now.");
      }
} 
```

****//输出:****

**`InvalidAgeException: Sorry, Age is expected to be greater than 18` `at Customized.validate(Int32 age) in F:C# TutorialC# ProgramsConsoleApp1ConsoleApp1Program.cs:line 18` `at Customized.Main(String[] args) in F:C# TutorialC# ProgramsConsoleApp1ConsoleApp1Program.cs:line 23`**

****最终阻止示例****

```
using System;
public class FinalExecption
{
    public static void Main(string[] args)
    {
        try
        {
            int a = 10;
            int b = 0;
            int x = a / b;
        }
        catch (Exception e) { Console.WriteLine(e); }
        finally { Console.WriteLine("Finally block is executed"); }
        Console.WriteLine("Catch block is executed");
    }
} 
```

****//输出:****

**`System.DivideByZeroException: Attempted to divide by zero.` `at FinalExecption.Main(String[] args) in F:C# TutorialC# ProgramsConsoleApp1ConsoleApp1Program.cs:line 10` `Finally block is executed`**

****系统异常签名****

```
[SerializableAttribute]  
[ComVisibleAttribute(true)]  
public class SystemException : Exception 
```

****系统异常构造函数****

| **构造器** | **描述** |
| **系统异常()** | 它用于初始化 SystemException 类的新实例。 |
| **SystemException****(序列化信息，流上下文)** | 它用于用序列化数据初始化 SystemException 类的新实例。 |
| **系统异常(字符串)** | 它用于用指定的错误信息初始化 SystemException 类的新实例。 |
| **系统异常(字符串，异常)** | 它用于使用指定的错误信息和对导致此异常的内部异常的引用来初始化 SystemException 类的新实例。 |

****系统异常属性****

| **属性** | **描述** |
| **数据** | 它用于获取键/值对的集合，这些键/值对提供关于异常的用户定义的附加信息。 |
| **帮助链接** | 它用于获取或设置与此异常相关的帮助文件的链接。 |
| **HResult** | 它用于获取或设置 HRESULT，即分配给特定异常的编码数值。 |
| **内部异常** | 它用于获取导致当前异常的异常实例。 |
| **消息** | 它用于获取描述当前异常的消息。 |
| **来源** | 它用于获取或设置导致错误的应用程序的名称。 |
| **堆栈跟踪** | 它用于获取调用堆栈上直接帧的字符串表示形式。 |
| **目标地点** | 它用于获取引发当前异常的方法。 |

****系统异常方法****

| **方法** | **描述** |
| **等于(对象)** | 它用于检查指定的对象是否等于当前对象。 |
| **Finalize()** | 它用于释放资源和执行清理操作。 |
| **GetBaseException()** | 它用于获取根异常。 |
| **GetHashCode()** | 它用于获取哈希代码。 |
| **GetObjectData****(序列化信息，流上下文)** | 它用于获取对象数据。 |
| **GetType()** | 它用于获取当前实例的运行时类型。 |
| **memberwisecolone()** | 它用于创建当前对象的浅表副本。 |
| **ToString()** | 它用于创建和返回当前异常的字符串表示形式。 |

****系统异常示例****

```
using System;
namespace CSharpProgram
{
    class SystemExceptionExample
    {
        static void Main(string[] args)
        {
            try
            {
                int[] arr = new int[5];
                arr[10] = 25;
            }
            catch (SystemException e)
            {
                Console.WriteLine(e);
            }
        }
    }
} 
```

****//输出:****

**`System.IndexOutOfRangeException: Index was outside the bounds of the array.`**

****同步****

**同步可以是一种仅允许一个线程在特定时间访问资源的技术。在指定线程完成其任务之前，没有替代线程会中断。**

**在多线程程序中，线程被允许 在指定的执行时间内访问任何资源。线程共享资源并异步执行。访问共享资源(数据)可能是一个重要的任务，通常会暂停系统。我们倾向于通过以同步方式 创建线程来影响它。**

****无同步的示例****

```
using System;
using System.Threading;
class Edureka
{
    public void PrintTable()
    {
        for (int i = 1; i <= 10; i++)
        {
            Thread.Sleep(100);
            Console.WriteLine(i);
        }
    }
}
class Program
{
    public static void Main(string[] args)
    {
        Edureka p = new Edureka();
        Thread t1 = new Thread(new ThreadStart(p.PrintTable));
        Thread t2 = new Thread(new ThreadStart(p.PrintTable));
        t1.Start();
        t2.Start();
    }
} 
```

****//输出:****

**`1``1``2``2``3``3``4``4``5``5``6``7``8``9``9``10``10`**

****同步示例****

```
using System;
using System.Threading;
class Edureka
{
    public void PrintTable()
    {
        lock (this)
        {
            for (int i = 1; i <= 10; i++)
            {
                Thread.Sleep(100);
                Console.WriteLine(i);
            }
        }
    }
}
class Program
{
    public static void Main(string[] args)
    {
        Edureka p = new Edureka();
        Thread t1 = new Thread(new ThreadStart(p.PrintTable));
        Thread t2 = new Thread(new ThreadStart(p.PrintTable));
        t1.Start();
        t2.Start();
    }
} 
```

****//输出:****

**`1``2``3``4``5``6``7``8``9``10``1``3``5``7``8``9``10`**

****新功能****

**微软给 C#语言增加了许多最新的特性，下面将提到其中的一些。**

## **C# 6.0**

***   使用静态指令*   异常过滤器*   在 catch/finally 块中等待*   自动属性初始值设定项*   仅 getter 属性的默认值*   表情丰富的成员*   零传播子*   字符串插值*   操作员姓名*   字典初始值设定项*   编译器即服务(罗斯林)**

## **C# 7.0**

***   模式匹配*   元组*   解构*   本地功能*   数字分隔符*   二进制文字*   引用返回和本地*   表达式体构造函数和终结器*   表达体吸气剂和设置剂*   输出变量*   通用异步返回类型**

## **C# 7.1**

***   异步干线*   默认表达式**

## ****基于 C#的面试问题****

**基于 C#编程语言的重要面试问题可以在本次更新的 [**篇**](https://www.edureka.co/blog/interview-questions/c-sharp-interview-questions/) 中找到。**

**到此，我们结束这篇“C#教程”文章。我希望您已经理解了数据结构、语法、功能和使用它们执行的操作的重要性。 *现在，您已经通过本 C#教程了解了 C#编程的基础知识，请查看 Edureka 提供的 [**java**](https://www.edureka.co/java-j2ee-training-course) 培训* *关于许多技术，如 java、 [Spring](https://spring.io/) 和更多技术，一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者，有一个* *问题要问我们吗？在这个“C#教程”博客的评论部分提到它，我们会尽快回复你。***