# 关于 C++中的字符串，你需要知道的一切

> 原文：<https://www.edureka.co/blog/strings-in-c/>

术语[字符串](https://www.edureka.co/blog/java-string/)表示有序的字符序列。在 C++中，可以使用类的对象来表示字符序列。提供这种定义的类称为字符串类。String 类将字符存储为字节序列，具有允许访问单字节字符的功能。在 C++中，封闭分隔符是双引号。在这篇“C++中的字符串”文章中，我将讨论以下主题:

*   [字符串类和字符数组的区别](#difference)
*   [在 C++ 中声明并初始化一个字符串](#declare)
*   [c++中对字符串的操作](#operations)
    *   字符串大小
    *   字符串串联
    *   追加字符串
    *   搜索字符串

## **字符串类和字符数组差异**

| **字符串类** | **字符数组** |
| 字符串类是一个定义了可以用字符流表示的对象的类 | 字符数组只是一个字符数组。 |
| 对于字符串，内存是动态分配的，因此在运行时可以按需分配更多的内存 | 字符数组的大小必须静态分配，因此如果需要，在运行时不能分配更多的内存 |
| String 类定义了许多允许对字符串进行多种操作的功能。 | 字符数组没有提供很多操作字符串的内置函数 |
| 与实现相比，字符串比字符数组慢。 | 字符数组的实现速度更快。 |

## **在 C++中声明并初始化一个字符串**

C++中字符串的初始化非常简单！。我们可以使用下列任何一种方法。

```
using namespace std;
string std_string;
```

或者

```
std::string std_string;
```

```
#include <iostream>

using namespace std;
int main () {

   char ch[12] = {'H', 'e', 'l', 'l', 'o', ' ', 'b', 'y',' ', 'c', 'h', ''};

   string st = "Hello by st";
   std::string std_st = "Hello by std_st";

   cout << ch << endl;
   cout << st << endl;
   cout << std_st << endl;

   return 0;
}
```

**输出:**

```
Hello by ch
Hello by st
Hello by std_st
```

在这个例子中，我们展示了字符数组(ch)和字符串 cl ass (st 和 std_st)的初始化方法。首先，我们使用字符数组方法，定义一个字符数组 ch[12]，它包含 12 个元素，以一个空字符结束。在第二部分中，我们使用了一个字符串类方法。

## **c++中对字符串的操作**

使用 string 类的好处是 C++中有几个内置函数可以操纵它们。这使得编程变得简单而有效。让我们开始学习一些重要的字符串操作函数，并通过一些例子来理解它们。

**字符串大小:**Size()和 length()方法都可以用来返回对象的大小。

```
cout << st.length() <<endl;
cout << st.size() <<endl;
```

**输出:**

```
11
11
```

**字符串连接:**我们可以简单地使用+运算符连接两个或更多的字符串

```
string new_string = st + " and " + std_st;
cout << new_string <<endl;
```

**输出:**

```
Hello by st and Hello by std_st
```

追加字符串:。append(string)类成员函数可用于在字符串中的特定字符位置连接和追加字符串。如果一个程序员放入 str.append(str1，p，n)，那么这意味着字符串 str1 中从位置 p 开始的 n 个字符将被追加到 str 的末尾。

```
string str = "I enjoy learning ";
string str1 = "Python, C++, or C";

str.append(str1, 8, 3);
cout << str << endl;
```

**输出:**

```
I enjoy learning C++
```

**搜索字符串:**我们可以使用 find()成员函数来查找一个字符串在另一个字符串中的第一次出现。find()将从位置 pos 开始在字符串 haystack 中查找字符串针，并返回该针第一次出现的位置。函数 rfind()的工作方式类似，只是它返回最后一次出现的传递的字符串。

```
string haystack = "Hello World!";
string needle = "o";
cout << haystack.find(needle)<<endl;
cout << haystack.find(needle, 4)<<endl;
cout << haystack.find(needle, 5)<<endl;
cout << haystack.find(needle, 8)<<endl;
```

**输出:**

```
4
4
7
4294967295
```

第一个 cout 命令将简单地打印“4 ”,这是“o”在干草堆字符串中第一次出现的索引。如果我们想要“世界”中的“o ”,我们需要修改“pos ”,使其指向第一次出现之后。haystack.find(needle，4)将再次返回 4，而 haystack.find(needle，5)将给出 7。如果没有找到子串，find()返回 std::string::npos。

Npos 是一个特殊值，等于 size_type 类型可表示的最大值。这里是 4294967295。通常，它或者被期望字符串索引的函数用作字符串结束指示符，或者被返回字符串索引的函数用作错误指示符。

这个简单的代码在字符串中搜索 str2 中所有出现的“C++ ”,并输出它们的位置:

```
string str2= "C++ is an object-oriented programming language and includes classes, inheritance, polymorphism, data abstraction and encapsulation.C++ allows exception handling, and function overloading which are not possible in C.C++ is a powerful, efficient and fast language.";

for(string::size_type i = 0, tfind; (tfind = wikistr.find("C++", i)) != string::npos; i = tfind + 1)
{
 std::cout << "Found occurrence of 'C++' at position " << tfind << std::endl;
}
```

**输出:**

```
Found occurrence of 'C++' at position 0
Found occurrence of 'C++' at position 132
Found occurrence of 'C++' at position 217
```

```
#include<iostream> 
using namespace std; 

class base 
{ 
public: 
    void fun_1() { cout << "base class function 1n"; } 
    virtual void fun_2() { cout << "base class function 2n"; } 
    virtual void fun_3() { cout << "base class function 3n"; } 
    virtual void fun_4() { cout << "base class function 4n"; } 
}; 

class derived : public base 
{ 
public: 
    void fun_1() { cout << "derived class function 1n"; } 
    void fun_2() { cout << "derived class function 2n"; } 
    void fun_4(int x) { cout << "derived class function 4n"; } }; int main() { base *ptr; derived obj1; ptr = &obj1; // Early binding because fun1() is non-virtual // in base ptr->fun_1(); 

    // Late binding (RTP) 
    ptr->fun_2(); 

    // Late binding (RTP) 
    ptr->fun_3(); 

    // Late binding (RTP) 
    ptr->fun_4(); 

    // Early binding but this function call is 
    // illegal(produces error) because pointer 
    // is of base type and function is of 
    // derived class 
    //p->fun_4(5); 
}
```

**输出:**

```
base class function 1
derived class function 2
base class function 3
base class function 4
```

至此，我们结束了这篇关于 C++中字符串的文章。我希望您已经了解了可以在其上执行的各种操作。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA](https://www.edureka.co/java-j2ee-soa-training) 培训和认证课程旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。