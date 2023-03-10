# C++如何实现构造函数和析构函数？

> 原文：<https://www.edureka.co/blog/constructor-and-destructor-in-cpp/>

如果你问当前的[编程](https://www.edureka.co/blog/c-data-structures)世界，C++很容易成为最重要的编程语言之一。它的众多原因之一是它提供的功能。本文将讨论 C++中的构造函数和析构函数。本文将涉及以下几点:

*   [构造器](#Constructor)
*   [默认构造函数](#Default%20Constructor)
*   [参数化构造器](#Parameterized%20Constructor)
*   [复制构造函数](#CopyConstructor)
*   [析构函数](#Destructor)
*   [虚拟析构函数](#Virtual%20Destructor)

让我们从这篇关于 C++中构造函数和析构函数的文章开始吧

## **c++中的构造函数和析构函数**

## **构造器**

构造函数是类的成员函数。它主要用于初始化类的对象。它与类同名。创建对象时，会自动调用构造函数。它是一种特殊的类成员函数。

构造函数和其他成员函数的区别:

1.构造函数与类名同名。 2。当创建类的对象时，调用构造函数。 3。构造函数没有返回类型。 4。如果没有指定构造函数，编译器会生成一个默认的构造函数，它什么也不做。 5。有 3 种类型的构造函数:

*   默认构造函数
*   参数化构造函数
*   复制构造函数

构造函数也可以在类的私有部分定义。

继续这篇关于 C++中构造函数和析构函数的文章

## **默认构造函数**

默认构造函数是一种不带任何参数的构造函数。

**下面是一个示例代码**

```
#include <iostream>
using namespace std;
class test {
public:
int y, z;
test()
{
y = 7;
z = 13;
}
};
int main()
{
test a;
cout <<"the sum is: "<< a.y+a.z;
return 1;
}

```

```
Output:
```

![Output- Constructor and Destructor in C++- Edureka](img/06a27b125948a4bc7c7803d2a9a98eac.png)

**说明:**

上面的程序是 c++中一个构造函数的基本演示。我们有一个类测试，有两个 int 类型的数据成员，分别叫 y 和 z。然后我们有一个默认的构造函数，它把 7 和 13 分别赋给变量 y 和 z。主函数有一个名为 a 的类 test 对象。当这个对象被创建时，构造函数被调用，变量 y 和 z 被赋值。main 函数有一个 cout 语句或一个 print 语句。在该语句中，将打印总和。关于类的对象，我们访问类的公共成员，也就是 a.y 给出 y 的值，对于 z 也是一样，我们显示 y 和 z 的和默认构造函数就是这样工作的。当我们不提供默认的构造函数时，编译器会生成一个默认的构造函数。接下来，让我们看看参数化构造函数。

继续这篇关于 C++中构造函数和析构函数的文章

## **参数化构造器**

将参数传递给构造函数是可能的。这样做是为了使用这些传递的参数初始化该值。这种类型的构造函数称为参数化构造函数。构造函数定义如下:

```
test(int x1) 
{ 
x = x1;
} 

```

有一个传递给构造函数的参数。当在 main 函数中创建对象时，传递该值，如下所示。

```
test t(10);
```

在 main 函数中，我们创建了一个类 test 的对象，并传递变量的值。

下面是一个示例代码:

```
#include <iostream> 
using namespace std;   
class test { 
public: 
int x; 
test(int x1) 
{ 
x = x1; 
}      
int getX() 
{ 
return x; 
}     
};   
int main() 
{    
test a(10); 
cout << "a.x = " << a.getX() ; 
return 0; 
}

```

**输出** 输出![Output- Constructor and Destructor in C++- Edureka](img/14e76440f7a4fcc9abb47673d0a73745.png)

## **解释**

上面的程序是一个参数化构造函数的基本演示。我们有一个类测试，有一个 int 类型的数据成员，名为 x。然后我们有一个参数化的构造函数，在创建对象时，x1 作为从主函数传递的参数。构造函数将 x1 的值赋给数据成员 x。接下来我们有一个 getX 函数，它只是简单地返回 x 的值。

```
test a(10);
```

然后，我们使用成员函数 getX 打印 x 的值。我们调用与测试类的对象相关的函数。

继续这篇关于 C++中构造函数和析构函数的文章

## **复制构造函数**

复制构造函数是一种构造函数，它使用一个类的另一个对象初始化该类的一个对象。

下面是一个示例代码:

```
#include<iostream>
using namespace std;
class test
{
private:
int x;
public:
test(int x1)
{
x = x1;
}
test(const test &t2)
{
x = t2.x;
}
int getX()
{
return x;
}
};
int main()
{
test t1(7); // Normal constructor is called here
test t2 = t1; // Copy constructor is called here
cout << "t1.x = " << t1.getX();
cout << "nt2.x = " << t2.getX();
return 0;
}

```

```
Output
```

![Output- Constructor and Destructor in C++- Edureka](img/85b7de0cac6c49e9624b266b879c071d.png)

**解释**

上面的程序是一个复制构造函数的基本演示。我们有一个类测试，有一个名为 x 的 int 类型的私有数据成员。然后我们有一个参数化的构造函数，它将 7 赋给变量 x。我们有一个复制构造函数，它用 t1 的值实例化 t2 的值。

```
test(const test &t2)
{
x = t2.x;
}

```

发送包含 t1 值的 t2 地址，并将其分配给 x。有一个 get 函数返回 x 的值。主函数有一个名为 t1 的类 test 对象。有一个值与此对象相关联，这是一个参数。

```
test t1(7);
```

main 函数有另一个名为 t2 的类测试对象。这是使用 t1 变量初始化的，这里调用复制构造函数。

```
test t2=t1;
```

最后，针对 t1 和 t2 调用 get 函数来获得 x 的值。

```
cout << "t1.x = " << t1.getX();
cout << "nt2.x = " << t2.getX();

```

接下来，我们看看析构函数。

继续这篇关于 C++中构造函数和析构函数的文章

## **析构函数**

析构函数是另一种负责销毁或删除对象的成员函数。它释放不再需要的对象所占用的空间。当对象超出范围不再需要时，会自动调用析构函数。析构函数的名称与类名相同，但唯一的区别是名称前面有一个瓷砖(~)。

```
~test()
```

一个类中只能有一个析构函数。析构函数没有返回类型和参数。如果我们在类中指定了一个析构函数，编译器就会创建一个默认的析构函数。除非动态分配内存或者在类中声明指针，否则默认析构函数工作正常。析构函数被调用时，

*   功能结束。
*   程序结束。
*   包含局部变量的块结束。
*   删除操作符在程序中被调用。

下面是一个示例代码:

```
#include <iostream>
using namespace std;
class test {
public:
int y, z;
test()
{
y = 7;
z = 13;
}
~test(){ }
};
int main()
{
test a;
cout <<"the sum is: "<< a.y+a.z;
return 1;
}

```

```
Output
```

![Output- Constructor and Destructor in C++- Edureka](img/39b64849e2250af3b57819554802aaa3.png)

这段代码中唯一的区别是出现了一个析构函数，用于在程序执行完成后销毁创建的对象。

继续这篇关于 C++中构造函数和析构函数的文章

## **虚拟析构函数**

析构函数的唯一变化是将析构函数虚拟化。这是在我们有遗产的时候做的。在继承过程中，普通析构函数的行为是不确定的。要解决这个问题，基类析构函数必须声明为虚拟的。

```
class base {
public:
base()
{ cout<<"base Constructor n"; }
virtual ~base()
{ cout<<"base destructorn"; }
};

```

将基础虚拟化可确保正确删除对象。

这样，我们就结束了这篇关于“C++中的构造函数和析构函数”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。