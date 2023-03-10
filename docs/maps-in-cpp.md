# C++中的 map 是什么，如何实现？

> 原文：<https://www.edureka.co/blog/maps-in-cpp/>

以映射方式存储元素的关联容器被称为 ***映射*** 。map 中的所有元素都存储在一个键-值对中，其中每个键都是唯一的。排序是在键的帮助下完成的，并且值与每个键相关联。可以根据需要插入和删除值。

本文将涉及以下几点:

*   [什么是 C++中的映射](#Maps)
*   [地图中的功能](#mapfunctions)
*   [地图示例:如何实现地图？](#example)

让我们开始吧。

## **什么是 C++中的映射**

c++中的映射是关联容器，存储由 *键值* 和 *映射值组合而成的元素。*

**考虑这个例子:**

| 按键 ( 卷号) | 名称 |
| Sixteen billion thirty million one hundred and forty-one thousand and one | 阿卡什 |
| Sixteen billion thirty million one hundred and forty-one thousand and two | 尤夫拉杰 |
| Sixteen billion thirty million one hundred and forty-one thousand and three | 阿希什 |
| Sixteen billion thirty million one hundred and forty-one thousand and four | 阿伦 |

上面的例子显示了一个键和值对。编号是关键，每个学生都有不同的编号，因此唯一的关键代表他们。

**语法:** map < key_type，value _ type>map _ name；

这是在 C++中创建地图的基本语法。我们有一个 key_type 类型的键值和一个与 value_type 类型的键相关联的值。当我们输入值时，它们应该成对输入，不能一个一个输入。

继续讨论 C++ Maps，让我们看看 Maps 中的不同函数。

## **地图中的功能**

有许多与地图相关的功能。他们是，

*   开始()
*   结束()
*   大小()
*   max_size()
*   空()
*   输入()
*   删除()
*   插入()
*   清除()

下面是创建 C++地图的代码:

```
#include <iostream> 
#include <iterator> 
#include 

<map> 

using namespace std; 

int main() 
{ 
     map<int, int> marks; 
     marks.insert(pair<int, int>(160, 42)); 
     marks.insert(pair<int, int>(161, 30)); 
     marks.insert(pair<int, int>(162, 40)); 
     marks.insert(pair<int, int>(163, 50)); 
     marks.insert(pair<int, int>(164, 31)); 
     marks.insert(pair<int, int>(165, 12)); 
     marks.insert(pair<int, int>(166, 34)); 

     map<int, int>::iterator itr; 
     cout << "nThe map marks is : n"; 
     cout << "ROLL NO.tMarksn"; 
     for (itr =  marks.begin(); itr !=  marks.end(); ++itr) { 
        cout  << itr->first 
             << "t   t" << itr->second << 'n'; 
     } 
     cout << endl; 
     return 0;     
  }
```

## 输出:

![Output - Maps in C++ - Edureka](img/e71752d3832ff182adfec99b408dccb7.png)

## **说明:**

在上面的程序中，我们创建了一个地图。我们必须包含不同的头文件来创建地图。 我们接着创建地图容器。

```
map<int,int> marks;
```

这里我们创建一个名为 marks 的映射，键和值的类型为 int。容器在开始时是空的。 然后我们调用 insert 函数来插入键和值对。然后，我们为映射创建一个名为 iter 的迭代器。我们在 for 循环中使用它，直到遇到 map 中的最后一对。我们首先打印键，然后是值。

## **地图示例:如何实现地图**

还有许多其他功能，如擦除功能。代码如下:

```
#include <iostream> 
#include <iterator> 
#include 

<map> 
  using namespace std; 

int main() 
{ 
     map<int, int> marks; 
     marks.insert(pair<int, int>(160, 42)); 
     marks.insert(pair<int, int>(161, 30)); 
     marks.insert(pair<int, int>(162, 40)); 
     marks.insert(pair<int, int>(163, 50)); 
     marks.insert(pair<int, int>(164, 31)); 
     marks.insert(pair<int, int>(165, 12)); 
     marks.insert(pair<int, int>(166, 34)); 

     map<int, int>::iterator itr; 
     cout << "nThe map marks is : n"; 
     cout << "ROLL NO.tMarksn"; 
     for (itr =  marks.begin(); itr !=  marks.end(); ++itr) { 
        cout  << itr->first 
             << "t   t" << itr->second << 'n'; 
     } 
     cout << endl; 
         int num; 
    num = marks.erase(164); 
    cout << "nmarks.erase(164) : "; 
    cout << num << " removed n"; 
    cout << "tROLL NO. tMarksn"; 
    for (itr = marks.begin(); itr != marks.end(); ++itr) { 
        cout << 't' << itr->first 
             << 't' << itr->second << 'n'; 
    } 
     return 0;     
  }

```

我们唯一要做的就是调用 marks.erase(164)来删除以 164 为关键字或卷号的元素。代码的其余部分是相同的。

*同样，我们可以用地图* 提供的所有其他功能来做到这一点。

这样，我们就结束了这篇关于“C++中的映射”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在“C++中的地图”博客的评论部分提到它，我们会尽快回复您。