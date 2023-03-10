# 如何使用动态内存分配 C++？

> 原文：<https://www.edureka.co/blog/dynamic-memory-allocation-cpp/>

C++中的动态内存分配是一个非常重要的特性，它允许您考虑自己的需求来处理对实时资源的需求。在本文中，我们将详细探讨动态内存的探索。本文将涉及以下几点:

*   [需要动态内存分配？](#NeedforDynamicmemoryallocation?)
*   [分配内存使用 ***新增*** 关键字](#AllocationofMemoryusingnewKeyword)
*   [使用 ***删除*** 关键字](#DeallocationofmemoryusingdeleteKeyword)解除内存分配
*   [动态分配数组](#DynamicallyAllocatingArrays)
*   [对象的动态内存分配](#DynamicMemoryAllocationforObjects)

让我们从这篇关于 C++中动态内存分配的文章开始

## **需要动态内存分配？**

比方说，我们想要输入一个句子作为一个字符数组，但是我们不确定数组中需要的字符的确切数量。

现在，在声明字符数组时，如果我们指定它的大小小于所需字符串的大小，那么我们将得到一个错误，因为分配给该数组的内存空间小于输入字符串的大小。如果我们指定它的大小大于输入字符串的大小，那么数组将在内存中分配一个比所需字符串的大小大得多的空间，从而不必要地消耗更多的内存，即使在不需要的时候也是如此。

在上面的例子中，直到编译时(计算机编译代码，用户输入字符串)，我们才知道数组的确切大小。在这种情况下，我们使用 **new** 操作符。

C++定义了两个一元操作符 **new** 和 **delete** ，它们在运行时执行分配和释放内存的任务。因为这些操作符(new 和 delete)是在自由存储内存(堆内存)上操作的，所以它们也被称为自由存储操作符。指针为 C++中的动态内存分配系统提供了必要的支持。

借助动态分配，程序可以在运行时获得内存。

全局和局部变量在编译时被分配到内存中。然而，我们不能在运行时添加任何全局或局部变量。如果程序需要使用可变数量的内存，我们需要在运行时按需分配内存。当然，这里的动态分配例程可以满足这个目的。

**静态内存分配和动态内存分配的区别:**

这是用于任何 C++程序的基本内存架构:

![Memory - Dynamic Memory Allocation - Edureka](img/035f4bff8d15a3f242e1c486a2d65912.png)

我们需要这样的图像

堆栈用于静态内存分配，堆用于动态内存分配，两者都存储在计算机的 RAM 中。

在堆栈上分配的变量，而静态内存分配是直接存储在内存中的，对内存的访问非常快，而且它的分配是在程序编译时处理的。当一个函数或方法调用另一个函数，而另一个函数又可能调用另一个函数，以此类推，所有这些函数的执行都保持暂停，直到最后一个函数返回值。堆栈总是以后进先出的顺序存储，最近保留的块总是下一个要释放的块。这有助于跟踪堆栈，从堆栈中释放一个块只不过是调整一个指针。

在堆上分配的变量在运行时分配内存，而动态内存分配。与 stack 相比，访问这个内存要慢一些，但是堆的大小只受虚拟内存大小的限制。堆中的元素相互之间没有依赖关系，并且可以随时随机访问。我们可以随时分配一个块，也可以随时释放它。这使得很难跟踪在任何给定时间堆的哪些部分被分配或释放。

继续这篇关于 C++中动态内存分配的文章

## **使用*新*关键字**分配内存

在 C++中， ***new*** 运算符用于在运行时分配内存，内存是以字节为单位分配的。 ***new*** 操作符表示对堆上动态内存分配的请求。如果有足够的内存可用，那么 ***new*** 操作符初始化内存，并将新分配和初始化的内存地址返回给指针变量。

### 语法:

```
datatype *pointer_name = new datatype
```

### 示例:

```
int *ptr = new int;
//We can declare a variable while dynamical allocation in the following two ways.
int *ptr = new int (10);
int *ptr = new int {15};
// new operator is also used to allocate a block(an array) of memory of type data-type.
int *ptr = new int[20];
// The above statement dynamically allocates memory for 20 integers continuously of type int and returns a pointer to the 
first element of the sequence to ‘ptr’ pointer.  

```

**注意**:如果堆没有足够的内存分配，新请求通过抛出异常 std::bad_alloc 来表示失败，除非“nothrow”与 new 运算符一起使用，在这种情况下，它会返回一个空指针。因此，在程序中使用 new 产生的指针变量之前，检查它是一个好的做法。

继续这篇关于 C++中动态内存分配的文章

## 使用 ***删除*** 关键字解除内存分配:

一旦使用 ***new*** 关键字将堆内存分配给一个变量或类对象，我们就可以使用 ***delete*** 关键字来释放内存空间。

**语法:**

```
delete pointer_variable;
// Here, pointer_variable is the pointer that points to the data object created by new.
delete[] pointer_variable; 
//To free the dynamically allocated array memory pointed by pointer-variable we use the following form of delete:

```

**举例:**

```
delete ptr;
delete[] ptr;

```

**注**:对象的范围或对象的生存期是程序执行过程中对象在内存中停留的时间。堆内存分配比堆栈慢，因为在堆中，内存分配没有特定的顺序，而在堆栈中，内存分配遵循 LIFO。

继续这篇关于 C++中动态内存分配的文章

## **动态分配数组**

动态内存分配概念的主要用途是，当我们必须通过指定数组的大小来声明它，但又不确定它的大小时，将内存分配给数组。

我们来看，一个理解其用法的例子。

```
#include <iostream>
using namespace std;
int main()
{
int len, sum = 0;
cout << "Enter the no. of students in the class" << endl; cin >> len;
int *marks = new int[len];  //Dynamic memory allocation
cout << "Enter the marks of each student" << endl;
for( int i = 0; i < len; i++ ) { cin >> *(marks+i);
}
for( int i = 0; i < len; i++ )            
{
sum += *(marks+i);
}
cout << "sum is " << sum << endl;
return 0;
}

```

**解释:** 在这个例子中，我们首先向用户询问一个班级的学生人数，并将它的值存储在 len 变量中。然后，我们声明一个整数数组，并使用下面的语句 int *marks = new int[length]动态地在内存中为它分配与 len 变量中存储的值相等的空间；因此，它被分配了一个等于“长度*(1 整数的大小)”的空间。代码的其余部分不言自明。

继续这篇关于 C++中动态内存分配的文章

## **对象的动态内存分配**

我们也可以动态分配对象。

正如我们所知，构造函数是一个特殊的类成员函数，用于初始化一个对象，析构函数也是一个类成员函数，每当对象超出作用域时就会被调用。

析构函数可以用来释放分配给对象的内存。在下列情况下调用它。

*   当本地对象超出范围时
*   对于全局对象，当运算符应用于指向该类对象的指针时

我们可以在动态分配内存给对象时再次使用指针。

让我们看一个对象数组的例子。

```
#include <iostream>
using namespace std;
class Random
{
public:
Random() {
cout << "Constructor" << endl;
}
~Random() {
cout << "Destructor" << endl;
}
};
int main()
{
Random* a = new Random[3];
delete [] a; // Delete array
return 0;
}

```

**输出:**

![Output- Dynamic memory allocation C++- Edureka](img/3fcda9063989e3ab64b5dd10de35977e.png)

**说明:**

这个构造函数将被调用三次，因为我们正在给 Random 类的三个对象分配内存。在处理这些对象时，析构函数也会被调用三次。Random * a = new Random[3]；”这个语句负责对象的动态内存分配。

这样，我们就结束了这篇关于“动态内存分配 C++”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。