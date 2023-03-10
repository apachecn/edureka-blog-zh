# Pig 编程:UDF 在 HDFS 模式下的 Apache Pig 脚本

> 原文：<https://www.edureka.co/blog/pig-programming-apache-pig-script-with-udf-in-hdfs-mode/>

在之前的博客文章中，我们看到了如何从 ***Pig 编程和脚本*** 开始。我们已经看到了在 HDFS 模式下编写 [**猪脚本的步骤**](https://www.edureka.co/blog/pig-programming-create-your-first-apache-pig-script/) 和 **[猪脚本本地模式下](https://www.edureka.co/blog/pig-programming-apache-pig-script-in-local-mode/)** 没有 UDF。在本系列的第三部分中，我们将回顾在 HDFS 模式 下用 ***UDF 编写一个猪脚本的步骤。***

我们已经解释了如何通过创建内置函数来实现 Pig UDF，以解释 Pig 内置函数的功能。为了更好地解释，我们采用了两个内置函数。我们在一个猪脚本的帮助下完成了这个任务。

在这里，我们举了一个例子，我们使用了 UDF(用户定义的函数),也就是说，让一个字符串大写，然后取一个值并提高它的幂。

下面描述了我们将在本例中使用的数据集:

[![table](img/2ae57ff7053a9dd7611b5a33de7ea600.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/table.png)

我们的目标是使第一列字母大写，并用第三列的值提高第二列的能力。

让我们从为每个 UDF 编写 java 代码开始。此外，我们必须在 java 项目中配置 4 个 jar 以避免编译错误。首先，我们将创建 java 程序，如下所示:

### Upper.java

```
import java.io.IOException;
import org.apache.pig.EvalFunc;
import org.apache.pig.data.Tuple;
import org.apache.pig.impl.util.WrappedIOException;

@SuppressWarnings("deprecation")
public class Upper extends EvalFunc<String> {

public String exec(Tuple input) throws IOException {

if (input == null || input.size() == 0)

return null;

try {

String str = (String) input.get(0);

str=str.toUpperCase();

return str;

}
catch (Exception e) {

throw WrappedIOException.wrap("Caught exception processing input row ", e);

}
}
}
```

### Power.java

```
import java.io.IOException;
import org.apache.pig.EvalFunc;
import org.apache.pig.PigWarning;
import org.apache.pig.data.Tuple;

public class Pow extends EvalFunc<Long> {

public Long exec(Tuple input) throws IOException {
try {

int base = (Integer)input.get(0);
int exponent = (Integer)input.get(1);
long result = 1;

/* Probably not the most efficient method...*/
for (int i = 0; i < exponent; i++) {
long preresult = result;
result *= base;
if (preresult > result) {
// We overflowed. Give a warning, but do not throw an
// exception.
warn("Overflow!", PigWarning.TOO_LARGE_FOR_INT);
// Returning null will indicate to Pig that we failed but
// we want to continue execution.
return null;
}
}
return result;
} catch (Exception e) {
// Throwing an exception will cause the task to fail.
throw new IOException("Something bad happened!", e);
}
}
}
```

为了消除编译错误，我们必须在 java 项目中配置 4 个 jar。

[![1](img/ac70eeff328cc228ac61c8ddb78da3d6.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/11.jpg)

**点击下载按钮下载 JARs**

[button leads form _ title = " Download Code " redirect _ URL = https://edu reka . wistia . com/medias/wt BOE 1 hmkr/Download？media _ file _ id = 76900193 course _ id = 166 button _ text = "下载 JARs"]

现在，我们导出两个 java 代码的 JAR 文件。请检查以下 JAR 创建步骤。

这里，我们已经展示了一个程序，在下一个程序中也以同样的方式进行。

[![2](img/12653fa04a10b585c67de304d3c2f6c3.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/2.jpg)

[![3](img/3605e6e9b554522da37dacd120ca6fc7.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/31.jpg)

[![4](img/6ca848bff7b95116fce749f7ba9d60af.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/4.jpg)

[![5](img/c43565a0c6a768b3820547593aada011.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/5.jpg)

创建 jar 和文本文件后，我们已经将所有数据移动到 HDFS 集群，如下图所示:

[![a1](img/dc627492ed9ef34735ef671575321465.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/a1.png)

在我们的数据集中，字段用逗号(，)分隔。

[![13](img/48ce7ff4223ea568bf4ae317dcc88f5d.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/13.png)

移动文件后，我们用。pig 扩展名，并将所有命令放在该脚本文件中。

现在，在“终端”中，键入 PIG，后跟脚本文件的名称，如下图所示:

[![14](img/4b84099a4bf5430278d03ce67cf0f505.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/14.png)

这里，这是运行 pig 脚本的输出。

[![15](img/770e69e9a53abe80037e65a11531b994.png)](https://www.edureka.co/blog/wp-content/uploads/2013/11/15.png)

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[阿帕奇猪创造 UDF 的步骤](https://www.edureka.co/blog/creating-udf-in-apache-pig/)

[阿帕奇蜂巢简介](https://www.edureka.co/blog/introduction-to-apache-hive/)

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop)