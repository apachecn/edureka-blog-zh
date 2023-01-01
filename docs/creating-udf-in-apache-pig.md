# 在 Apache Pig 中创建 UDF 的步骤

> 原文：<https://www.edureka.co/blog/creating-udf-in-apache-pig/>

这篇文章包含了在 Apache Pig 中创建 UDF 的必要步骤。所有 UDF 都应该扩展一个过滤函数，并且必须包含一个名为 exec 的方法，该方法包含一个元组。这里应用的逻辑是，如果元组为 null 或零，它会给你一个布尔值:True 或 False。“年龄”用于检查给出的年龄是否正确。用户定义函数的逻辑是用 Java 代码编写的，JAR 文件将在这里创建，然后导出。JAR 文件稍后被注册。这些 JAR 文件可以在加载时在 Apache Pig 的库文件中找到。

```
public class IsOfAge extends FilterFunc {
@Override
publicBoolean exec(Tuple tuple) throwsIOException {
if(tuple == null|| tuple.size() == 0) {
returnfalse;
}
try{
Object object= tuple.get(0);
if(object == null) {
returnfalse;
}
inti = (Integer) object;
if(i == 18 || i == 19 || i == 21 || i == 23 || i == 27) {
returntrue;
} else{
returnfalse;
}
} catch(ExecExceptione) {
thrownewIOException(e);
}
}
}
```

## **如何称呼一头猪为 UDF？**

一旦创建了 UDF，就必须使用下面的命令来注册 JAR 文件。

```
register myudf.jar;
X = filter A by IsOfAge(age);
```

## **在猪身上创造 UDF 的步骤:**

Apache Pig 中有多个预定义的函数。我们还可以创建自己的功能，即用户定义的功能(UDF)。猪 UDF 是用 Java 写的，这需要猪库使用预定义的类。阿帕奇猪库**Pig-0 . 8 . 0-cdh3u 0-core . jar**可以从网上下载。

[点击这里查看在 HDFS 模式下用 UDF 创建猪脚本的步骤。](https://www.edureka.co/blog/pig-programming-apache-pig-script-with-udf-in-hdfs-mode/)

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[阿帕奇与 UDF 在 HDFS 模式下的猪脚本](https://www.edureka.co/blog/pig-programming-apache-pig-script-with-udf-in-hdfs-mode/ "Pig Programming: Apache Pig Script with UDF in HDFS Mode")

[Apache Pig 中的运算符:第 1 部分-关系运算符](https://www.edureka.co/blog/operators-in-apache-pig/ "Operators in Apache Pig: Part 1- Relational Operators")

[Apache Pig 中的运算符:第 2 部分–诊断运算符](https://www.edureka.co/blog/operators-in-apache-pig-diagnostic-operators/ "Operators in Apache Pig: Part 2- Diagnostic Operators")

[大数据和 Hadoop 培训](https://www.edureka.co/big-data-and-hadoop)