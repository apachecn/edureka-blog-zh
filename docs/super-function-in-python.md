# 如何在 Python 中实现超级函数

> 原文：<https://www.edureka.co/blog/super-function-in-python/>

在编码行业 [Python](https://www.edureka.co/blog/python-tutorial/) 经常被描述为一个至高无上的编程平台。由于 Python 提供了广泛的特性和巨大的多功能性，这个名字是名副其实的。但令人惊讶的是，Python 中有一个函数被恰当地命名为超级函数。以下指针将在这篇 Python 中的超级函数文章中讨论。

*   [超级功能小介绍](#ASmallIntroductionforSuper)
*   [在编程中使用 Super](#MakinguseofSuperinyourProgramming)
*   [超级功能的使用](#UsesofSuperFunction)

## **超级功能小介绍**

当 Python 的最新版本，也就是 2.2 版发布时，超级函数就出现了。这本质上是一个内置函数，当使用它时，它返回一个对象的代理，以便将方法委托给类。这个函数有趣的一面是这样一个事实，形成的类本质上既可以是父类，也可以是后代。

简单地说，当你需要访问继承的模块时，你可以使用超级函数，这些模块以前已经在类对象中过度暴露了。

Python 网站对超级函数的官方定义如下:

"[Super 用于]返回一个代理对象，该对象将方法调用委托给类型的父类或姐妹类。这对于访问在类中被重写的继承方法很有用。搜索顺序与 getattr()使用的顺序相同，只是类型本身被跳过了。"

让我们继续编程。

## **在编程中使用 Super**

现在您已经知道了超级函数的基本定义，让我们来探索如何使用它来满足您的日常编程需求。下面提到的是使用超级功能的一些最重要的方法。

您可以在本质上是动态的环境中调用超级函数，以便在协作和多重继承中使用。需要注意的一点是，这个用例是 Python 语言独有的，因为其他语言总是统计编译的，或者只支持单一继承函数。如果你愿意，你可以通过单一继承调用超级函数，引用多个类或父类，而不必先命名它们。虽然这种方法绝对是一种捷径，但使用这种方法的明显优势是使您的代码简短而精确，以满足未来的审计和执行需求。

当 super 函数首次在 Python 环境中引入时，它引起了很多争议，但是后来看到它的用法，开发人员很快开始在他们的日常编码需求中使用它。

如果使用的是 Python 版及以上，使用 super 函数的方法如下。

超级()。方法名(参数)

如果您使用的是 Python 的早期版本，super function 的语法将是，

超级(子类，实例)。方法(参数)

如何在 Python 中启动&调用超级函数？

现在你已经知道了超级函数的基本知识和语法，让我们看看如何使用这个函数。

代码的第一行将是，

```

class MyParentClass(object):
def __init__(self):
pass

class SubClass(MyParentClass):
def __init__(self):
MyParentClass.__init__(self)

```

如果您使用的是 Python 版本 2，请使用以下代码

```
class SubClass(MyParentClass):
def __init__(self):
super(SubClass, self).__init__()

```

然而在 Python 中，代码将是

```
class MyParentClass():
def __init__(self):
pass

class SubClass(MyParentClass):
def __init__(self):
super()

```

让我们了解一下 Python 中 Super 函数的用法。

## **Python 中超级函数的使用**

![Output- Super function in Python- Edureka](img/97fb49053a656e16c0188b8f2076b5af.png)

让我们快速回顾一下超级函数最突出的用途。

如果您担心转发兼容性，Python 中的 super 函数被证明是非常有用的。在你的代码中使用它，基本上确保你的代码可以在未来使用，只需要做少量的修改。如果使用正确，它减少了声明您在 Python 代码中创建的所有类的特征的需求。

但是为了确保您的超级函数正常工作，您需要始终满足以下先决条件。

Python 库中必须存在名为 super()的方法。在执行期间，被调用方和调用方函数必须具有相同的签名和地址。每次使用超级函数时，都需要使用 super()关键字来调用它。

**结论**

自从 super 函数出现以来，就出现了一场关于在依赖注入情况下使用 super 的持续辩论，尽管到目前为止还没有实质性的证据来证明这一点。

但是不管是什么情况，超级函数是 Python IDLE 最方便的特性之一，如果使用正确，它可以用来实现和分析许多复杂的问题。

**文章摘要**

了解所有关于超级函数的知识，它的用途，以及如何在日常 Python 编程中使用它。请继续阅读，了解更多信息。