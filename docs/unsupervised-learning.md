# 什么是无监督学习，它是如何工作的？

> 原文：<https://www.edureka.co/blog/unsupervised-learning/>

就在几十年前，教你的电脑并期望它给出聪明的答案对我们所有人来说都是一个梦想。但是现在，随着 [**机器学习**](https://www.edureka.co/blog/what-is-machine-learning/) 的崛起，一切都变了。我甚至可以说，机器已经变得比我们更聪明了。在本文中，我们将讨论以下主题:

*   [机器学习概述](#overview)
*   [什么是无监督学习？](#unsupervised)
*   [为什么重要？](#importance)
*   [无监督学习的类型](#types)
*   [无监督学习的应用](#apps)
*   [监督学习与非监督学习](#versus)
*   [无监督学习的弊端](#disadv)

因此，深入研究一下，了解无监督机器学习的一切。我们开始吧！:)

## **机器学习概述**

![Icon image](img/2e0299794b40d672bb6b591c4cbf5abc.png)机器学习，用最简单的话来说，就是 **教你的机器一些** 的东西。你 * 收集并清理数据**创建算法**从数据中教会[算法](https://www.edureka.co/blog/machine-learning-algorithms/)本质模式 * 然后 * 期待算法给你一个有帮助的答案 * 。如果算法不辜负你的期望，你就成功教会了你的算法。如果没有，就废弃一切，从头开始。这就是这里的工作方式。如果你正在寻找一个正式的定义，机器学习就是创建模型的过程，这些模型可以执行特定的任务，而不需要人类**明确地对它进行编程**来做一些事情。

基于算法的创建方式，有 3 种类型的机器学习。他们是:

*   **[监督学习](https://www.edureka.co/blog/machine-learning-tutorial/#SupervisedLearning)–**你监督学习过程，这意味着你在这里收集的数据被标记，因此你知道什么输入需要映射到什么输出。如果你的算法在给你答案时出错，这有助于你纠正它。
*   **无监督学习**——这里收集的数据没有标签，你无法确定输出结果。因此，您对算法进行建模，使其能够理解数据中的模式，并输出所需的答案。当算法学习时，你不干涉。
*   [**强化学习**](https://www.edureka.co/blog/q-learning/)——这种学习没有数据，也不教算法任何东西。你给算法建模，让它与环境互动，如果算法做得好，你奖励它，否则惩罚它。随着不断的互动和学习，对于分配给它的问题，它会从不好变得最好。

现在我们知道了什么是机器学习和不同类型的机器学习，让我们深入讨论这里的实际主题，并回答什么是无监督学习？无监督学习用在哪里？无监督学习算法等等。

## **什么是无监督学习？**

![](img/1c8f8a874e6aaee6e031fbdf17ccb336.png)

如前所述，无监督学习可以被认为是**自我学习**，其中算法可以在没有任何标签的数据集中找到之前**未知的模式**。它有助于建模概率密度函数，发现数据中的异常，等等。举个简单的例子，想象一个学生有课本和所有需要学习的材料，但是没有老师指导。最终，学生将不得不自学才能通过考试。这种自我学习是我们对机器的无监督学习。

让我给你一个现实生活中的例子，说明无监督学习可能已经被你用来学习一些东西。

**无监督学习的例子**

假设你一生中从未看过板球比赛，你的朋友邀请你去他们家看印度和澳大利亚的比赛。你不知道板球是什么，但只是为了你的朋友，你说好，和他们一起去。比赛开始了，你只是坐在那里，一片空白。您的朋友正在享受 Virat Kohli 的游戏方式，并希望加入其中。这是你开始了解这个游戏的时候。你分析屏幕并得出一些结论，你可以用这些结论来更好地理解游戏。

![](img/0e6e12025ae29708b6dc6208bde81c34.png)

*   有两个队穿着蓝色和黄色的球衣。因为 Virat Kohli 属于印度，你在屏幕上看到印度的得分，你得出结论印度有蓝色球衣，这使得澳大利亚有黄色球衣。
*   球场上有不同类型的球员。2 属于印度的人手中拿着球棒，表示他们正在击球。有人跑上去投球，使他成为投球手。大约有 9 名球员在球场周围试图阻止球到达球场的边界。有人在三柱门后和 2 名裁判员管理比赛。
*   如果球击中了三柱门，或者球被守场员接住，击球手出局，必须走回来。
*   Virat Kohli 的球衣背面有 18 号和他的名字，如果这个球员得了 4 分或 6 分，你需要为他欢呼。

你一个接一个地观察，现在知道当三柱门倒下时，什么时候该欢呼，什么时候该嘘。从一无所知到知道板球的基本知识，你现在可以和你的朋友一起享受比赛了。

这里发生了什么？你有学习板球基础知识所需的所有材料。电视，你的朋友何时为谁加油。这让你在没有任何人指导你的情况下自己学习板球。这是无监督学习遵循的原则。因此，理解了什么是无监督学习之后，让我们转而理解是什么让它在机器学习领域如此重要。

## 为什么它很重要？

那么，无监督学习帮助我们获得了什么？让我告诉你关于它的一切。

*   无监督学习算法在未标记的数据集上工作，并发现我们以前不知道的模式。
*   如果我们需要对元素进行分类或者找到它们之间的关联,获得的这些模式是很有帮助的。
*   他们还可以帮助我们发现数据中的异常和缺陷。

最后也是最重要的，我们收集的数据通常是未标记的，这使得我们在使用这些算法时更容易工作。

现在我们知道了重要性，让我们继续前进，了解不同类型的无监督学习。

## **无监督学习的类型**

无监督学习主要分为两种类型:

*   **聚类**
*   **关联**

聚类是一种无监督学习，在这种学习中，您可以在正在处理的数据中找到模式。可能是形状、大小、颜色等等。可用于对数据项分组或创建聚类。下面讨论了一些流行的聚类算法:

**![Clustering Algorithms - Data Science Tutorial - Edureka](img/cc338820c1574d7767b4ec9c9650901a.png)**

*   **层次聚类**–该算法基于数据集中不同数据点之间的相似性来构建聚类。它检查数据点的各种特征，并寻找它们之间的相似性。如果发现数据点相似，则将它们分组在一起。这一直持续到数据集被分组，这为这些聚类中的每一个创建了一个层次结构。
*   [**K-Means 聚类**](https://www.edureka.co/blog/k-means-clustering-algorithm/)–这种算法一步一步地工作，主要目标是实现具有标签来识别它们的聚类。该算法通过计算聚类的质心并确保该质心和新数据点之间的距离尽可能小，来创建尽可能同质的不同数据点的聚类。数据点和质心之间的最小距离决定了它属于哪个聚类，同时确保这些聚类不会相互交错。质心就像星团的心脏。这最终为我们提供了可以根据需要进行标记的集群。

![K-means - Artificial Intelligence Algorithms - Edureka](img/da7b4417a7d5cb72953fec0ab091d594.png)

*   **[K-NN 聚类](https://www.edureka.co/blog/knn-algorithm-in-r/)–**这可能是最简单的机器学习算法，因为该算法并不真正学习，而是根据已经存储的数据集对新数据点进行分类。这种算法也被称为懒惰学习器，因为它只在给定算法一个新的数据点时才学习。它适用于较小的数据集，因为大型数据集需要时间来学习。

关联是一种无监督的学习，在这种学习中，你可以找到一个数据项与另一个数据项之间的依赖关系，并对它们进行映射，从而帮助你更好地获利。下面讨论关联规则挖掘中的一些流行算法:

![association-rules-apriori-algorithm](img/8e0f4ff6e87bdf8d10c31c013a079034.png)

*   **[Apriori 算法](https://www.edureka.co/blog/apriori-algorithm/)–**Apriori 算法是一种基于广度优先搜索的算法，用于计算项目之间的支持度。这种支持基本上映射了一个数据项与另一个数据项的依赖关系，这可以帮助我们理解什么数据项影响另一个数据项发生某些事情的可能性。例如，面包影响购买者购买牛奶和鸡蛋。因此，地图有助于增加商店的利润。这种映射可以使用这种算法来学习，这种算法产生关于其输出的规则。
*   **FP-Growth Algorithm–**频率模式(FP)算法查找重复出现的模式的计数，将其添加到表格中，然后查找最可能的项目，并将其设置为树的根。然后将其他数据项添加到树中，并计算支持度。如果该特定分支未能满足支持度的阈值，则将其修剪掉。一旦所有的迭代都完成了，将创建一个带有该项目的根的树，然后使用它来制定关联规则。该算法比 Apriori 算法更快，因为支持度是随着迭代次数的增加而计算和检查的，而不是创建规则并从数据集中检查支持度。

既然你对这两种无监督学习有了清楚的了解，现在让我们了解一下无监督学习的一些应用。

## **无监督学习的应用**

无监督学习以多种方式提供帮助，可用于解决各种现实世界的问题。

*   它们有助于我们理解可用于根据各种特征对数据点进行聚类的模式。
*   理解数据集中我们最初无法检测到的各种缺陷。
*   它们有助于根据彼此的依赖关系来映射各种项目。
*   通过删除机器学习中不需要的特征来清理数据集。

这最终会带来对我们有用的应用。下面讨论使用无监督学习算法的某些例子:

*   AirBnB 该应用程序使用无监督学习，用户查询他或她的需求，Airbnb 学习这些模式，并推荐属于同一组或群的住宿和体验。
*   **亚马逊**–亚马逊也使用无监督学习来学习顾客的购买，并一起推荐最常购买的产品，这是关联规则挖掘的一个例子。
*   **信用卡欺诈检测**–无监督学习算法学习用户的各种模式以及他们对信用卡的使用。如果卡被用在与行为不符的地方，就会发出警报，可能被标记为欺诈，并会打电话给你，以确认是否是你在使用该卡。

这些是无监督学习算法大放异彩并显示其勇气的一些应用。既然我们已经完成了非监督学习的应用，让我们继续讨论监督学习和非监督学习的区别。

## **监督学习与非监督学习**

| **参数** | **监督学习** | **无监督学习** |
| 数据集 | 带标签的数据集 | 未标记的数据集 |
| 学习方法 | 引导式学习 | 该算法使用数据集进行自我学习 |
| 复杂度 | 更简单的方法 | 计算复杂 |
| 精度 | 更精确 | 不太准确 |

## **无监督学习的缺点**

即使无监督学习在许多众所周知的应用程序中使用，并且工作出色，它仍然有许多缺点。

*   由于数据集未标记，因此无法获得数据排序的方式或方法。
*   它们可能不太准确，因为输入数据是未知的，也没有被让机器输入数据的人标注出来。
*   由算法获得的信息可能不总是对应于我们需要的输出类。
*   用户必须理解并映射用相应标签获得的输出。

这些基本上是你在使用无监督学习算法时可能面临的主要缺点。现在，让我们继续，总结你在文章中学到的一切。

我们概述了什么是[机器学习](https://www.edureka.co/blog/machine-learning-tutorial/)及其各种类型。然后我们深入了解了无监督学习是什么，为什么它如此重要。后来，我们经历了各种类型的无监督学习，即聚类和关联挖掘。之后，我们讨论了各种算法、无监督学习的应用、监督学习和无监督学习之间的差异以及使用无监督学习算法时可能面临的不利因素。

这就把我们带到了文章的结尾。我希望它已经帮助你以一种清晰而精确的方式理解了什么是无监督学习。下次再见，学习愉快！

*既然你已经知道了**无监督学习**，那就去看看 Edureka 的 [**机器学习工程师硕士项目**](https://www.edureka.co/masters-program/machine-learning-engineer-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*Edureka 的 [**机器学习工程师硕士项目**](https://www.edureka.co/masters-program/machine-learning-engineer-training) 课程是为想成为机器学习工程师的学生和专业人士设计的。本课程旨在让你精通监督学习、非监督学习和自然语言处理等技术。它包括人工智能&机器学习方面的最新进展和技术方法的培训，如深度学习、图形模型和强化学习。*

*有问题吗？请在这个“**的评论区提一下，什么是无监督学习，它是如何工作的？**“博客，我们会尽快回复您。*