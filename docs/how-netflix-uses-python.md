# Python 和网飞:当你播放一部电影时会发生什么？

> 原文：<https://www.edureka.co/blog/how-netflix-uses-python/>

每个电影迷的一站式目的地当然是网飞。但是，如果你正在看你最喜欢的电影，它会时不时地缓冲一下呢？你只需关闭应用程序，选择另一个选项。但是，它如何快速管理数百万用户的流量呢？感谢 [PYTHON](https://www.edureka.co/blog/python-programming-language) 。在本文中，让我们探索网飞如何使用 Python。

让我们先快速浏览一下这篇文章的主题:

*   [网飞简介](#whatisnetflix)
*   [网飞如何使用 Python？](#hownetflixusespython)
    *   [打开连接](#openconnect)
    *   [需求工程团队](#demandengineering)
    *   [机器学习基础设施](#machinelearning)
    *   [大数据](#bigdata)
    *   [科学实验](#scientificexperimentation)
    *   [视频编码/媒体云工程](#videoencoding)
    *   [网飞动画和 NVFX](#nvfx)
    *   [IS(信息安全)](#is)
    *   [监控和自动修复](#monitoring)

所以让我们开始吧。:)

## **网飞简介**

网飞是一家提供视频点播服务的美国公司。总部位于加州洛斯加托斯的网飞在全球拥有大约 1.48 亿用户，而且这个数字每天都在增长。在大约二十年的时间里，网飞已经成为世界上最大的电视剧和电影的“家族之王”。作为美国增长最快的品牌，2019 年的收入为 205 亿美元，这足以让它成为一个“引人注目的品牌”，从而吸引所有人对其技术领域的兴趣。

基于同样的兴趣领域，网飞展示了它如何将最流行的语言 [Python](https://www.edureka.co/blog/10-reasons-why-you-should-learn-python) 用于其基础设施。

现在让我们来看看网飞实际上是如何使用 Python 的？

## **网飞如何使用 Python？**

*“We use Python through the full content lifecycle, from deciding which content to fund all the way to operating the CDN that serves the final video to 148 million members”                                                 – Engineers at Netflix *

**从管理领域的到可靠性和[数据科学的](https://www.edureka.co/blog/what-is-data-science/)到[机器学习的](https://www.edureka.co/blog/machine-learning-tutorial/)等等，网飞几乎在他们业务的每个边缘都使用 Python。**

**现在让我们更深入地了解一下 [Python](https://www.edureka.co/blog/learn-python-for-data-science/) 在网飞的各个领域是如何使用的:**

### ****打开连接:****

**网飞使用的 CDN(内容交付网络)是 Open Connect。当你点击“播放”按钮时，打开连接基本上进入画面。交付给最终用户的所有内容都由这个 CDN 负责。**

**Open connect 需要各种其他软件系统来设计、构建和操作它，而这些软件系统又是用 Python 编写的。不仅如此，这个 CDN 底层的网络设备是 Python 应用，因为 Python 在解决网络问题方面很突出。**

### ****需求工程团队:****

**需求工程团队负责处理网飞云的区域故障转移、流量管理、容量运营管理(关注内容可服务的上限)和设备效率。该团队使用的 Python 元素有:**

#### ****NumPy 和 SciPy:****

**NumPy 和 T2 是用于科学计算的库。网飞使用这些 Python 库来执行数值分析，从而允许管理区域故障转移。**

#### ****波特 3:****

**Boto3 是针对 Python 的 [AWS(亚马逊网络服务)](https://www.edureka.co/blog/amazon-aws-tutorial/)的软件开发包(SDK)。这有助于 Python 开发人员将 Python 集成到 AWS 中，从而允许在基础设施中进行开发。**

#### **rq(重定向队列):**

**这是一个 Python 库，有助于跟踪队列中出现的任务，并允许执行这些任务，从而允许管理异步工作负载。**

#### ****烧瓶:****

**最后，网飞使用 Flask (Python Web 开发库)API 将前面的所有部分绑定在一起。**

**网飞使用的 [**Jupyter Notebook**](https://www.edureka.co/blog/cheatsheets/Jupyter-Notebook-Cheat-Sheet) 是一款开源的 web app，与**interact**(Jupyter 的扩展)一起大规模用于 Python 开发。众所周知，Jupyter 在数据分析方面很受欢迎。它在运营数据分析和可视化方面非常有用，这反过来有助于检测容量退化。**

### ****机器学习基础设施:****

**[机器学习](https://www.edureka.co/blog/what-is-machine-learning/)的范围从创建个性化算法到找出用例。个性化算法有助于按照网飞标准训练机器学习模型。它提供个性化推荐、每日概要、标签生成等。**

**学习[深度神经网络](https://www.edureka.co/blog/what-is-deep-learning)需要的库有 **TensorFlow** 、 **Keras** 、 **Pytorch** 而 **XGBoost** 和 **LightGBM** 用于梯度提升决策树。他们还开发了相当多的高级库，帮助结合事实记录、特征提取、发布等工作领域。除此之外，网飞还使用 **MetaFlow** 来创建机器学习项目。**

***“Metaflow pushes the limits of Python: We leverage well parallelized and optimized Python code to fetch data at 10Gbps, handle hundreds of millions of data points in memory, and orchestrate computation over tens of thousands of CPU cores”                                                            – Netflix*** ****### **大数据:**

[大数据](https://www.edureka.co/blog/hadoop-ecosystem)团队负责执行 ETL(提取、转换、加载)和临时管道。这个编排的主要部分是用 Python 编写的。这个团队使用一个在 Jupyter 笔记本和 papermill 上运行的调度程序来生成带有模板的作业类型，例如， [Spark](https://www.edureka.co/blog/spark-tutorial/) ，Presto 等。

除此之外，该团队还创建了一个完全基于 Python 的事件驱动平台。他们已经创建了许多事件，并将其合并成一个单一的允许网飞过滤，反应和路由事件。Pygenie 也是这个基础设施的一部分，它与 genie(特色作业执行服务)接口。

### **科学实验:**

这是一个由科学实验团队创建的平台，允许 **A/B 测试**以及其他一些实验。在这里，科学家和工程师可以展示数据、统计和可视化方面的新创新。

这里实现的 Python [框架](https://www.edureka.co/blog/python-frameworks/)是基于 **PyPika** 的**度量报告**，允许编写可重用的参数化查询。对于统计扇区，使用 **PyArrow** 和 **RPy2** 来计算 Python 或 r 中的统计数据。

### **视频编码/媒体云工程:**

该团队负责网飞目录的编码和重新编码任务。Python 大约用于 50 个项目，如 **VMAF** (视频多方法评估融合) **MezzFS** (夹层文件系统)**计算机视觉解决方案**(处理图像)使用 **Archer** 等。

### **网飞动画和 NVFX:**

Python 是网飞所有动画和视觉效果(VFX)的基础。所有的 Maya 和 Nuke 联盟都是在 Python 上完成的。

### **IS(信息安全):**

网飞将 Python 驱动的 IS 系统用于自动补救、安全自动化、风险分类等。这个团队最活跃的开源 Python 项目是**安全猴**。网飞还使用**祝福** ( Bastion 的 Lambda 短命 SSH 服务)来保护 **SSH** (安全外壳)资源。 **RepoKid** 用于授予 **IAM** 权限，TLS 证书通过 Lemur 分配。这两项任务都主要依赖于 Python。

### **监控和自动修复:**

这个团队被称为洞察工程团队。他们构建并执行工具,用于运营洞察、诊断、自动补救和变更。对于它的大多数服务，这个团队使用 Python，例如，旁观者 Python 客户端库。该库用于记录维度时间序列。除了这些库，像 Winston 和 Bolt 这样的产品也是基于 Python 框架构建的，这些框架是 [Flask](https://www.edureka.co/blog/python-frameworks/#7) 、Gunicorn 和 Flask-RestPlus。

综上所述，人们很容易认为 Python 是网飞的驱动力。至此，关于“网飞如何使用 Python？”的博客到此结束。我希望你清楚所讨论的一切。

*要深入了解 Python 及其各种应用，您可以注册参加实时 **[Python 在线培训](https://www.edureka.co/data-science-python-certification-course)** ，该培训提供全天候支持和终身访问。*

*有问题吗？请在“Python 如何使用网飞”博客的评论部分提到它，我们会尽快回复您。*****