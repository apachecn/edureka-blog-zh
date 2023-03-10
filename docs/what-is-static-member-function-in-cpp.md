# C++中的静态成员函数是什么？

> 原文：<https://www.edureka.co/blog/what-is-static-member-function-in-cpp>

Static 是 C 和 C++中的一个关键字，用于声明类内部或外部的一个特殊类型的变量或函数。在这篇文章中，我们将简要了解 c++中静态成员变量和静态成员函数的概念，并按照以下顺序将它们与普通变量和函数进行比较:

*   [静态成员变量](#variable)
*   [c++中的静态成员函数](#function)

## **静态成员变量**

分类为静态的变量也是 c 的一部分，假设在一个函数中有 2 个变量，一个是普通变量，另一个是静态变量。normal 变量是在函数被调用时创建的，它的作用域是有限的。而静态变量只创建一次，在程序结束时销毁。这些变量在整个程序中有一个生命周期。

```
#include <iostream>

using namespace std;
void Test(){

    static int x = 1;
     x = ++x;

    int y = 1;
    y = ++y;
    cout<<"x = "<<x<<"n";
    cout<<"y = "<<y<<"n";
}
int main()
{  
    Test();
    Test();

    return 0;
}
```

**输出:**

![static-member-variables-1](img/561008aa10fdb0ca158942903adaeb87.png)

从上面的输出中，我们可以得出结论，每次调用 Test()函数时，都会创建变量“y”的副本，而每次调用 Test()函数时，都会使用变量“x”的相同副本。

现在，让我们讨论静态变量的特征

1.  静态变量被初始化为 0。它只初始化一次。

2.  在整个程序中，整个类只创建一个静态成员变量的副本，因此静态成员变量也被称为类变量。它由该类的所有实例共享。

3.  静态成员变量只在类中可见，但它的生命周期直到程序结束。

让我们考虑一个类中静态成员变量的例子。

```
#include <iostream>

using namespace std;

class Example{

    static int x;

public:

    void function1(){
        x++;
    }

    void function2(){
        cout<<"x = "<<x<<"n";
    }

};

int Example :: x;

int main()
{
    Example obj1, obj2, obj3;

    cout<<"Initial value of x" <<"n";

    obj1.function2();
    obj2.function2();
    obj3.function2();

    obj1.function1();
    obj2.function1();
    obj3.function1();

    cout<<"Value of x after calling function1"<<"n";

    obj1.function2();
    obj2.function2();
    obj3.function2();

    return 0;
}
```

**输出:**

![static-member-variables-2](img/c6448c58c6332a423086eae2855c27ab.png)

从上面的输出中，我们可以看到变量‘x’被所有对象共享。为了详细理解静态数据变量的概念，我们可以想象一个图书馆，里面有几本书放在不同的书架上。将图书馆视为一个类，将某本书的位置“x”视为一个静态成员变量，将学生视为该类的对象。当第一个学生到达时，他将“x”放在一个新的位置。现在，当另一个学生到达时,“x”不会回到原来的位置，但会留在第一个学生离开的地方。

## **c++中的静态成员函数**

就像静态成员变量一样，我们也有用于特定目的的静态成员函数。要创建一个静态成员函数，我们需要在声明函数时使用 static 关键字。因为静态成员变量是类属性而不是对象属性，所以要访问它们，我们需要使用类名而不是对象名。

**静态成员函数的属性:**

1.  静态函数只能访问同一个类中的其他静态变量或函数

2.  使用类名调用静态成员函数。语法-class _ name::function _ name()

让我们考虑一个经典的例子来详细理解静态成员函数的概念。在这个例子中，我们将理解与静态成员函数相关的所有概念。

```
#include <iostream>

using namespace std;

class Example{
    static int Number;
    int n;

    public:

    void set_n(){

        n = ++Number;
    }

    void show_n(){

        cout<<"value of n = "<<n<<endl;
    }

    static void show_Number(){

        cout<<"value of Number = "<<Number<<endl;
    }

};

int Example:: Number;

int main()
{
    Example example1, example2;

    example1.set_n();
    example2.set_n();

    example1.show_n();
    example2.show_n();

    Example::show_Number();

    return 0;
}
```

**输出:**

![static-member-function-in-c++](img/64e282f1585f55ca76440251bb3020ab.png)

从上面的输出中，我们可以看到变量“n”的值对于类“example”的对象“example1”和“example2”是不同的。因为变量“Number”是一个类变量，所以它的值对于对象“example1”和“example2”是相同的。当所有对象共享公共值时，使用静态成员变量和函数。在编程时，应该明智地使用 static 关键字。

至此，我们结束了这篇关于 c++中静态成员函数的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。