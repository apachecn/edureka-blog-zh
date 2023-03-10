# 爬山算法简介

> 原文：<https://www.edureka.co/blog/hill-climbing-algorithm-ai/>

为了获得问题的最佳解决方案，我们经常准备等待。但是如果，你就是没有时间呢？ ***爬山*** 就是这样一种 [***算法***](https://www.edureka.co/blog/machine-learning-algorithms/) 就是一种能在最合理的时间内为你找到问题的最佳解决方案的算法！

希望接下来是算法的彻底崩溃。所以，让我们从以下话题开始；

*   [**什么是爬山算法？**](#hillclimbingalgorithm)
*   [**爬山的特点**](#featuresofhillclimbing)
*   [**爬山状态空间图**](#statespacediagram)
*   [**爬山算法的工作原理**](#codehillclimbing)
*   [**爬山的种类**](#typesofhillclimbing)
*   [**爬山中不同地区的问题**](#hillclimbingproblems)
*   [](#simulatedannealing)模拟退火
*   [**爬山技术的应用**](#hillclimbingapplications)

## **什么是爬山算法？**

***爬山是一种启发式搜索，用于人工智能领域的数学优化问题。***

因此，给定一大组输入和一个好的启发式函数，该算法试图在最合理的时间内找到问题的最佳可能解决方案。这个解决方案可能不是绝对最好的(全局最优最大值)，但是考虑到分配的时间，它已经足够好了。

上面的定义意味着爬山法解决了我们需要通过从给定输入中选择值来最大化或最小化给定实函数的问题。

一个很好的例子就是 ***旅行推销员问题*** 这里我们需要最小化推销员旅行的距离。

****

## **爬山的特点**

### ***它执行启发式搜索。***

**启发式函数** 是基于可用信息在搜索算法中对所有潜在备选方案进行排序的函数。它有助于算法选择解决方案的最佳路径。

这基本上意味着这种搜索 [***算法***](https://www.edureka.co/blog/classification-algorithms/) 可能找不到问题的最优解，但它会在合理的时间内给出最佳可能解。

### ***它是生成-测试算法的变种。***

算法如下:

**第一步:**生成可能的解。

**步骤 2:** 评估这是否是预期的解决方案。

第三步:如果已经找到解决方案，退出，否则返回第一步*。*

![generate-and-test flowchart - hill climbing algorithm - edureka](img/37c8267dbc7fc412ef01c47f5b566b27.png)

爬山从测试过程中获取反馈，生成器使用它来决定搜索空间中的下一步。因此，我们称之为生成和测试 *算法*的*变体。*

### ***It u****ses****贪婪的做法。***

在状态空间中的任何一点上，搜索只在优化功能成本的方向上移动，希望最终找到最优解。

![greedy approach flowchart - hill climbing algorithm - edureka](img/fd28c8e04ccfa8441436ee911a6247b6.png)

## **爬山状态空间图**

状态空间图是状态(输入) 集合的 ***的图形表示，我们的搜索算法可以达到 vs 我们的 ***目标函数(我们打算最大化/最小化的函数)*** 的值。这里； 1。 **X 轴** 表示我们的算法可能达到的状态空间，即状态或配置。 2。 **Y 轴** 表示对应于特定状态的目标函数值。 ***最佳解将是目标函数具有最大值或全局最大值的状态空间。******

![state space diagram - hill climbing algorithm - edureka](img/d63cc493d1d94f5c88b7dd82859798cf.png)

以下是状态空间图中的不同区域；

*   **局部最大值:** 它是一个比其相邻状态更好的状态，然而存在一个比它更好的状态(全局最大值)。这种状态更好，因为这里目标函数的值高于它的邻居。

*   **全局极大值:** 它是状态空间图中可能出现的最佳状态。这是因为在这种状态下，目标函数具有最高值。

*   **坪/平局部极大值:** 它是状态空间中相邻状态具有相同值的平坦区域。

*   **山脊:** 它是一个比邻居的高，但本身有斜坡的地区。这是一种特殊的局部最大值。

*   **当前状态:** 状态空间图中搜索时我们当前所在的区域。(由给定图像中突出显示的圆圈表示。)

****

## **爬山算法的工作原理**

爬山是最简单的一种遗传算法的实现。它没有关注实现的容易程度，而是完全摆脱了群体和交叉等概念。与更传统的遗传算法相比，它的迭代速度更快，但反过来，它比传统的遗传算法更不彻底。

爬山的方式非常简单。因此，我们将从尝试打印“Hello World”开始。

尽管这不是一个具有挑战性的问题，但仍然是一个很好的介绍。

这是解决方案的基本框架。

```
best = generate_random_solution()
best_score = evaluate_solution(best)

while True:
    print('Best score so far', best_score, 'Solution', best)
    new_solution = copy_solution(best)
    mutate_solution(new_solution)

    score = evaluate(new_solution)
    if evaluate(new_solution) < best_score:
        best = new_solution
        best_score = score
```

### 第一步:从一个随机的或空的溶液开始。这将是你的“最佳解决方案”。

```
def generate_random_solution(length=11):
return [random.choice(string.printable) for _ in range(length)]
```

这个函数需要返回一个随机解。在爬山算法中，使这成为一个独立的函数可能太抽象了，但是如果你想把你的代码结构改为基于群体的遗传算法，这将是有帮助的。

### 第二步:评估。

```
def evaluate(solution): 
target = "Hello, World!".split("") 
diff = 0 
for i in range(len(target)): 
s = solution[i] 
t = target[i] 
diff += abs(ord(s) - ord(t)) 
return diff
```

所以我们的评估函数将返回两个字符串之间的距离度量。

### 第三步:复制一份解决方案，并对其稍加修改。

```
def mutate_solution(solution): 
index = random.randint(0, len(solution) - 1) 
solution[index] = random.choice(string.printable)
```

### 第四步:现在，评估新的解决方案。如果它比最优解好，我们就用这个替换最优解。 **转到步骤二，重复步骤二和步骤三。**

基本上，要找到一个问题的解决方案，你需要写三个函数。

1.  **创建随机解决方案。**
2.  **评估解决方案并返回结果。**
3.  以随机的方式改变溶液。

让我们让代码处于准备运行的状态。

```
import random 
import string 

def generate_random_solution(length=13): 
return [random.choice(string.printable) for _ in range(length)] 

def evaluate(solution): 
target = list("Hello, World!") 
diff = 0 
for i in range(len(target)): 
s = solution[i] 
t = target[i] 
diff += abs(ord(s) - ord(t)) 
return diff 

def mutate_solution(solution): 
index = random.randint(0, len(solution) - 1) 
solution[index] = random.choice(string.printable) 

best = generate_random_solution() 
best_score = evaluate(best) 

while True: 
print('Best score so far', best_score, 'Solution', "".join(best)) 

if best_score == 0: 
break 

new_solution = list(best) 
mutate_solution(new_solution) 

score = evaluate(new_solution) 
if evaluate(new_solution) < best_score: 
best = new_solution 
best_score = score
```

```
Testing the Code
```

```
*Best score so far 392 Solution #KAKZ'yjrJo/5
Best score so far 392 Solution #KAKZ'yjrJo/5
Best score so far 390 Solution #KAKZ/yjrJo/5
Best score so far 347 Solution #KAKZ/yjrJon5
...
Best score so far 27 Solution Jojon,"osld
...
Best score so far 12 Solution H_mmn, Vosld
...
Best score so far 4 Solution Hemmo, Vorld
...
Best score so far 0 Solution Hello, World!*
```



## **爬山的种类**

### **1。** **简单爬山**

简单爬山是实现爬山算法的最简单的方法。它一次仅评估邻居节点状态，并选择优化当前成本的第一个节点，并将其设置为当前状态。它只检查它的一个继承状态，如果它发现比当前状态更好，那么移动到相同的状态。该算法具有以下特点:

*   耗时更少

*   次优解

*   该解决方案并不可靠

#### **简单爬山算法**

*   **步骤 1:** 评估初始状态，如果是目标状态则返回成功并停止。

*   **步骤 2:** 循环，直到找到一个解或者没有新的算子可应用。

*   **第三步:** 选择并应用一个操作符到当前状态。

*   **第四步:** 检查新状态:

*   **第五步:** 退出。

### **2。最陡爬坡**

最速上升算法是简单爬山算法的变体。该算法检查当前状态的所有邻居节点，并选择一个最接近目标状态的邻居节点。该算法在搜索多个邻居时会消耗更多的时间。

#### **最陡爬坡算法**

*   **步骤 1:** 评估初始状态，如果是目标状态则返回成功并停止，否则将当前状态作为你的初始状态。

*   **第二步:** 循环，直到找到解或者当前状态不变。

*   **第五步:** 退出。

**3。随机爬山**

随机爬山在移动之前不会检查所有的邻居。相反，该搜索算法随机选择一个邻居节点，并将其评估为当前状态或检查另一个状态。

## **爬山中不同地区的问题**

如果进入以下任何一个区域，爬山都无法达到最佳状态:

1.  **局部最大值:** 在局部最大值时，所有邻居状态的值都比当前状态差。由于爬山使用了贪婪的方法，所以它不会移动到更差的状态并终止自己。即使可能存在更好的解决方案，该过程也将结束。 **克服局部极值问题:** 利用***回溯技术*** 。维护访问过的州的列表。如果搜索到达不期望的状态，它可以回溯到先前的配置并探索新的路径。

2.  **高原:在高原上，所有的邻居都有相同的价值。因此，不可能选择最佳方向。**

**克服停滞状态:** 来个大跳跃。随机选择一个远离当前状态的状态。我们很可能会在非高原地区着陆

3.  **山脊:** 山脊上的任何一点看起来都像峰，因为所有可能方向的运动都是向下的。因此，当算法到达这样的状态时，它停止。 **克服山脊:** 你可以在测试之前使用两个或者更多的规则。它意味着同时向几个方向移动。

## **模拟退火**

一个爬山算法永远不会向一个更低的值移动，它肯定是不完整的，因为它会陷入局部最大值。并且如果算法通过移动后继者来应用随机行走，那么它可能完成但不是有效的。

*****模拟退火是一种既高效又完备的算法**。***

**机械上，术语  **退火** 是将金属或玻璃硬化到高温然后逐渐冷却的过程，因此这允许金属达到低能结晶状态。**

**在模拟退火中使用了相同的过程，在模拟退火中，算法选择随机移动，而不是选择最佳移动。如果随机移动改善了状态，那么它遵循相同的路径。否则，该算法沿着概率小于 1 的路径，或者它向下移动并选择另一条路径。**

## ****爬山技术的应用****

**![applications of hill climbing - hill climbing algorithm - edureka](img/a808e273869f4db9c66f7a026cbdb1b6.png)**

***   爬山技术可用于解决许多问题，其中当前状态允许精确的评估函数，例如网络流、旅行商问题、8 皇后问题、集成电路设计等。*   爬山也用在归纳学习方法中。这种技术也用在机器人学中，用于协调团队中的多个机器人。** 

***所以有了这个，希望这篇文章能引发你对* [***人工智能***](https://www.edureka.co/blog/what-is-artificial-intelligence) 中爬山等此类有趣算法的兴趣。**

***Edureka 的 [**数据科学硕士**](https://www.edureka.co/masters-program/data-scientist-certification) 培训由行业专业人士根据行业需求&策划。你将掌握 S 统计学、数据科学、Python、Apache Spark & Scala、Tensorflow 和 Tableau 等概念。该课程由行业专家通过实时案例研究特别策划。***