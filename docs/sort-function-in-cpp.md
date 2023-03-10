# 如何在 C++中实现排序函数？

> 原文：<https://www.edureka.co/blog/sort-function-in-cpp/>

[排序](https://www.edureka.co/blog/sort-arraylist-string-map-set-in-java/)是应用于数据的最基本、最有用的函数之一。它旨在以特定的方式排列数据，可以根据需要增加或减少。C++ STL 中有一个名为“sort()”的内置函数，它允许我们轻松地执行排序算法。在本文中，我们将探索 C++中的排序函数，

本文将涉及以下几点:

*   [Sort()函数](#Sort()function)
*   [示例-按升序对数据进行排序](#Example-Tsortdatainascendingorder)
*   [示例–按降序对数据进行排序](#Example-Tosortdataindescendingorder)
*   [部分 _ 排序](#Partial_sort)

继续这篇关于 C++中排序函数的文章

## **排序** ( **)功能**

这是一个算法头文件的内置函数，它被用来对容器进行排序，就像一个数组，一个指定顺序的向量。在内部，这个函数被实现为快速排序快速排序是一个分治算法。快速排序首先将一个大的元素列表分成两个较小的子列表:较低的元素和较高的元素。快速排序然后递归排序子列表。

步骤如下: 1。从列表中选择一个随机元素(通常是最后一个元素)，称为轴心。 2。对列表进行重新排序，使所有值小于中枢的元素排在中枢之前，而所有值大于中枢的元素排在中枢之后，并且值相等的元素可以向任意方向移动。这一过程称为分区操作。 3。递归地排序较小元素的子列表和较大元素的子列表，再次在子列表中选择一个枢轴并划分它们。递归的基本情况是大小为 0 或 1 的列表，它们从不需要排序，因此通过组合它们，我们对列表进行排序。

实际上，快速排序比其他 O(n log n)算法更快，如插入排序或冒泡排序。快速排序可以通过就地分区算法实现，这意味着整个排序只需要 O(log n)额外的空间。快速排序不是一种稳定的排序。其复杂度如下:最佳情况–o(n log n)最差情况–o(n^2)一般情况–o(n log n)

**语法:** 排序(first，last)；这里，first–是要排序的范围中第一个元素的索引(指针)。last–是要排序的范围中最后一个元素的索引(指针)。例如，我们想对数组‘arr’的元素从 1 到 10 的位置进行排序，我们将使用 sort(arr，arr+10 ),它将按升序对 10 个元素进行排序。返回值无

**复杂度**

排序复杂度的平均值是 N*log2 (N)，其中 N = last–first。

**数据范围** 对范围【第一个，最后一个】中的对象进行修改。

**异常** 带有名为 ExecutionPolicy 的模板参数的重载如下报错:如果算法分配内存失败，std::bad_alloc 作为异常抛出。如果作为算法的一部分调用的函数的执行抛出异常 std::terminate。

继续这篇关于 C++中排序函数的文章

## **示例–按升序排列数据:**

```
#include <bits/stdc++.h> 
using namespace std;   
int main() 
{ 
int array[] = {10, 35, 85, 93, 62, 77, 345, 43, 2, 10}; 
int n = sizeof(array)/sizeof(array[0]); 
// 'sizeof' gives the size of total array i.e. size of each character * no. of characters
// so to get no. of characters
// we divide the sizeof(array) with the size of any one character of the array
// here it is array[0]
sort(array, array+n);   
cout << "nArray after sorting using "
"default sort is : n"; 
for (int i = 0; i < n; ++i) 
cout << array[i] << " ";   
return 0; 
} 

```

**输出:**

![Output- Sort Function in C++- Edureka](img/77e23aaa5fa10bfe2eff75e53c969879.png)

**说明**

从上面的例子中，我们看到 sort()函数默认情况下对数组进行升序排序。

继续这篇关于 C++中排序函数的文章

## **示例–按降序排列数据:**

为了对数组数据进行降序排序，我们需要引入第三个参数，该参数用于指定元素的排序顺序。我们可以使用“greater()”函数对数据进行降序排序。

```
#include <bits/stdc++.h> 
using namespace std;   
int main() 
{ 
int array[] = {41, 53, 4, 459, 60, 7, 23, 4, 232, 10}; 
int n = sizeof(array)/sizeof(array[0]); 
sort(array, array+n, greater<int>());   
cout << "Array after sorting : n"; 
for (int i = 0; i < n; ++i) 
cout << array[i] << " ";   
return 0; 
} 

```

**输出:**

![Output- Sort Function in C++- Edureka](img/9f22026c963d73fb177a8f48c1f99b93.png)

**Exp**l**anation**Here sort()函数以将较大元素放在前面的方式进行比较。

继续这篇关于 C++中排序函数的文章

## **部分 _ 排序**

C++ STL 为我们提供了一个部分排序函数，这个函数类似于 sort()函数，但不同于 sort()函数，它不是用来排序整个范围，而是用来排序它的一个子部分。它对[first，last 范围内的元素进行排序，中间元素之前的元素按升序排序，而中间元素之后的元素保持不变。

如果我们使用一个函数对象对第一个位置进行排序，它可以用来找到最大的元素

**例子**

```
#include <iostream> 
#include <algorithm> 
#include <vector> 
using namespace std; 
int main() 
{ 
vector<int> vec = { 10, 45, 60, 78, 23, 21, 30 };   
vector<int>::iterator iptr;   
partial_sort(vec.begin(), vec.begin() + 1, vec.end(), 
greater<int>()); 
iptr = vec.begin(); 
cout << "The largest element is = " << *iptr;   
return 0; 
} 

```

**输出:**

![Output- Sort Function in C++- Edureka](img/27a4d66f4eed672024fc92d5c36885e5.png)

**解释:** 上面的代码可以用来寻找一个数列中最大的数，要寻找数列中最小的数我们只需要去掉比较大的< int >命令。

至此，我们已经结束了这篇关于“C++中的排序函数”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA 培训与认证](https://www.edureka.co/java-j2ee-soa-training/)课程旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。