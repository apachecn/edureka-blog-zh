# 胶囊神经网络–一组嵌套的神经层

> 原文：<https://www.edureka.co/blog/capsule-networks/>

## **胶囊网络:**

什么是胶囊网络？它基本上是一组嵌套神经层的网络。

我建议你也去看看下面的博客:

*   [**单层感知器**](https://www.edureka.co/blog/perceptron-learning-algorithm/)
*   [**神经网络教程**](https://www.edureka.co/blog/neural-network-tutorial/)
*   [](https://www.edureka.co/blog/backpropagation/)

我假设，你们知道卷积神经网络(CNN)。在这里，我将给你一个同样的小介绍，这样我可以讨论 CNN 的局限性。

也可以参考下面关于卷积神经网络的视频。

## **【CNN】**

[https://www.youtube.com/embed/umGJ30-15_A?rel=0&showinfo=0](https://www.youtube.com/embed/umGJ30-15_A?rel=0&showinfo=0)

卷积神经网络，基本上是各层人工神经元的堆叠，用于计算机视觉。下面，我已经提到了那些层:

**![Convolutional Neural Network - Capsule Neural Network - Edureka](img/e47e34d18e01604fa8bb188204051395.png)**

**卷积层:**当我们使用前馈神经网络(多层感知器)进行图像分类时，会遇到很多挑战。最令人沮丧的挑战是，它引入了许多参数，考虑 CNN 上的视频教程。

克服这种挑战 ***卷积层*** 被引入。假设在空间上靠得更近的像素在形成感兴趣的特定特征时将比图像对角上的像素“合作”得多。此外，如果在定义图像的标签时发现某个特定的(较小的)特征非常重要，那么如果该特征在图像中的任何位置都存在，则该特征也同样重要，而与位置无关。

**ReLU 层:**整流线性单位(ReLU)变换函数只在输入在一定量以上时才激活一个节点，而输入在零以下时，输出为零，但当输入上升到一定阈值以上时，与因变量成线性关系。

*   在这一层，我们从过滤后的图像中移除所有负值，并用零来代替
*   这样做是为了避免数值累加为零

**![ReLU Activation Function - Capsule Neural Networks - Edureka](img/7f81c0750e297b5cbaa1d8e7257f8c24.png)**

聚合有几种可能的方案——最流行的是***Max-Pooling***，其中取每个块内的最大像素值。它使网络对输入图像中的小变换、失真和平移不变(输入中的小失真不会改变汇集的输出-因为我们在局部邻域中取最大值/平均值)。

**全连通层:**这一层将计算类分数，其中每个数字对应一个类分数。与普通神经网络一样，顾名思义，这一层中的每个神经元都将连接到前一卷中的所有神经元。简而言之，它执行最后的分类。

**[*注:这个模型的训练是通过反向传播完成的，所以你可以在反向传播上查看这个单独的博客。*](https://www.edureka.co/blog/backpropagation/)**

通过这种方式，ConvNets 将原始图像从原始像素值逐层变换到最终的类得分。

这是对卷积神经网络的一个非常简短的介绍，我仍然建议你看看我在这篇文章中嵌入的 CNN 视频。

在这篇胶囊网络博客中，我将讨论卷积神经网络的一些局限性

## **卷积神经网络的局限性:**

好吧，让我用一个类比来解释一下。

假设有一个人，他的眼睛可以察觉到各种图像的特征。让我们以人脸为例。所以，这个不幸的家伙可以识别各种特征，比如眼睛，鼻子等等。但是，不能识别特征之间的空间关系(视角、大小、方向)。举个例子，下面这张图可能会骗过那个家伙，把它归类为一张很好的人脸素描。

![Limitations of Convolutional Neural Networks - Capsule Networks - Edureka](img/daa8d820124b70b7ea59e1c88ff01a6f.png)

这也是卷积神经网络的问题。CNN 擅长检测特征，但会错误地激活神经元进行人脸检测。这是因为它在探索要素之间的空间关系时效率较低。

简单的 CNN 模型可以正确提取鼻子、眼睛和嘴巴的特征，但会错误地激活用于人脸检测的神经元。在没有意识到空间方向和尺寸的不匹配的情况下，面部检测的激活将会过高。

![CNN - Capsule Networks - Edureka](img/366346ffad45a98303725df61034756b.png)

这个限制是因为最大池层。

CNN 中的最大池处理平移方差。即使一个特征被轻微移动，如果它仍然在池窗口内，它仍然可以被检测到。然而，这种方法只保留了 max 特性(最主要的),而丢弃了其他特性。

所以，上图这张脸会被归类为正常脸。池层也增加了这种类型的不变性。

这从来都不是池层的意图。汇集应该做的是引入位置，方向，比例不变。

实际上，这个池层增加了各种各样的位置不变性。正如你在上面的图表中看到的，这导致了正确检测人脸的困境。

让我们看看 **[杰弗里·辛顿](https://arxiv.org/abs/1710.09829)提出的解决方案是什么。**

## **如何解决这个问题？**

现在，我们假设每个神经元都包含特征的可能性和属性。例如，它输出一个包含[可能性，方向，大小]的向量。利用该空间信息，我们可以检测鼻子、眼睛和耳朵特征之间的方向和大小的不一致，并因此输出低得多的面部检测激活。

在杰弗里·辛顿发表的论文中，这些类型的神经元被称为胶囊。这些胶囊输出一个矢量，而不是一个单一的标量值。

让我来介绍一下什么是胶囊网络。

## **什么是胶囊网络？**

胶囊基本上是一组嵌套的神经层。胶囊内神经元的状态捕捉图像内一个实体的各种属性，如姿势(位置、大小、方向)、变形、速度、纹理等。

胶囊被训练来捕捉特征及其变体的可能性，而不是捕捉具有特定变体的特征。因此，胶囊的目的不仅是检测特征，而且是训练模型来学习变体。

使得同一个胶囊可以检测不同方位(例如顺时针旋转)的同一物体类别:

![Capsule Neural Network Example - Capsule Networks - Edureka](img/44a55d3cb15ce8c1b592d57955c110c1.png)

我们可以说它作用于等方差而不是不变性。

**不变性:**是对特征的检测，不考虑变体。例如，鼻子检测神经元检测鼻子，而不考虑方向。

**等方差:**是对可以相互变换的物体的检测(比如检测不同朝向的人脸)。直观地，胶囊网络检测到脸部被向右旋转 31(等变)，而不是意识到脸部匹配旋转 31 的变型。通过迫使模型学习胶囊中的特征变体，我们可以用更少的训练数据更有效地推断可能的变体。此外，我们可以更有效地拒绝对手。

一个胶囊输出一个矢量来表示实体的存在。向量的方向代表实体的属性。

向量被发送给神经网络中所有可能的亲本。对于每个可能的亲本，胶囊可以找到一个预测向量。预测向量是基于乘以其自身的权重和权重矩阵来计算的。无论哪一个亲本具有最大的标量预测矢量积，都会增加胶囊结合。其余的父母减少他们的债券。这就是所谓的。

与最大池相比，这无疑是一种更好的方法，在最大池中，路由基于在较低层中检测到的最强特征。

在此之后，增加了挤压功能。这样做是为了引入非线性。这个挤压函数应用于每个胶囊的矢量输出。

现在让我告诉你，胶囊网络是如何工作的。

## **胶囊网络如何工作？**

让我们后退一步。在全连接网络中，每个神经元的输出是输入的加权和。

![Fully Connected Network - Capsule Neural Network - Edureka](img/12150c9895c51aaa6187bf7830a97dd8.png)

现在，让我们看看胶囊网络会发生什么。

### **胶囊神经网络:**

让我们考虑一个胶囊神经网络，其中‘uI是在 下面的层中的胶囊’I’的活动向量。T17

Step–1:将一个变换矩阵 W ij 应用于上一层的胶囊输出 u i 。比如，用一个 m×k 矩阵，我们把一个 k-duI变换成一个 m-du^j | I。((m×k)×(k×1)= m×1)。

![Capsule Neural Network Input - Capsule Neural Network - Edureka](img/705e1cbad58a47251b6afc8c41b48cd4.png)

![Prediction Vector - Capsule Neural Network - Edureka](img/5d947e872e7bd33fd6905c5588698dee.png) 是从胶囊‘I’对上面胶囊‘j’的输出的预测(**投票**)。vj’是上一层中胶囊' j' 的活动向量

第二步:用权重 c ij 计算加权和 s j 。cij为耦合系数。这些系数的总和等于 1。这是我们之前讨论过的影响胶囊组关系的实际参数。

![Weighted Sum - Capsule Neural Networks - Edureka](img/6ac40f2dd84d83c1854614269f7e5fc7.png)

第三步:在卷积神经网络中，我们使用 ReLU 函数。这里，我们将应用一个挤压函数在 0 和单位长度之间缩放向量。它将小向量收缩为零，将长向量收缩为单位向量。因此，每个胶囊的可能性被限制在零和一之间。

![Squashing Function - Capsule Neural Networks - Edureka](img/dbaa9fe5209bfd03c264d578207ce1c0.png)

![Squashing Function Condition - Capsule Neural Networks - Edureka](img/3cdd9bf324e59df3d82e2e0ba35695f5.png)

![Prediction Vector - Capsule Neural Network - Edureka](img/5d947e872e7bd33fd6905c5588698dee.png) 是从胶囊‘I’对上面胶囊‘j’的输出的预测(**投票**)。如果活动向量与预测向量具有密切的相似性，我们推断胶囊'I '与胶囊'【j’高度相关。(比如鼻囊和面囊高度相关。)使用预测和活动向量的标量积来测量这种相似性。因此，相似性同时考虑了可能性和特征属性。(而不仅仅是神经元中的可能性)。

步骤–4:计算相关性分数‘bij’。它将是活动向量和预测向量的点积。耦合系数cI计算为bIj

![Relevance Score - Capsule Neural Networks - Edureka](img/4d30c6af64930ee5fda6df6a9dddfeee.png)

耦合系数 c ij 计算为 b ij 的 softmax。

![Coupling Coefficient - Capsuule Neural Networks - Edureka](img/6ea269001dceacfef2cb5eeedbfcdc0f.png)

这个 b ij 在多次迭代中迭代更新。

![Updating Relevance - Capsule Neural Networks - Edureka](img/72044d465c58c3ca994ba143800690bc.png)

这就是所谓的 ***协议路由*** 。

下图是一个例子:

![Capsule Neural Network Architecture - Capsule Networks - Edureka](img/36227e2d531ec16dff7aec0551792c6a.png)

在这篇关于胶囊网络的博客之后，我将写一篇关于使用 TensorFlow 实现胶囊神经网络的博客。

*我希望你喜欢在 capsule networks 上阅读这篇博客，请查看 Edureka 的* ***[深度学习与 TensorFlow 培训](https://www.edureka.co/ai-deep-learning-with-tensorflow/)*** *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

查看 Edureka 的这个[](https://www.edureka.co/python-natural-language-processing-course)NLP 课程，将您的人工智能技能提升到下一个级别 Edureka 深度学习 TensorFlow 认证培训课程帮助学习者成为使用实时项目和任务以及 SoftMax 函数、自动编码器神经网络、受限玻尔兹曼机器(RBM)等概念来培训和优化基本和卷积神经网络的专家。

*有问题吗？请在评论区提到它，我们会给你回复。*