# 性能测试教程——它是什么及其类型？

> 原文：<https://www.edureka.co/blog/performance-testing-tutorial/>

现代 IT 时代已经见证了软件测试行业的巨大发展，让位给了更好的前景。因此，确保软件应用程序的有效性能变得非常重要。通过这篇“**性能测试教程**，我将向您提供关于性能测试基础的深入知识，以及一个负载测试工具 JMeter 的细节。

本文涵盖了以下主题。

*   [什么是性能测试？](#WhatisPerformanceTesting?)
*   为什么需要性能测试？
*   [性能测试类型](#TypesofPerformanceTesting)
*   [性能测试流程](#PerformanceTestingProcess)
*   [性能测试指标](#PerformanceTestingMetrics)
*   [性能测试工具](#PerformanceTestingTools)
*   [JMeter 简介](#IntroductiontoJMeter)

你也可以浏览一下这个软件测试教程的录音，我们的 ***[软件测试培训](https://www.edureka.co/software-testing-certification-courses)*** 的专家已经对这些概念进行了深入的解释。

**初学者性能测试教程|爱德华卡**



[https://www.youtube.com/embed/CypSI1Fn2w4?rel=0&showinfo=0](https://www.youtube.com/embed/CypSI1Fn2w4?rel=0&showinfo=0)

这段关于性能测试教程的视频完整地介绍了性能测试、其类型以及如何在 JMeter 的帮助下进行性能测试。

## **什么是性能测试？**

**性能测试**是一种软件测试，确保软件应用程序在预期的工作负载下运行良好。验证产品是否满足预期或要求的性能水平至关重要。性能测试测量系统的质量属性，比如可伸缩性、可靠性和资源使用。

![Performance Testing - Performance Testing Tutorial - Edureka](img/4fbe516b81192a1d81758509fcf2f381.png)  它主要关注软件程序的某些因素，如:

*   **速度**–它标识应用程序的响应是否快速。
*   **可扩展性**——它决定了最大的用户负载。
*   **稳定性**–检查应用程序在变化的负载下是否稳定。

现在您已经知道了什么是性能测试，让我们看看为什么您需要性能测试。

## **为什么需要进行性能测试？**

性能测试提供了关于速度、稳定性和可伸缩性的应用信息。更重要的是，它揭示了产品上市前需要改进的地方。没有这一点，软件可能会遇到一些问题，比如:几个用户同时使用时运行缓慢，不同操作系统之间不一致，可用性差。

[性能测试](https://www.edureka.co/blog/performance-testing-tools/) 确定他们的软件是否满足预期工作负载下的速度、可伸缩性和稳定性要求。由于不存在性能测试或性能测试不佳而导致性能指标不佳的应用程序被推向市场时，很可能会名声不佳，无法达到预期的销售目标。这些是描述性能测试需求的一些原因。

现在让我们更深入地研究这篇性能测试教程文章，看看它的不同类型。

## **性能测试类型**

下图显示了不同类型的性能测试。**![Performance Testing Types - Performance testing Tutorial - Edureka](img/e0f58d0236abb103b8f298a12dd9cc63.png)**

下面我们来深入了解一下它的各种类型的细节。

*   **负载测试—**[负载测试](https://www.edureka.co/blog/load-testing-using-jmeter/) 检查应用程序在预期用户负载下的执行能力。该测试的主要目的是在软件应用程序上线之前识别性能瓶颈。
*   **压力测试—**该测试包括在极端工作负载下测试应用程序，以了解它如何处理高流量或数据处理。在这里，它标识了应用程序的断点。
*   **耐久性测试—**进行该测试是为了确保软件能够长时间处理预期的负载。
*   **峰值测试—**用于测试软件对用户产生的负载突然出现大峰值的反应。
*   **容量测试**–在这里，大量的数据被填充到数据库中，整个软件系统的行为被监控。该测试的主要目的是检查软件应用程序在不同数据库容量下的性能。
*   **可扩展性测试**–可扩展性测试的主要目标是确定软件应用程序在“向上扩展”以支持用户负载增加方面的有效性。

现在您已经对性能测试的基础有了一些了解，让我们进一步了解性能测试过程中涉及的工作和步骤。

## **性能测试流程**

下面的信息图描述了性能测试过程中涉及的步骤。让我们更深入地了解这些步骤的细节:

#### **![Performance testing process - Performance Testing Tutorial - Edureka](img/b782ba3e4376f1493b1ef204e969f232.png) 第一步:确定测试环境**

确定可用于测试的硬件、软件、网络配置和工具。  性能测试环境选项  包括:

*   生产系统的子集，具有较少的低规格服务器
*   生产系统的子集，具有较少的相同规格的服务器
*   生产系统的复制品
*   实际生产系统

#### **第二步:确定绩效指标**

除了确定响应时间、吞吐量和约束等指标之外，还要确定性能测试的成功标准。

#### **第三步:计划和设计性能测试**

确定考虑用户可变性、测试数据和目标度量的性能测试场景。这基本上会创建一个或两个模型。

#### **步骤 4:配置测试环境**

您需要准备监控资源所需的测试环境和仪器的元素。

#### **第五步:实现你的测试设计**

为执行开发和实现测试。

#### **第六步:执行测试**

除了运行性能测试，您还必须监控和捕获生成的数据。

#### **第七步:分析、报告、复试**

最后一步是分析数据并分享发现。这里，您必须使用相同和不同的参数再次运行性能测试。

所以，这就是性能测试过程。现在让我们知道什么是性能测试的测试指标或参数。

## **性能测试指标**

1.  **处理器使用量—**它是处理器执行非空闲线程所花费的时间量。
2.  **内存使用—**它是计算机上进程可用的物理内存量。
3.  **磁盘时间—**磁盘忙于执行读或写请求的时间。
4.  **带宽—**这意味着网络接口每秒使用的位数。
5.  **Private bytes—**它是一个进程已经分配的不能被其他进程共享的字节数。
6.  **提交的内存—**这是使用的虚拟内存的数量。
7.  **内存页数/秒—**这是为了解决硬页面错误而写入或读取磁盘的页数。

现在让我们继续我们的“性能测试教程”,并找出一些用于性能测试的最佳工具。

## **性能测试工具**

性能测试在实时中是非常重要的，尤其是从客户满意度的角度来看。有各种各样的[性能测试工具](https://www.edureka.co/blog/performance-testing-tools/)可用，例如:

*   阿帕奇 JMeter
*   负载运行器
*   WebLOAD
*   装载机队
*   LoadView
*   新负载

谈到性能测试，JMeter 是最受欢迎的工具之一。因此，让我们继续我们的“性能测试教程”来了解这个特定的测试工具。

## **JMeter**简介

[Apache JMeter](https://www.edureka.co/blog/jmeter-tutorial/) 是一款用于测试、分析和衡量不同软件服务和产品性能的工具。它是一个纯 Java 开源软件，用于测试 Web 应用程序或 FTP 应用程序。

主要用于执行 web 应用的性能测试、负载测试和功能测试。JMeter 还可以通过为 web 服务器创建大量虚拟并发用户来模拟服务器上的重负载。

### **JMeter 如何进行测试？**

让我们看看 JMeter 在测试过程中执行的不同步骤:

1.  首先，它创建一个请求并发送给服务器。
2.  一旦它收到来自服务器的响应，它就收集这些响应，并在图表中显示这些细节。
3.  之后，它处理来自服务器的响应。
4.  最后，它以 TXT、XML、JSON 等多种格式生成测试结果，以便测试人员分析数据。

如果你想了解更多关于 *JMeter* 及其工作原理，请阅读这篇关于 **[JMeter 教程](https://www.edureka.co/blog/jmeter-tutorial/)** 的文章。

至此，我们来结束这篇关于性能测试的教程。希望它有助于增加你的知识。快乐学习。

*现在您已经了解了性能测试教程，请查看由 Edureka 提供的使用 JMeter 课程 进行的 [**性能测试，Edureka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。本课程让您深入了解工作负载期间的软件行为。在本课程中，您将学习如何检查软件的响应时间和延迟，以及测试软件包是否能够高效扩展。本课程将帮助您检查强度并分析应用在不同负载类型下的整体性能。**](https://www.edureka.co/jmeter-training-performance-testing)*

*有问题吗？请在**性能测试教程**文章的评论部分提到它，我们会给你回复。*