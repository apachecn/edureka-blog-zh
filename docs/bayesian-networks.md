# 如何用 Python 实现贝叶斯网络？–举例说明贝叶斯网络

> 原文：<https://www.edureka.co/blog/bayesian-networks/>

贝叶斯网络已经形成了提供有限信息和资源的复杂问题。它正在人工智能和机器学习等时代最先进的技术中实现。拥有这样一个系统是当今以技术为中心的世界的需要。记住这一点，这篇文章完全致力于贝叶斯网络的工作，以及如何应用它们来解决错综复杂的问题。

要获得人工智能和机器学习的深入知识，可以报名参加 Edureka 提供的全天候支持和终身访问的直播 [***机器学习工程师硕士项目***](https://www.edureka.co/masters-program/machine-learning-engineer-training) 。

以下是我将在这篇博客中涉及的话题列表:

1.  [什么是贝叶斯网络？](#What%20is%20a%20Bayesian%20Network)
2.  [什么是有向无环图？](#What%20Is%20A%20Directed%20Acyclic%20Graph)
3.  [贝叶斯网络背后的数学](#Math%20Behind%20Bayesian%20Networks)
4.  [通过示例了解贝叶斯网络](#Understanding%20Bayesian%20Networks%20with%20an%20example)
5.  [用 Python 实现贝叶斯网络](#Implementing%20Bayesian%20Networks%20In%20Python)
6.  [贝叶斯网络应用](#Bayesian%20Networks%20Application)

## **什么是贝叶斯网络？**

贝叶斯网络属于概率图形建模(PGM)技术的范畴，该技术通过使用**概率**的概念来计算不确定性。贝叶斯网络通常被称为信念网络，它通过使用 **有向无环图** (DAG)来对不确定性建模。

这给我们带来了一个问题:

## **什么是有向无环图？**

有向非循环图用于表示贝叶斯网络，并且像任何其他统计图一样，DAG 包含一组节点和链接，其中链接表示节点之间的关系。

![Directed Acyclic Graphs - Bayesian Networks - Edureka](img/e8bd42b24f2099fe1315ec36c42616d0.png)

这里的节点代表随机变量，边定义这些变量之间的关系。但是这些图表模拟了什么呢？您可以从 DAG 获得什么输出？

DAG 基于每个随机变量的*条件概率分布* (CDP)对事件发生的不确定性进行建模。一个*条件概率表* (CPT)被用来表示网络中每个变量的 CPD。

在我们继续前进之前，让我们理解贝叶斯网络背后的基本数学。

## **贝叶斯网络背后的数学**

如前所述，贝叶斯模型基于简单的概率概念。那么我们来理解一下条件概率和联合概率分布是什么意思。

### **什么是联合概率？**

联合概率是两个或两个以上事件同时发生的统计量，即 P(A，B，C)，事件 A，B，C 发生的概率。它可以表示为两个或两个以上事件交叉发生的概率。

### **什么是条件概率？**

事件 X 的条件概率是在事件 Y 已经发生的情况下，事件发生的概率。

p(X| Y)是事件 X 发生的概率，假设事件 Y 发生。

*   如果 X 和 Y 是相关事件，则条件概率的表达式由以下给出: *P (X| Y) = P (X 和 Y) / P (Y)*
*   如果 A 和 B 是独立事件，则条件概率的表达式由以下给出: *P(X| Y) = P (X)*

要了解更多关于统计和概率的概念，你可以浏览这个，[关于统计和概率你需要知道的一切](https://www.edureka.co/blog/statistics-and-probability/) 的博客。

现在让我们看一个例子来理解贝叶斯网络是如何工作的。

## **贝叶斯网络示例**

让我们假设我们正在创建一个贝叶斯网络，它将对学生的考试分数(m)进行建模。分数将取决于:

1.  考试水平(e):这是一个离散变量，可以有两个值，(难，容易)

2.  学生的智商(I):一个离散变量，可以取两个值(高，低)

分数将会预测他/她是否会被大学录取。

智商也能预测学生的能力倾向分数。

有了这些信息，我们就可以建立一个贝叶斯网络来模拟学生在考试中的表现。贝叶斯网络可以表示为 DAG，其中每个节点表示预测学生表现的变量。

![Bayesian Networks Example - Bayesian Networks - Edureka](img/ae980b39866dbf8b3bd0a7f847521d5e.png)

上面我已经通过 DAG 和条件概率表表示了这种分布。我们现在可以计算这 5 个变量的联合概率分布，即条件概率的乘积:

![Joint Probability Distribution - Bayesian Networks - Edureka](img/159490f3406cf4a6e7afe1ab8a1e7b33.png)

这里，

*   p(a | m)代表学生根据分数被录取的条件概率。

*   p(m | I，e)代表学生分数的条件概率，给定他的智商水平和考试水平。

*   p(i)表示他的智商水平(高或低)的概率

*   p(e)表示考试水平的概率(难或易)

*   p(s | i)表示根据他的智商水平，他的能力得分的条件概率

DAG 清楚地显示了每个变量(节点)如何依赖于其父节点，即学生的分数依赖于考试水平(父节点)和智商水平(父节点)。同样，能力倾向分数取决于智商水平(父节点)，最后，他能否被大学录取取决于他的分数(父节点)。这种关系由 DAG 的边来表示。

如果你仔细观察，我们可以看到一个模式。一个随机变量的概率取决于他的父母。因此，我们可以将贝叶斯网络公式化为:

**![Bayesian Networks Formula - Bayesian Networks - Edureka](img/93f53df8b2ab5acb5c17fb6aaed09082.png)**

其中，X_i 表示随机变量，其概率取决于父节点𝑃𝑎𝑟𝑒𝑛𝑡𝑠(𝑋_𝑖).的概率

很简单，不是吗？

贝叶斯网络是一种最简单但有效的技术，应用于预测建模、描述性分析等等。

为了让事情更清楚，让我们使用 Python 从头开始构建一个贝叶斯网络。

## **贝叶斯网络 Python**

在这个演示中，我们将使用贝叶斯网络来解决著名的蒙蒂霍尔问题。对于那些不知道天魔堂问题是什么的人，我来解释一下:

以电视剧《我们做个交易吧》主持人命名的蒙蒂·霍尔问题(Monty Hall problem)，是一个悖论式的概率谜题，十多年来一直困扰着人们。

这就是它的工作原理。这个游戏包括三扇门，假设其中一扇门后是一辆汽车，其余两扇门后有山羊。所以你从随机选择一扇门开始，比如说 2 号门。另一方面，主人知道车藏在哪里，他打开另一扇门，比如 1 号门(后面有一只山羊)。这里有一个问题，你现在有一个选择，主持人会问你是否想选择 3 号门，而不是你的第一选择 2 号门。

![The Monty Hall Problem - Bayesian Networks - Edureka](img/d110ccf0c1c3473752fc422c7f71a944.png)

是换个选择更好还是应该坚持第一选择？

这正是我们要模拟的。我们将创建一个贝叶斯网络来了解参与者决定改变选择时的获胜概率。

在我们开始演示之前，有一个简短的免责声明。

我将使用 Python 实现贝叶斯网络，如果你不了解 Python，你可以浏览以下博客:

1.  [Python 教程——学习 Python 编程的完整指南](https://www.edureka.co/blog/python-tutorial/)
2.  [Python 编程语言——Python 基础入门](https://www.edureka.co/blog/python-programming-language)
3.  [Python 函数初学者指南](https://www.edureka.co/blog/python-functions)
4.  [用于数据科学的 Python](https://www.edureka.co/blog/learn-python-for-data-science/)

现在让我们开始吧。

第一步是建立一个有向无环图。

该图有三个节点，每个节点代表由以下人员选择的门:

1.  客人选择的门
2.  装有奖品(汽车)的门
3.  蒙蒂选择打开的门

![The Monty Hall Problem DAG - Bayesian Networks - Edureka](img/b1eba2c54fd25b5d3eecfa54d6175049.png)

我们来理解一下这里的依赖关系，客人选择的门和包含汽车的门是完全随机的过程。然而，蒙蒂选择打开的门取决于这两扇门；客人选的门，奖品在后面的门。蒙蒂必须以这样的方式选择，门不包含奖品，它不能是客人选择的那个。

```
#Import required packages
import math
from pomegranate import *

# Initially the door selected by the guest is completely random
guest =DiscreteDistribution( { 'A': 1./3, 'B': 1./3, 'C': 1./3 } )

# The door containing the prize is also a random process
prize =DiscreteDistribution( { 'A': 1./3, 'B': 1./3, 'C': 1./3 } )

# The door Monty picks, depends on the choice of the guest and the prize door
monty =ConditionalProbabilityTable(
[[ 'A', 'A', 'A', 0.0 ],
[ 'A', 'A', 'B', 0.5 ],
[ 'A', 'A', 'C', 0.5 ],
[ 'A', 'B', 'A', 0.0 ],
[ 'A', 'B', 'B', 0.0 ],
[ 'A', 'B', 'C', 1.0 ],
[ 'A', 'C', 'A', 0.0 ],
[ 'A', 'C', 'B', 1.0 ],
[ 'A', 'C', 'C', 0.0 ],
[ 'B', 'A', 'A', 0.0 ],
[ 'B', 'A', 'B', 0.0 ],
[ 'B', 'A', 'C', 1.0 ],
[ 'B', 'B', 'A', 0.5 ],
[ 'B', 'B', 'B', 0.0 ],
[ 'B', 'B', 'C', 0.5 ],
[ 'B', 'C', 'A', 1.0 ],
[ 'B', 'C', 'B', 0.0 ],
[ 'B', 'C', 'C', 0.0 ],
[ 'C', 'A', 'A', 0.0 ],
[ 'C', 'A', 'B', 1.0 ],
[ 'C', 'A', 'C', 0.0 ],
[ 'C', 'B', 'A', 1.0 ],
[ 'C', 'B', 'B', 0.0 ],
[ 'C', 'B', 'C', 0.0 ],
[ 'C', 'C', 'A', 0.5 ],
[ 'C', 'C', 'B', 0.5 ],
[ 'C', 'C', 'C', 0.0 ]], [guest, prize] )

d1 = State( guest, name="guest" )
d2 = State( prize, name="prize" )
d3 = State( monty, name="monty" )

#Building the Bayesian Network
network = BayesianNetwork( "Solving the Monty Hall Problem With Bayesian Networks" )
network.add_states(d1, d2, d3)
network.add_edge(d1, d3)
network.add_edge(d2, d3)
network.bake()

```

在上面的代码' A '，' B '，' C '，分别代表客人选的门，奖品门，蒙蒂选的门。这里我们画出了每个节点的条件概率。因为奖品门和客人门是随机抽取的，所以没有什么可考虑的。然而，Monty 选择的门取决于其他两扇门，因此在上面的代码中，我已经考虑了所有可能的情况，画出了条件概率。

下一步是使用这个模型进行预测。贝叶斯网络的优势之一是能够根据“观察变量”的值推断出任意“隐藏变量”的值。这些隐藏变量和观察变量不需要预先指定，观察的变量越多，对隐藏变量的推断就越好。

现在我们已经建立了模型，是时候做预测了。

```
beliefs = network.predict_proba({ 'guest' : 'A' })
beliefs = map(str, beliefs)
print("n".join( "{}t{}".format( state.name, belief ) for state, belief in zip( network.states, beliefs ) ))

guest A
prize {
"class" :"Distribution",
"dtype" :"str",
"name" :"DiscreteDistribution",
"parameters" :[
{
"A" :0.3333333333333333,
"B" :0.3333333333333333,
"C" :0.3333333333333333
}
],
}

monty {
"class" :"Distribution",
"dtype" :"str",
"name" :"DiscreteDistribution",
"parameters" :[
{
"C" :0.49999999999999983,
"A" :0.0,
"B" :0.49999999999999983
}
],
}

```

在上面的代码片段中，我们假设客人选择了门“A”。给定该信息，奖励门为“A”、“B”、“C”的概率是相等的(1/3)，因为它是一个随机过程。但是，既然客人选了门‘A’，那么蒙蒂选‘A’的概率显然是零。另外两扇门有 50%的机会被蒙蒂选中，因为我们不知道哪扇门是奖品门。

```
beliefs = network.predict_proba({'guest' : 'A', 'monty' : 'B'})
print("n".join( "{}t{}".format( state.name, str(belief) ) for state, belief in zip( network.states, beliefs )))

guest A
prize {
"class" :"Distribution",
"dtype" :"str",
"name" :"DiscreteDistribution",
"parameters" :[
{
"A" :0.3333333333333334,
"B" :0.0,
"C" :0.6666666666666664
}
],
}
monty B

```

在上面的代码片段中，我们为贝叶斯网络提供了两个输入，这就是事情变得有趣的地方。我们提到了以下内容:

1.  客人选择门“A”
2.  蒙蒂打开了 B 门

注意输出，汽车在门“C”后面的概率大约是。66%.这就证明了，如果嘉宾切换选择，他获胜的概率更大。虽然这可能会让你们中的一些人感到困惑，但众所周知的事实是:

*   决定换门的客人赢了大约 2/3 的时间
*   拒绝转换的客人赢了大约 1/3 的时间

贝叶斯网络用于预测不确定任务和结果的情况。在下面的部分中，你将理解贝叶斯网络是如何被用来解决更多这样的问题的。

## **贝叶斯网络应用**

贝叶斯网络在医疗保健、医学、生物信息学、信息检索等领域有着无数的应用。下面是贝叶斯网络在现实世界中的应用列表:

1.  **疾病诊断:**贝叶斯网络常用于医学领域对疾病的检测和预防。它们可以用来模拟可能的症状，并预测一个人是否患病。

2.  **优化的网络搜索:**贝叶斯网络用于通过理解搜索的意图并提供最相关的搜索结果来提高搜索的准确性。它们可以有效地将用户意图映射到相关内容，并提供搜索结果。

3.  **垃圾邮件过滤:**贝叶斯模型已经在 Gmail 垃圾邮件过滤算法中使用了多年。他们可以通过理解邮件的上下文含义来有效地对文档进行分类。它们也用于其他文档分类应用。

4.  **基因调控网络:** GRNs 是由许多 DNA 片段组成的基因网络。它们被有效地用来直接或间接地与细胞的其他部分进行通讯。诸如贝叶斯网络的数学模型被用于模拟这种细胞行为，以便形成预测。

5.  **生物监测:**贝叶斯网络在监测药品中使用的化学剂量的数量方面发挥着重要作用。

既然您已经知道了贝叶斯网络是如何工作的，我相信您一定很想了解更多。这里有一个博客列表，可以帮助你开始了解其他统计学概念:

1.  [数据科学数学和统计学完全指南](https://www.edureka.co/blog/math-and-statistics-for-data-science/)
2.  [关于统计和概率你需要知道的一切](https://www.edureka.co/blog/statistics-and-probability/)
3.  [举例介绍马尔可夫链——用 Python 实现马尔可夫链](https://www.edureka.co/blog/introduction-to-markov-chains/)

说到这里，我们就到此为止了。如果你对这个话题有任何疑问，请在下面留下评论，我们会尽快回复你。

敬请关注更多关于趋势技术的博客。

如果你希望报名参加人工智能和机器学习的完整课程，Edureka 有一个专门策划的 ***[机器学习工程师硕士项目](https://www.edureka.co/masters-program/machine-learning-engineer-training)*** ，它将使你精通监督学习、非监督学习和自然语言处理等技术。它包括人工智能&机器学习方面的最新进展和技术方法的培训，如深度学习、图形模型和强化学习。