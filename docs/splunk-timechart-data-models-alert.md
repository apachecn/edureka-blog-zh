# Splunk 知识对象:Splunk 时间表、数据模型和警报

> 原文：<https://www.edureka.co/blog/splunk-timechart-data-models-alert/>

在我之前的博客中，我讨论了 Splunk 架构(T2)、各种组件以及 Splunk 的内部工作方式。在这篇博客中，我们将了解知识对象的相关性以及它在为您的企业带来运营效率方面所扮演的角色。在这里，我将解释 3 个主要的知识对象:Splunk 时间表、数据模型和警报。

请看下图，了解知识对象是如何工作的。

![Splunk knowledge objects - Edureka](img/d02ce0b546b45d524feb5c8cf8cbdd44.png)

数据首先存储在索引器中，然后您可以编写搜索查询并对数据执行各种操作。您可以设置知识对象来使操作更加智能&来为您的系统带来智能。这些知识对象将监控您的事件&在某些情况发生时给出通知。这些结果可以通过创建报告和时间表进行整理和可视化。总而言之，知识对象是丰富数据和创造智能的核心。

知识对象是用户定义的实体，用于从现有或运行时数据中提取知识，以丰富数据。

那么，让我们从第一个知识对象开始，即 Splunk 时间表。

## **Splunk 时间表**

让我来解释一下 Splunk 时间表以及它们的使用场合。例如，假设您有大量数据，您需要衡量一家国际服装连锁店每月的销售额和收入。Splunk Timechart 可用于分析绩效指标(本例中为销售额和收入)随着时间的推移是呈上升趋势还是下降趋势。

Splunk 时间图是指任何数据相对于时间的可视化。 在 Timechart 中，数据以折线图、面积图或柱形图的形式表示，x 轴始终是时间字段，而 y 轴是变量字段。对于上面的例子，如果我们必须每月为一家服装连锁店的销售和收入数字创建时间表，我们可以在 y 轴上绘制销售和收入，在 x 轴上绘制时间。Splunk 时间表可视化效果如下:

![Splunk Timechart - Edureka](img/bb6e08ec960dcfedb54361f8fecfe351.png)

Splunk Timechart 经常被比作 Stats 和 chart 命令。这三个命令之间的底层结构有很大不同，您可以参考解释它们之间区别的表格。

| **统计数据** | **图表** | **时间表** |
| Stats 是一个报告命令，用于以表格格式显示数据。 | 图表以条形图、折线图或面积图的形式显示数据。它还提供了生成饼图的能力。 | time chart 允许您查看条形图和折线图。然而，饼图是不可能的。 |
| 在 Stats 命令中，你可以使用多个字段来构建一个表。 | 在图表中，只需要 2 个字段，每个字段分别在 X 轴和 Y 轴上。 | 在 Timechart 中，由于 X 轴固定为时间字段，所以只需要 1 个字段。 |

现在，您知道如何使用 Splunk Timechart 可视化数据。接下来，我们来学习另一个知识对象——Splunk 数据模型。让我帮助你正确地理解它。

## **Splunk 数据模型**

假设您有大量对您的业务至关重要的非结构化数据，并且您想要一种简单的方法来访问这些信息，而不需要使用复杂的搜索查询。这可以通过使用数据模型来实现，因为它以一种排序和分层的方式呈现您的数据。 数据模型的主要好处是:

*   它帮助非技术用户通过 pivot UI 与数据交互，因为他们不必沉迷于编写复杂的搜索查询。枢纽是数据集的一种表现形式，以表格、图表或任何一种可视化。创建透视后，可以将其保存为报表或仪表板面板。

*   数据模型使得重用领域知识变得容易。【T2

*   由于 Splunk 机器分析难以理解，数据模型有助于提供一种结构化的方法来映射复杂的数据。

![Splunk Data Models - Edureka](img/593ecdb50a84363713bfee00d44cc89b.png)

