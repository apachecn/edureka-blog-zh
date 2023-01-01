# 如何用 C++实现这个指针？

> 原文：<https://www.edureka.co/blog/this-pointer-in-cpp/>

在编程时，你可能遇到过“this”关键字。这是一个指向调用者对象的指针。在这篇文章中，我们将深入探讨 c++T3 中这个[指针的概念](https://www.edureka.co/blog/pointers-in-cpp/)

本文将涉及以下几点，

*   [指向对象的指针](#PointerstoObjects)
*   [指向对象的指针示例代码](#SamplecodeforPointerstoObjects)
*   [这个指针](#Thispointer)
*   [该指针的示例代码](#SamplecodeforThispointer)

让我们从这篇关于 C++中指针的文章开始

## **c++中的这个指针**

## **指向对象的指针**

人们倾向于远离指针，因为他们的工作听起来有点混乱。在这篇文章中，我们将以最简单的方式理解指针的概念。指针用于保存特定变量的地址。它们用来引用它所存储地址的变量。这里需要注意的重要一点是，指针只能存储与指针类型相匹配的变量的地址。换句话说，int 类型指针只能保存 int 类型变量的地址。

用来存储对象地址的指针应该是什么类型？为了找到这个问题的答案，我们需要了解特定对象的类型是什么？Int，char，float？不，对象的类型是 class。换句话说，对象的类型就是它所属的类。因为特定的类是用户定义的数据类型，并且该类的对象属于该类型。

到目前为止，您可能已经将指针指向了原始数据类型的引用变量。让我们看看如何使用可以指向特定对象的指针。

继续看指向对象的指针的示例代码

**语法**

```
class_name *pointer_name;
```

```
#include <iostream>
using namespace std;
class Car{
public:
int Number_of_wheels;
int Number_of_passengers;
void getinfo(int x, int y){
Number_of_wheels = x;
Number_of_passengers = y;
}       
void showinfo(){
cout<<"Number of Wheels = "<<Number_of_wheels<<"n";
cout<<"Number of Passengers = "<<Number_of_passengers<<"n"; } }; int main() { Car car; Car *ptr; ptr=&car; ptr->getinfo(4,5);
ptr->showinfo();
Car car2;
car2.getinfo(6,8);
car2.showinfo();
return 0;
}

```

**输出**

车轮数量= 4

乘客数量= 5

车轮数量= 6

乘客数量= 8

这就是我们如何使用指针来引用一个对象。

**注** 本。运算符用于对象的名称，而- >运算符用于通过指针访问方法。

继续这篇关于 C++指针的文章

## **这个指针**

如果你使用 python，你可能会遇到“自我”这个词。“这个”和“自我”的功能是相似的。“This”是一个传递给类的所有非静态方法的参数，我们看不到它，但它可以用于类的任何非静态或实例方法中。“This”指针一被调用就被传递给非静态成员函数。它是一个类的所有非静态成员函数的隐式参数。

继续这个指针的示例代码

```
#include <iostream>
using namespace std;
class Car{
private:
int Number_of_wheels;
int Number_of_passengers;
public:
void getinfo(int x, int y){
this->Number_of_wheels = x;
this->Number_of_passengers = y;
}        
void showinfo(){
cout<<"Number of Wheels = "<<Number_of_wheels<<"n";
cout<<"Number of Passengers = "<<Number_of_passengers<<"n";
cout<<"Address of the current object is = "<<this<<"n"; } }; int main() { Car car; Car *ptr; ptr=&car; ptr->getinfo(4,5);
ptr->showinfo();
Car car2;
car2.getinfo(6,8);
car2.showinfo();
return 0;
}

```

**输出**

车轮数量= 4

乘客数量= 5

当前对象的地址= 0x7ffdbac81740

车轮数量= 6

乘客数量= 8

当前对象的地址= 0x7ffdbac81748

上面的程序让我们对“this”关键字有了一个简单的了解。当变量名冲突或者当一个方法中涉及多个对象时,“this”关键字很有用。

**指针指向派生类**

指针不仅可以用来引用基类，还可以用来指向派生类对象。例如，如果类 Car 继承自类 Vehicles，那么类型 Vehicles 的指针也可以用来指向类型 Car 的对象。

```
Vehicles *ptr;
Vehicles vehicles;
Car car;
ptr = &vehicles;
ptr = & car;

```

这里唯一的问题是，如果我们使用基类指针指向派生类对象，我们将只能访问由派生类对象继承的基类方法。我们不能使用基类指针访问派生类的成员。

如果类 Car 的成员与类 Vehicles 的成员之一同名，那么在这种情况下，指针将访问基类成员。

这样，我们就结束了这篇关于“C++中的指针”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。