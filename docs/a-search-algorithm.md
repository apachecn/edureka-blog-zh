# 什么是 A*算法，它是如何工作的？

> 原文：<https://www.edureka.co/blog/a-search-algorithm/>

在[计算机编程](https://www.edureka.co/blog/python-basics/)中，寻路是最古老也是最受欢迎的应用之一。通过增加代表时间、金钱等的成本，你几乎可以找到从源到目的地的最佳路径。【a*】是最[流行的算法](https://www.edureka.co/blog/artificial-intelligence-algorithms/)之一。在这篇文章中，让我们找出原因。

如果你想获得认证并了解 *[人工智能](https://www.edureka.co/blog/pros-and-cons-of-ai/)* 和 *[机器学习](https://www.edureka.co/blog/what-is-machine-learning/)* ，今天就加入 Edureka 的 ***[研究生项目](https://www.edureka.co/post-graduate/machine-learning-and-ai)*** ！

本条由以下部分组成:

*   [什么是搜索算法？](#whatissearch)
*   [为什么是 A*算法？](#whyastar)
*   [a*算法的进出](#inoutastar)
*   [实用性中的 A*算法](#astarpractical)

让我们开始吧:)

## **什么是搜索算法？**

![search algorithm - a star - edureka](img/db1e4997200216715fe9f3e0ed566205.png)

从一个地方搬到另一个地方是我们人类几乎每天都要做的事情。我们试图找到最短的路径，使我们能够更快地到达目的地，并尽可能提高整个旅行过程的效率。在过去，我们会对可用的路径进行反复试验，并且必须假设哪条路径更短或更长。

现在，我们有算法可以帮助我们找到虚拟的最短路径。我们只需要增加成本(时间、金钱等)。)到图表或地图上，算法会尽可能快地找到我们到达目的地所需的路径。多年来，针对这个问题开发了许多算法，A*是最流行的算法之一。

## **为什么是 A*算法？**

那么 A*算法到底是什么？ *首先搜索较短的路径，而不是较长的路径* ，这是一种 **高级 [BFS 算法](https://www.edureka.co/blog/breadth-first-search-algorithm/)** 。一个*是 **最优的** 以及一个 **完备的** 算法。

我说的 **优** 和 **全** 是什么意思？ **最优** 意即 *A*一定会找到从源到目的地的最小成本***完全** 意即 *它会找到从源到目的地的所有可用路径* 。

所以 A*是最好的算法，对吗？大多数情况下，是的。但是 A*很慢，而且它需要的空间也很大，因为它保存了我们可用的所有可能的路径。这使得其他更快的算法比 A*更胜一筹，但它仍然是最好的算法之一。

***那么为什么要选择 A*而不是其他更快的算法呢？***

让下面的图表为你解答这个问题。我拿 Dijkstra 的算法和 A*算法做了比较。

您可以在这里看到，Dijkstra 算法找到了所有可以选择的路径，但没有找到或知道哪条路径对于我们面临的问题是最优的。这导致算法的非优化工作和不必要的计算。

![Astar - Dijkstras - edureka](img/5abb52a6a2401b2c28278f280bf6ef58.png)

另一方面，A*算法找到从源到达目的地的最佳路径。它知道从当前状态出发哪条路径是最佳路径，以及需要如何到达目的地。**![a star - a star - edureka](img/87269800019042baba04e28f1efa8e0f.png)**

## A*算法的输入和输出

现在你知道了我们为什么选择 A*，让我们来了解一些关于它的理论，因为它对帮助你理解这个算法是如何工作的至关重要。

众所周知，A*用于寻找从源到目的地的最佳路径。它通过计算从一个节点到另一个节点的最短距离来优化路径。

有一个公式你们所有人 **需要记住** ，因为它是算法的核心和灵魂。

***F = G+H***

**那么这三个变量是什么？为什么它们如此重要？现在就来了解一下吧。**

***   F—**F 是 A*的** 参数，是其他参数 G 和 H 的和，是从一个节点到下一个节点 的 **最小成本。这个参数负责帮助我们找到从源到目的地的最佳路径。***   G—**G 是从一个节点移动到另一个节点** 的 **代价。当我们向上移动以寻找最佳路径时，这个参数对于每个节点都是变化的。***   H—**H 是当前代码到目的节点** 之间的启发式/估计路径。这个成本不是实际的，实际上是一个猜测成本，我们用它来寻找源和目的地之间的最佳路径。**

**一旦你理解了这个公式，让我给你看一个简单的例子来帮助你理解这个算法是如何工作的。**

**![a star - a star - edureka](img/9a50a16f7655c8553c407c3c0f46eacf.png)**

**假设我们有一个小图，它的顶点是:S，A，B，E，其中 S 是起点，E 是终点。**

**请记住，输入源和目的地的成本始终为 0。**

**启发式值为:**

***>-********A->4************B->5**************E->*******

******现在让我们使用公式计算从源到目的地的最短路径。******

******f = g + h，其中 g 是旅行成本，h 是启发式值。******

******到达来源:******

********f(S) = 0 + 5 = 5********

******从 S 到其他顶点的路径:******

********f(S-A) = 1 + 4 = 5********

********f(S-B) = 2 + 5 = 7********

******所以，我们首先会选择 S - > A 的路径，因为它是最少的。******

******从 A 和 B 到目的地的路径:******

********f(S-A-E) = (1 + 13) + 0 = 14********

********f(S-B-E) = (2 + 5) + 0 = 7********

******经过计算，我们现在已经发现 B 后来给了我们最少的路径。因此，我们将最短路径改为 S-B-E，到达了目的地。这就是我们如何使用公式找出最佳路径。******

******了解了公式的用法后，让我们来看看算法是如何工作的:******

******首先创建 2 个列表来帮助你理解路径，我们将它们命名为 **开放** 和 **封闭** 列表。******

********A*算法():********

*******   将开始节点添加到列表中*   对于所有的邻居节点，找到最小成本的 F 节点*   切换到关闭列表
    *   对于与当前节点相邻的 8 个节点
    *   如果节点不可达，忽略它。否则
        *   如果节点不在开放列表上，将其移动到开放列表并计算 f，g，h。
        *   如果节点在开放列表上，检查它提供的路径是否小于当前路径，如果是，则改变到当前路径。*   当时停止工作
    *   你找到了目的地
    *   你无法通过所有可能的点找到目的地******

******算法的伪代码是这样的。******

```
******let the openList equal empty list of nodes
let the closedList equal empty list of nodes
put the startNode on the openList (leave it's f at zero)
while the openList is not empty
    let the currentNode equal the node with the least f value
    remove the currentNode from the openList
    add the currentNode to the closedList
    if currentNode is the goal
        You've found the end!
    let the children of the currentNode equal the adjacent nodes
    for each child in the children
        if child is in the closedList
            continue to beginning of for loop
        child.g = currentNode.g + distance between child and current
        child.h = distance from child to end
        child.f = child.g + child.h
        if child.position is in the openList's nodes positions
            if the child.g is higher than the openList node's g
                continue to beginning of for loop
        add the child to the openList****** 
```

******这就是我们需要知道的关于 A*算法的所有理论。我们来看看 A*在实际案例中是如何使用的。******

## ********实用的 A*算法********

******在寻找从一个地方到另一个地方的路径方面，A*非常聪明。它还确保找到最有效的路径。现在，我将向您展示两个代码。一个是 Dijkstra，另一个是 A*，由此，你可以理解为什么 A*在寻找从源到目的地的路径时是最好的。******

******让我们首先从 Dijkstra 的实现开始。******

```
******def Dijkstra(maze, source):
    infinity = float('infinity')
    n = len(maze)
    dist = [infinity] * n
    previous = [infinity] * n
    dist = 0
    Q = list(range(n))
    while Q:
        u = min(Q, key=lambda n: dist[n])
        Q.remove(u)
        if dist[u] == infinity:
            break
        for v in range(n):
            if maze[u][v] and (v in Q):
                alt = dist[u] + maze[u][v]
                if alt < dist[v]:
                    dist[v] = alt
                    previous[v] = u
    return dist, previous

def display_solution(predecessor):
    cell = len(predecessor) - 1
    while cell:
        print(cell, end='<')
        cell = predecessor[cell]
    print(0)

maze = ((0, 0, 0, 0, 1, 0),
        (0, 0, 0, 0, 1, 0),
        (0, 0, 0, 0, 1, 0),
        (0, 0, 0, 0, 1, 0),
        (0, 0, 0, 0, 1, 0),
        (0, 0, 0, 0, 0, 0))
graph = (
    (0, 1, 0, 0, 0, 0,),
    (1, 0, 1, 0, 1, 0,),
    (0, 1, 0, 0, 0, 1,),
    (0, 0, 0, 0, 1, 0,),
    (0, 1, 0, 1, 0, 0,),
    (0, 0, 1, 0, 0, 0,),
)
values = Dijkstra(graph, 0)
print(values)
display_solution(values[1])
values = Dijkstra(maze, 0)
print(values)
display_solution(values[1])****** 
```

********输出**:******

```
******([0, 1, 2, 3, 2, 3], [inf, 0, 1, 4, 1, 2])
5<2<1<0
([0, inf, inf, inf, 1, inf], [inf, inf, inf, inf, 0, inf])
5<inf<Traceback (most recent call last):
  File "C:/Users/AkashkumarJainS/PycharmProjects/A Star/dijkstra.py", line 50, in <module>
    display_solution(values[1])
  File "C:/Users/AkashkumarJainS/PycharmProjects/A Star/dijkstra.py", line 26, in display_solution
    cell = predecessor[cell]
TypeError: list indices must be integers or slices, not float******
```

******你可以看到这里有两个图，其中一个图的 **Dijkstra 失败了，另一个图的**成功了。哪里有障碍或者没有一条清晰的道路，Dijkstra 就在那里失败。它无法找到如何以及为什么需要遍历图的确切方式和方法。输出显示它需要浮点值等等，但实际上， **Dijkstra 无法找到节点**之间的路径，正因为如此，它将许多路径标记为无限。然后我们的程序说，没有办法处理这个图，并抛出一个错误。******

******让我们做同样的事情，但是使用 A*实现。******

```
******class Node():
    def __init__(self, parent=None, position=None):
        self.parent = parent
        self.position = position
        self.g = 0
        self.h = 0
        self.f = 0
    def __eq__(self, other):
        return self.position == other.position
def astar(maze, start, end):
    start_node = Node(None, start)
    start_node.g = start_node.h = start_node.f = 0
    end_node = Node(None, end)
    end_node.g = end_node.h = end_node.f = 0
    open_list = []
    closed_list = []
    open_list.append(start_node)
    while len(open_list) > 0:
        current_node = open_list[0]
        current_index = 0
        for index, item in enumerate(open_list):
            if item.f < current_node.f:
                current_node = item
                current_index = index
        open_list.pop(current_index)
        closed_list.append(current_node)
        if current_node == end_node:
            path = []
            current = current_node
            while current is not None:
                path.append(current.position)
                current = current.parent
            return path[::-1]
        children = []
        for new_position in [(0, -1), (0, 1), (-1, 0), (1, 0), (-1, -1), (-1, 1), (1, -1), (1, 1)]:
            node_position = (current_node.position[0] + new_position[0], current_node.position[1] + new_position[1])
            if node_position[0] > (len(maze) - 1) or node_position[0] < 0 or node_position[1] > (
                    len(maze[len(maze) - 1]) - 1) or node_position[1] < 0:
                continue
            if maze[node_position[0]][node_position[1]] != 0:
                continue
            new_node = Node(current_node, node_position)
            children.append(new_node)
        for child in children:
            for closed_child in closed_list:
                if child == closed_child:
                    continue
            child.g = current_node.g + 1
            child.h = ((child.position[0] - end_node.position[0]) ** 2) + (
                    (child.position[1] - end_node.position[1]) ** 2)
            child.f = child.g + child.h
            for open_node in open_list:
                if child == open_node and child.g > open_node.g:
                    continue
            open_list.append(child)
def main():
    maze = [[0, 0, 0, 0, 1, 0],
            [0, 0, 0, 0, 1, 0],
            [0, 0, 0, 0, 1, 0],
            [0, 0, 0, 0, 1, 0],
            [0, 0, 0, 0, 1, 0],
            [0, 0, 0, 0, 0, 0]]
    graph = [[0, 1, 0, 0, 0, 0],
             [1, 0, 1, 0, 1, 0],
             [0, 1, 0, 0, 0, 1],
             [0, 0, 0, 0, 1, 0],
             [0, 1, 0, 1, 0, 0],
             [0, 0, 1, 0, 0, 0]
             ]
    start = (0, 0)
    end = (5, 5)
    end1 = (5, 5)
    path = astar(maze, start, end)
    print(path)
    path1 = astar(graph, start, end1)
    print(path1)
if __name__ == '__main__':
    main()******
```

********输出**:******

```
******[(0, 0), (1, 1), (2, 2), (3, 3), (4, 3), (5, 4), (5, 5)]
[(0, 0), (1, 1), (2, 2), (3, 3), (4, 4), (5, 5)]****** 
```

******另一方面，A*在这里表现出色，因为它清楚地知道图形，而**知道何时有障碍物。**然后它就能相应地驱动自己达到所需的输出。这是一个非常实际的例子，说明 A*在其他人失败的情况下取得了成功。******

******所以我希望你现在对什么是 A*算法、它的工作和实现以及更多有一个清晰的概念。这就是我今天给你们的全部内容。下次再见，保重，快乐学习:)******

*******既然你已经了解了 A*算法，那就来看看 Edureka 的机器学习和人工智能硕士项目[](https://www.edureka.co/post-graduate/machine-learning-and-ai)**吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*******

*******Edureka 的**机器学习和人工智能硕士项目**课程是为希望以最有效的方式掌握这一领域的学生和专业人士设计的。该课程提供 Python 代码及其简介和所有必要的概念、预测分析概念和机器学习、图形模型、强化学习、自然语言处理、深度学习和人工智能，以及大量项目和作业。*******

*******有问题吗？请在这个“**的评论区提一下什么是 A*算法，它是如何工作的？**“博客，我们会尽快回复您。*******