# 反向传播–训练神经网络的算法

> 原文：<https://www.edureka.co/blog/backpropagation/>

## **反向传播:**

反向传播是一种监督学习算法，用于训练多层感知器(人工神经网络)。

我推荐你去看看下面这些 ***[深度学习认证](https://www.edureka.co/ai-deep-learning-with-tensorflow)*** 博客太:

*   **[什么是深度学习？](https://www.edureka.co/blog/what-is-deep-learning)**
*   [](https://www.edureka.co/blog/deep-learning-tutorial)
*   **[张量流教程](https://www.edureka.co/blog/tensorflow-tutorial/)**
*   **[神经网络教程](https://edureka.co/blog/neural-network-tutorial)**

但是，你们中的一些人可能想知道为什么我们需要训练神经网络，或者训练的确切含义是什么。

## **为什么我们需要反向传播？**

在设计神经网络时，一开始，我们用一些随机值或任何变量来初始化权重。

现在很明显，我们不是*超人。*因此，我们选择的权重值不一定是正确的，也不一定最符合我们的模型。

好吧，我们一开始选择了一些权重值，但我们的模型输出与实际输出相差甚远，即误差值非常大。

现在，你将如何减少误差？

基本上，我们需要做的是，我们需要以某种方式解释模型来改变参数(权重)，以使误差变得最小。

换句话说，我们需要训练我们的模型。

训练我们的模型的一种方法叫做反向传播。请看下图:

![Training A Neural Network - Backpropagation - Edureka](img/f8a74337f8a9b89bf02350a8e7d2502c.png)

我给你总结一下步骤:

*   **计算误差**——你的模型输出与实际输出有多远。
*   **最小误差**–检查误差是否最小化。
*   **更新参数**–如果误差很大，则更新参数(权重和偏差)。之后，再次检查错误。重复该过程，直到误差最小。
*   **模型准备好进行预测**–一旦误差最小，你可以向你的模型输入一些输入，它就会产生输出。

我很确定，现在你知道了，为什么我们需要反向传播，或者为什么，训练一个模特 的意义是什么。

现在是理解什么是反向传播的正确时机。

## **什么是反向传播？**

反向传播算法使用一种称为 delta 规则或梯度下降的技术在权重空间中寻找误差函数的最小值。最小化误差函数的权重然后被认为是学习问题的解决方案。

让我们通过一个例子来理解它是如何工作的:

你有一个数据集，它有标签。

考虑下表:

| **输入** | **期望输出** |
| 0 | 0 |
| 1 | 2 |
| 2 | 4 |

现在当‘W’值为 3 时你的模型的输出:

| **输入** | **期望输出** | **【W = 3】**模型输出 |
| 0 | 0 | 0 |
| 1 | 2 | 3 |
| 2 | 4 | 6 |

注意实际输出和期望输出之间的差异:

| **输入** | **期望输出** | **【W = 3】**模型输出 | **绝对误差** | **平方误差** |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 2 | 3 | 1 | 1 |
| 2 | 4 | 6 | 2 | 4 |

让我们改变‘W’的值。注意当' W ' = ' 4 'T3 时的错误

| **输入** | **期望输出** | **【W = 3】**模型输出 | **绝对误差** | **平方误差** | **【W = 4】**模型输出 | **平方误差** |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 2 | 3 | 1 | 1 | 4 | 4 |
| 2 | 4 | 6 | 2 | 4 | 8 | 16 |

现在如果你注意到，当我们增加‘W’的值时，误差也增加了。因此，显然没有必要进一步增加“W”的值。但是，如果我减小 W 的值，会发生什么呢？请看下表:

| **输入** | **期望输出** | **【W = 3】**模型输出 | **绝对误差** | **平方误差** | **【W = 2】**模型输出 | **平方误差** |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 2 | 3 | 2 | 4 | 3 | 0 |
| 2 | 4 | 6 | 2 | 4 | 4 | 0 |

现在，我们在这里做了:

*   我们先将某个随机值初始化为‘W’并向前传播。
*   然后，我们注意到有一些误差。为了减少这种误差，我们向后传播并增加“W”的值。
*   在那之后，我们也注意到误差有所增加。我们开始知道，我们不能增加“W”值。
*   因此，我们再次向后传播，并降低“W”值。
*   现在，我们注意到误差已经减少了。

因此，我们试图得到使误差最小的权值。基本上，我们需要弄清楚是否需要增加或减少权重值。一旦我们知道了，我们继续在那个方向更新权重值，直到误差变得最小。您可能会达到一个点，如果您进一步更新权重，误差将会增加。这时你需要停下来，那就是你的最终重量值。

考虑下图:

![Optimizer - Backpropagation - Edureka](img/81604127abbfad8b522aa9280d0495fc.png)

我们需要达到‘全局损失最小’。

这只不过是反向传播。

现在让我们理解反向传播背后的数学原理。

## **反向传播是如何工作的？**

考虑下面的神经网络:

![Backpropagation Example - Backpropagation - Edureka](img/4e1b077805e425ee0e40a3c7cd4fa4a0.png)

以上网络包含以下:

*   两个输入
*   两个隐藏神经元
*   两个输出神经元
*   两个偏差

以下是反向传播的步骤:

*   第一步:正向传播
*   第二步:反向传播
*   步骤–3:将所有值放在一起，并计算更新的重量值

### **第一步:正向传播**

我们将从向前传播开始。

![Forward Propagation - Backpropagation - Edureka](img/435e032a64b6d21f329ae93ce3d8b768.png)

我们将使用隐藏层神经元的输出作为输入，对输出层神经元重复这一过程。

![Output Forward Propagation - Backpropagation - Edureka](img/23d0c6d885a863fdb24f9dd11de3530c.png)

现在，让我们看看错误的值是多少:

![Error - Backpropagation - Edureka](img/dd9a0210321b4dd76f8def4cd5c44033.png)

### **第二步:反向传播**

现在，我们将向后传播。这样，我们将尝试通过改变权重和偏差的值来减少误差。

考虑 W5，我们将计算误差相对于重量 W5 变化的变化率。

![Backward Propagation - Backpropagation - Edureka](img/c37603b977438df2b4523e1d4ea334d9.png)

由于我们是反向传播，我们需要做的第一件事是计算输出 O1 和 O2 的总误差变化。

![Backward Propagation - 1 - Backpropagation - Edureka](img/9c8e60dbc6817e6c06da9c99a04d8250.png)

现在，我们将进一步向后传播，并计算输出 O1 w.r.t 相对于其总净输入的变化。

![Backward Propagation - 2 - Backpropagation - Edureka](img/8ccd20a0b37e161926fedefdc0d1e0d9.png)

让我们看看 O1 的总净投入对 W5 的影响有多大？

![Backward Propagation -3 - Backpropagation - Edureka.](img/cb9a769d3964f437e675e37ecee6a799.png)

### **第三步:将所有值放在一起，计算更新后的权重值**

现在，让我们把所有的值放在一起:

![Change In Error W.R.T Weight - Backpropagation - Edureka](img/917ff4dc9b8ea4428469ab77aea72608.png)

让我们来计算一下 W5 的更新值:

![Updated Weight Value - Backpropagation - Edureka](img/bc3bbd7d0ad3eb947fedfeba69893d9f.png)

*   类似地，我们也可以计算其他重量值。
*   之后，我们将再次向前传播并计算输出。同样，我们将计算误差。
*   如果误差最小，我们将停止，否则我们将再次向后传播并更新权重值。
*   这个过程将不断重复，直到误差最小。

## **结论:**

好吧，如果我必须得出反向传播的结论，最好的选择是写同样的伪代码。

### **反向传播算法:**

```
initialize network weights (often small random values)

  **do**

     **forEach** training example named ex

        prediction = neural-net-output(network, ex)  *// forward pass*

        actual = teacher-output(ex)

        compute error (prediction - actual) at the output units

        compute {displaystyle Delta w_{h}} for all weights from hidden layer to output layer  *// backward pass*

        compute {displaystyle Delta w_{i}} for all weights from input layer to hidden layer   *// backward pass continued*

        update network weights *// input layer not modified by error estimate*

  **until** all examples classified correctly or another stopping criterion satisfied

**return** the network 
```

*我希望你喜欢阅读这篇关于反向传播的博客，看看 Edureka 的* ***[深度学习与 TensorFlow 培训](https://www.edureka.co/ai-deep-learning-with-tensorflow/)*** *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 深度学习 TensorFlow 认证培训课程使用实时项目和任务以及 SoftMax 函数、自动编码器神经网络、受限玻尔兹曼机器(RBM)等概念，帮助学习者成为培训和优化基本和卷积神经网络的专家。*

*有问题吗？请在评论区提到它，我们会给你回复。*