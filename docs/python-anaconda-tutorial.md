# 蟒蛇教程:您需要知道的一切

> 原文：<https://www.edureka.co/blog/python-anaconda-tutorial/>

Anaconda 是面向未来数据科学家、IT 专业人员和商业领袖的数据科学平台。是 [Python](https://www.edureka.co/blog/introduction-to-python/) 、 [R](https://www.edureka.co/blog/r-programming-language) 等的分布。拥有 300 多个用于[数据科学](https://www.edureka.co/blog/learn-python-for-data-science/)的软件包，它成为任何项目的最佳平台之一。在这篇 python anaconda 教程中，我们将讨论如何使用 anaconda 进行 python 编程。以下是本博客讨论的主题:

*   [蟒蛇简介](#introduction)
*   [安装和设置](#installation)
*   [如何在 Anaconda 中安装 Python 库？](#libraries)
*   [蟒蛇领航员](#navigator)
*   [用例](#usecase)
    *   [Python 基础知识](#fundamentals)
    *   [分析](#analytics)
    *   [机器学习和 AI](#ml/ai)

## **蟒蛇简介**

Anaconda 是 python 和 r 的开源发行版，用于[数据科学](https://www.edureka.co/blog/how-to-learn-data-science/)、[机器学习](https://www.edureka.co/blog/introduction-to-machine-learning/)、[深度学习](https://www.edureka.co/blog/deep-learning-with-python/)等。有了 300 多个用于数据科学的库，对于任何程序员来说，使用 anaconda 进行数据科学研究都是相当理想的。

![logo-python anaconda tutorial-edureka](img/c6b4b1e88121fec533ea3667c7a0aa7a.png)

Anaconda 有助于简化包管理和部署。Anaconda 附带了各种各样的工具，可以使用各种机器学习和人工智能算法轻松地从各种来源收集数据。它有助于获得一个易于管理的环境设置，只需单击一个按钮就可以部署任何项目。

现在我们知道了 anaconda 是什么，让我们试着理解如何安装 anaconda 并建立一个在我们的系统上工作的环境。

## **安装和设置**

要安装 anaconda，请前往 https://www.anaconda.com/distribution/。

![anaconda home-python anaconda tutorial-edureka](img/d3e832ad63578e28918894837762724d.png)

选择一个适合你的版本，点击下载。完成下载后，打开设置。

![setup-python anaconda tutorial - edureka](img/8f92447763942c09e582c0d0a3032835.png)

按照设置中的说明进行操作。不要忘记点击 add anaconda 到我的 path 环境变量。安装完成后，您将看到一个如下图所示的窗口。

![setup-python anaconda tutorial-edureka](img/b76fbf3af924d46f94f1f984d4aa9da0.png)

安装完成后，打开 anaconda 提示符，输入 [jupyter notebook](https://www.edureka.co/blog/cheatsheets/Jupyter-Notebook-Cheat-Sheet) 。

![anaconda prompt - python anaconda tutorial-edureka](img/ea97960ca95c21ab780ba98b349e4c0d.png)

您将看到一个如下图所示的窗口。

![](img/2e62aa48ee5846ea786225038506c451.png)

现在我们已经知道了如何为 python 使用 anaconda，让我们看看如何在 anaconda 中为任何项目安装各种库。

## **如何在 Anaconda 中安装 Python 库？**

打开 anaconda 提示符并检查库是否已经安装。

![](img/6943ecced46c254f47c972e628ec0392.png)

由于没有名为 numpy 的模块，我们将运行以下命令来安装 numpy。

![](img/dd3aebefaf50a21aa9511a06d8693fec.png)

完成安装后，您将看到如图所示的窗口。

![](img/619fb73d6aac2ba45e036b6fb72af9ea.png)

一旦你安装了一个库，只需再次尝试导入模块以确保安全。

![](img/374919af3470a5b22c0909b7ce2d0bcc.png)

如您所见，我们在开始时没有遇到任何错误，所以这就是我们如何在 anaconda 中安装各种库。

## **巨蟒领航员**

![](img/e1d91f186104729f39a19ddefac569bc.png)

Anaconda Navigator 是 Anaconda 发行版附带的一个桌面 GUI。它允许我们在不使用命令行命令的情况下启动应用程序和管理 conda 包、环境。

## **用例——Python 基础**

![](img/1a3b48dee0f7333391adf0d866fdc1fe.png)

### **变量和数据类型**

[变量和数据类型](https://www.edureka.co/blog/variables-and-data-types-in-python/)是任何编程语言的构建模块。Python 有 6 种数据类型，具体取决于它们拥有的属性。列表、字典、集合、元组，是 python 编程语言中的集合数据类型。

下面的示例展示了如何在 python 中使用变量和数据类型。

```
#variable declaration
name = "Edureka"
f = 1991
print("python was founded in"  , f)
#data types
a = [1,2,3,4,5,6,7]
b = {1 : 'edureka' , 2: 'python'}
c = (1,2,3,4,5)
d = {1,2,3,4,5}
print("the list is" , a)
print("the dictionary is" , b)
print("the tuple is" , c)
print("the set is " , d)

```

### **操作员**

[Python 中的运算符](https://www.edureka.co/blog/operators-in-python/)用于值或变量之间的运算。python 中有 7 种类型的运算符。

*   赋值运算符
*   算术运算符
*   逻辑算子
*   比较运算符
*   逐位运算符
*   隶属算子
*   恒等运算符

下面是一个在 python 中使用一些运算符的示例。

```
a = 10
b = 15
#arithmetic operator
print(a + b)
print(a - b)
print(a * b)
#assignment operator
a += 10
print(a)
#comparison operator
#a != 10
#b == a
#logical operator
a > b and a > 10
#this will return true if both the statements are true. 

```

### **控制语句**

像 [if，否则](https://www.edureka.co/blog/if-else-in-python/)、break、continue 这样的语句被用作控制语句来控制执行，以获得最佳结果。我们可以在 python 的不同循环中使用这些语句来控制结果。下面是一个演示如何使用控件和条件语句的示例。

```
name = 'edureka'
for i in name:
     if i == 'a':
         break
     else:
         print(i)

```

### **功能**

[Python 函数](https://www.edureka.co/blog/python-functions)以一种高效的方式提供了代码的可重用性，我们可以为一个问题语句编写逻辑，并运行一些参数来获得最优的解决方案。下面是我们如何在 python 中使用函数的一个例子。

```
def func(a):
      return a ** a
res = func(10)
print(res)

```

### **类和对象**

由于 python 支持面向对象的编程，我们也可以使用[类和对象](https://www.edureka.co/blog/python-class/)。下面是一个我们如何在 python 中使用类和对象的例子。

```
class Parent:
      def func(self):
            print('this is parent')

class Child(Parent):
      def func1(self):
           print('this is child')

ob = new Child()
ob.func()

```

这些是 python 中的一些基本概念。现在讨论 anaconda 中更大的包支持，我们可以使用很多库。让我们看看如何使用 python anaconda 进行数据分析。

## **用例分析**

![](img/548ac6eec3121921b902c5bce15fc519.png)

这些是[数据分析](https://www.edureka.co/blog/what-is-data-analytics/)中涉及的某些步骤。让我们看看 anaconda 中的数据分析是如何工作的，以及我们可以使用的各种库。

### **收集数据**

[收集数据](https://www.edureka.co/blog/python-pandas-tutorial/)就像在程序中加载一个 CSV 文件一样简单。然后，我们可以利用相关数据来分析数据中的特定实例或条目。下面是在程序中加载 CSV 数据的代码。

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df  = pd.read_csv('filename.csv')
print(df.head(5))

```

### **![](img/7cd93cf3a5dff034f417ee87eddb0768.png)**

### **切片和切块**

在我们将数据集加载到程序中之后，我们必须对数据进行一些修改，例如删除空值和不必要的字段，这些可能会导致分析中的歧义。

下面是一个我们如何根据需求过滤数据的例子。

```
print(df.isnull().sum())
#this will give the sum of all the null values in the dataset.
df1 = df.dropna(axis=0 , how= 'any')
#this will drop rows with null values.

```

![](img/ba7ab21d5070a520d346f6351d7c014c.png)

我们也可以删除空值。

**![](img/aef421779b8c3ab716780a111defdbaf.png)**

**箱式打印**

```
sns.boxplot(x=df['Salary Range From'])
sns.boxplot(x=df['Salary Range To'])

```

**![](img/6a6aef78c8abdfcc5a9e2087f6a83e17.png)**

**![](img/d3d1963509cc8e4a54199477db74df3e.png)**

**散点图**

```
import matplotlib.pyplot as plt
fig, ax = plt.subplots(figsize=(16,8))
ax.scatter(df['Salary Range From'] , df['Salary Range To'])
ax.set_xlabel('Salary Range From')
ax.set_ylabel('Salary Range TO')
plt.show()

```

**![](img/29d9065a2f0f7c7a1a89902549686c1a.png)**

### **可视化**

一旦我们根据需求更改了数据，就有必要对这些数据进行分析。这样做的一种方法是将结果可视化。更好的[可视化表示](https://www.edureka.co/blog/python-matplotlib-tutorial/)有助于数据投影的优化分析。

下面是一个可视化数据的示例。

```
sns.countplot(x= "Full-Time/Part-Time indicator" , data= df)
sns.countplot(x="Full-Time/Part-Time indicator" , hue="Salary Frequency" , data= df)
sns.countplot(hue="Full-Time/Part-Time indicator", x="Posting Type" ,data= df)
df["Salary Range From"].plot.hist()
df["Salary Range To"].plot.hist()

```

### **![](img/e03bb3c0f60f0384e84305f488d7efc8.png)**

### **![countplot-python anaconda tutorial-edureka](img/92dc51dda98f686729372e9d684f540e.png)**

### **![countplot-python anaconda tutorial-edureka](img/2cc75ef13b81726ea23beca442592c5e.png)**

### **![histogram-python anaconda tutorial-edureka](img/3d570ccdca33a637d9a157b3276c551b.png)**

### **![histogram-python anaconda tutorial -edureka](img/f3f8b89263437eced0760070546b5cf4.png)**

```
import matplotlib.pyplot as plt
fig = plt.figure(figsize = (10,10))
ax = fig.gca()
sns.heatmap(df1.corr(), annot=True, fmt=".2f")
plt.title("Correlation",fontsize=5)
plt.show()

```

![heatmap - python anaconda tutorial - edureka](img/109cf963b868226bf75411f79cdeefac.png)

### **分析**

可视化之后，我们可以通过各种图表进行分析。假设我们正在处理工作数据，通过查看一个区域中特定工作的可视化表示，我们可以得出特定领域中的工作数量。

根据以上分析，我们可以假设以下结果

*   与全职工作相比，数据集中兼职工作的数量非常少。
*   兼职工作不到 500 份，全职工作超过 2500 份。
*   基于这个分析，我们可以建立一个[预测模型。](https://www.edureka.co/blog/logistic-regression-in-python/)

在这篇 python anaconda 教程中，我们已经了解了如何使用涵盖 python 基础、数据分析和机器学习的用例为 python 设置 anaconda。anaconda 拥有 300 多个数据科学包，提供了最佳的支持和高效的结果。要掌握 python 技能，请注册 Edureka 的 [Python 认证课程](https://www.edureka.co/python-programming-certification-training)计划，开始学习。

*有什么问题吗？在这篇关于“python anaconda 教程”的文章的评论中提到它们，我们会尽快回复您。*