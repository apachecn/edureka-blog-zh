# 如何在 C++中实现虚函数？

> 原文：<https://www.edureka.co/blog/virtual-function-in-cpp/>

[C++](https://www.edureka.co/blog/data-abstraction-in-cpp/) 中的虚函数是我们在派生类中重定义的基类中的成员函数。本文将帮助您详细探索这个概念。本文将涉及以下几点:

*   [什么是虚函数？](#WhatisVirtualFunction?)
*   [c++中的虚函数规则](#RulesforVirtualFunctioninC++)
*   [什么是绑定？](#WhatisBinding?)
*   [早期绑定](#Earlybinding)
*   [后期绑定](#Latebinding)
*   [纯虚函数](#PureVirtualFunction)
*   [抽象类](#AbstractClass)
*   [虚拟功能示例](#ExampleforVirtualFunction)

让我们从这篇关于 C++虚函数的文章开始吧

## **什么是虚函数？**

虚函数是我们在派生类中重新定义的基类中的成员函数。它是使用虚拟关键字声明的。当包含虚函数的类被继承时，派生类重新定义虚函数以适应自己的需要。

继续这篇关于 C++虚函数的文章

## **c++中虚函数的规则:**

*   它们总是在基类中定义，并在派生类中重写，但在派生类中重写并不是强制性的。
*   虚函数必须在类的公共部分声明。
*   它们不能是静态的或者友元函数也不能是另一个类的虚函数。
*   应该使用指针来访问虚函数，以实现运行时多态性。

继续这篇关于 C++虚函数的文章。

## **什么是绑定？**

函数的绑定意味着无论哪里有函数调用，编译器都需要知道它应该匹配哪个函数定义。这取决于每个函数声明的签名&所采用的赋值。此外，编译器需要知道函数调用和选择正确定义之间的匹配何时发生。

继续这篇关于 C++虚函数的文章

## **早期绑定**

早期绑定是一种现象，其中匹配各种函数调用的决定发生在编译时本身，编译器直接将链接与地址相关联。它也被称为静态绑定或编译时绑定。

*   众所周知，我们用高级语言编写代码
*   然后编译器将其转换成计算机可以理解的低级语言，在编译时主要是机器语言
*   在早期绑定中，编译器直接向函数调用指令提供函数声明指令的地址
*   因此，顾名思义，绑定发生在程序运行之前很早的时候。

**例子**

```
#include <iostream>
using namespace std;
class Animals
{
public:
void sound()
{
cout << "Genric animal sound" << endl;
}
};
class Cats: public Animals
{
public:
void sound()
{
cout << "Cat meow" << endl; } }; int main() { Animals *a; Cats c; a= &c; a -> sound();   //  early binding
return 0;
}

```

**输出**

![Output- Virtual function in C++- Edureka](img/9c9b3a0af650f927ff5caf5f1e904bd7.png)

解释在这个例子中，我们创建了一个指向父类 Animals 的指针 a。然后通过写 a= & c，指针‘a’开始指向 Cats 类的对象 c。 a - >音()；–在通过指针“a”调用两个类中都存在的函数 sound()时，父类的函数被调用，即使指针指向 Cats 类的对象。

这是由于早期绑定。我们知道‘a’是指向子类对象的父类指针。由于早期绑定发生在编译时，因此当编译器看到“a”是父类的指针时，它将调用与父类的“sound()”函数匹配，而不搜索它所引用的对象。

继续这篇关于 C++虚函数的文章

## **后期绑定**

在后期绑定中，编译器在运行时识别对象，然后将函数调用与正确的函数匹配。它也被称为动态绑定或运行时绑定。

上述问题中的后期绑定可以通过在基类中使用虚拟关键字来解决。让我们通过使用上面的例子本身来看看这是如何发生的，只是添加了虚拟关键字。

**例子**

```
#include <iostream>
using namespace std;
class Animals
{public:
virtual void sound()
{
cout << "Genric aniaml sound" << endl;
}
};
class Cats: public Animals
{
public:
void sound()
{
cout << "Cats meow" << endl; } }; int main() { Animals *a; Cats c; a= &c; a -> sound();
return 0;
}

```

**输出**

![Output- Virtual function in C++- Edureka](img/a1070c10c823300e43cf1699d4ddf35c.png)

**解释** 这里基类的函数 sound()是虚的，因此编译器现在为这个函数执行后期绑定。现在，sound()函数的函数调用将在运行时与函数定义相匹配。因为编译器现在将指针“a”标识为指向派生类 Cats 的对象“c ”,所以它将调用 Cats 类的 sound()函数。

继续这篇关于 C++虚函数的文章

## **纯虚函数**

C++中的纯虚函数是没有实现的虚函数，我们只声明它。纯虚函数是通过在声明中赋值 0 来声明的。

虚空音()= 0；

这里 sound_)是一个纯虚函数。

继续这篇关于 C++虚函数的文章

## **抽象类**

抽象类被定义为具有一个或多个纯虚函数的类。如上所述，纯虚函数是被标记为没有实现的虚拟成员函数。它不可能用类中提供的信息实现，包括任何基类。抽象类也称为抽象基类。

**例子**

```
#include <iostream>
using namespace std;
class Employee  //  abstract base class
{
virtual int getSalary() = 0;  // pure virtual function
};
class Employee_1: public Employee
{
int salary;
public:
Employee_1(int s)
{
salary = s;
}
int getSalary()
{
return salary;
}
};
class Employee_2: public Employee
{
int salary;
public:
Employee_2(int t)
{
salary = t;
}
int getSalary()
{
return salary;
}
};
int main()
{
Employee_1 e1(5000);
Employee_2 e2(3000);
int a, b;
a = e1.getSalary();
b = e2.getSalary();
cout << "Salary of Developer : " << a << endl;
cout << "Salary of Driver : " << b << endl;
return 0;
}

```

**输出**

![Output- Virtual function in C++- Edureka](img/b5072fa0d6984453668fc6d7fb7eba19.png)

**解释**Employee 类中的' getSalary()'函数是一个纯虚函数。由于 Employee 类包含纯虚函数，所以它是一个抽象基类。由于纯虚函数是在子类中定义的，因此函数“getSalary()”在雇员类的两个子类中都有定义，即雇员 _1 和雇员 _2。

继续这篇关于 C++虚函数的文章

## **虚拟功能示例**

```
#include<iostream>
using namespace std;
class base
{
public:
void function_1() { cout << "base class function 1n"; }
virtual void function_2() { cout << "base class function 2n"; }
virtual void function_3() { cout << "base class function 3n"; }
virtual void function_4() { cout << "base class function 4n"; }
};
class derived : public base
{
public:
void function_1() { cout << "derived class function 1n"; }
void function_2() { cout << "derived class function 2n"; }
void function_4(int x) { cout << "derived class function 4n"; } }; int main() { base *ptr; derived obj1; ptr = &obj1; ptr->function_1();
ptr->function_2();
ptr->function_3();
ptr->function_4();
}

```

**输出**

![Output- Virtual function in C++- Edureka](img/d77b5994cc7853d30e373262a27d2f7a.png)

**解释** 对于 function_1()函数调用，调用函数的基类版本，function_2()在派生类中被重写，所以调用派生类版本，function_3()在派生类中没有被重写，是虚函数，所以调用基类版本，同样 function_4()没有被重写，所以调用基类版本。

这样，我们就结束了这篇关于“C++中的虚函数”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。