数据模型，顾名思义，是由一个或多个数据集组成的模型。数据模型有助于为复杂的数据提供结构，并提供更广阔的视角来理解源、逻辑和领域知识。这可以基于数据集生成专门的搜索。 数据模型是 Splunk 中的主要知识对象之一，因为它结合了其他知识对象来为您的数据提供有意义的表示。数据模型是多个知识对象的组合，如查找、事件类型、字段等(参见下图)。

![Components of Data Models - Edureka](img/69974f3e2e54725dd0594c33635b8862.png)

我将在下一篇博客中详细解释这些知识对象。

到目前为止，您可能已经理解了什么是数据模型以及它们的用处。您一定也想知道是否可以生成自己的数据模型。答案是肯定的，您可以设计一个新的数据模型，也可以编辑现有的模型。这可以使用数据模型编辑器来完成。但是，只有被分配了 Admin 或 Power 角色的用户才能创建数据模型。其他用户必须首先管理他们的权限才能创建数据模型。【T2

让我带你看一下创建数据模型的步骤:

**第一步** **:** 进入设置- >数据模型。【T6

**第二步** **:** 点击‘新建数据模型’创建新的数据模型。

**第三步** **:** 给你的数据模型指定一个‘标题’。您可以在标题中使用 任何字符，除了星号。数据模型“ID”字段将自动填充，因为它是唯一的标识符。它只能包含字母、数字和下划线。字符之间不允许有空格。

**第四步** **:** 选择你目前正在使用的‘App’。默认情况下，它将是“home”。

**第五步** **:** 给你的数据模型添加一个‘描述’。

**第六步:** 点击【创建】 ，在数据模型编辑器中打开新的数据模型。 下面，我附上了一个截图，可以帮助你理解创建数据模型的过程:

![Creation of data models Edureka](img/b2ab659cef342d8f7693e35c11175a85.png)

现在让我们了解一下数据模型是如何被使用的:

**Splunk 用例** **项目陈述:**创建数据模型，解决达美乐比萨的大数据挑战。

我们都熟悉达美乐比萨。它在 81 个国家有分店，是世界上最大的比萨饼连锁店之一。首先，你知道他们是如何从几个接触点实时收集数据的吗？其次，他们如何在全球范围内检查实时数据以提高客户绩效？

在这种情况下，数据模型是理想的，因为它们有助于以结构化的方式组织和管理大量数据。 以 Domino 为例，它将返回一个 JSON 文件作为“Domino 的数据”数据模型。它具有模型 ID“Splunk 数据模型教程”。现在，让我们看看数据模型是如何组织数据的:

![Data models json response - Edureka](img/353b1a92c31fa10d8a7e0f55beb99861.png)

*注:所使用的促销数据示例具有代表性，所提供的数据可能不准确。

在本例中，如果您将原始数据发送到 Splunk，数据模型将通过在 JSON 中表示该数据来帮助您创建结构。

从上图可以看出， t 这是一个对象名称列表，包含五个子集:客户错误、订单失败、电话订单、网站订单和促销优惠。第一个子集“客户错误”包含客户在处理订单时面临的所有错误数据。第二个子集，“失败订单”包含处理失败订单的所有相关数据。第三个子集“电话订单”包含通过电话处理的数据。“网站订单”将收集通过 domino 网站订购的数据，第五个子集“促销优惠”处理来自 Domino 的所有优惠券和优惠。

由于数据模型将数据划分为不同的子集，它使您的数据变得清晰，有助于您以分层格式对其进行分析，从而解决 Domino 的大数据挑战。

到目前为止，您已经让了解了如何使用 Splunk 时间表可视化数据，以及如何使用数据模型管理数据。接下来，让我解释另一个知识对象，即 Splunk 警报，以及如何使用它。

## **Splunk 预警**

让我们考虑这样一种情况，您有一个实时应用程序需要一直运行。如果它崩溃或在操作过程中出现错误，需要立即识别并修复问题。但是你怎么知道什么时候出了问题呢？您不能手动坐在系统前全天候监控其状态。方便的解决方法是在出现问题时立即得到通知。这就是 Splunk 提醒可以帮助您的地方。

