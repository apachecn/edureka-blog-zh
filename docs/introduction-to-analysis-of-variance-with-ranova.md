# R 方差分析简介(ANOVA)

> 原文：<https://www.edureka.co/blog/introduction-to-analysis-of-variance-with-ranova/>

[//www.youtube.com/embed/FpSao4vWVgQ](//www.youtube.com/embed/FpSao4vWVgQ)

## **什么是方差分析？**

R 中的方差分析(ANOVA)用于比较两个或多个项目之间的平均值。这是一种统计方法，产生的值可以进行测试，以确定变量之间是否存在显著的关系。

示例:

*   一家汽车公司希望比较三种相似型号汽车的平均汽油消耗量，每种型号有六辆汽车。它遵循 6×3 矩阵，列有汽车，行有模型。在这里，我们比较平均汽油消耗量。
*   一位教师对比较五门不同科目考试的平均分数感兴趣，八名学生完成每门考试后即可获得分数。如果老师想要比较五个不同科目的所有学生的平均分数%,为了比较两个实体之间的平均值，我们使用方差分析。

以汽车为例，这里我们假设有 3 种汽车型号:汽车 A、汽车 B 和汽车 C。汽车 A 有 6 排，汽车 B 有 6 排，汽车 C 有 6 排。首先，我们计算所有组的平均值，称为总体平均值。然后，它计算每组中每个人的分数与组均值的总偏差——组内变异。接下来，它计算每个组的平均值除以总平均值，即组间方差。在 ANOVA 中，我们计算两个组变量，这是总平均值(18 辆车的平均值)，然后计算每个单独得分与组平均值的总偏差。

现在，它计算每组平均值与总体平均值的偏差(组间差异)。然后，ANOVA 使用 f 检验比较“组间变异”和“组内变异”，然后根据 f 检验值，得出所有模型的平均值应该相等还是不同的结论。

## **![ANOVA - edureka](img/bdee4de63ce65307bb5d67ae5f576b7a.png)双向方差分析**

让我们以一个案例为例，该案例包含观察值、性别、剂量等元素，每个元素有 16 个观察值。它们都必须是数字，因为使用了均值和方差。

在这里的性别，我们必须转换成虚拟变量，这涉及到分配数字，如 1 和 0 的男性和女性。但是方差 LSS 只能应用于定量数据。

方差分析是统计假设检验的一种特殊形式，常用于实验数据的分析。统计假设检验是一种利用数据做出决策的方法。假设零假设为真，如果一个测试结果被认为不太可能是偶然发生的，那么这个测试结果(从零假设和样本计算出来的)被称为具有统计显著性。当概率(p 值)小于阈值(显著性水平)时，统计上显著的结果证明拒绝零假设是合理的，但仅当零假设的先验概率不高时。

## **单向方差分析**

上表中有 Df 和 Sum Sq 等元素，它们是单向方差分析的组成部分。

**Df(自由度)**–从统计学的角度来看，假设数据是没有统计约束的终点。这里，自由度是 N。当 N 个数据的平均值是 1000 时，自由度将是 N-1。如果有更多的统计约束，那么自由度将是 N-2，依此类推。

**Sum Sq(平方和)**–这是一种计算变化的方法。当我们谈论变化时，它总是在价值和平均值之间计算。

方差分析是几种观点的综合，用于多种目的。因此，很难简明或精确地定义。它也用于逻辑回归。它不仅用于计算平均值，还用于检查不同模型的性能。f 检验用于比较解释方差和未解释方差之间的差异。在方差分析中，我们采用基于组内变异到组间变异的 f 检验。

有问题要问我们吗？？在评论区提到它们，我们会给你回复。

**相关帖子:**

[商业分析与 R 培训](https://www.edureka.co/r-for-analytics)

[商业分析学导论](https://www.edureka.co/blog/videos/introduction-business-analytics-with-r/ "Introduction to Business Analytics with R")