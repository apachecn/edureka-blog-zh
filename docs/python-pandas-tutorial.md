# Python 熊猫教程:学习熊猫进行数据分析

> 原文：<https://www.edureka.co/blog/python-pandas-tutorial/>

在这篇关于’**Python 熊猫教程** 的博客中，我们将使用 Python 中的 [熊猫](https://www.youtube.com/watch?v=UB3DE5Bgfx4) 库来深入研究 [数据分析](https://www.edureka.co/masters-program/data-analyst-certification) 。 [*Python 编程*](https://www.edureka.co/blog/python-tutorial/) 是一种超越其他更著名的编程语言如 Java、C++和 C#的技能。但是在我们谈论熊猫之前，让我们先来理解 NumPy 数组的概念。为什么？因为熊猫是建立在[NumPy](https://www.edureka.co/blog/python-numpy-tutorial/)之上的开源软件库。

在 这个 Python 熊猫教程中，我将带你浏览以下主题，这些主题将作为未来博客的基础:

*   [什么是熊猫？](#WhatIsPandas)
*   [熊猫行动](#PandasOperations)
    *   [切片数据帧](#Slicing)
    *   [合并&加入](#Merging&Joining)
    *   [串联](#Concatenation)
    *   [改变指数](#ChangeIndex)
    *   [改变列标题](#ChangeHeaders)
    *   [数据蒙格](#Munging)
*   [用例:分析青年失业数据](#Use-Case)

让我们开始吧。:-)

## **什么是蟒蛇熊猫？**

Pandas 是 Python 中的一个库，用于数据操作、数据分析和数据清理。Python Pandas 非常适合不同类型的数据，比如

*   具有不同类型列的表格数据
*   有序和无序时间序列数据
*   带有行&列标签的任意矩阵数据
*   未标记的数据
*   任何其他形式的观察或统计数据集

### **如何安装熊猫？**

要在 Python 中安装熊猫，你需要打开你的命令提示符(终端在 [Linux](https://www.youtube.com/watch?v=Wgi-OfbP2Gw) 或 macOS)并输入“ *pip 安装熊猫* ”(不要复制引号！)

或者，如果您的系统中安装了 Anaconda 发行版，您可以输入“conda install pandas”。安装完成后，您可以通过转至您喜欢的 IDE (Jupyter、PyCharm 等)来验证安装。)并通过键入“import pandas”在您的代码中导入库。如果它执行时没有任何错误，则安装成功。如果你面临一个问题，你可以参考这里的视频:

### Python 熊猫教程|熊猫图书馆–Python 编程| Python 教程| Edureka

[https://www.youtube.com/embed/UB3DE5Bgfx4?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent](https://www.youtube.com/embed/UB3DE5Bgfx4?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent)

继续我们的 Python 熊猫博客，让我们看看它的一些操作。

## **巨蟒熊猫运营**

使用 python 中的 Pandas，您可以对 NumPy 系列、数据帧、缺失数据的纠正、分组操作等执行多种操作。。下面列出了一些常见的数据操作:

![PandasOperations - Python Pandas Tutorial - Edureka](img/05dc9ed0ed8ccb87b7a557a8d0511e13.png)

现在，让我们逐一了解所有这些操作。

### **对数据帧进行切片**

在这里，你的第一个要求是能够访问数据框！如果您不知道什么是数据框，请不要担心。数据框只是一种二维数据结构，是熊猫对象最常见的变体之一。首先，让我们从创建数据框开始。

参考下面的代码实现数据帧

```
import pandas as pd

XYZ_web= {'Day':[1,2,3,4,5,6], "Visitors":[1000, 700,6000,1000,400,350], "Bounce_Rate":[20,20, 23,15,10,34]}

df= pd.DataFrame(XYZ_web)

print(df)

```

#### **:**

```
     Bounce_Rate Day Visitors
0     20          1   1000
1     20          2   700
2     23          3   6000
3     15          4   1000
4     10          5   400
5     34          6   350

```

上面的代码将把一个字典转换成一个 pandas 数据框，并在左边加上一个索引。现在，让我们从这个数据帧中截取一个特定的列。

参考下图更准确的理解:

```

print(df.head(2))

```

#### **输出:**

```
     Bounce_Rate Day Visitors
0      20         1   1000
1      20         2    700

```

同样，如果你想要最后两行数据，输入下面的命令:

```
print(df.tail(2))

```

**输出:**

```

  Bounce_Rate Day Visitors 
4      10      5    400
5      34      6    350

```

在我们的 Python 熊猫教程中，接下来是操作——合并和连接。

### **合并&加盟**

在合并时，可以将两个或多个数据帧合并成一个数据帧。您还可以决定并过滤您想要保持通用的列 。让我来告诉你如何实际地实施。首先我将创建三个数据帧，它们有一些键值对，然后将这些数据帧合并在一起。参考下面的代码:

```

   HPI   IND_GDP Int_Rate
0  80      50      2
1  90      45      1
2  70      45      2
3  60      67      3

```

#### **输出:**

```
import pandas as pd

df1= pd.DataFrame({ "HPI":[80,90,70,60],"Int_Rate":[2,1,2,3],"IND_GDP":[50,45,45,67]}, index=[2001, 2002,2003,2004])

df2=pd.DataFrame({ "HPI":[80,90,70,60],"Int_Rate":[2,1,2,3],"IND_GDP":[50,45,45,67]}, index=[2005, 2006,2007,2008])

merged= pd.merge(df1,df2)

print(merged)

```

正如你在上面看到的，两个数据帧已经合并成一个数据帧。现在，您还可以指定要成为公共列的列。例如，我希望“HPI”列是通用的，而对于其他所有内容，我希望有单独的列。所以，让我实际实现一下:

```
df1 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3], "IND_GDP":[50,45,45,67]}, index=[2001, 2002,2003,2004])

df2 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3],"IND_GDP":[50,45,45,67]}, index=[2005, 2006,2007,2008])

merged= pd.merge(df1,df2,on ="HPI")

print(merged)

```

#### **输出:**

```
      IND_GDP  Int_Rate  Low_Tier_HPI  Unemployment
2001     50      2         50.0            1.0
2002     45      1         NaN             NaN
2003     45      2         45.0            3.0
2004     67      3         67.0            5.0
2004     67      3         34.0            6.0

```

接下来，让我们在 Python 熊猫教程 中了解加入是如何工作的。 这是将两个不同索引的数据帧合并成一个结果数据帧的另一种便捷方法。 这个操作与我们之前看到的“合并”操作非常相似，唯一的区别是“”操作将对“ *索引* ”而不是“ *列* ”。同样，让我们通过演示来了解这一点。

```
df1 = pd.DataFrame({"Int_Rate":[2,1,2,3], "IND_GDP":[50,45,45,67]}, index=[2001, 2002,2003,2004])

df2 = pd.DataFrame({"Low_Tier_HPI":[50,45,67,34],"Unemployment":[1,3,5,6]}, index=[2001, 2003,2004,2004])

joined= df1.join(df2)
print(joined)

```

#### **输出:**

```

       IND_GDP  Int_Rate Low_Tier_HPI  Unemployment
2001     50       2         50.0           1.0
2002     45       1         NaN            NaN
2003     45       2         45.0           3.0
2004     67       3         67.0           5.0
2004     67       3         34.0           6.0

```

您可能已经注意到，在 2002 年(index)中,“low_tier_HPI”和“失业”列没有值，因此它打印了 NaN(不是数字)。在 2004 年晚些时候，这两个值都可用，函数精确地修改了数据帧

*你可以浏览一下 Python 熊猫教程的录音，我们的讲师已经用例子详细解释了这些主题，这将有助于你更好地理解这个概念。*

**Python 进行数据分析| Python 熊猫教程| Python 培训| Edureka**

[https://www.youtube.com/embed/B42n3Pc-N2A?rel=0&showinfo=0](https://www.youtube.com/embed/B42n3Pc-N2A?rel=0&showinfo=0)

继续我们的 Python 熊猫教程，让我们了解如何连接两个数据框。这种操作称为串联。

### **串联**

这个操作基本上是把数据帧粘在一起。您可以选择想要连接的尺寸。为此，只需使用“pd.concat”并传入要连接在一起的数据帧列表。考虑下面的例子。

```

df1 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3], "IND_GDP":[50,45,45,67]}, index=[2001, 2002,2003,2004])

df2 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3],"IND_GDP":[50,45,45,67]}, index=[2005, 2006,2007,2008])

concat= pd.concat([df1,df2])

print(concat)

```

#### **输出:**

```
       HPI  IND_GDP Int_Rate
2001    80    50       2
2002    90    45       1
2003    70    45       2
2004    60    67       3
2005    80    50       2
2006    90    45       1
2007    70    45       2
2008    60    67       3

```

正如你在上面看到的，这两个数据框被粘合在一个数据框中，索引从 2001 年一直到 2008 年。 接下来，你还可以指定一个参数:` *axis=1* `以便沿列进行联接、合并或串接。对此，可以参考下面的代码:

```
df1 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3], "IND_GDP":[50,45,45,67]}, index=[2001, 2002,2003,2004])

df2 = pd.DataFrame({"HPI":[80,90,70,60],"Int_Rate":[2,1,2,3],"IND_GDP":[50,45,45,67]}, index=[2005, 2006,2007,2008])

concat= pd.concat([df1,df2],axis=1)

print(concat)

```

**输出:**

```
       HPI  IND_GDP  Int_Rate HPI  IND_GDP Int_Rate
2001   80.0  50.0       2.0   NaN    NaN     NaN
2002   90.0  45.0       1.0   NaN    NaN     NaN
2003   70.0  45.0       2.0   NaN    NaN     NaN
2004   60.0  67.0       3.0   NaN    NaN     NaN
2005   NaN   NaN        NaN   80.0   50.0    2.0
2006   NaN   NaN        NaN   90.0   45.0    1.0
2007   NaN   NaN        NaN   70.0   45.0    2.0
2008   NaN   NaN        NaN   60.0   67.0    3.0

```

如果观察上面列出的的值，有一堆值是缺失的。发生这种情况的原因是，数据框没有包含您想要连接的所有索引的值。因此，在轴上进行联接或连接时，应该确保所有信息都正确排列。

### **改变索引**

接下来，在我们的 Python 熊猫教程中，我们将了解如何更改数据框中的索引值。例如，让我们用字典中的一些键值对创建一个数据帧，并更改索引值。考虑下面的例子:

让我们看看它实际上是如何发生的:

```
import pandas as pd

df= pd.DataFrame({"Day":[1,2,3,4], "Visitors":[200, 100,230,300], "Bounce_Rate":[20,45,60,10]}) 

df.set_index("Day", inplace= True)

print(df)

```

**输出:**

```
     Bounce_Rate  Visitors
Day 
1      20           200
2      45           100
3      60           230
4      10           300

```

正如您在上面的输出中所注意到的，索引值已经相对于“日”列进行了更改。

### **更改列标题**

我们现在来看看如何在 这个 Python 熊猫教程中改变列的标题。让我们举一个同样的例子，我将把列标题从“访问者”改为“用户”。所以，我来实际实现一下。

```
import pandas as pd

df = pd.DataFrame({"Day":[1,2,3,4], "Visitors":[200, 100,230,300], "Bounce_Rate":[20,45,60,10]})

df = df.rename(columns={"Visitors":"Users"})

print(df)

```

#### **输出:**

```
  Bounce_Rate  Day  Users
0    20         1    200
1    45         2    100
2    60         3    230
3    10         4    300

```

如上所示，列标题“访问者”已被更改为“用户”。接下来，在 python 熊猫教程中，让我们执行数据管理。

### **数据窗格**

在数据管理中，您可以将特定的数据转换成不同的格式。例如，如果您有一个. csv 文件，您可以将其转换为。你也可以把它转换成任何其他的数据格式。

```
import pandas as pd

country= pd.read_csv("D:UsersAayushiDownloadsworld-bank-youth-unemploymentAPI_ILO_country_YU.csv",index_col=0)

country.to_html('edu.html')

```

运行这段代码后，将会创建一个名为“edu.html”的 HTML 文件。您可以直接复制文件的路径并将其粘贴到浏览器中，浏览器会以 HTML 格式显示数据。参考下面截图:

![HTMLformat - Python Pandas Tutorial - Edureka](img/b1f9ca6866b54fb00e738389058a0a2f.png) 接下来在 python 熊猫教程中，我们来看一个关于全球青年失业的用例。

## **Python 熊猫教程:用案例分析青年失业数据**

**问题陈述** : 给你一个数据集包含了 2010 年到 2014 年全球失业青年的百分比。你必须使用这个数据集，找出从 2010 年到 2011 年每个国家的青年百分比的变化。

![](img/48dd2106cf07435640bab541b88f12bb.png)

首先，让我们了解包含国家名称、国家代码和 2010 年到 2014 年这几列的数据集。 现在用熊猫，我们来读一下。 *csv* 文件使用代码片段“*PD . read _ CSV*”。 参考下面截图:

![](img/0c01e2d084b4051bd8587df456ba840a.png)

让我们继续进行数据分析，我们将找出 2010 年至 2011 年间失业青年中的百分比差异。然后，我们将使用 [Matplotlib](https://www.edureka.co/blog/python-matplotlib-tutorial/#matplotlib) 库对其进行可视化，这是 Python 中一个强大的可视化库。它可以用于 Python 脚本、shell、web 应用服务器和其他 GUI 工具包。可以在这里使用 read more:[Matplotlib 教程。](https://www.edureka.co/blog/python-matplotlib-tutorial/)

现在，让我们在 PyCharm 中实现代码:

```
import pandas as pd

import matplotlib.pyplot as plt

from matplotlib import style

style.use('fivethirtyeight')

country= pd.read_csv("D:UsersAayushiDownloadsworld-bank-youth-unemploymentAPI_ILO_country_YU.csv",index_col=0)

df= country.head(5)

df= df.set_index(["Country Code"])

sd = sd.reindex(columns=['2010','2011'])

db= sd.diff(axis=1)

db.plot(kind="bar")

plt.show()

```

正如你在上面看到的，我已经对国家数据框的前 5 行进行了分析。接下来，我将一个索引值定义为“国家代码”，然后将该列重新索引为 2010 年和 2011 年。然后，我们还有一个数据框 DB，它打印了两列之间的差异或 2010 年到 2011 年之间失业青年的百分比变化。最后，我使用 Python 中的 Matplotlib 库绘制了一个条形图。

![BarGraph - Python Pandas Tutorial Edureka](img/06dedfbedd29a383cac800f5116f2ba0.png)

现在，如果你注意到上面的图表，在 2010 年到 2011 年间，阿富汗的失业青年增加了大约。0.25%.然后在安哥拉(AGO)，出现了一种消极趋势，这意味着失业青年的比例已经下降。 你可以自己动手实验数据。花几分钟时间，想出一些见解。让我们知道你在评论中发现了什么！

我希望我的博客“Python 熊猫教程”对你有用。 *要深入了解 python 及其各种应用，您可以注册 Edureka 提供的实时 [**Python 在线课程**](https://www.edureka.co/python-programming-certification-training) ，该课程提供全天候支持和终身访问。*

*有问题吗？请在这个“Python 熊猫教程”博客的评论部分提到它，我们会尽快回复你。*