*   警报用于监控您的事件，并在预定义的条件发生时执行操作。
*   根据搜索结果和用户定义的条件触发警报。
*   警报使用保存的搜索来实时或在预定时间查找事件。
*   这里的是一组提醒动作，帮助你获得关于特定事件的通知。警报操作是指当警报被触发时发生的响应。一些主要的警报动作有:
    *   邮件通知:向指定的收件人发送邮件通知
    *   运行脚本:调用自定义脚本
    *   发送日志 事件:发送日志事件到 Splunk 接收端点
    *   Webhook:通用 HTTP POST 到一个指定的 URL。

现在您对什么是 Splunk 警报及其工作原理有了基本的了解，让我进一步列出不同类型的警报以及它们的使用时间:

![Types of alerts - Edureka](img/da92112ded3156552a43a1f50f27fa49.png)

在上图中，您可以看到有两种类型的警报:预设警报和实时警报。此外，实时警报还可进一步分为基于结果的警报和滚动窗口警报。别担心，我会详细解释每一个问题。首先，让我们从定时预警开始:

假设您属于一家零售公司，并且需要了解每天结束时的销售状态，您可以创建一个计划预警，在每天上午 12 点通知总销售额。只要不需要对事件做出立即响应，就可以使用这种类型的警报。

**实时警报:**这种类型的警报在需要对事件做出即时响应时使用。如前所述，实时警报根据进一步分为-结果警报和滚动窗口警报，解释如下:

*   **每结果警报:**让我们来看一个场景，网络网站管理员想知道网站何时因错误“500”而关闭。在这里，管理员可以选择每个结果的触发条件，以便可以跟踪每个失败的尝试。 如果您希望在搜索返回与搜索条件匹配的结果时收到实时通知，可以使用按结果警报类型。
*   **滚动窗口警报:**假设您需要创建一个警报，通知用户在 15 分钟内连续 5 次登录失败。这可以通过滚动时间窗口触发的实时警报来实现。它用于监视特定时间间隔内的结果，如每 30 分钟或 1 小时，只要它匹配搜索条件。

现在您已经知道了不同类型的警报，您一定想知道如何创建警报。

**问题陈述:**假设每当您在 web 主机上遇到异常多的服务器错误时，您都希望得到警报。

对于这些类型的场景，您可以按照以下步骤创建警报。 **步骤 1:** 打开您的 Splunk Enterprise，并编写您想要作为警报的搜索条件。 在上面的场景中，您可以保存下面的搜索查询来设置预警:source type = access _ combined status>= 500

**第二步** **:** 编写完搜索查询后，当您点击“另存为”按钮时，将会询问您一系列问题，如警报标题、描述、类型、权限等等。 您可以使用 cron 时间表，它简化了这个过程，并带来了在任何时间点执行任务的灵活性。可以通过使用一些 cron 参数对应到分钟，小时，月日，月日星期来实现。我们使用 cron 表达式来定制一个时间表。 例如:*/5 * * * *–每 5 分钟一次*/30 * * * *–每 30 分钟一次0 */12 * * *–每 12 小时一次，整点 0 */20 ***-每 20 分钟一次，周一至周五。 0 9 1-7 * 1-每月第一个星期一，上午 9 点。

下面，我附上了一个截图，可以帮助您理解创建提醒的步骤:

![Creation of Alert - Edureka](img/751f4bc73d19657d072eb098d5ba5fe2.png)

在这篇博客中，我解释了三个与通知和可视化数据相关的知识对象。在我的下一篇博客中，我将解释一些有助于简化搜索的知识对象，如事件、事件类型、标签、字段、宏和查找。希望你喜欢阅读我的第一篇关于知识对象的博客。请继续关注我这个系列的下一篇博客！

*您是否希望学习 Splunk 并在您的企业中实施？点击此处查看我们的 [Splunk 认证培训](https://www.edureka.co/splunk-certification-training)，该培训包含讲师指导的现场培训和真实项目体验。*