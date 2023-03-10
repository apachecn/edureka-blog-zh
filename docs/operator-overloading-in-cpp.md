# 如何在 c++中实现运算符重载？

> 原文：<https://www.edureka.co/blog/operator-overloading-in-cpp/>

在本文中，我们将探索另一个面向对象的概念，它使操作者的操作变得容易。也就是说，我们将进入 C++ 中操作符[重载的细节。本文将涉及以下几点:](https://www.edureka.co/blog/function-overloading-and-overriding-in-cpp/)

*   [c++中的重载](#OverloadinginC++)
*   [c++中重载的类型](#TypesofoverloadinginC++)
*   [为什么使用运算符重载？](#Whyisoperatoroverloadingused?)
*   [在 C++中实现运算符重载](#ImplementingOperatorOverloadinginC++)
*   [超载方法的类型](#Typesofoverloadingapproaches)
*   [重载一元运算符](#OverloadingUnaryOperator)
*   [重载二元运算符](#OverloadingBinaryOperator)

那么，让我们从这篇关于 C++中运算符重载的文章开始吧。

**c++中的重载**

如果我们创建同一个类的两个或多个成员，它们有相同的名字，但是参数的数量或类型不同，这就是 C++重载。

在 C++中，我们可以重载:

*   方法
*   构造器
*   索引属性

这是因为这些成员只有参数。

继续这篇关于 C++中运算符重载的文章。

## **c++中重载的类型**

*   函数重载
*   运算符重载

![Overloading - Operator Overloading In C++ - Edureka](img/e94d3b323d26763da215ee4e4c06a7d0.png)

继续这篇关于 C++中运算符重载的文章。

## **为什么使用运算符重载？**

C++程序可以在不知道运算符重载的情况下编写。然后，操作员操作也被程序员深刻地用来使程序变得直观。举个例子，

我们可以将代码替换为:

```
calculation = add(divide(a, b),multiply(a, b));
```

对于等式

计算=(a/b)+(a * b)；

运算符重载为 C++中大多数运算符的新定义的开发提供了一种简单易行的方法。有了足够的知识，我们几乎可以通过创造性地使用函数和操作符重载技术来创建我们自己的新语言。我们可以重载 C++中的所有操作符，除了下面这些: ●范围操作符(::) ●大小操作符(Sizeof) ●成员选择器(。) ●成员指针选择器(*) ●三元运算符(？:)

**运算符重载的语法**

```
return_type class_name  : : operator op(argument_list)  
{  
// function body
}  

```

其中，返回类型是函数返回值的类型。class_name 是类的名称。

继续这篇关于 C++中运算符重载的文章。

## **在 C++中实现运算符重载**

运算符函数必须是非静态的(成员函数)或友元函数才能重载。如果左操作数是该类的对象，则运算符重载函数可应用于成员函数，但如果左操作数不同，则运算符重载函数必须定义为非成员函数。如果运算符重载函数需要访问该类的私有和受保护成员，它可以成为友元函数。例如，运算符 op 是一个运算符函数，其中 op 是被重载的运算符，运算符是关键字。运算符重载可以通过实现一个函数来实现，该函数可以是成员函数、非成员函数或友元函数。

**算子函数和正规函数有什么区别？**

运算符功能与普通功能相同。唯一的区别是，操作符函数的名字总是 operator 关键字，后跟操作符符号，当相应的操作符被使用时，操作符函数被调用。

继续这篇关于 C++中运算符重载的文章。

## **超载方法的类型**

运算符重载可以通过三种方法实现，它们是

*   重载一元运算符。
*   重载二元运算符。
*   使用友元函数重载二元运算符。

继续这篇关于 C++中运算符重载的文章。

## **重载一元运算符**

让我们考虑一元“–”运算符。用作一元运算符时，它只需要一个操作数。我们知道这个操作符在应用于基本数据变量时会改变操作数的符号。让我们看看如何重载这个操作符，以便它可以像应用于 int 或 float 变量一样应用于一个对象。一元减号应用于一个对象时，应该递减它的每个数据项。

**举例:**

```
#include <iostream> 
using namespace std; 
class Height { 
public:   
// Member Objects
int feet, inch;   
// Constructor to initialize the object's value 
Height(int f, int i) 
{ 
feet = f; 
inch = i; 
}   
// Overloading(-) operator to perform decrement 
// operation of Height object 
void operator-() 
{ 
feet--; 
inch--; 
cout << "Feet & Inches after decrement: " << feet << " ' " << inch <<endl; 
} 
};   
int main() 
{ 
//Declare and Initialize the constructor of class Height
Height h1(6, 2);   
//Use (-) unary operator by single operand 
-h1; 
return 0; 
} 

```

**输出:**

![Output- Operator Overloading in c++- Edureka](img/d34681c5c5b3b756f9c08c6d53ed1198.png)

**说明:** 在上面的例子中，我们重载' –'一元运算符对 Height 类的两个变量进行减量。我们将两个参数传递给构造函数，并将它们的值保存在英尺和英寸变量中。然后我们定义运算符重载函数(void operator-() )，其中两个变量递减一个位置。当我们写-h1 时，它调用操作符重载函数，并递减传递给构造函数的值。

继续这篇关于 C++中运算符重载的文章。

## **重载二元运算符**

它是对两个操作数进行操作的运算符的重载。让我们以相同的类高度为例，但这一次，添加两个高度对象 h1 和 h2。

**举例:**

```
#include <iostream>   
using namespace std; 
class Height 
{ 
public: 
int feet, inch; 
Height() 
{ 
feet = 0; 
inch = 0; 
}   
Height(int f, int i) 
{ 
feet = f; 
inch = i; 
}   
// Overloading (+) operator to perform addition of 
// two distance object using binary operator
Height operator+(Height& d2) // Call by reference 
{ 
// Create an object to return 
Height h3;   
// Perform addition of feet and inches 
h3.feet = feet + d2.feet; 
h3.inch = inch + d2.inch; 
// Return the resulting object 
return h3; 
} 
};  
int main() 
{ 
Height h1(3, 7);   
Height h2(6, 1); 
Height h3;   
//Use overloaded operator 
h3 = h1 + h2; 
cout << "Sum of  Feet & Inches: " << h3.feet << "'" << h3.inch << endl; 
return 0; 
} 

```

**输出:**

**解释:** Height 运算符+(Height & h2)，这里 returns_type 的函数是 class Height 因此它返回一个 class Height 的对象 h3。在 h3 = h1 + h2 这一行中，h1 调用其 classes 对象的 operator 函数并将 h2 作为参数，然后我们应用 H3 . foots = foots+D2 . foots；而 H3 . inch = inch+D2 . inch；它在与 h3 对象相关联的变量中存储变量英尺和英寸的值的总和。当语句“h3 = h1 + h2”调用运算符重载函数时，对象 h1 负责调用该函数，h2 扮演传递给该函数的参数的角色。上面的调用语句等价于 H3 = h1 . operator+(H2)；因此，h2 的数据成员是直接访问的，而 h2 的数据成员(作为参数传递)是使用点运算符访问的。

**运算符重载规则**

*   只能重载现有的运算符，不能重载新的运算符
*   重载运算符必须至少包含一个用户定义数据类型的操作数。
*   我们不使用友元函数来重载某些运算符。但是，成员函数可用于重载这些运算符。
*   当一元运算符通过成员函数重载时，它们不带显式参数，但是，如果它们被友元函数重载，它们会带一个参数。
*   当二元操作符通过成员函数重载时，它们有一个显式参数，如果通过友元函数重载，它们有两个显式参数。

至此，我们已经结束了这篇关于“C++中的运算符重载”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA 培训与认证](https://www.edureka.co/java-j2ee-soa-training/)课程旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。