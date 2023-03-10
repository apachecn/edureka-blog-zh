# 了解 Python 3.8 新特性的快速指南

> 原文：<https://www.edureka.co/blog/whats-new-python-3-8/>

随着 Python 3.8 的发布，人们很想知道对 [Python 编程语言](https://www.edureka.co/blog/python-tutorial/)做了哪些重大改变。在本文中，我们将了解到 [Python](https://www.edureka.co/data-science-python-certification-course) 3.8 的新特性、新的[模块](https://www.edureka.co/blog/python-modules/)等。本博客涵盖了以下主题。

*   [Python 3.8 中的新特性](#new)
    *   [赋值表达式](#expressions)
    *   [仅位置参数](#params)
    *   [并行文件系统缓存](#cache)
    *   [调试版本](#debug)
    *   [f 弦支持](#fstring)
    *   [Python 运行时审计钩子](#hooks)
    *   [Python 初始化配置](#config)
    *   [向量呼叫](#vector)
    *   [酸洗协议 5](#pickle)
*   [新模块](#mod)
*   [其他语言变化](#other)

## **Python 3.8 中的新特性**

Python 3.8 于 2019 年 10 月 14 日发布。随着 [Python 3.8](https://www.python.org/downloads/release/python-380/) 的发布，关于该版本带来的新特性，有很多东西需要补充。开发人员必须了解新特性将如何影响他们项目的结果，以及对旧模块和添加到编程语言中的新模块进行了哪些修改，才能走上正轨。

![Python logo](img/cc0a5119e07a2d3aa82bf7118ff978eb.png)

在新版本中，需要理解移植是如何工作的，以及即使在移植完成后，需要做什么样的改变才能使代码高效。考虑到这一点，让我们来看看 Python 3.8 新版本中引入的新特性。

## **赋值表达式**

Python 3.8 发布了一个新特性，叫做海象操作符，名字类似海象的眼睛和长牙。

![what's new in python 3.8](img/d7bac86117bd3ce2c053028d1b94f2b9.png)

赋值运算符 **":="** 用于将值赋给变量，作为表达式的较大部分。让我们看一个例子来理解它是如何工作的。

```
if (n := len(a)) > 10:
    print(f"List is too long ({n} elements, expected <= 10)")

```

walrus 操作符在 while 循环中很有用，while 循环需要一个值来终止循环，然后在[循环](https://www.edureka.co/blog/loops-in-python/)的主体中再次使用相同的值。它也可以用在[列表](https://www.edureka.co/blog/lists-in-python/)理解中，其中过滤条件中需要的值在表达式体中也需要。

**While 循环示例**

```
# Loop over fixed length blocks
while (block := f.read(256)) != '':
    process(block)

```

**列举理解示例**

```
[clean_name.title() for name in names
 if (clean_name := normalize('NFC', name)) in allowed_names]

```

由于 walrus 操作符是一个表达式，它可以用于语句非法的 [lambda 函数](https://www.edureka.co/blog/python-lambda/)和理解。下面列出了 walrus 操作符的一些限制。

*   不直接支持多个目标

*   不支持单个名称以外的单个分配目标

*   逗号前后的优先级不同

*   不支持可重复打包和解包

*   不支持内联类型批注

*   不支持扩充赋值

让我们看一个例子，看看它是如何改进代码的。

```
if self._is_special:
    ans = self._check_nans(context=context)
    if ans:
        return ans

```

**改良代码**

```
if self._is_special and (ans := self._check_nans(context=context)):
    return ans

```

## **仅位置参数**

有一个新的函数参数语法**"/**，用来表示有些参数可以位置使用，不能作为关键字使用。

让我们看一个例子来理解它是如何工作的。

```
def f(a, b, /, c, d, *, e, f):
    print(a, b, c, d, e, f)

f(10, 20, 30, d=40, e=50, f=60)

```

它允许纯粹的 [python 函数](https://www.edureka.co/blog/python-functions)完全模拟现有的 [C](https://www.edureka.co/blog/c-programming-tutorial/) 编码函数。pow()函数不能使用位置参数。

使参数只具有位置性的另一个好处是，它允许在将来改变参数名，而没有破坏代码的风险。仅位置参数极大地解决了需要接受任意关键字参数的函数和方法的实现。

## **编译字节码文件的并行文件系统缓存**

python 3.8 中有一个新的 [PYTHONPYCACHEPREFIX](https://docs.python.org/3/using/cmdline.html#envvar-PYTHONPYCACHEPREFIX) 设置，它将隐式字节码缓存配置为使用单独的并行文件系统树。

缓存的位置在 **sys.pycache_prefix** 中报告， **none** 表示 __pycache__ 目录中的默认位置。

Python 3.8 中 PYTHONPYCACHEPREFIX 也可以作为-X pycache_prefix 使用。

## **调试版本使用与发布版本相同的 ABI**

对于 Python 3.8，无论是在调试模式还是发布模式下构建，都使用相同的 ABI。当 Python 在调试模式下使用 UNIX 时，现在可以加载在发布模式下构建的 C 扩展，并且扩展使用稳定的 ABI 构建。

发布版本和调试版本已经成为与 Python 3.8 兼容的 ABI 版本。在 UNIX 上，除了 android 和 Cygwin，C 扩展不再需要链接到 libpython。我们可以使用共享库 python 轻松加载 C 扩展。

现在，当 UNIX 在调试模式下构建时，import 也会查找在发布模式和稳定 ABI 下编译的 C 扩展。

## **f 字符串支持=用于自我记录表达式和调试**

Python 3.8 为 f- [字符串](https://www.edureka.co/blog/strings-in-python)增加了一个 **=** 说明符。让我们举个例子来理解这一点。

```
user = 'eric_idle'
member_since = date(1975, 7, 31)
f'{user=} {member_since=}'

```

**输出:`"user='eric_idle' member_since=datetime.date(1975, 7, 31)"`**

通常的 f 字符串说明符允许对结果的显示方式进行更多的控制，但是 **=** 说明符显示整个表达式，因此可以显示计算结果。

## **Python 运行时审计钩子**

新的 python 版本增加了审计挂钩和验证开放挂钩，它们允许用纯 Python 代码编写的应用程序和框架利用额外的通知。它们还允许系统管理员或嵌入者在审计始终可用的地方部署 python 的构建。

**审计挂钩**

应用程序中的审计挂钩是一个出口点，它允许审计人员随后添加模块。这是通过激活钩子将控制转移到审计模块来实现的。

**已验证的开放式挂钩**

经验证的开放钩子允许 python 嵌入器在启动脚本或导入 Python 代码时集成操作系统支持。

## **Python 初始化配置**

Python 3.8 增加了新的 C API 来配置初始化，以获得更好的控制和更好的错误报告。添加了以下新结构。

*   PyConfig
*   PyPreConfig
*   PyStatus
*   PyWideStringList

以下是添加的功能列表。

| **功能** | **描述** |
| **PyConfig_Clear()** | 释放配置存储器 |
| **PyConfig _ InitIsolatedConfig()** | 使用隔离配置初始化配置 |
| **PyConfig _ initpython config()** | 使用 python 配置初始化配置 |
| **PyConfig_Read()** | 读取所有 python 配置 |
| **PyConfig_SetArgv()** | 从更宽的字符串中设置命令行参数 |
| **PyConfig _ SetBytesString()** | 使用 Py_DecodeLocale()解码字符串，并将结果设置到*config_str 中 |
| **PyConfig_SetString()** | 将宽字符串复制到*config_str 中 |
| **PyPreConfig _ InitIsolatedConfig()** | 使用 python 配置初始化预配置 |
| **PyPreConfig _ initpython config()** | 使用隔离配置初始化预配置 |
| **PyStatus_Error()** | 带有消息的初始化错误 |
| **PyStatus_Exception()** | 如果真异常必须被处理，它是错误或退出的状态。 |
| **PyStatus_Exit()** 的缩写形式 | 用指定的退出代码退出 python |
| **PyStatus_IsError()** | 检查结果是否为错误 |
| **PyStatus_IsExit()** | 检查结果是否是退出 |
| **PyStatus_NoMemory()** | 内存分配失败 |
| **PyStatus_Ok()** 的缩写形式 | 成功 |
| **PyWideStringList _ Append()** | 将项目追加到列表 |
| **PyWideStringList _ Insert()** | 在索引处将项目插入列表 |
| **Py_BytesMain()** | 类似于 Py_Main()，但 argv 是一个字节字符串数组 |
| **py _ existstatus exception()** | 如果状态为错误，则打印错误并使用非零退出代码退出 |
| **Py _ InitializeFromConfig()** | 从配置配置初始化 python |
| py _ pre initialize() | 从预配置配置预初始化 python |
| **py _ pre initialize fromargs()** | 从预配置配置和命令行参数预初始化 python |
| **Py _ PreInitializeFromBytesArgs()** | 通过预配置配置和命令行参数预初始化 python(字节字符串) |
| **Py_RunMain()** | 完成 python 并返回退出状态 |
| **pyconfig _ setbytes sarv()** | 设置命令行参数-使用 Py_DecodeLocale()解码字节 |

## **向量呼叫**

它是 CPython 的快速调用协议，被添加到 Python/C API 中。它基本上意味着将已经为各种类进行的现有优化形式化。vector 调用只处理 Python/C API，不对 Python 语言和标准库做任何更改。

在 Python 3.8 中，任何实现可调用的扩展类型都可以使用该协议。

虽然它已经被添加到当前版本中，但它仍然是临时的，将在 Python 3.9 的下一个版本中完全公开。

## **Pickle 协议 5，带外数据缓冲器**

Python 对象层次结构转换为字节流的过程称为“酸洗”。也称为序列化、编组等。

当 pickle 用于在 python 进程之间传输大型数据以充分利用多核或多机处理时，通过减少内存副本来优化传输非常重要。

pickle 5 协议引入了对带外缓冲区的支持，其中数据可以与主 pickle 流分开传输。

*   它涵盖了带外数据缓冲区所需的额外元数据

*   Pickle 5 有一个新的 **PickleBuffer** 类型，用于 **__reduce_ex__** 实现返回带外数据缓冲区

*   pickling 时有一个新的 **buffer_callback** 参数，用于处理带外数据缓冲区

*   它还有一个新的 **buffers** 参数，用于提供带外数据缓冲。

## **新模块**

Python 3.8 中增加了一个新的[模块](https://www.edureka.co/blog/python-modules/)，新的 importlib.metadata 模块为从第三方包中读取元数据提供了临时支持。让我们看一个例子，在这个例子中，它被用来提取一个已安装的包的版本号、入口点列表等。

```
from importlib.metadata import version, requires, files
version('requests')

```

**输出:** `'2.22.0'`

```
list(requires('requests'))

```

**输出:** `['chardet (<3.1.0,>=3.0.2)'] `

```
list(files('requests'))[:5]

```

**输出:**

`[PackagePath('requests-2.22.0.dist-info/INSTALLER'),``PackagePath('requests-2.22.0.dist-info/LICENSE'),``PackagePath('requests-2.22.0.dist-info/METADATA'),``PackagePath('requests-2.22.0.dist-info/RECORD'),`

## **其他语言变化**

这里有一些其他的语言变化，在使用 Python 3.8 时会非常有用。

**多处理共享内存**

在 python 3.8 中，在多处理模块中，有一个新的 SharedMemory 类，它允许在不同的 python 进程之间创建和共享内存区域。

**![](img/f1be6832a5a87709f8e4bacff21d5c97.png)**

**打字模块改进**

Python 3.8 对类型模块进行了新的修改，使健壮的检查成为可能。

*   final 类型注释和 Final 关键字表示对象在任何时候都不应该被覆盖、子类化或重新分配。

*   文字类型将表达式限制为特定的值或值列表。

*   TypeDict 类型允许您创建字典，其中关联的值被限制为一个或多个类型。

**可逆词典**

Python 3.8 允许用[字典](https://www.edureka.co/blog/dictionary-in-python/)反转()。这里有一个简单的例子来说明它是如何工作的

```
my_dict = {a: 'edureka', b: 'python'}
list(reversed(my_dict.items()))

```

**输出** : `[(b, 'python'), (a, 'edureka')]`

**语法警告**

随着 Python 3.8 的发布，如果在 Python 代码中出现语法错误，Python 解释器会抛出语法警告。通过警告可以更清楚地识别真正丢失了什么。

这将我们带到本文的结尾，我们已经了解了 Python 3.8 的新特性。我希望你清楚本教程中与你分享的所有内容。

*如果您发现了这篇关于“Python 3.8 的新特性”的文章，请查看一下  [Edureka Python 认证培训、](https://www.edureka.co/data-science-python-certification-course) 一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*我们在这里帮助你踏上旅程的每一步，并为想要成为  [Python 开发者](https://www.edureka.co/blog/how-to-become-a-python-developer/)的学生和专业人士设计课程。该课程旨在让您在 Python 编程方面有一个良好的开端，并训练您掌握核心和高级 Python 概念以及各种  [Python 框架](https://www.edureka.co/blog/python-frameworks/) ，如  [Django。](https://www.edureka.co/blog/django-tutorial/)*

如果您遇到任何问题，请在“Python 3.8 新特性”的评论部分提出您的所有问题，我们的团队将很乐意回答。