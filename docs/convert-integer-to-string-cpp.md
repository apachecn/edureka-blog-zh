# C++中如何把整数转换成字符串？

> 原文：<https://www.edureka.co/blog/convert-integer-to-string-cpp/>

有时候，[在编写](https://www.edureka.co/blog/c-data-structures)的时候，我们会遇到一个问题，我们需要将一个变量从整数转换成字符串。在这篇文章中，我们将学习如何在 C++中将整数转换成字符串。本文将讨论以下几点:

*   使用字符串流
*   使用字符串函数
*   使用增强词汇转换

所以让我们从这篇文章开始吧

## **在 C++中将整数转换成字符串**

## **使用字符串流**

第一种方法是使用字符串流，即输入或输出字符串流。

#### **在 C++中将整数转换为字符串:示例**代码

```
#include<iostream>
#include <sstream>
#include <string>
using namespace std;
int main()
{
int num;
cout<<"Enter the number:&nbsp; "<<endl;
cin>>num;
ostringstream strg;
strg<< num;
string s1 = strg.str();
cout <<endl<< "The newly formed string from number is : ";
cout << s1 << endl;
return 0;
}

```

**输出**

**![Output - Convert Integer To String - Edureka](img/437e4737161e3592eb16c5e740f75e07.png)**

**解释**

在上面的程序中，我们从用户那里获取一个整数输入，并将其转换为字符串。我们通过使用字符串流方法来做到这一点。我们有两个头文件，一个用于字符串，另一个用于字符串输入/输出流。我们声明了两个变量。第一个是 int 类型的。它用于保存用户输入的数字。

我们创建一个输出字符串流类的变量，并创建一个变量 str。然后，我们将 num 中存储的数字传递给输出流。然后我们调用 str()函数将数字转换成字符串并打印出来。

让我们转到本文的下一个主题“在 C++中将整数转换为字符串”

## **使用串函数**

下一个方法是使用字符串函数 to_string。使用 to_string 可以将任何数据类型转换为字符串。

#### **样本代码**

```
#include<iostream>
#include<string>
using namespace std;
int main()
{
int intVal;
cout << "Enter a Integer : "<<endl;
cin>>intVal;
string str = to_string(intVal);
cout << "The integer in string is : ";
cout << str << endl;
return 0;
}

```

**输出**

**![Output - Convert Integer To String - Edureka](img/1796e3757ad949cec6eb380eafee2c0a.png)**

**解释**

在上面的程序中，我们从用户那里获取一个整数输入，并将其转换为字符串。我们通过使用 to_string 函数来实现这一点。我们包含了一个头文件，它是用于字符串和 to_string 函数的。

我们接受来自用户的值，并将其存储在 intVal 中。然后，我们创建一个字符串变量 str，并在传递 intVal 时将 to_string()函数的值赋值。

然后我们打印 str，整数被转换成一个字符串。

让我们转到本文的下一个主题“在 C++中将整数转换为字符串”

## **使用 Boost 词法强制转换**

*助推。LexicalCast* 可以将一个数字从字符串转换成数字，反之亦然。它存在于“boost/lexical_cast.hpp”库中。这里，我们将使用 Boost.LexicalCast 将数字转换为字符串。

**样本代码**

```
#include<iostream>
#include <boost/lexical_cast.hpp>
#include <string>
using namespace std;
int main()
{
int m = 9487;
string str = boost::lexical_cast<string>(m);
cout << "The string value is : ";
cout << str << endl;
return 0;
}

```

**输出**

字符串值是:9487

**解释**

在上面的程序中，我们从用户那里获取一个整数输入，并将其转换为字符串。我们通过使用 Boost.LexicalCast 来做到这一点。我们包含了两个头文件，一个用于字符串，另一个用于 Boost.LexicalCast。

我们给 m 赋值 9487。我们创建字符串变量 str，并赋予从 Boost 得到的值。词汇成本。转换过程在这里进行。然后我们打印输出。

这样，我们就结束了这篇关于“在 C++中将整数转换成字符串”的文章。如果你想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。