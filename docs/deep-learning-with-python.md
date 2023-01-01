# Python 深度学习:深度学习初学者指南

> 原文：<https://www.edureka.co/blog/deep-learning-with-python/>

[](https://www.edureka.co/ai-deep-learning-with-tensorflow)深度学习是 2018-19 年最热门的话题之一，这是有充分理由的。在工业中已经有了如此多的进步，其中机器或计算机程序实际上代替人类的时代已经到来。这篇使用 Python 的 ***深度学习*** 文章将帮助你理解深度学习到底是什么，以及这种转变是如何实现的。或者，你可以查看 Edureka 的[深度学习课程](https://www.edureka.co/ai-deep-learning-with-tensorflow)，获得认证！

在本文中，我将涉及以下主题:

*   [数据科学及其组成部分](#ds-components)
*   [对深度学习的需求](#need-for-dl)
*   [什么是深度学习？](#what-is-dl)
*   [感知器和人工神经网络](#perceptron)
*   [深度学习的应用](#applications-of-dl)
*   [为什么用 Python 做深度学习？](#why-python)
*   [用 Python 进行深度学习:感知器示例](#dl-perceptron)
*   [用 Python 进行深度学习:创建深度神经网络](#dl-deep-neural-network)

## 数据科学及其组成部分

数据科学已经存在很长时间了。 [**数据科学**](https://www.edureka.co/blog/what-is-data-science/) 是利用不同的技术和算法从数据中提取知识。

![AI Timeline - Deep Learning with Python - Edureka](img/762363579229bafefb0b6c8ef7486806.png)

[**人工智能**](https://www.edureka.co/blog/what-is-artificial-intelligence) 是一种使机器能够模仿人类行为的技术。人工智能背后的想法相当简单却又令人着迷，那就是制造能够自己做出决定的智能机器。多年来，人们认为计算机永远比不上人脑的能力。

![Machine Learning - Deep Learning with Python](img/2850bcadac5ffca37a8047a4384ed5a9.png)

嗯，当时我们没有足够的数据和计算能力，但现在随着 [**大数据**](https://www.edureka.co/blog/big-data-tutorial) 的出现，以及 GPU 的出现，人工智能成为可能。

[**机器学习**](https://www.edureka.co/blog/what-is-machine-learning/) 是人工智能技术的一个子集，它使用统计方法使机器能够随着经验而改进。

**深度学习** 是 ML 的子集，使得多层神经网络的计算变得可行。它使用神经网络来模拟类似人类的决策。

## 对深度学习的需求

迈向人工智能的一步是机器学习。机器学习是人工智能的一个子集，它基于这样一种想法，即机器应该能够访问数据，应该能够自己学习和探索。它处理从大型数据集中提取模式。处理大型数据集不是问题。

*   机器学习算法**无法处理高维数据**——我们有大量的输入和输出:对数千维进行舍入。处理和加工这种类型的数据变得非常复杂，而且会耗尽资源。这被称为**维度诅咒。**

![Need for Deep Learning - Deep Learning with Python](img/4f6b6a7b94d25652713ef4b295072bf1.png)

*   面临的另一个挑战是，指定要提取的特征。这在预测结果以及实现更高的准确性方面起着重要的作用。因此，没有特征提取，程序员的挑战增加了，因为算法的有效性很大程度上取决于程序员的洞察力。

现在，这就是深度学习来拯救我们的地方。深度学习**能够处理高维数据**，并且在**专注于正确的特征**方面也很有效。

这里有[深度学习认证](https://www.edureka.co/ai-deep-learning-with-tensorflow)课程，可以给你提供轻松创建深度学习系统的智能和专业水平。

## 什么是深度学习？

深度学习是机器学习的一个子集，其中类似的机器学习算法用于训练[](https://www.edureka.co/blog/pytorch-tutorial/)深度神经网络，以便在前者表现不达标的情况下实现更好的准确性。基本上，**深度学习模仿了我们大脑的运作方式**，即它从经验中学习。

![deep-learning-with-python](img/88852faabfe8a366f1ff1ba92beebff9.png)

如你所知，我们的大脑是由数十亿个神经元组成的，这些神经元让我们能够做出惊人的事情。即使小孩子的大脑也能解决复杂的问题，而这些问题即使使用超级计算机也很难解决。那么，我们如何在一个程序中实现同样的功能呢？现在，这就是我们理解**人工神经元(感知器)**和**人工神经网络的地方。**

## 感知器和人工神经网络

深度学习研究大脑的基本单元，称为脑细胞或神经元。现在，让我们了解生物神经元的功能，以及我们如何在感知或人工神经元中模仿这种功能。

![neuron-Deep Learning with Python](img/c9e969df34e0f7433fb518820d3b97c2.png)

*   **树突:**接收来自其他神经元的信号
*   **单元体:**对所有输入进行求和
*   **轴突:**用于向其他细胞传递信号

人工神经元或**感知器**是用于二元分类的线性模型。它模拟了一个有一组输入的神经元，每个输入都有一个特定的权重。神经元对这些**加权**输入计算一些函数，并给出输出。

![Perceptron- Deep Learning with Python](img/c68956f6dc24fcd65a77fcf74de0e319.png)

它接收 n 个输入(对应于每个特征)。然后，它将这些输入相加，应用一个变换并产生一个输出。它有两个功能:

*   总和
*   转化(激活)

权重显示了特定输入的有效性。**输入的权重越大，对神经网络的影响就越大**。另一方面，**偏差**是感知器中的**附加参数**，用于调整输出以及神经元输入的加权和，这有助于模型最适合给定数据。

**激活功能**将输入转化为输出。它使用阈值来产生输出。有许多功能可用作激活功能，例如:

*   线性或恒等式
*   单位或二进制步长
*   乙状结肠或逻辑
*   双曲正切
*   热卢
*   Softmax

好吧。如果你认为感知器解决了问题，那你就错了。有两个主要问题:

*   单层感知器**无法对非线性可分离数据点**进行分类。
*   单层感知器无法解决涉及大量参数的复杂问题。

考虑一下这个例子，以及营销团队做出决策所涉及的参数的复杂性。

![Limitations of Single Layer Perceptron - Neural Network Tutorial - Edureka](img/ca75ab2b34c1e1a0f3e94100d26d9db8.png)

一个神经元不能接受这么多的输入，这就是为什么要用一个以上的神经元来解决这个问题。神经网络实际上只是感知器的**组合，以不同的方式**连接，并对不同的激活功能进行操作。

![Neural-net Deep Learning with Python](img/a00c3c0a71f5214306f12c9ce80a2a82.png)

*   **输入节点**向网络提供来自外界的信息，统称为“输入层”。
*   **隐藏节点**执行计算并将信息从输入节点传输到输出节点。隐藏节点的集合形成了“隐藏层”。
*   **输出节点**统称为“输出层”，负责计算并将信息从网络传输到外部世界。

现在你对感知机的行为方式、涉及的不同参数和神经网络的不同层有了一个概念，让我们通过 Python 博客继续这个深度学习，看看深度学习的一些很酷的应用。

## 深度学习的应用

深度学习在行业中有各种各样的应用，这里有几个在我们日常任务中存在的重要应用。

*   **语音识别**

**![speech-recognition](img/68e7a66906790ff8cc198343bbdc194a.png)**

*   **机器翻译**

**![machine-translation](img/d3fdc35a6c91c5b09767ad94929e867b.png)**

*   **面部识别和自动标记**

**![Fb-PhotoTag-applications-of-machine-learning](img/bdc62ae077e7551e5f04679f3239c70d.png)**

*   **虚拟个人助理**

![virtual-assistants-applications-of-deep-learning](img/a26b2c027d2606dab6d860cf16827a1e.png)

*   **自动驾驶汽车**

**![self-driving-car](img/76b8ef980f2a8591a094fde4f0992ffc.png)**

*   聊天机器人

![chatbot](img/c67600d2ba427727f40715295f41ab5e.png)

## 为什么用 Python 做深度学习？

*   [**Python**](https://www.edureka.co/blog/python-tutorial/) 就是这样一种工具，它有一个独特的属性，即作为一种**通用编程语言**在分析和定量计算方面易于使用**。**
*   这很容易理解
*   Python 是**动态类型的**
*   巨大的 [**社区支持**](https://www.edureka.co/community/tag/python)
*   各种不同用途的库，如 Numpy、Seaborn、Matplotlib、Pandas 和 Scikit-learn

![python-libraries](img/0e2c0f2521058690b6551fdeb93dd073.png)

现在，理论已经足够了，让我们看看如何通过一个小而令人兴奋的例子开始用 Python 进行深度学习。

## 使用 Python 进行深度学习:感知器示例

现在，我相信你们一定很熟悉“**或“**门”的工作原理。如果任何输入也是 **1，则输出为 **1** 。**

![or-gate](img/dd268f96f01a92e702612355cbe70608.png)

因此，感知器可用作分隔符或判定线，将 or 门的输入集分为两类:

**第 1 类:**输出为 0 的输入位于判定线以下。 **第 2 类:**输入输出为 1，位于判定线或分隔符之上。

到目前为止，我们知道线性感知器可以用来将输入数据集分为两类。但是，它是如何对数据进行分类的呢？

![perceptron-equation](img/b08ef1ae6d82984f0195a490f42abfd2.png)

在数学上，感知器可以被认为是一个权重、输入和偏差的等式。

### **第一步:导入所有需要的库**

在这里，我将只导入一个库。TensorFlow

```

import tensorflow as tf

```

### **第二步:定义输入和输出的向量变量**

接下来，我们需要创建变量来存储感知器的输入、输出和偏差。

```

train_in = [
[0,0,1],
[0,1,1],
[1,0,1],
[1,1,1]]

train_out = [
[0],
[1],
[1],
[1]]

```

### **第三步:定义权重变量**

这里，我们将为我们的权重定义形状为 3×1 的张量变量，并最初为其分配一些随机值。

```

w = tf.Variable(tf.random_normal([3, 1], seed=15))

```

### **步骤 4:为输入和输出定义占位符**

我们需要定义占位符，以便它们可以在运行时接受外部输入。

```

x = tf.placeholder(tf.float32,[None,3])
y = tf.placeholder(tf.float32,[None,1])

```

### **第五步:计算输出和激活函数**

如前所述，感知器接收的输入首先乘以各自的权重，然后，所有这些加权的输入相加在一起。然后，该求和值被馈送到激活，以获得最终结果。

![or-gate-perceptron](img/79d6f6d0d2e4df0c8255d51761efcd39.png)

```

output = tf.nn.relu(tf.matmul(x, w))

```

注意:在这种情况下，我使用了 ***relu*** 作为我的激活函数。您可以根据需要自由使用任何激活功能。

### **第六步:计算成本或误差**

我们需要计算成本=均方差，也就是感知器输出和期望输出之差的平方。

```

loss = tf.reduce_sum(tf.square(output - y))

```

### **第七步:最小化误差**

感知器的目标是最小化损失或成本或错误。这里我们将使用梯度下降优化器。

```

optimizer = tf.train.GradientDescentOptimizer(0.01)
train = optimizer.minimize(loss)

```

### **步骤 8:初始化所有变量**

变量只能用 *tf.Variable.* 来定义，所以，我们需要初始化定义的变量。

```

init = tf.global_variables_initializer()
sess = tf.Session()
sess.run(init)

```

### **步骤 9:在迭代中训练感知器**

我们需要训练我们的感知器，即在连续迭代中更新权重和偏差的值，以最小化误差或损失。在这里，我将用 100 个纪元来训练我们的感知机。

```

for i in range(100):
sess.run(train, {x:train_in,y:train_out})
cost = sess.run(loss,feed_dict={x:train_in,y:train_out})
print('Epoch--',i,'--loss--',cost)

```

### **第十步:输出**

![perceptron-output](img/e60fc8b167b5ca218a6ccbb05102ceaa.png)

……

……

![perceptron-output-2](img/1706146a6943226b0dd7f8f05ed2b0ef.png)

正如你在这里看到的，损失开始于 **2.07** ，结束于 **0.27**

。

## 用 Python 进行深度学习:创建深度神经网络

现在，我们已经成功地创建了一个感知器，并训练它用于或门。让我们继续这篇文章，看看如何可以从头开始创建我们自己的神经网络，我们将创建一个输入层，隐藏层和输出层。

我们将使用 MNIST 的数据集。MNIST 数据集由手写数字图像的 **60，000 个训练**样本和 **10，000 个测试**样本组成。图像大小为 **28×28 像素**，输出可以在 **0-9** 之间。

**这里的任务是训练一个模型，它可以准确地识别图像上出现的数字**

![Image Recognition - Deep Learning With Python - Edureka](img/023fc54d3cf478bc199884ea0bb70c57.png)

首先，我们将使用下面的导入将打印功能从 Python 3 引入 Python 2.6+。__future__ 语句需要放在文件的顶部附近，因为它们改变了语言的基本特性，所以编译器需要从一开始就了解它们

```

from __future__ import print_function

```

**下面是每一步都有注释的代码**

```

# Import MNIST data
from tensorflow.examples.tutorials.mnist import input_data
mnist = input_data.read_data_sets("/tmp/data/", one_hot=True)

import tensorflow as tf
import matplotlib.pyplot as plt

# Parameters
learning_rate = 0.001
training_epochs = 15
batch_size = 100
display_step = 1

# Network Parameters
n_hidden_1 = 256 # 1st layer number of features
n_hidden_2 = 256 # 2nd layer number of features
n_input = 784 # MNIST data input (img shape: 28*28)
n_classes = 10 # MNIST total classes (0-9 digits)

# tf Graph input
x = tf.placeholder("float", [None, n_input])
y = tf.placeholder("float", [None, n_classes])

# Create model
def multilayer_perceptron(x, weights, biases):
    # Hidden layer with RELU activation
    layer_1 = tf.add(tf.matmul(x, weights['h1']), biases['b1'])
    layer_1 = tf.nn.relu(layer_1)
    # Hidden layer with RELU activation
    layer_2 = tf.add(tf.matmul(layer_1, weights['h2']), biases['b2'])
    layer_2 = tf.nn.relu(layer_2)
    # Output layer with linear activation
    out_layer = tf.matmul(layer_2, weights['out']) + biases['out']
    return out_layer

# Store layers weight & bias
weights = {
    'h1': tf.Variable(tf.random_normal([n_input, n_hidden_1])),
    'h2': tf.Variable(tf.random_normal([n_hidden_1, n_hidden_2])),
    'out': tf.Variable(tf.random_normal([n_hidden_2, n_classes]))
}

biases = {
    'b1': tf.Variable(tf.random_normal([n_hidden_1])),
    'b2': tf.Variable(tf.random_normal([n_hidden_2])),
    'out': tf.Variable(tf.random_normal([n_classes]))
}

# Construct model
pred = multilayer_perceptron(x, weights, biases)

# Define loss and optimizer
cost = tf.reduce_mean(tf.nn.softmax_cross_entropy_with_logits(logits=pred, labels=y))
optimizer = tf.train.AdamOptimizer(learning_rate=learning_rate).minimize(cost)

# Initializing the variables
init = tf.global_variables_initializer()

#create an empty list to store the cost history and accuracy history
cost_history = []
accuracy_history = []

# Launch the graph
with tf.Session() as sess:
    sess.run(init)

    # Training cycle
    for epoch in range(training_epochs):
        avg_cost = 0.
        total_batch = int(mnist.train.num_examples/batch_size)
        # Loop over all batches
        for i in range(total_batch):
            batch_x, batch_y = mnist.train.next_batch(batch_size)

            # Run optimization op (backprop) and cost op (to get loss value)
            _, c = sess.run([optimizer, cost], feed_dict={x: batch_x,y: batch_y})
            # Compute average loss
            avg_cost += c / total_batch
        # Display logs per epoch step
        if epoch % display_step == 0:

            correct_prediction = tf.equal(tf.argmax(pred, 1), tf.argmax(y, 1))
            # Calculate accuracy
            accuracy = tf.reduce_mean(tf.cast(correct_prediction, "float"))
            acu_temp = accuracy.eval({x: mnist.test.images, y: mnist.test.labels})
            #append the accuracy to the list
            accuracy_history.append(acu_temp)
            #append the cost history
            cost_history.append(avg_cost)
            print("Epoch:", '%04d' % (epoch + 1), "- cost=", "{:.9f}".format(avg_cost), "- Accuracy=",acu_temp)

    print("Optimization Finished!")
    #plot the cost history
    plt.plot(cost_history)
    plt.show()
    #plot the accuracy history
    plt.plot(accuracy_history)
    plt.show()

    # Test model
    correct_prediction = tf.equal(tf.argmax(pred, 1), tf.argmax(y, 1))
    # Calculate accuracy
    accuracy = tf.reduce_mean(tf.cast(correct_prediction, "float"))
    print("Accuracy:", accuracy.eval({x: mnist.test.images, y: mnist.test.labels}))

```

**输出:**

![mnist-output-deep learning with python](img/42cd863bb7bfd2200bc5f987cf21f159.png)

![final-graph](img/4fe17ed5e3f86aeb71aef4ae3c705aca.png)

至此，我们结束了这篇关于 Python 深度学习的文章。我希望你理解了深度学习的各个组成部分，它是如何开始的，以及我们如何使用 Python 来创建简单的感知机和深度神经网络。

*Edureka 的 [**深度学习在 TensorFlow 带 Python 认证培训**](https://www.edureka.co/ai-deep-learning-with-tensorflow) 由行业专业人士根据行业要求&需求策划。您将掌握 SoftMax 函数、自动编码器神经网络、受限玻尔兹曼机(RBM)等概念，并使用 Keras & TFLearn 等库。该课程由行业专家通过实时案例研究特别策划。*

通过我们的[人工智能课程](https://www.edureka.co/executive-programs/machine-learning-and-ai) 发现你成为 AI 和 ML 专业人士的全部能力。了解各种人工智能相关技术，如机器学习、深度学习、计算机视觉、自然语言处理、语音识别和强化学习。

有问题要问我们吗？请在“用 Python 进行深度学习”的评论部分提到它，我们会给你回复。或者，去查查夏洛特的[深度学习培训！](https://www.edureka.co/ai-deep-learning-with-tensorflow-charlotte)