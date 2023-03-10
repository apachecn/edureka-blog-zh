# Python 人工智能综合指南

> 原文：<https://www.edureka.co/blog/artificial-intelligence-with-python/>

## **用 Python 实现人工智能:**

人工智能已经存在了半个多世纪，它的进步正以指数速度增长。对人工智能的需求正处于高峰期，如果你希望学习人工智能，你已经来到了正确的地方。这篇用 Python 写的关于人工智能的博客将帮助你理解人工智能的所有概念以及用 Python 的实际实现。

要获得人工智能和机器学习的深入知识，可以报名参加 Edureka 提供的全天候支持和终身访问的直播 *[**机器学习工程师硕士项目**](https://www.edureka.co/masters-program/machine-learning-engineer-training)* 。

本人工智能与 Python 博客涵盖了以下主题:

1.  [为什么 Python 最适合 AI？](#Why%20Is%20Python%20Best%20For%20AI)
2.  [对人工智能的需求](#Demand%20For%20AI)
3.  [什么是人工智能？](#What%20Is%20Artificial%20Intelligence)
4.  [人工智能的种类](#Types%20Of%20Artificial%20Intelligence)
5.  [机器学习基础知识](#Machine%20Learning%20Basics)
6.  [机器学习的类型](#Types%20Of%20Machine%20Learning)
7.  [利用机器学习解决的问题类型](#Types%20Of%20Problems%20Solved%20By%20Using%20Machine%20Learning)
8.  [机器学习过程](#Machine%20Learning%20Process)
9.  [用 Python 进行机器学习](#Machine%20Learning%20With%20Python)
10.  [机器学习的局限性](#Limitations%20Of%20Machine%20Learning)
11.  [为什么要深度学习？](#Why%20Deep%20Learning)
12.  [深度学习是如何工作的？](#How%20Deep%20Learning%20Works)
13.  [什么是深度学习？](#What%20Is%20Deep%20Learning)
14.  [深度学习用例](#Deep%20Learning%20Use%20Case)
15.  [感知器](#Perceptrons)
16.  [多层感知器](#Multilayer%20Perceptrons)
17.  [用 Python 进行深度学习](#Deep%20Learning%20With%20Python)
18.  [自然语言处理(NLP)简介](#Introduction%20To%20Natural%20Language%20Processing)
19.  [NLP 应用](#NLP%20Applications)
20.  [自然语言处理中的术语](#Terminologies%20In%20NLP)

## **为什么 Python 最适合 AI？**

很多人问我，“哪种编程语言最适合人工智能？”或者“*为什么 Python 对于 AI？”*

尽管是一种通用语言，Python 已经进入了最复杂的技术，如人工智能、机器学习、深度学习等。

***为什么 Python 在所有这些领域都获得了这么大的人气？***

以下是为什么 Python 是每个核心开发人员、数据科学家、机器学习工程师等选择语言的原因列表:

**![Why Python For AI - Artificial Intelligence With Python - Edureka](img/7f533f49300dd9809a0571fe32382231.png)**

*为什么用 Python 开发 AI——用 Python 开发人工智能——edu reka*

*   **代码少:**实现 AI 涉及到成吨成吨的算法。感谢 Pythons 对预定义包的支持，我们不必编写算法。为了使事情更简单，Python 提供了“边编码边检查”的方法，减少了测试代码的负担。
*   **预建库:** Python 有上百个预建库，用来实现各种机器学习和深度学习算法。所以每次你想在一个数据集上运行一个算法的时候，你所要做的就是用一个命令安装并加载必要的包。预构建库的例子包括 NumPy、Keras、Tensorflow、Pytorch 等等。
*   **易于学习:** Python 使用一种非常简单的语法，可以用来实现简单的计算，比如将两个字符串添加到复杂的过程中，比如构建机器学习模型。
*   **平台无关** : Python 可以在多种平台上运行，包括 Windows、MacOS、Linux、Unix 等等。在将代码从一个平台转移到另一个平台时，您可以使用 PyInstaller 之类的包来解决任何依赖问题。
*   大规模社区支持: Python 有一个巨大的用户社区，当我们遇到编码错误时，它总是很有帮助。除了大量的粉丝，Python 还有多个社区、团体和论坛，程序员可以在那里发布错误并互相帮助。

如果你想深入学习 Python 编程，这里有几个链接，一定要看看这些博客:

1.  [Python 教程——学习 Python 编程的完整指南](https://www.edureka.co/blog/python-tutorial/)
2.  [Python 编程语言——Python 基础入门](https://www.edureka.co/blog/python-programming-language)
3.  [Python 函数初学者指南](https://www.edureka.co/blog/python-functions)
4.  [用于数据科学的 Python](https://www.edureka.co/blog/learn-python-for-data-science/)

由于这个博客是关于 Python 的人工智能，我将向你介绍最有效和最流行的基于人工智能的 Python 库。

1.  **[Tensorflow](https://www.edureka.co/blog/tensorflow-tutorial/) :** 由谷歌开发，这个库广泛用于编写[机器学习算法](https://www.edureka.co/blog/machine-learning-algorithms/)和执行涉及神经网络的繁重计算。
2.  **[Scikit-Learn](https://www.edureka.co/blog/scikit-learn-machine-learning/):**Scikit-Learn 是一个与 NumPy 和 SciPy 相关联的 Python 库。它被认为是处理复杂数据的最佳库之一。
3.  **[NumPy](https://www.edureka.co/blog/python-numpy-tutorial/) :** Numpy 是一个专门用于计算科学/数学数据的 python 库。
4.  **Theano:** Theano 是一个函数库，可以有效地计算和运算涉及多维数组的数学表达式。
5.  这个库简化了神经网络的实现。它还具有计算模型、评估数据集、可视化图表等最佳功能。
6.  **NLTK:** NLTK 或自然语言工具包是一个开源的 Python 库，专门用于自然语言处理、文本分析和文本挖掘。

除了上面提到的库，请确保在 2019 年 博客中查看这个 [*你必须知道的 10 大 Python 库，以获得更清晰的了解。*](https://www.edureka.co/blog/python-libraries/)

既然你已经知道了用于实现人工智能技术的重要 Python 库，让我们来关注一下人工智能。在下一部分，我将会介绍人工智能的所有基本概念。

首先，我们先来了解一下对 AI 的突然需求。

## **对人工智能的需求**

自从 20 世纪 50 年代人工智能出现以来，我们已经看到它的潜力呈指数增长。但是，如果人工智能已经存在了半个多世纪，为什么它突然变得如此重要？为什么现在说人工智能？

![Demand For AI - Artificial Intelligence With Python - Edureka](img/e1152a020bae009c04514fd628b6c8ae.png)

*对人工智能的需求——使用 Python 的人工智能——edu reka*

人工智能大受欢迎的主要原因是:

**更强的计算能力:**实现人工智能需要强大的计算能力，因为构建人工智能模型需要大量的计算和复杂神经网络的使用。GPU 的*发明让这成为可能。我们终于可以进行高级计算和实现复杂的算法。*

**数据生成:**在过去的几年里，我们一直在生成不可估量的数据。这些数据需要通过使用机器学习算法和其他人工智能技术进行分析和处理。

**更有效的算法:**在过去的十年里，我们成功地开发了最先进的算法，其中涉及深度神经网络的实现。

**广泛投资:**随着特斯拉、网飞和脸书等科技巨头开始投资人工智能，人工智能越来越受欢迎，导致对人工智能系统的需求增加。

人工智能的增长是指数级的，它也加速了经济的发展。所以这是你进入人工智能领域的合适时机。

查看这些由 E & ICT Academy NIT Warangal 提供的[人工智能和机器学习课程](https://www.edureka.co/executive-programs/machine-learning-and-ai)，学习并建立人工智能职业生涯。

## **什么是人工智能？**

人工智能一词是几十年前由约翰·麦卡锡在达特茅斯会议上首次提出的。他将人工智能定义为:

***“制造智能机器的科学与工程。”***

换句话说，人工智能是让机器像人类一样思考和决策的科学。

在最近的过去，人工智能已经能够通过创造机器和机器人来实现这一目标，这些机器和机器人已经被用于广泛的领域，包括医疗保健、机器人、市场营销、商业分析等等。

现在我们来讨论一下人工智能的不同阶段。

## **人工智能的种类**

人工智能分为三个进化阶段:

1.  人工狭义智能
2.  人工通用智能
3.  人工超级智能

**![Types Of AI - Artificial Intelligence With Python - Edureka](img/6306040e0ec3d174eb0ec82ced4f8778.png)**

*人工智能的类型——使用 Python 的人工智能——edu reka*

## **人工狭义智能**

人工狭义智能通常被称为弱人工智能，它涉及到将人工智能仅应用于特定的任务。

现有的声称使用“人工智能”的基于人工智能的系统实际上是作为一个弱人工智能运行的。Alexa 就是一个很好的窄智例子。它在有限的预定功能范围内运行。Alexa 没有真正的智力或自我意识。

谷歌搜索引擎，索菲亚，自动驾驶汽车，甚至著名的 AlphaGo，都属于弱 AI 的范畴。

## **人工通用智能**

人工智能通常被称为强人工智能，它涉及拥有执行人类可以执行的任何智力任务的能力的机器。

你看，机器不具备类似人类的能力，它们有强大的处理单元，可以进行高级计算，但它们还不能像人类一样思考和推理。

许多专家怀疑 AGI 是否可能实现，也有许多人质疑它是否可取。

例如，斯蒂芬·霍金警告说:

强大的人工智能会自己起飞，并以越来越快的速度重新设计自己。受到缓慢生物进化限制的人类无法竞争，将会被取代。”

## **人工超级智能**

人工超级智能是一个术语，指的是计算机的能力将超过人类的时候。

ASI 目前被视为电影和科幻小说中描述的一种假设情况，机器已经接管了世界。然而，像 Elon Musk 这样的技术大师认为，ASI 将在 2040 年接管世界！

*你怎么看待人工超级智能？*在评论区让我知道你的想法。

在我继续之前，让我澄清一个非常普遍的误解。每个初学者都会问我这些问题:

***AI 和机器学习、深度学习有什么区别？***

## ***AI 和 ML 一样吗？***

让我们来分解一下:

## **AI vs ML vs DL(人工智能 vs 机器学习 vs 深度学习)**

人们倾向于认为人工智能、机器学习和深度学习是相同的，因为它们有共同的应用。比如 Siri 就是 AI、机器学习、深度学习的一个应用。

那么这些技术是如何关联的呢？

*   人工智能是让机器模仿人类行为的科学。
*   *机器学习是人工智能 (AI)的**子集，专注于通过向机器提供数据来让它们做出决策。***
*   *深度学习是机器学习的**子集，使用神经网络的概念来解决复杂的问题。***

总结一下 AI，机器学习和深度学习是互联互通的领域。机器学习和深度学习通过提供一套算法和神经网络来解决数据驱动的问题，从而辅助人工智能。

然而，人工智能并不仅限于机器学习和深度学习。它涵盖了自然语言处理、目标检测、计算机视觉、机器人学、专家系统等众多领域。

现在让我们从机器学习开始。

## **机器学习基础知识**

机器学习这个术语是由亚瑟·塞缪尔在 1959 年首次提出的。回顾过去，就技术进步而言，那一年可能是最重要的一年。

简单来说，

*机器学习是人工智能(AI)的一个子集，它通过向机器提供大量数据&使其能够通过经验改进，从而为机器提供自动学习的能力。因此，机器学习是一种让机器通过获得思考能力来解决问题的实践。*

但是机器怎么做决定呢？

如果你给一台机器输入大量数据，它将学会如何使用机器学习算法来解释、处理和分析这些数据。

![What Is Machine Learning - Artificial Intelligence With Python - Edureka](img/c5cc6c7fc8a39be971291c03f73c8c34.png)

*什么是机器学习——用 Python 实现人工智能——edu reka*

总结一下，看一下上图:

*   机器学习过程始于向机器输入大量数据。
*   然后，机器根据这些数据进行训练，以检测隐藏的见解和模式。
*   这些见解用于通过使用算法来建立机器学习模型，以便解决问题。

现在我们知道了什么是机器学习，让我们看看机器可以学习的不同方式。

## **机器学习的类型**

机器可以通过以下三种方法中的任何一种来学习解决问题:

1.  监督学习

2.  无监督学习

3.  强化学习

## **监督学习**

监督学习是一种技术，在这种技术中，我们使用良好标记的数据来教授或训练机器。

为了理解监督学习，让我们考虑一个类比。小时候，我们都需要有人指导我们解决数学问题。我们的老师帮助我们理解加法是什么以及如何做加法。

类似地，你可以将监督学习视为一种涉及指导的机器学习。带标签的数据集是训练你理解数据模式的老师。被标记的数据集只不过是训练数据集。

*![Supervised Learning - Artificial Intelligence With Python - Edureka](img/f2a19a462c5eec7e43cd27b41cb7b36b.png)监督学习——用 Python 实现人工智能——edu reka*

考虑上图。在这里，我们给机器输入汤姆和杰里的图像，目标是让机器识别图像并将其分为两组(汤姆图像和杰里图像)。

输入到模型中的训练数据集被标记为“我们告诉机器，‘这是汤姆的长相，这是杰瑞’”。通过这样做，您可以使用标记的数据来训练机器。在监督学习中，有一个在标记数据的帮助下完成的明确定义的训练阶段。

## **无监督学习**

*无监督学习涉及通过使用未标记的数据进行训练，并允许模型在没有指导的情况下对该信息进行操作。*

把无监督学习想象成一个在没有任何指导的情况下学习的聪明孩子。在这种类型的机器学习中，模型没有被输入带标签的数据，因为模型没有“这个图像是汤姆，这个是杰里”的线索，它通过接受大量数据，自己找出模式以及汤姆和杰里之间的差异。

![Unsupervised Learning - Artificial Intelligence With Python - Edureka](img/0b2be0f0051505074bb0a695ecfc4a22.png) *无监督学习——用 Python 实现人工智能——edu reka*

例如，它识别 Tom 的突出特征，如尖耳朵、较大的尺寸等，以理解该图像是类型 1。类似地，它在杰瑞身上发现了这样的特征，并且知道这个图像属于类型 2。

因此，它将图像分为两个不同的类别，而不知道谁是汤姆或杰里。

## **强化学习**

强化学习是机器学习的一部分，其中一个代理被置于一个环境中，他通过执行某些动作并观察从这些动作中获得的回报来学习在这个环境中的行为。

想象一下你被丢在一个孤岛上！

你会怎么做？

恐慌？是的，当然，最初我们都会。但是久而久之，你将学会如何在岛上生活。你将探索环境，了解气候条件，那里生长的食物类型，岛上的危险等等。

这正是强化学习的工作方式，它涉及到一个被放在未知环境(岛)中的代理人(你，被困在岛上)，他必须通过观察和执行导致奖励的行动来学习。

*强化学习主要用于高级机器学习领域，如自动驾驶汽车、AplhaGo 等。*以上总结了机器学习的类型。

现在，让我们看看使用机器学习解决的问题的类型。

## **机器学习可以解决哪些问题？**

使用机器学习可以解决三大类问题:

### **什么是回归？**

在这类问题中，输出是一个连续的量。举个例子，给定距离，你想预测一辆车的速度，这就是一个回归问题。回归问题可以通过使用像线性回归这样的监督学习算法来解决。

### **什么是分类？**

在这种类型中，输出是分类值。将电子邮件分为垃圾邮件和非垃圾邮件两类是一个分类问题，可以通过使用支持向量机、朴素贝叶斯、逻辑回归、K 近邻等监督学习分类算法来解决。

### **什么是聚类？**

这类问题包括根据特征相似性将输入分配到两个或多个聚类中。例如，可以通过使用无监督学习算法(如 K-Means 聚类)来根据观众的兴趣、年龄、地理位置等将观众聚类成相似的组。

下表总结了回归、分类和聚类之间的区别:

![Regression vs Classification vs Clustering - Artificial Intelligence With Python - Edureka](img/7f97b364f28d9f3e14b7cb5d33654913.png)

*回归 vs 分类 vs 聚类 Python 人工智能——edu reka*

现在让我们看看机器学习过程是如何工作的。

## **机器学习过程步骤**

机器学习过程包括建立预测模型，该模型可用于找到问题陈述的解决方案。

为了理解机器学习过程，让我们假设你已经被给予了一个需要使用机器学习来解决的问题。

*问题是利用机器学习来预测你所在地区的降雨发生情况。*

在机器学习过程中遵循以下步骤:

**步骤 1:定义问题陈述的目标**

在这一步，我们必须明白到底需要预测什么。在我们的案例中，目标是通过研究天气状况来预测下雨的可能性。

记住什么样的数据可以用来解决这个问题，或者你必须遵循什么样的方法才能得到解决方案，这也是很重要的。

**第二步:数据收集**

在这个阶段，你必须问这样的问题，

*   解决这个问题需要什么样的数据？
*   数据是否可用？
*   我如何能得到数据？

一旦您知道了所需的数据类型，您就必须了解如何获得这些数据。数据收集可以手动完成，也可以通过网络搜集完成。

然而，如果你是一个初学者，你只是想学习机器学习，你不必担心获得数据。网上有成千上万的数据资源，你可以下载数据集并开始使用。

回到手头的问题，天气预报所需的数据包括湿度、温度、压力、地点、你是否住在山区等等。

必须收集和存储这些数据以供分析。

**第三步:数据准备**

你收集的数据几乎从来没有正确的格式。你会在数据集中遇到很多不一致的地方，比如缺失值、冗余变量、重复值等。

消除这种不一致是非常必要的，因为它们可能导致错误的计算和预测。因此，在这一阶段，您扫描数据集以寻找任何不一致的地方，然后立即修复它们。

**第四步:探索性数据分析**

带上你的侦探眼镜，因为这个阶段是关于深入研究数据和发现所有隐藏的数据秘密。

EDA 或探索性数据分析是机器学习的头脑风暴阶段。数据探索包括理解数据中的模式和趋势。在这个阶段，所有有用的见解都被提取出来，变量之间的相关性也得到理解。

例如，在预测降雨的情况下，我们知道如果温度下降很低，很有可能会下雨。在这个阶段，必须理解和绘制这种相关性。

**第五步:建立机器学习模型**

在数据探索期间获得的所有见解和模式都用于构建机器学习模型。这个阶段总是从将数据集分成两部分开始，即训练数据和测试数据。

*训练数据将用于建立和分析模型。*模型的逻辑基于正在实施的机器学习算法。

在预测降雨量的情况下，由于输出会以 True(如果明天会下雨)或 False(明天不会下雨)的形式出现，所以我们可以使用 Logistic 回归或决策树等分类算法。

选择正确的算法取决于你要解决的问题的类型、数据集和问题的复杂程度。

**第六步:模型评估&优化**

在使用训练数据集建立模型之后，最后是测试模型的时候了。

测试数据集用于检查模型的效率以及预测结果的准确性。

一旦计算出精度，就可以在这个阶段对模型进行任何进一步的改进。可以使用参数调整和交叉验证等方法来提高模型的性能。

**第七步:预测**

一旦模型被评估和改进，它最终被用于进行预测。最终输出可以是分类变量(例如真或假)，也可以是连续量(例如股票的预测值)。

在我们的例子中，为了预测降雨的发生，输出将是一个分类变量。

这就是整个机器学习过程。

在下一节中，我们将讨论各种类型的机器学习算法。

## **机器学习算法**

机器学习算法是每个机器学习模型背后的基本逻辑。这些算法是基于简单的概念，如统计和概率。

关注下面提到的博客，了解机器学习算法背后的数学和统计数据:

1.  [数据科学数学和统计学完全指南](https://www.edureka.co/blog/math-and-statistics-for-data-science/)
2.  [关于统计和概率你需要知道的一切](https://www.edureka.co/blog/statistics-and-probability/)

![Machine Learning Algorithms - Artificial Intelligence With Python - Edureka](img/33609cebe48674ce9e78f66f5f304c05.png)

*机器学习算法 Python 人工智能——edu reka*

上图显示了使用机器学习解决问题的不同算法。

监督学习可用于解决两种类型的机器学习问题:

1.  回归
2.  分类

要解决回归问题，您可以使用著名的线性回归算法。这里有一个从零开始的 [*线性回归算法博客*](https://www.edureka.co/blog/linear-regression-in-python/) 将帮助你理解它是如何工作的。

分类问题可以使用以下分类算法来解决:

1.  [逻辑回归](https://www.edureka.co/blog/logistic-regression-in-python/)
2.  决策图表
3.  随机森林
4.  [朴素贝叶斯分类器](https://www.edureka.co/blog/naive-bayes-tutorial/)
5.  支持向量机
6.  [K 个最近邻居](https://www.edureka.co/blog/k-nearest-neighbors-algorithm/)

无监督学习可用于解决聚类和关联问题。著名的聚类算法之一是 K-means 聚类算法。

你可以在 K-means 聚类上查看这个视频来了解更多。

**K 表示聚类算法| edu reka**



[https://www.youtube.com/embed/1XqG0kaJVHY?rel=0&showinfo=0](https://www.youtube.com/embed/1XqG0kaJVHY?rel=0&showinfo=0)﻿This Edureka video will help you learn the concepts of K-Means clustering and its implementation using python.

强化学习可以用来解决基于奖励的问题。著名的 Q 学习算法通常用于解决强化学习问题。

这里有一个关于强化学习的视频，它涵盖了强化学习的所有重要概念，以及一个使用 Python 的 Q-learning 的实际实现。

## 强化学习教程| Edureka



[https://www.youtube.com/embed/LzaWrmKL1Z4?rel=0&showinfo=0](https://www.youtube.com/embed/LzaWrmKL1Z4?rel=0&showinfo=0)In this video you will get an in-depth understanding of how reinforcement learning is used in the real world.

现在为了更好地理解整个机器学习流程，让我们使用 Python 来执行一个机器学习的实际实现。

## **用 Python 进行机器学习**

在本节中，我们将使用 Python 实现机器学习。让我们开始吧。

**问题陈述:**建立一个机器学习模型，通过学习过去的数据来预测明天是否会下雨。

**数据集描述:**该数据集包含大约 145，000 条来自澳大利亚多个气象站的每日天气条件观测数据。数据集大约有 24 个特征，我们将使用 23 个特征(预测变量)来预测目标变量，即“明天下雨”。

这个目标变量(RainTomorrow)将存储两个值:

1.  是:表示明天会下雨
2.  否:表示明天不会下雨

所以，这显然是一个分类问题。机器学习模型会将输出分为两类，是或否。

**逻辑:**建立分类模型，根据天气情况预测明天是否下雨。

既然目标已经明确，让我们开动脑筋，开始编码吧。

**第一步:导入所需的库**

```
# For linear algebra
import numpy as np
# For data processing
import pandas as pd

```

**第二步:加载数据集**

```
#Load the data set
df = pd.read_csv('. . . Desktop/weatherAUS.csv')
#Display the shape of the data set
print('Size of weather data frame is :',df.shape)
#Display data
print(df[0:5])

Size of weather data frame is : (145460, 24)
        Date         Location   MinTemp ... RainToday  RISK_MM  RainTomorrow
0   2008-12-01   Albury           13.4 ...         No             0.0                   No
1   2008-12-02   Albury            7.4 ...          No             0.0                   No
2   2008-12-03   Albury          12.9 ...          No             0.0                   No
3   2008-12-04   Albury            9.2 ...          No             1.0                   No
4   2008-12-05   Albury          17.5 ...          No             0.2                   No

```

**第三步:数据预处理**

```

# Checking for null values
print(df.count().sort_values())

[5 rows x 24 columns]
Sunshine 75625
Evaporation 82670
Cloud3pm 86102
Cloud9am 89572
Pressure9am 130395
Pressure3pm 130432
WindDir9am 134894
WindGustDir 135134
WindGustSpeed 135197
Humidity3pm 140953
WindDir3pm 141232
Temp3pm 141851
RISK_MM 142193
RainTomorrow 142193
RainToday 142199
Rainfall 142199
WindSpeed3pm 142398
Humidity9am 142806
Temp9am 143693
WindSpeed9am 143693
MinTemp 143975
MaxTemp 144199
Location 145460
Date 145460
dtype: int64

```

请注意输出，它显示前四列有超过 40%的空值，因此，最好是删除这些列。

在数据预处理过程中，总是需要删除不重要的变量。不必要的数据只会增加我们的计算量。因此，我们将删除“位置”变量和“日期”变量，因为它们对于预测天气并不重要。

我们还将删除“RISK_MM”变量，因为我们希望预测“RainTomorrow”和 RISK_MM(第二天的降雨量)可能会向我们的模型泄露一些信息。

```

df = df.drop(columns=['Sunshine','Evaporation','Cloud3pm','Cloud9am','Location','RISK_MM','Date'],axis=1)
print(df.shape)

(145460, 17)

```

接下来，我们将移除数据框中的所有空值。

```

#Removing null values
df = df.dropna(how='any')
print(df.shape)

(112925, 17)

```

删除空值后，我们还必须检查数据集是否有异常值。异常值是与其他观察值显著不同的数据点。异常值通常是由于收集数据时的误算造成的。

在下面的代码片段中，我们去掉了离群值:

```

from scipy import stats
z = np.abs(stats.zscore(df._get_numeric_data()))
print(z)
df= df[(z < 3).all(axis=1)]
print(df.shape)

[[0.11756741 0.10822071 0.20666127 ... 1.14245477 0.08843526 0.04787026]
[0.84180219 0.20684494 0.27640495 ... 1.04184813 0.04122846 0.31776848]
[0.03761995 0.29277194 0.27640495 ... 0.91249673 0.55672435 0.15688743]
...
[1.44940294 0.23548728 0.27640495 ... 0.58223051 1.03257127 0.34701958]
[1.16159206 0.46462594 0.27640495 ... 0.25166583 0.78080166 0.58102838]
[0.77784422 0.4789471 0.27640495 ... 0.2085487 0.37167606 0.56640283]]
(107868, 17)

```

接下来，我们将用“0”和“1”来代替“是”和“否”。

```

#Change yes and no to 1 and 0 respectvely for RainToday and RainTomorrow variable
df['RainToday'].replace({'No': 0, 'Yes': 1},inplace = True)
df['RainTomorrow'].replace({'No': 0, 'Yes': 1},inplace = True)

```

现在是时候将数据正常化，以避免在预测结果时出现任何偏差。为此，我们可以利用 sklearn 库中的 MinMaxScaler 函数。

```

from sklearn import preprocessing
scaler = preprocessing.MinMaxScaler()
scaler.fit(df)
df = pd.DataFrame(scaler.transform(df), index=df.index, columns=df.columns)
df.iloc[4:10]

MinTemp  MaxTemp  Rainfall  ...  WindDir9am_W  WindDir9am_WNW  WindDir9am_WSW
4   0.628342  0.696296    0.035714 ...         0.0                 0.0                                        0.0
5   0.550802  0.632099    0.007143 ...         1.0                 0.0                                        0.0
6   0.542781  0.516049    0.000000 ...         0.0                 0.0                                        0.0
7   0.366310  0.558025    0.000000 ...         0.0                 0.0                                        0.0
8   0.419786  0.686420    0.000000 ...         0.0                 0.0                                        0.0
9   0.510695  0.641975    0.050000 ...         0.0                 0.0                                        0.0

[6 rows x 62 columns]

```

**第四步:探索性数据分析(EDA)**

既然我们已经完成了数据集的预处理，那么是时候检查执行分析并确定将帮助我们预测结果的重要变量了。为此，我们将利用 sklearn 库中的 SelectKBest 函数:

```

#Using SelectKBest to get the top features!
from sklearn.feature_selection import SelectKBest, chi2
X = df.loc[:,df.columns!='RainTomorrow']
y = df[['RainTomorrow']]
selector = SelectKBest(chi2, k=3)
selector.fit(X, y)
X_new = selector.transform(X)
print(X.columns[selector.get_support(indices=True)])

Index(['Rainfall', 'Humidity3pm', 'RainToday'], dtype='object')

```

输出为我们提供了三个最重要的预测变量:

1.  降雨

2.  湿度下午 3 点

3.  今天下雨了

本演示的主要目的是让您了解机器学习是如何工作的，因此，为了简化计算，我们将只指定这些重要变量中的一个作为输入。

```

#The important features are put in a data frame
df = df[['Humidity3pm','Rainfall','RainToday','RainTomorrow']]

#To simplify computations we will use only one feature (Humidity3pm) to build the model

X = df[['Humidity3pm']]
y = df[['RainTomorrow']]

```

在上面的代码片段中，“X”和“y”分别表示输入和输出。

**第五步:建立机器学习模型**

在这一步，我们将通过使用训练数据集来建立机器学习模型，并通过使用测试数据集来评估模型的效率。

我们将使用以下算法构建分类模型:

1.  逻辑回归
2.  随机森林
3.  决策图表
4.  支持向量机

下面是每个分类模型的代码片段:

**逻辑回归**

```

#Logistic Regression
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
import time

#Calculating the accuracy and the time taken by the classifier
t0=time.time()
#Data Splicing
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.25)
clf_logreg = LogisticRegression(random_state=0)
#Building the model using the training data set
clf_logreg.fit(X_train,y_train)

#Evaluating the model using testing data set
y_pred = clf_logreg.predict(X_test)
score = accuracy_score(y_test,y_pred)

#Printing the accuracy and the time taken by the classifier
print('Accuracy using Logistic Regression:',score)
print('Time taken using Logistic Regression:' , time.time()-t0)

Accuracy using Logistic Regression: 0.8330181332740015
Time taken using Logistic Regression: 0.1741015911102295

```

**随机森林分类器**

```

#Random Forest Classifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split

#Calculating the accuracy and the time taken by the classifier
t0=time.time()
#Data Splicing
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.25)
clf_rf = RandomForestClassifier(n_estimators=100, max_depth=4,random_state=0)
#Building the model using the training data set
clf_rf.fit(X_train,y_train)

#Evaluating the model using testing data set
y_pred = clf_rf.predict(X_test)
score = accuracy_score(y_test,y_pred)

#Printing the accuracy and the time taken by the classifier
print('Accuracy using Random Forest Classifier:',score)
print('Time taken using Random Forest Classifier:' , time.time()-t0)

Accuracy using Random Forest Classifier: 0.8358363926280269
Time taken using Random Forest Classifier: 3.7179694175720215

```

**决策树分类器**

```

#Decision Tree Classifier
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split

#Calculating the accuracy and the time taken by the classifier
t0=time.time()
#Data Splicing
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.25)
clf_dt = DecisionTreeClassifier(random_state=0)
#Building the model using the training data set
clf_dt.fit(X_train,y_train)

#Evaluating the model using testing data set
y_pred = clf_dt.predict(X_test)
score = accuracy_score(y_test,y_pred)

#Printing the accuracy and the time taken by the classifier
print('Accuracy using Decision Tree Classifier:',score)
print('Time taken using Decision Tree Classifier:' , time.time()-t0)

Accuracy using Decision Tree Classifier: 0.831423591797382
Time taken using Decision Tree Classifier: 0.0849456787109375

```

**支持向量机**

```

#Support Vector Machine
from sklearn import svm
from sklearn.model_selection import train_test_split

#Calculating the accuracy and the time taken by the classifier
t0=time.time()
#Data Splicing
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.25)
clf_svc = svm.SVC(kernel='linear')

#Building the model using the training data set
clf_svc.fit(X_train,y_train)

#Evaluating the model using testing data set
y_pred = clf_svc.predict(X_test)
score = accuracy_score(y_test,y_pred)

#Printing the accuracy and the time taken by the classifier
print('Accuracy using Support Vector Machine:',score)
print('Time taken using Support Vector Machine:' , time.time()-t0)

Accuracy using Support Vector Machine: 0.7886676308080246
Time taken using Support Vector Machine: 88.42247271537781

```

除了支持向量机之外，所有的分类模型都给了我们大约 83-84 %的准确度分数。考虑到我们数据集的规模，精确度已经相当不错了。

因此，给自己一个鼓励，因为你现在知道如何通过使用机器学习来解决问题。

要了解更多关于机器学习的信息，请阅读这些博客:

1.  [什么是机器学习？面向初学者的机器学习](https://www.edureka.co/blog/what-is-machine-learning)
2.  [初学者机器学习教程](https://www.edureka.co/blog/machine-learning-tutorial/)
3.  [2019 年尝试的最新机器学习项目](https://www.edureka.co/blog/machine-learning-projects/)

现在我们来看一个更高级的概念，叫做深度学习。

在我们了解什么是深度学习之前，我们先了解一下机器学习的局限性。这些限制催生了深度学习的概念。

## **机器学习的局限性**

以下是机器学习的局限性:

1.  机器学习无法处理和加工**高维数据。**
2.  它不能用于**图像识别**和**物体检测**，因为它们需要实现高维数据
3.  机器学习的另一个主要挑战是告诉机器它应该寻找哪些重要特征，以便精确预测结果。这个过程叫做**特征提取**。特征提取是机器学习中的手动过程。

上述限制可以通过使用深度学习来解决。

## **为什么要深度学习？**

*   深度学习是我们能够克服特征提取挑战的唯一方法之一。这是因为深度学习模型能够学习自己专注于正确的特征，只需要最少的人工干预。

*   深度学习主要用于处理高维数据。它基于神经网络的概念，通常用于对象检测和图像处理。

现在我们来了解一下深度学习是如何工作的。

## **深度学习是如何工作的？**

*深度学习模仿了人脑的基本组成部分，称为脑细胞或神经元。受神经元的启发，人工神经元被开发出来。*

深度学习是基于生物神经元的功能，所以让我们了解一下我们如何在人工神经元(也称为感知机)中模仿这种功能:

![Biological Neuron - Artificial Intelligence With Python - Edureka](img/779b26cfe72f71b327c705c467aaf031.png)

*生物神经元 Python 人工智能——edu reka*

*   在生物神经元中，树突用于接收输入。这些输入在细胞体中相加，并通过轴突传递给下一个神经元。
*   类似于生物神经元，感知器接收多个输入，应用各种变换和功能，并提供输出。
*   人类大脑由多个连接的神经元组成，称为神经网络，类似地，通过组合多个感知机，我们开发了所谓的深度神经网络。

现在我们来了解一下深度学习到底是什么。

## **什么是深度学习？**

*“深度学习是一组统计机器学习技术，用于基于人工神经网络概念的* *来学习特征层次。”*

深度神经网络由以下几层组成:

1.  输入层
2.  隐藏层
3.  输出层

![What Is Deep Learning - Artificial Intelligence With Python - Edureka](img/d8205b9031889830e84d8a02c51463fa.png)

*什么是深度学习——用 Python 实现人工智能——edu reka*

在上图中，

*   第一层是接收所有输入的输入层
*   最后一层是提供所需输出的输出层
*   这些层之间的所有层称为隐藏层。
*   可以有 n 个隐藏层，隐藏层的数量和每层中感知器的数量将完全取决于您试图解决的用例。

深度学习用于高度计算的用例，如人脸验证、自动驾驶汽车等等。让我们通过看一个真实世界的用例来理解深度学习的重要性。

## **深度学习用例**

考虑一下 PayPal 如何使用深度学习来识别任何可能的欺诈活动。PayPal 处理了超过 1.7 亿客户的 40 亿笔交易，支付金额超过 2350 亿美元。

PayPal 使用机器学习和深度学习算法从客户的购买历史中挖掘数据，此外还审查存储在其数据库中的可能欺诈模式，以预测特定交易是否欺诈。

![Deep Learning Use Case - Artificial Intelligence With Python - Edureka](img/47e3bbbb505a48ab2f5d294b6c5741b8.png)

*深度学习用例 Python 人工智能——edu reka*

该公司已经依赖深度学习和机器学习技术大约 10 年了。最初，欺诈监控团队使用简单的线性模型。但多年来，该公司转向了一种更先进的机器学习技术，称为深度学习。

王柯 PayPal 的欺诈风险经理和数据科学家引用了:

“我们从更现代、更先进的机器学习中享受到的是，它能够消耗更多的数据，处理一层又一层的抽象，并能够‘看到’更简单的技术无法看到的东西，甚至人类也可能看不到。”

一个简单的线性模型能够消耗大约 20 个变量。然而，通过深度学习技术，人们可以运行数千个数据点。

王柯说:“这有很大的不同——你将能够分析更多的信息，识别更复杂的模式。”。

因此，通过实施深度学习技术，PayPal 最终可以分析数百万笔交易，以识别任何欺诈活动。

为了更好地理解深度学习，我们来理解一个感知机是如何工作的。

## **什么是感知器？**

感知器是用于分类线性数据的单层神经网络。感知器有 4 个重要组件:

1.  投入
2.  权重和偏差
3.  求和函数
4.  激活或转换功能

![Perceptron - Artificial Intelligence With Python - Edureka](img/2e0ce5c2072e918dfb782ec8b00af9e4.png)

*感知器 Python 人工智能——edu reka*

感知器背后的基本逻辑如下:

从输入层接收的输入(x)乘以其分配的权重 w。然后将相乘的值相加以形成加权和。输入的加权和以及它们各自的权重然后被应用于相关的激活函数。激活功能将输入映射到相应的输出。

### **深度学习中的权重和偏差**

为什么我们必须给每个输入分配权重？

一旦一个输入变量被输入到网络，一个随机选择的值被指定为该输入的权重。每个输入数据点的权重表明该输入在预测结果中的重要性。

另一方面，*偏差*参数允许您调整激活函数曲线，以获得精确的输出。

### **求和功能**

一旦输入被赋予某个权重，就取相应输入和权重的乘积。将所有这些乘积相加得到加权和。这是通过求和函数完成的。

### **激活功能**

激活函数的主要目的是将加权和映射到输出。激活函数如 tanh、ReLU、sigmoid 等都是变换函数的例子。

想了解更多关于感知器的功能，可以去看看这篇 *[深度学习:感知器学习算法](https://www.edureka.co/blog/perceptron-learning-algorithm/)* 的博客。

现在让我们来理解多层感知器的概念。

**为什么要用多层感知器？**

单层感知器不能处理高维数据，也不能用于分类非线性可分离数据。

因此，涉及大量参数的复杂问题可以通过使用多层感知器来解决。

## **什么是多层感知器？**

多层感知器是一种包含一个或多个隐藏层的分类器，它基于前馈人工神经网络。在前向网络中，每个神经网络层都完全连接到下一层。

## **![Multilayer Perceptron - Artificial Intelligence With Python - Edureka](img/b8b8f213a5f7abb17ee0d3321333bde5.png)**

*多层感知器 Python 人工智能——edu reka*

## **多层感知器是如何工作的？**

在多层感知器中，在开始时分配给每个输入的权重被更新，以便最小化计算中的合成误差。

这样做是因为最初我们为每个输入随机分配权重值，这些权重值显然不会给出我们想要的结果，因此有必要以输出精确的方式更新权重。

这个更新权重和训练网络的过程被称为*反向传播*。

反向传播是多层感知器背后的逻辑。 ***该方法用于更新权重，使最重要的输入变量获得最大的权重，从而减少计算输出时的误差。***

这就是人工神经网络背后的逻辑。如果你想了解更多，请务必阅读这篇文章，[神经网络教程——多层感知器](https://www.edureka.co/blog/neural-network-tutorial/)博客。

## **用 Python 进行深度学习**

为了总结深度学习是如何工作的，让我们来看看用 Python 实现深度学习。

**问题陈述:**研究一个银行信贷数据集，根据过去的数据确定一笔交易是否欺诈。

**数据集描述:**数据集描述了 2013 年欧洲持卡人的交易。它包含两天的交易详细信息，其中 284，807 笔交易中有 492 笔欺诈活动。

**逻辑:**建立一个神经网络，可以根据过去的交易将交易分类为欺诈或不欺诈。

现在，您已经知道了本次演示的目标，让我们继续进行演示。

步骤 1:导入必要的包

```

#Import requires packages

import numpy as np
import pandas as pd
import os
os.environ["TF_CPP_MIN_LOG_LEVEL"]="3"
from sklearn.utils import shuffle
import matplotlib.pyplot as plt

# Import Keras, Dense, Dropout
from keras.models import Sequential
from keras.layers import Dense
from keras.layers import Dropout

import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import MinMaxScaler
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score
, fbeta_score, classification_report, confusion_matrix, precision_recall_curve, roc_auc_score
, roc_curve

```

步骤 2:加载数据集

```

# Import the dataset
df_full = pd.read_csv('C://Users//NeelTemp//Desktop//ai with python//creditcard.csv')

# Print out first 5 row of the data set
print(df_full.head(5))

    Time          V1                V2            V3          ...    V27              V28         Amount    Class
0    0.0    -1.359807     -0.072781    2.536347    ... 0.133558    -0.021053      149.62        0
1    0.0     1.191857       0.266151    0.166480   ... -0.008983     0.014724      2.69            0
2    1.0    -1.358354     -1.340163    1.773209   ... -0.055353    -0.059752      378.66        0
3    1.0    -0.966272     -0.185226    1.792993   ... 0.062723      0.061458      123.50         0
4    2.0    -1.158233      0.877737    1.548718   ... 0.219422      0.215153      69.99           0

```

在上面的描述中，目标变量是“类”变量。它可以包含两个值:

1.  类别 0:表示交易不是欺诈性的
2.  类别 1:表示交易是欺诈性的

其余的变量是预测变量，将帮助我们了解交易是否是欺诈性的。

```

# Count the number of samples for each class (Class 0 and Class 1)
print(df_full.Class.value_counts())

0   284315
1   492

Name: Class, dtype: int64

```

上面的输出显示，我们有大约 284，000 个非欺诈性交易和“492”个欺诈性交易。这两个类别之间的差异是巨大的，这使得我们的数据集非常不平衡。因此，我们必须以欺诈性交易与非欺诈性交易数量平衡的方式对数据集进行抽样。

为此，我们可以利用一种叫做[分层抽样](https://www.edureka.co/blog/statistics-and-probability/#Sampling%20Techniques)的统计抽样技术。

**第三步:数据准备**

```

#Sort the dataset by "class" to apply stratified sampling

df_full.sort_values(by='Class', ascending=False, inplace=True)

```

接下来，我们将删除时间列，因为不需要它来预测输出。

```

# Remove the "Time" coloumn
df_full.drop('Time', axis=1, inplace=True)

# Create a new data frame with the first "3000" samples
df_sample = df_full.iloc[:3000, :]

# Now count the number of samples for each class
print(df_sample.Class.value_counts())

0   2508
1   492
Name: Class, dtype: int64

```

我们的数据集现在看起来很平衡。

```

#Randomly shuffle the data set

shuffle_df = shuffle(df_sample, random_state=42)

```

**第四步:数据拼接**

*数据拼接是将数据集拆分成训练和测试数据的过程。*

```

# Spilt the dataset into train and test data frame
df_train = shuffle_df[0:2400]
df_test = shuffle_df[2400:]

# Spilt each dataframe into feature and label
train_feature = np.array(df_train.values[:, 0:29])
train_label = np.array(df_train.values[:, -1])
test_feature = np.array(df_test.values[:, 0:29])
test_label = np.array(df_test.values[:, -1])

# Display the size of the train dataframe
print(train_feature.shape)

(2400, 29)

# Display the size of test dataframe
print(train_label.shape)

(2400,)

```

**第五步:数据标准化**

```

# Standardize the features coloumns to increase the training speed
scaler = MinMaxScaler()
scaler.fit(train_feature)
train_feature_trans = scaler.transform(train_feature)
test_feature_trans = scaler.transform(test_feature)

# A function to plot the learning curves
def show_train_history(train_history, train, validation):
plt.plot(train_history.history[train])
plt.plot(train_history.history[validation])
plt.title('Train History')
plt.ylabel(train)
plt.xlabel('Epoch')
plt.legend(['train', 'validation'], loc='best')
plt.show()

```

**步骤 6:构建神经网络**

在这个演示中，我们将构建一个包含 3 个全连接层的神经网络。第一和第二层具有 200 个神经元单元，ReLU 作为激活函数，第三层，即输出层具有单个神经元单元。

为了构建神经网络，我们将使用我们之前讨论过的 Keras 包。模型类型将是顺序的，这是在 Keras 中构建模型的最简单的方法。在顺序模型中，每一层都以这样的方式分配权重，即对应于前一层的下一层中的权重。

```

#Select model type
model = Sequential()

```

接下来，我们将使用 add()函数添加密集层。“密集”是最基本的图层类型，适用于大多数情况。密集层中的所有节点被设计成使得前一层中的节点连接到当前层中的节点。

```

# Adding a Dense layer with 200 neuron units and ReLu activation function
model.add(Dense(units=200,
input_dim=29,
kernel_initializer='uniform',
activation='relu'))

# Add Dropout
model.add(Dropout(0.5))

```

放弃是一种正则化技术，用于避免神经网络中的过度拟合。在这种技术中，随机选择的神经元在训练期间被丢弃。

```

# Second Dense layer with 200 neuron units and ReLu activation function
model.add(Dense(units=200,
kernel_initializer='uniform',
activation='relu'))

# Add Dropout
model.add(Dropout(0.5))

# The output layer with 1 neuron unit and Sigmoid activation function
model.add(Dense(units=1,
kernel_initializer='uniform',
activation='sigmoid'))

# Display the model summary
print(model.summary())

Layer (type) Output Shape Param #
=================================================================
dense_1 (Dense) (None, 200) 6000
_________________________________________________________________
dropout_1 (Dropout) (None, 200) 0
_________________________________________________________________
dense_2 (Dense) (None, 200) 40200
_________________________________________________________________
dropout_2 (Dropout) (None, 200) 0
_________________________________________________________________
dense_3 (Dense) (None, 1) 201
=================================================================
Total params: 46,401
Trainable params: 46,401
Non-trainable params: 0

```

对于优化，我们将使用 Adam optimizer(Keras 内置的)。优化器用于在模型训练期间更新权重和偏置参数的值。

```

# Using 'Adam' to optimize the Accuracy matrix
model.compile(loss='binary_crossentropy', optimizer='adam',
metrics=['accuracy'])

# Fit the model
# number of epochs = 200 and batch size = 500
train_history = model.fit(x=train_feature_trans, y=train_label,
validation_split=0.8, epochs=200,
batch_size=500, verbose=2)

Train on 479 samples, validate on 1921 samples
Epoch 1/200
- 1s - loss: 0.6916 - acc: 0.5908 - val_loss: 0.6825 - val_acc: 0.8360
Epoch 2/200
- 0s - loss: 0.6837 - acc: 0.7933 - val_loss: 0.6717 - val_acc: 0.8360
Epoch 3/200
- 0s - loss: 0.6746 - acc: 0.7996 - val_loss: 0.6576 - val_acc: 0.8360
Epoch 4/200
- 0s - loss: 0.6628 - acc: 0.7996 - val_loss: 0.6419 - val_acc: 0.8360
Epoch 5/200
- 0s - loss: 0.6459 - acc: 0.7996 - val_loss: 0.6248 - val_acc: 0.8360

# Display the accuracy curves for training and validation sets
show_train_history(train_history, 'acc', 'val_acc')

```

![Accuracy Plot - Artificial Intelligence With Python - Edureka](img/8d2dee06e8e55a2936a6b2293135e662.png)

*准确度图 Python 人工智能——edu reka*

```

# Display the loss curves for training and validation sets
show_train_history(train_history, 'loss', 'val_loss')

```

**![Loss Plot - Artificial Intelligence With Python - Edureka](img/261a5a92bb137ce17604be8bfe90a4ca.png)**

*损失图–Python 人工智能–edu reka*

**步骤 7:模型评估**

```

# Testing set for model evaluation
scores = model.evaluate(test_feature_trans, test_label)

# Display accuracy of the model
print('n')
print('Accuracy=', scores[1])

Accuracy= 0.98

prediction = model.predict_classes(test_feature_trans)

df_ans = pd.DataFrame({'Real Class': test_label})
df_ans['Prediction'] = prediction

df_ans['Prediction'].value_counts()

df_ans['Real Class'].value_counts()

cols = ['Real_Class_1', 'Real_Class_0'] # Gold standard
rows = ['Prediction_1', 'Prediction_0'] # Diagnostic tool (our prediction)

B1P1 = len(df_ans[(df_ans['Prediction'] == df_ans['Real Class']) & (df_ans['Real Class'] == 1)])
B1P0 = len(df_ans[(df_ans['Prediction'] != df_ans['Real Class']) & (df_ans['Real Class'] == 1)])
B0P1 = len(df_ans[(df_ans['Prediction'] != df_ans['Real Class']) & (df_ans['Real Class'] == 0)])
B0P0 = len(df_ans[(df_ans['Prediction'] == df_ans['Real Class']) & (df_ans['Real Class'] == 0)])

conf = np.array([[B1P1, B0P1], [B1P0, B0P0]])
df_cm = pd.DataFrame(conf, columns=[i for i in cols], index=[i for i in rows])
f, ax = plt.subplots(figsize=(5, 5))
sns.heatmap(df_cm, annot=True, ax=ax, fmt='d')
plt.show()

```

![Heatmap - Artificial Intelligence With Python - Edureka](img/cfe48c83581b772cba5adfca18f6a1c7.png)

*热图——使用 Python 的人工智能——edu reka*

```

# Making x label be on top is common in textbooks.
ax.xaxis.set_ticks_position('top')

print('Total number of test cases: ', np.sum(conf))

Total number of test cases: 600

# Model summary function
def model_efficacy(conf):
total_num = np.sum(conf)
sen = conf[0][0] / (conf[0][0] + conf[1][0])
spe = conf[1][1] / (conf[1][0] + conf[1][1])
false_positive_rate = conf[0][1] / (conf[0][1] + conf[1][1])
false_negative_rate = conf[1][0] / (conf[0][0] + conf[1][0])

print('Total number of test cases: ', total_num)

Total number of test cases: 600

print('G = gold standard, P = prediction')

# G = gold standard; P = prediction
print('G1P1: ', conf[0][0])
print('G0P1: ', conf[0][1])
print('G1P0: ', conf[1][0])
print('G0P0: ', conf[1][1])
print('--------------------------------------------------')
print('Sensitivity: ', sen)
print('Specificity: ', spe)
print('False_positive_rate: ', false_positive_rate)
print('False_negative_rate: ', false_negative_rate)

```

输出:

```

G = gold standard, P = prediction
G1P1: 74
G0P1: 5
G1P0: 7
G0P0: 514
--------------------------------------------------
Sensitivity: 0.9135802469135802
Specificity: 0.9865642994241842
False_positive_rate: 0.009633911368015413
False_negative_rate: 0.08641975308641975

```

正如你所看到的，我们已经达到了 98%的准确率，这是非常好的。

这就是深度学习演示的全部内容。

现在让我们集中在最后一个模块，我将介绍自然语言处理。

## 自然语言处理是什么意思？

自然语言处理(NLP)是一门从自然语言文本中获取有用见解以进行文本分析和文本挖掘的科学。

NLP 使用计算机科学和人工智能的概念来研究数据并从中获取有用的信息。它是计算机和智能手机用来理解我们的语言，包括口语和书面语。

在我们了解 NLP 在哪里使用之前，让我澄清一个常见的误解。人们经常会混淆文本挖掘和自然语言处理。

看看这个由 Edureka 提供的 [NLP 认证](https://www.edureka.co/python-natural-language-processing-course)课程，将你的人工智能技能提升到下一个水平

### **文本挖掘和 NLP 有什么区别？**

*   文本挖掘是从文本中获取有用信息的过程。
*   自然语言处理是一种用于执行文本挖掘和文本分析的技术。

因此，我们可以说文本挖掘可以通过使用各种 NLP 方法来进行。

现在我们来了解一下 NLP 用在哪里。

## **自然语言处理应用**

以下是利用 NLP 技术的真实应用程序列表:

*   **感性分析:**通过实施 NLP 技术巨头如亚马逊和网飞，深入了解他们的客户，以改进他们的产品并提出更好的建议。
*   聊天机器人:聊天机器人在客户服务领域越来越受欢迎。一个很受欢迎的例子是 HDFC 聊天机器人伊娃，她处理了超过 300 万个客户查询，与超过 50 万个独立用户进行了互动，并进行了超过 100 万次对话。
*   **语音识别:**自然语言处理已经广泛应用于语音识别，我们都知道 Alexa、Siri、谷歌助手和 Cortana。都是 NLP 的应用。
*   **机器翻译:**流行的谷歌翻译器使用自然语言处理来处理和翻译一种语言到另一种语言。它也用于拼写检查，关键字搜索，信息提取。
*   **广告匹配:** NLP 也用于广告匹配，根据搜索历史推荐广告。

现在让我们来理解 NLP 中的重要概念。

## **自然语言处理中的术语**

在本节中，我将介绍 NLP 下的所有基本术语。以下过程用于分析自然语言，以便获得一些有意义的见解:

### **标记化**

标记化基本上意味着将数据分解成更小的块或标记，以便于分析。

例如，句子“记号很简单”可以分解成以下记号:

1.  代币
2.  是
3.  简单的

通过进行标记化，你可以理解句子中每个标记的重要性。

### **词干**

*词干化就是把单词的前缀和后缀去掉，只考虑词根的过程。*

![Stemming - Artificial Intelligence With Python - Edureka](img/87433908da5858dee36bc16c48b4538b.png)

*词干处理——使用 Python 的人工智能——edu reka*

我们用一个例子来理解这个。如图所示，单词，

1.  侦查
2.  探测
3.  发现
4.  侦查

都可以被削减到它们的词根，即**检测**。词干有助于编辑这样的单词，从而使分析文档变得更简单。然而，这个过程在某些情况下是成功的。因此，使用了另一个称为词汇化的过程。

### **词汇化**

词汇化类似于词干化，但是，它更有效，因为它考虑了单词的形态分析。词汇化的输出是一个合适的词。

词元化的一个例子是，通过使用词元化，单词“gone”、“going”和“got”都可以归结为单词“go”。

### **停止字**

停用词是任何语言中的一组常用词。停用词对于文本分析至关重要，为了更好地理解任何文档，必须将其移除。其逻辑是，如果常用词从文档中删除，那么我们可以专注于最重要的词。

![Stop Words - Artificial Intelligence With Python - Edureka.jpg](img/16e709675aa42b70767548772ff1205f.png)

*Stop Words——用 Python 实现人工智能——edu reka*

比如说，你想做一个草莓奶昔。如果你打开谷歌，输入“如何制作草莓奶昔”，你会得到“如何制作”草莓奶昔的结果。即使你只想要草莓奶昔的结果。这些词被称为停用词。在进行任何分析之前，最好是去掉这些词。

如果你想了解更多关于自然语言处理的知识，你可以观看我们的自然语言处理专家的视频。

**【自然语言处理】&文本挖掘教程使用 NLTK | edu reka**



[https://www.youtube.com/embed/05ONoGfmKvA?rel=0&showinfo=0](https://www.youtube.com/embed/05ONoGfmKvA?rel=0&showinfo=0)This Edureka video will provide you with a comprehensive and detailed knowledge of Natural Language Processing, popularly known as NLP.

就这样，我们用 Python 博客结束了这个人工智能。如果你想了解更多关于人工智能的知识，你可以看看这些博客:

1.  人工智能——它是什么，有什么用处？
2.  [人工智能教程:关于 AI 你需要知道的一切](https://www.edureka.co/blog/artificial-intelligence-tutorial/)
3.  [AI vs 机器学习 vs 深度学习](https://www.edureka.co/blog/ai-vs-machine-learning-vs-deep-learning/)
4.  [人工智能的十大好处](https://www.edureka.co/blog/benefits-of-artificial-intelligence/)
5.  [人工智能应用:10 大现实世界人工智能应用](https://www.edureka.co/blog/artificial-intelligence-applications/)

如果你希望注册一门关于人工智能和机器学习的完整课程，Edureka 有一个专门策划的 [**机器学习工程师硕士项目**](https://www.edureka.co/masters-program/machine-learning-engineer-training) ，它将使你精通监督学习、非监督学习和自然语言处理等技术。它包括人工智能&机器学习方面的最新进展和技术方法的培训，如深度学习、图形模型和强化学习。