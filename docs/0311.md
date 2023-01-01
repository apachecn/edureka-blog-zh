# Oozie 简介

> 原文：<https://www.edureka.co/blog/brief-introduction-to-oozie/>

Oozie 是一个工作流调度系统，用于管理 Apache Hadoop 作业。它与 Hadoop 堆栈的其余部分集成，支持多种类型的 Hadoop 作业，如 Java MapReduce、Streaming MapReduce、Pig、Hive 和 Sqoop。Oozie 是一个可伸缩、可靠和可扩展的系统。这项技术被用于雅虎的生产中。，每天运行 20 多万个作业。

[//www.youtube.com/embed/HcDvRnYAaHU](//www.youtube.com/embed/HcDvRnYAaHU)

## **特征:**

*   在 Hadoop 中执行和监控工作流
*   工作流程的定期调度
*   触发数据可用性的执行
*   HTTP 和命令行界面以及 web 控制台

## **工作流-作业的有向无环图:**

## **工作流示例:**

```
<workflow-app nome='wordcount –wf’>
 <start to= ‘wordcount’/>
<action name=’Wordcount'>
 <map-reduce>
<job-tracker>foo.com:9001</job-tracker>
<name-node>hdfs://bar.com:9000</name-node>
 <configuration>
<property>
 <name>mapred.input.dir</name>
 <value>${inputDir}</value,>
 </property>
<property>
 <name>mapred.output.dir</name>
 <value> ${outputDir}</value>
 </property>
 </configuration>
 </map-reduce>
<ok to='end’/>
 <error to='kill'/>
 </action>
<kill name='kill'/>
<end name='end'/>
 </Workflow-app>
```

## **工作流定义:**

工作流定义是具有控制流节点或动作节点的 DAG，其中节点由转换箭头连接。

**控制流程节点:**

控制流提供了一种控制工作流执行路径的方法。工作流应用程序中的流控制操作可以通过以下节点完成:

*   开始/结束/终止
*   决定
*   分叉/连接

**动作节点:**

*   地图缩小
*   猪
*   HDFS
*   子工作流程
*   Java–运行定制的 Java 代码

## **工作流应用:**

工作流应用程序是一个 ZIP 文件，其中包含工作流定义和运行所有操作所需的文件。它包含以下文件:

*   配置文件–config-default . XML
*   App 文件–包含 JAR 和 SO 文件的 lib/目录
*   猪脚本

## **应用部署:**

```
$ hadoop fs-put wordcount-wf hdfs://bar.com:9000/usr/abc/wordcount
```

## **工作流作业参数:**

```
$ cat job.properites
Oozie.wf.application.path=hdfs://bar.com:9000/usr/abc/wordcount
Input=/usr/abc/input-data
Output=/usr/abc/output-data
```

## **作业执行:**

```
$ oozie job –run –config job.properties
Job:1-20090525161321-oozie-xyz-W
```

有问题要问我们吗？在评论区提到它们，我们会给你回复。

![edureka](img/981b79f2904efe6f9320df33611b9823.png)