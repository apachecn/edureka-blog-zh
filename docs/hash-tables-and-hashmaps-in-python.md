# Python 中的哈希表和哈希表:它们是什么，如何实现？

> 原文：<https://www.edureka.co/blog/hash-tables-and-hashmaps-in-python/>

数据需要多种存储和访问方式。最重要的实现之一包括哈希表。在 [Python](https://www.edureka.co/blog/python-basics/) 中，这些哈希表是通过内置的[数据类型](https://www.edureka.co/blog/python-data-types/)即[字典](https://www.edureka.co/blog/dictionary-in-python/)实现的。在本文中，您将学习什么是 Python 中的哈希表和哈希表，以及如何使用字典实现它们。

在继续之前，让我们看一下所有的讨论主题:

*   [Python 中什么是哈希表或者哈希表？](#whatishashtable)
*   [散列表 vs 散列表](#hashtablevshashmap)
*   [创建字典](#creatingdictionaries)
*   [创建嵌套字典](#creatingnesteddictionaries)
*   [使用字典对哈希表执行操作](#operations)
    *   [取值](#accessing)
    *   [更新数值](#updating)
    *   [删除项目](#deleting)
*   [将字典转换成数据帧](#converting)

## **Python 中什么是哈希表或者哈希表？**

在计算机科学中，哈希表或哈希表是一种类型的[数据结构](https://www.edureka.co/blog/data-structures-in-python/)，它将键映射到它的值对(实现抽象数组数据类型)。它基本上利用了一个[函数](https://www.edureka.co/blog/python-functions)，该函数计算一个索引值，该索引值依次保存要搜索、插入、删除等的元素。这使得访问数据变得简单而快速。通常，哈希表存储键值对，并且使用哈希函数生成密钥。

Python 中的哈希表或哈希映射是通过内置的字典数据类型实现的。Python 中字典的键是由哈希函数生成的。一个[字典](https://www.edureka.co/blog/dictionary-in-python/)的元素没有排序，它们可以被改变。

字典的一个例子可以是雇员姓名和他们的雇员 id 的映射，或者是学生姓名和他们的学生 id 的映射。

接下来，让我们看看 Python 中哈希表和 hashmap 的区别。

## **哈希表 vs hashmap:Python 中哈希表和 Hashmap 的区别**

| 散列表 | 散列表 |
| 同步的 | 非同步 |
| 快的 | 慢的 |
| 允许一个空键和多个空值 | 不允许空键或空值 |

## **创建词典:**

可以通过两种方式创建词典:

*   使用花括号({})
*   使用 *dict()* 函数

### **使用花括号:**

Python 中的字典可以使用花括号创建，如下所示:

**举例:**

```
my_dict={'Dave' : '001' , 'Ava': '002' , 'Joe': '003'}
print(my_dict)
type(my_dict)
```

**输出:**

{ '戴夫':' 001 '，'艾娃':' 002 '，'乔':' 003'} 字典

### **使用 *dict()* 函数:**

Python 有一个内置函数， *dict()* 可以用来在 Python 中创建[字典](https://www.edureka.co/blog/sort-dictionary-by-value-in-python/)。例如:

**举例:**

```
new_dict=dict()
print(new_dict)
type(new_dict)
```

**输出:**

{} 字典

在上面的例子中，创建了一个空字典，因为没有键值对作为参数提供给 dict()函数。如果您想要添加值，您可以执行以下操作:

**举例:**

```
new_dict=dict(Dave = '001' , Ava= '002' , Joe= '003')
print(new_dict)
type(new_dict)
```

**输出:**

{ '戴夫':' 001 '，'艾娃':' 002 '，'乔':' 003'} 字典

## **创建嵌套字典:**

嵌套字典基本上是位于其他字典中的字典。例如:

**举例:**

```
emp_details = {'Employee': {'Dave': {'ID': '001',
                                     'Salary': 2000,
                                     'Designation':'Python Developer'},
                            'Ava': {'ID':'002',
                                    'Salary': 2300,
                                    'Designation': 'Java Developer'},
                            'Joe': {'ID': '003',
                                    'Salary': 1843,
                                    'Designation': 'Hadoop Developer'}}}
```

## **使用字典对哈希表执行操作:**

在 Python 中，可以通过字典对散列表执行许多操作，例如:

*   访问值
*   更新值
*   删除元素

### **取值:**

可以通过多种方式访问字典的值，例如:

*   使用键值
*   使用[功能](https://www.edureka.co/blog/python-functions)
*   执行循环的

#### **使用键值:**

可以使用如下键值来访问字典值:

**举例:**

```
my_dict={'Dave' : '001' , 'Ava': '002' , 'Joe': '003'}
my_dict['Dave']
```

**输出:'** 001 '

#### **使用功能:**

有许多可以使用的内置函数，如 get()、keys()、values()等。

**举例:**

```
my_dict={'Dave' : '001' , 'Ava': '002' , 'Joe': '003'}
print(my_dict.keys())
print(my_dict.values())
print(my_dict.get('Dave'))
```

**输出:**

字典值(['戴夫'，'艾娃'，'乔']) 字典值(['001 '，' 002 '，' 003']) 001

**了解我们在顶级城市/国家的 Python 培训**

| **印度** | **美国** | **其他城市/国家** |
| [班加罗尔](https://www.edureka.co/python-programming-certification-training-bangalore) | [纽约](https://www.edureka.co/python-programming-certification-training-new-york-city) | [英国](https://www.edureka.co/python-programming-certification-training-uk) |
| [海德拉巴](https://www.edureka.co/python-programming-certification-training-hyderabad) | [芝加哥](https://www.edureka.co/python-programming-certification-training-chicago) | 伦敦 |
| [德里](https://www.edureka.co/python-programming-certification-training-delhi) | 亚特兰大 | [加拿大](https://www.edureka.co/python-programming-certification-training-canada) |
| [钦奈](https://www.edureka.co/python-programming-certification-training-chennai) | [休斯顿](https://www.edureka.co/python-programming-certification-training-houston) | [多伦多](https://www.edureka.co/python-programming-certification-training-toronto) |
| [孟买](https://www.edureka.co/python-programming-certification-training-mumbai) | 洛杉矶 | [澳大利亚](https://www.edureka.co/python-programming-certification-training-australia) |
| [浦那](https://www.edureka.co/python-programming-certification-training-pune) | [波士顿](https://www.edureka.co/python-programming-certification-training-boston) | 阿联酋 |
| 加尔各答 | [迈阿密](https://www.edureka.co/python-programming-certification-training-miami) | [迪拜](https://www.edureka.co/python-programming-certification-training-dubai) |
| 艾哈迈达巴德 | [旧金山](https://www.edureka.co/python-programming-certification-training-san-francisco) | [菲律宾](https://www.edureka.co/python-programming-certification-training-philippines) |

#### **实现 for 循环:**

for 循环允许您通过迭代轻松地访问字典的键值对。例如:

```
my_dict={'Dave' : '001' , 'Ava': '002' , 'Joe': '003'}
print("All keys")
for x in my_dict:
    print(x)       #prints the keys
print("All values")
for x in my_dict.values():
    print(x)       #prints values
print("All keys and values")
for x,y in my_dict.items():
    print(x, ":" , y)       #prints keys and values
```

**输出:**

所有键戴夫艾娃乔所有值 001 002 003 所有键和值戴夫:001 艾娃:002 乔:003

### **更新值:**

字典是可变的数据类型，因此你可以在需要的时候更新它们。例如，如果我想将名为 Dave 的雇员的 ID 从“001”更改为“004 ”,并且如果我想将另一个键-值对添加到我的字典中，我可以执行以下操作:

**举例:**

```
my_dict={'Dave' : '001' , 'Ava': '002' , 'Joe': '003'}
my_dict['Dave'] = '004'   #Updating the value of Dave
my_dict['Chris'] = '005'  #adding a key-value pair
print(my_dict)
```

**输出:** { '戴夫':' 004 '，'艾娃':' 002 '，'乔':' 003 '，'克里斯':' 005'}

### **从字典中删除条目:**

有很多函数可以让你从字典中删除条目，比如 *del()、pop()、popitem()、clear()、*等等。例如:

**举例:**

```
my_dict={'Dave': '004', 'Ava': '002', 'Joe': '003', 'Chris': '005'}
del my_dict['Dave']  #removes key-value pair of 'Dave'
my_dict.pop('Ava')   #removes the value of 'Ava'
my_dict.popitem()    #removes the last inserted item
print(my_dict)
```

**输出:** { '乔':' 003'}

上面的输出显示，除了' Joe: 003 '之外的所有元素都已经使用各种函数从字典中删除了。

## **将字典转换成数据帧:**

正如您之前看到的，我已经创建了一个嵌套字典，其中包含员工姓名和映射到它的详细信息。现在为了制作一个清晰的表格，我将使用 [pandas 库](https://www.edureka.co/blog/python-pandas-tutorial/)来把所有的东西作为一个数据帧。

**举例:**

```
import pandas as pd
emp_details = {'Employee': {'Dave': {'ID': '001',
                                     'Salary': 2000,
                                     'Designation':'Python Developer'},
                            'Ava': {'ID':'002',
                                    'Salary': 2300,
                                    'Designation': 'Java Developer'},
                            'Joe': {'ID': '003',
                                    'Salary': 1843,
                                    'Designation': 'Hadoop Developer'}}}
df=pd.DataFrame(emp_details['Employee'])
print(df)
```

**输出:**

![dataframe-Hash tables and hashmaps in Python-Edureka](img/e219f6921e3e47ca5213d8dfc5caee15.png)

我希望你清楚本教程中与你分享的所有内容。这就把我们带到了关于 Python 中哈希表和哈希表的文章的结尾。 ***确保你尽可能多的练习，恢复你的经验。***

*有问题吗？请在这个“Python 中的散列表和散列表”博客的评论部分提到它，我们会尽快回复你或者加入 [Python 大师课程](https://www.edureka.co/masters-program/python-developer-training)。*

*要深入了解 Python 及其各种应用，您可以注册参加实时 [**Python 在线培训**](https://www.edureka.co/python-programming-certification-training) ，该培训提供全天候支持和终身访问。*