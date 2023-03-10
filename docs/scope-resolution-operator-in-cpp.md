# 如何在 C++中最好地利用范围解析运算符？

> 原文：<https://www.edureka.co/blog/scope-resolution-operator-in-cpp/>

顾名思义，作用域解析操作符用于获得由于可变作用域而隐藏的名称，以便您仍然可以使用它们。在本文中，我们将了解如何在 C++中使用作用域解析操作符&从[编程的角度来看](https://www.edureka.co/programming-and-frameworks-certification-courses)它有什么不同的用途。

在 C++中，范围解析运算符是::。C++中的范围解析运算符可用于:

*   [存在同名的局部变量时访问全局变量](#Accessingaglobalvariablewhenthereisalocalvariablewithsamename)
*   [在类外定义函数](#Definingafunctionoutsideaclass)
*   [访问一个类的静态变量](#Accessingaclass%E2%80%99sstaticvariables)
*   [引用另一个类中的一个类](#Referringtoaclassinsideanotherclass)
*   [在多重继承的情况下](#IncaseofmultipleInheritance)
*   [命名空间](#Namespace)

现在让我们借助例子逐一理解每一个目的。

## **当存在与**同名的局部变量时，访问全局变量

如果有一个同名的局部变量，可以使用范围解析运算符来访问全局变量。在下面的例子中，我们有两个变量，名字都是 num，范围是全局和局部。因此，要访问主类中的全局 num 变量，您需要使用范围解析操作符(即:* num)。

**例子**

```
#include<iostream>  
using namespace std;    
int num = 30;  // Initializing a global variable num   
int main() 
{ 
int num = 10; // Initializing the local variable num
cout << "Value of global num is " << ::num; 
cout << "nValue of local num is " << num;   
return 0;
}

```

**输出**

继续这篇关于 C++中作用域解析操作符的文章

## **在类外定义函数**

如果在类中声明一个函数，然后想在类外定义它，可以使用范围解析操作符。在下面的例子中，我们在类 Bike 中声明了一个函数 Speed。稍后，我们将使用范围解析操作符在主类中定义函数。

**例子**

```
#include<iostream>  
using namespace std;   
class Bike  
{ 
public:  
// Just the Function Declaration
void Speed(); 
};  
// Defining the Speed function outside Bike class using :: 
void Bike::Speed() 
{ 
cout << "Speed of Bike is 90 KMPH"; 
}   
int main() 
{ 
Bike bike; 
bike.Speed(); 
return 0; 
}

```

**输出**

继续这篇关于 C++中作用域解析操作符的文章

## **访问类的静态**变量

您可以使用类名和范围解析操作符(即 class_name::static_variable)来访问类的静态变量。你可以在下面的例子中看到，我们在类中声明了一个静态变量。我们使用范围解析操作符在类外定义变量。然后我们使用类名和范围解析操作符来访问它。

**例子**

```
#include<iostream> 
using namespace std;    
class Try 
{ 
static int num1;   
public: 
static int num2;    
// Local parameter hides class member 
// Class member can be accessed it using ::
void function(int num1)   
{  
// num1 static variable can be accessed using :: 
// inspite of local variable num1
cout << "Static num1: " << Try::num1; 
cout << "nLocal num1: " << num1;   
} 
};    
// Defining a static members explicitly using ::
int Try::num1 = 10; 
int Try::num2 = 15;    
int main() 
{ 
Try o; 
int num1 = 20 ; 
o.function(num1); 
cout << "nTry::num2 = " << Try::num2; 
return 0; 
}

```

**输出**

继续这篇关于 C++中作用域解析操作符的文章

## **引用另一个类中的一个类**

您可以在两个类中创建具有相同变量名的嵌套类。您可以使用范围解析操作符来访问这两个变量。对于内部类变量，需要使用***Outer _ Class::Inner _ Class::variable。***

**例子**

```
#include<iostream> 
using namespace std;   
class Outside_class
{ 
public: 
int num; 
class Inside_class 
{ 
public: 
int num; 
static int x;  
}; 
}; 
int Outside_class::Inside_class::x = 5;    
int main(){ 
Outside_class A; 
Outside_class::Inside_class B; 
}

```

继续这篇关于 C++中作用域解析操作符的文章

## **在多重继承的情况下**

如果有两个变量名相同的父类，并且在子类中继承了这两个类，那么可以对类名使用作用域解析运算符来访问单个变量。

在下面的例子中，我们创建了两个父类 Parent1 & Parent2，它们都有变量 num。当我们在子类中继承这两个变量时，我们可以使用类名和范围解析操作符来访问这两个 num 变量。

**例子**

```
#include<iostream> 
using namespace std;  
class Parent1 
{ 
protected: 
int num; 
public: 
Parent1() { num = 100; } 
};   
class Parent2
{ 
protected: 
int num; 
public: 
Parent2() { num = 200; } 
};   
class Child: public Parent1, public Parent2 
{ 
public: 
void function() 
{ 
cout << "Parent1's num is " << Parent1::num; 
cout << "nParent2's num is " << Parent2::num; 
} 
};  
int main() 
{ 
Child obj; 
obj.function(); 
return 0; 
}

```

**输出**

继续这篇关于 C++中作用域解析操作符的文章

## **命名空间**

假设我们有两个名称空间&都包含同名的类。因此，为了避免任何冲突，我们可以将名称空间名称与范围解析操作符一起使用。在下面的例子中，我们使用了 ***std::cout*** 。

**例子**

```
#include<iostream>  
int main(){ 
std::cout << "Hello" << std::endl;  
}

```

**输出**

现在，在浏览了上面的程序之后，你应该已经理解了 C++中作用域解析操作符的所有内容。我希望这篇博客能给你带来信息和附加值。

现在，在执行了上面的程序之后，你应该已经理解了 C++中的作用域解析操作符。这样我们就结束了这篇关于“Java 中的快速排序”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题吗？请在这个博客的评论部分提到它，我们会尽快回复你。

现在，在执行了上面的程序之后，你应该已经理解了 C++中的作用域解析操作符。这样我们就结束了这篇关于“Java 中的快速排序”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题吗？请在这个博客的评论部分提到它，我们会尽快回复你。