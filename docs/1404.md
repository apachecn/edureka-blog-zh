# 如何在 Python 中实现 Round 函数？

> 原文：<https://www.edureka.co/blog/round-function-in-python/>

Python 中的 Round 函数，返回一个浮点数，它是指定数字的舍入版本。本文将详细探讨这一概念。本文将涉及以下几点:

*   [Python round()](#Pythonround())
*   [实际应用](#PracticalApplication)
*   [舍入 NumPy 数组](#RoundingNumPyArrays)
*   [四舍五入熊猫系列和数据框](#RoundingPandasSeriesandDataFrame)
*   [数据帧](#DataFrame)

那么让我们开始吧，

## **Python 中的 Round 函数**

方法 round(x，n)将返回四舍五入到小数点后 n 位数的值 x。

**例:** 圆(7.6 + 8.7，1)

**输出:** 16.3

Round 赋予了这种给出最接近值的能力

**例:** 圆(6.543231，2)

**输出:** 6.54

有时它不会给出正确的输出

**例:** round(2.675，2)#应该返回 2.68 但没有

**输出:** 2.67

有时它会给出正确的输出

**例:** 圆(8.875，2)

**输出:** 8.88

继续这篇关于 Python 中的 Round 函数的文章。

## **蟒轮** ( **)**

python 中的 Round 函数将十进制值四舍五入为给定的位数，如果我们不提供 n，即小数点后的位数，它会将数字四舍五入为最接近的整数。

如果后面的整数> = 5，它将舍入到上限；如果小数是不带第二个参数的< 5 . round()，它将舍入到下限整数

```
#int
print(round(12))
#float
print(round(66.6))
print(round(45.5))
print(round(92.4))

```

**输出:** 12 67 46 92

现在，如果提供了第二个参数，那么最后一个十进制数字将增加 1，直到舍入值，如果 last _ digit+1 > = 5，否则将与提供的相同。

带有第二个参数的 round()

```
# when last_digit+1 =5
print(round(3.775, 2))
# when last_digit+1 is >=5
print(round(3.776, 2))
# when if last_digit+1 is <5
print(round(3.773, 2))

```

**产量:** 3.77 3.78 3.77

继续这篇关于 Python 中的 Round 函数的文章。

## **实际应用:**

舍入函数的一些应用是将数字舍入到有限的数字，例如，如果我们想将分数表示为小数，我们通常在小数后取 2 或 3 个数字，这样我们就可以准确地表示分数。

```
b=2/6
print(b)
print(round(b, 2))

```

**输出:**0.333333333333330.33

在这个数据科学和计算的时代，我们经常将数据存储为 Numpy 数组或 pandas 数据帧，其中舍入在精确计算操作中起着非常重要的作用，类似于 python 中的 round 函数 Numpy 或 Pandas 采用两个参数数据和数字，即我们要舍入的数据和小数点后需要舍入的位数，它将此应用于所有行和列。让我们看一些例子。

继续这篇关于 Python 的文章:Round 函数。

## **舍入 NumPy 数组**

要安装 NumPy，您可以使用:

```
pip3 install numpy
```

除此之外，如果您使用的是 Anaconda 环境，它将已经安装，为了舍入 NumPy 数组的所有值，我们将把数据作为参数传递给 np.around()函数。现在我们将创建一个 3×4 大小的 NumPy 数组，包含浮点数，如下所示:

```
import numpy as np
np.random.seed(444)
data = np.random.randn(3, 4)
print(data)

```

**输出:**【0.35743992 0.3775384 1.38233789 1.17554883】【0.9392757-1.14315015-0.54243951-0.54870808】【0.20851975 0.21268956 1。

例如，以下代码将数据中的所有值四舍五入到三位小数:

```
import numpy as np
np.random.seed(444)
data = np.random.randn(3, 4)
print(np.around(data, decimals=3))

```

**输出:**[[0.357 0.378 1.382 1.176][-0.939-1.143-0.542-0.549][0.209 0.213 1.268-0.807]]

np.around()可以用来纠正浮点错误。

在下面的示例中，我们可以看到 3×1 处的元素是 0.20851975。您预期该值是 0.208，但它被舍入为 0.209。您还可以看到 1×2 处的值被正确地舍入为 0.378。

因此，如果需要将数据舍入到所需的形式，NumPy 有许多方法:

*   numpy.ceil()
*   numpy.floor()
*   numpy.trunc()
*   numpy.rint()

np.ceil()函数将数组中的每个值舍入为大于或等于原始值的最接近的整数:

print(np.ceil(data))

**输出:**【1。1.2.2.] [-0。-1.-0.-0.】【1。1.2.-0.]]

要将每个值向下舍入到最接近的整数，请使用 np.floor():

```
print(np.floor(data))
```

**输出:** [[ 0。0.1.1.] [-1。-2.-1.-1.】【0。0.1.-1.]]

您还可以使用 np.trunc()将每个值截断为其整数部分:

```
print(np.trunc(data))
```

**输出:** [[ 0。0.1.1.] [-0。-1.-0.-0.】【0。0.1.-0.]]

最后，要使用“四舍五入”策略四舍五入到最接近的整数，请使用 np.rint():

```
print(np.rint(data))
```

**输出:** [[ 0。0.1.1.] [-1。-1.-1.-1.】【0。0.1.-1.]]

继续这篇关于 Python 的文章:Round 函数。

## **四舍五入熊猫系列和数据框**

Pandas 是另一个受数据科学家欢迎的库，用于分析数据。

与 NumPy 类似，我们可以使用以下命令安装这个库:

```
pip3 install pandas
```

Pandas 的两个主要数据结构是数据帧和系列，数据帧基本上类似于数据库中的表，而系列是列。我们可以使用 Series.round()和 DataFrame.round()对对象进行舍入。

```
import pandas as pd
import numpy as np
np.random.seed(444)
series = pd.Series(np.random.randn(4))
print(series)

```

**输出:**0 0.3574401 0.3775382 1.3823383 1.175549dtype:float 64print(series . round(2))0.361 0.382 1.383 1.18dtype:float 64

继续这篇关于 Python 的文章:Round 函数

## **数据帧:**

```
import pandas as pd
import numpy as np
np.random.seed(444)
df = pd.DataFrame(np.random.randn(3, 3), columns=["Column 1", "Column 2", "Column 3"])
print(df)
print(df.round(3))

```

**输出:**1 列 2 列 30 0.357440 0.377538 1.3823381 1.175549-0.939276-1.1431502-0.542440-0.548708 0.2085201 列 2 列 30.357 0.377

对于 DataFrame，我们可以为每一列指定不同的精度。因此，的 round 函数可以接受一个字典或序列，这样我们就可以为不同的列提供不同的精度。

print(df.round({ "列 1": 1，"列 2": 2，"列 3": 3}))

**输出:** 第 1 列第 2 列第 3 列 0 0.4 0.38 1.3821 1.2-0.94-1.1432-0.5-0.55 0.209

在本文中，我们介绍了什么是 round 函数，以及它是如何在 python 中从核心实现的。我们还讨论了 round 函数的一些缺点，以及我们如何纠正它们，以及它如何在数据科学中广泛使用的库中有用。

这样我们就结束了这篇关于 Python 中的循环函数’的文章。随着越来越受欢迎，在机器学习、人工智能、数据科学等领域的需求也在增加。要掌握你的技能，请参加 edureka 的 [python 认证项目](https://edureka.co/python) ，开始你的学习。

*有什么问题吗？请在评论中提及它们。我们将尽快回复您*