# Python JSON 是什么，如何实现？

> 原文：<https://www.edureka.co/blog/python-json/>

你知道如何将你的数据从在线 API 中传输出来，或者将不同种类的数据存储到你的本地机器上吗？无论如何，你已经让自己沉浸在 JSON 中，JSON 代表着 [Java Script 对象符号。](https://www.edureka.co/blog/what-is-json)这是一种著名且流行的数据格式，用于表示半结构化数据。下面我们来详细了解一下 Python JSON。

本文将讨论以下几个方面:

## **Python 中的 JSON 简介:**

JSON 代表**J**ava**S**script**O**object**N**rotation是一种以有组织且简单的方式存储信息的方式。当在浏览器和服务器之间交换数据时，数据必须是文本形式的。

![JSON logo- Python JSON-Edureka](img/0ce94815f08845305b8ab6748f6ea0b8.png)

万一你想知道是不是 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) ？那么，答案是 ***号*** 它是一个由文本组成的脚本，用于以人类和机器可读的格式存储和传输数据。它是一种受 JavaScript 启发的小型轻量级数据格式，通常用于文本或字符串格式。一包 [JSON](https://www.edureka.co/blog/what-is-json) 几乎等同于一个 python 字典。现在，你一定在想；

## **如何用 Python 读取一个 JSON 文件？**

这个问题的答案是，您必须导入 JSON 模块，该模块通常将 Python 数据类型转换为 JSON 字符串文件。它由直接读写 JSON 文件的 JSON 函数组成。 [Python](https://www.edureka.co/blog/python-programming-language) 内置 JSON 包，是标准库的一部分，不用安装。

### **举例:**

```
 import json

```

现在您已经了解了 Python 中的 JSON，让我们更深入地了解一下解析。

## **解析:**

JSON 库可以从[字符串](https://www.edureka.co/blog/what-is-json#jsonfundamentals)或文件中解析 JSON。它还可以将 JSON 解析成 [Python 字典](https://www.edureka.co/blog/dictionary-in-python/)或 list，反之亦然。解析通常分两个阶段进行:

1.  从 JSON 到 Python 的转换
2.  从 Python 到 JSON 的转换

让我们更好地理解这两个阶段。

### **从 JSON 到 Python 的转换:**

您可以使用`json.loads().` 将 JSON 字符串转换成 Python。让我向您展示实际的实现:

#### **举例:**

```
import json
people_string = '''
{
"people":[
{
"emp_name": "John smith",
"emp_no.": "924367-567-23",
"emp_email": ["johnsmith@dummyemail.com"],
"has_license": "false"
},
{
"emp_name": "harshit kant",
"emp_number": "560-555-5153",
"emp_email": "null",
"has_license": "true"
}
]
}
'''
data = json.loads(people_string)
print(data)

```

#### **输出:**

![Output - Python JSON - Edureka](img/206075338e7477f0f39891068b36a754.png)

从上面的输出可以看出，它打印了一个 [Python 字典](https://www.edureka.co/blog/dictionary-in-python/)。为了更好地理解，让我们打印数据类型。

#### **举例:**

```
import json
people_string = '''
{
"people":[
{
"emp_name": "John smith",
"emp_no.": "924367-567-23",
"emp_email": ["johnsmith@dummyemail.com"],
"has_license": "false"
},
{
"emp_name": "harshit kant",
"emp_number": "560-555-5153",
"emp_email": "null",
"has_license": "true"
}
]
}
'''
data = json.loads(people_string)
print(type(data))  #prints the datatype

```

#### **输出:**

<class>现在，既然你已经熟悉了其中一种转换，让我们来看看第二阶段中的另一种转换类型。</class>

### **从 Python 到 JSON 的转换:**

使用`json.dumps().` 可以将 Python 对象转换成 JSON 字符串。让我们来看看下面的例子:

#### **举例:**

```
import json
people_string = '''
{
"people":[
{
"emp_name": "John smith",
"emp_no.": "924367-567-23",
"emp_email": ["johnsmith@dummyemail.com"],
"has_license": "false"
},
{
"emp_name": "harshit kant",
"emp_no.": "560-555-5153",
"emp_email": "null",
"has_license": "true"
}
]
}
'''
data = json.loads(people_string)
new_string = json.dumps(data)
print(new_string)
```

#### **输出:**

#### **![Python-to-JSON-Python JSON-Edureka](img/a45b185d3ca0a9a5322acce27c9dde09.png)**

输出将是 JSON 字符串类型。我已经演示了 JSON 到 Python 转换中的数据类型，打印数据类型将遵循相同的过程。

我们往前走，看看熊猫是怎么解析 JSON 的。

## **熊猫解析 JSON:**

JSON 字符串可以通过以下步骤解析成一个 [pandas](https://www.edureka.co/blog/python-pandas-tutorial/) Dataframe:

*   以下通用结构可用于将 JSON 字符串加载到 DataFrame 中。

```
import pandas as pd

pd.read_json(r'Path where you saved the JSON fileFile Name.json')
```

*   准备 JSON 字符串。
*   创建一个 JSON 文件，我们使用的是 nobel_prize.json。
*   将 JSON 文件加载到 pandas 数据框架中。

下面实现的代码将我的 JSON 文件加载到 DataFrame 中。

```
import pandas as pd
import json

with open(r'C:UsersHarshit_KantDesktopnobel.prize.json') as f:
   data = json.load(f)
print (data)

df = pd.DataFrame

print(df)
```

#### **输出:**

![Parse-Pandas-JSON-Python JSON-Edureka](img/d376dded502ced626757718a0338dbfd.png)

接下来，让我们看看如何用 Python 序列化 JSON。

## **JSON[Encode]的序列化:**

序列化 JSON 仅仅意味着你正在编码 JSON。它将给定的 Python 数据结构(例如:dict)转换成有效的 JSON 对象。为了处理文件中的数据流，Python 中的 JSON 库使用了一个 ***dump()*** 和 ***dumps()*** 方法来进行转换，并使数据写入文件变得容易。

下面给出了一个表格，说明了如何将 [Python](https://www.edureka.co/blog/variables-and-data-types-in-python/) [数据类型](https://www.edureka.co/blog/variables-and-data-types-in-python/)转换成它们各自的 JSON 类型。

| **Python** | **JSON** |
| **字典** | 目标 |
| **列表，数组** | 元组 |
| **字符串** | 线 |
| **int，long，float** | 数字 |
| **真** | 真实的 |
| **假** | 错误的 |
| **无** | 空 |

**要点记住:**

*dump()*–将数据转换为 JSON 文件*dumps()*–将数据转换为 JSON 字符串*load()*–将 JSON 文件转换为 Python 对象*loads()–*将 JSON 字符串的对象转换为 Python 对象

## **漂亮印刷:**

Pretty Printing 负责代码对齐，并使其成为人类可读的格式。让我们看看下面的例子，我传递了两个参数' sort_keys ',它总是返回一个布尔值和' indent '空格。

#### **举例:**

```
import json
people_string = '''
{
"people":[
{
  "emp_name": "John smith",
  "emp_no.": "924367-567-23",
  "emp_email": ["johnsmith@dummyemail.com"],
  "has_license": "false"
},
{
  "emp_name": "harshit kant",
  "emp_no.": "560-555-5153",
  "emp_email": "null",
  "has_license": "true"
}
]
}
'''

data = json.loads(people_string)
new_string = json.dumps(data, sort_keys=True, indent=3)
print(new_string)
```

**输出:**

继续学习 Python JSON 教程，让我们了解 JSON 的反序列化。

## **JSON[Decode]的反序列化:**

JSON 的反序列化与序列化正好相反，也就是说，它意味着你正在解码 JSON。它通过使用执行转换的 ***load()*** 和 ***loads()*** 方法，将给定的 JSON 字符串转换为 [Python](https://www.edureka.co/blog/python-class/#Objects) [对象](https://www.edureka.co/blog/python-class/#Objects)。

下面的表格说明了 JSON 数据类型到其各自 Python 类型的转换。

| **JSON** | **Python** |
| **物体** | 字典 |
| **元组** | 列表，数组 |
| **字符串** | 线 |
| **数字** | int，long，float |
| **真** | 真实的 |
| **假** | 错误的 |
| ** null** | 没有人 |

继续学习“Python JSON”教程。我将从编码的角度向您展示一个序列化和反序列化的实时示例。

## **编码演示:**

在这个代码演示中，我使用了一个名为“诺贝尔奖”的 JSON 数据集，这里给出了。您将学习如何通过 JSON 文件进行序列化和反序列化。

### **示例(JSON 数据集的序列化):**

```
import json

with open('nobel_prize.json.html') as f:
    data = json.load(f)

with open('new_nobel_prize.json.html') as f:
    json.dump(data,f,indent=2)
```

#### **输出:**

[Python 代码](https://www.edureka.co/blog/python-programming-language)编译成功，创建了一个新文件“new_nobel_prize.json ”,其中的数据是从一个已经存在的文件“nobel_prize.json”中转储的。

**![](img/1f2cbd19cc129add69a7a10e380d1b23.png)**

### **示例(JSON 数据集的反序列化):**

```
import json

with open('nobel_prize.json.html') as f:
data = json.load(f)

for nobel_prize in data['prizes']:
print(nobel_prize['year'],nobel_prize['category'])
```

#### **输出:**

代码片段展示了从 JSON 文件到其各自的 Python 对象的变化。

![Output - Python JSON - Edureka](img/3c2bbb436572097eb002031890c4ff5e.png)

这就把我们带到了文章“Python JSON”的结尾。我希望您清楚与 JSON、解析、序列化和反序列化相关的所有概念。

确保你尽可能多地练习，并恢复你的体验。

有问题吗？请在这篇 Python JSON 文章的评论部分提到它，我们会尽快回复您。要深入了解 Python 及其各种应用，您可以  ***[在这里注册](https://www.edureka.co/python)*** 参加我们的在线实时培训，24/7 全天候支持，终身访问。