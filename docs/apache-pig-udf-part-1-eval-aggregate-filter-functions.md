# Apache Pig UDF:第 1 部分——评估、聚集和过滤函数

> 原文：<https://www.edureka.co/blog/apache-pig-udf-part-1-eval-aggregate-filter-functions/>

Apache Pig 提供了对用户定义函数(UDF)的广泛支持，作为指定定制处理的一种方式。Pig UDFs 目前可以用三种语言执行: *Java，Python，JavaScript，Ruby。*为 Java 函数提供了最广泛的支持。

Java UDFs 可以通过多种方式调用。最简单的 UDF 可以扩展 EvalFunc，只需要实现 exec 函数。每个评估 UDF 必须实现这一点。此外，如果一个函数是代数的，它可以实现代数接口来显著提高查询性能。

## **猪 UDF 的重要性:**

Pig 允许用户通过 UDF 将现有的操作符与自己或他人的代码结合起来。Pig 的优势在于它能够让用户通过 UDF 将它的操作符与自己或他人的代码结合起来。从 0.7 版本开始，所有的 UDF 都必须用 Java 编写，并作为 Java 类来实现。通过编写一个 Java 类并通知 Pig 关于 JAR 文件的信息，这使得向 Pig 添加新的 UDF 变得更加容易。

猪本身自带一些 UDF。在 0.8 版本之前，它是一个非常有限的集合，只有标准的 SQL 聚合函数和一些其他函数。在 0.8 中，添加了大量的标准字符串处理、数学和复杂类型的 UDF。

## **什么是小猪银行？**

Piggybank 是一个用户贡献的 UDF 集合，与 Pig 一起发布。Piggybank UDFs 不包含在 Pig JAR 中，所以您必须在脚本中手动注册它们。您也可以编写自己的 UDF 或使用其他用户编写的 UDF。

## **Eval 函数**

UDF 类扩展了 EvalFunc 类，它是所有 Eval 函数的基础。所有的求值函数都扩展了 Java 类“org.apache.pig.EvalFunc”，它用 UDF 的返回类型参数化，在本例中是一个 Java 字符串。这个类的核心方法是“exec”代码的第一行表明该函数是 myudfs 包的一部分。

它接受一条记录并返回一个结果，将为通过执行管道的每条记录调用该结果。它接受一个元组，该元组包含脚本作为输入传递给 UDF 的所有字段。然后它返回参数化 EvalFunc 的类型。

这个函数在每个输入元组上都被调用。该函数的输入是一个元组，其中的输入参数按照它们在 Pig 脚本中传递给函数的顺序排列。在下面的示例中，该函数将字符串作为输入。下面的函数将字符串从小写转换成大写。现在函数已经实现了，需要编译并包含在一个 JAR 中。

```
package myudfs;
import java.io.IOException;
import org.apache.pig.EvalFunc;
import org.apache.pig.data.Tuple;
public class UPPER extends EvalFunc<String>
{
public String exec(Tuple input) throws IOException {
if (input == null || input.size() == 0)
return null;
try{
String str = (String)input.get(0);
return str.toUpperCase();
}catch(Exception e){
throw new IOException("Caught exception processing input row ", e);
}
}
}
```

## **聚合函数:**

聚合函数是另一种常见的 Eval 函数。聚合函数通常应用于分组数据。聚合函数接受一个包并返回一个标量值。许多聚合函数的一个有趣且有价值的特性是，它们可以以分布式方式进行增量计算。在 Hadoop 世界中，这意味着部分计算可以由 Map 和 Combiner 来完成，最终结果可以由 Reducer 来计算。

非常重要的一点是，要确保代数聚合函数是这样实现的。这种类型的示例包括内置计数、最小值、最大值和平均值。

**COUNT** 是一个代数函数的例子，我们可以计算数据子集中元素的数量，然后对这些计数求和以产生最终输出。让我们看看 COUNT 函数的实现:

```
public class COUNT extends EvalFunc<Long> implements Algebraic{
public Long exec(Tuple input) throws IOException {return count(input);}
public String getInitial() {return Initial.class.getName();}
public String getIntermed() {return Intermed.class.getName();}
public String getFinal() {return Final.class.getName();}
static public class Initial extends EvalFunc<Tuple> {
public Tuple exec(Tuple input) throws IOException {return TupleFactory.getInstance().newTuple(count(input));}
}
static public class Intermed extends EvalFunc<Tuple> {
public Tuple exec(Tuple input) throws IOException {return TupleFactory.getInstance().newTuple(sum(input));}
}
static public class Final extends EvalFunc<Long> {
public Tuple exec(Tuple input) throws IOException {return sum(input);}
}
static protected Long count(Tuple input) throws ExecException {
Object values = input.get(0);
if (values instanceof DataBag) return ((DataBag)values).size();
else if (values instanceof Map) return new Long(((Map)values).size());
}
static protected Long sum(Tuple input) throws ExecException, NumberFormatException {
DataBag values = (DataBag)input.get(0);
long sum = 0;
for (Iterator (Tuple) it = values.iterator(); it.hasNext();) {
Tuple t = it.next();
sum += (Long)t.get(0);
}
return sum;
}
}
```

COUNT 实现如下所示的代数接口:

```
public interface Algebraic{
public String getInitial();
public String getIntermed();
public String getFinal();
}
```

对于一个代数函数，它需要实现由从 EvalFunc 派生的三个类的定义组成的代数接口。约定是初始类的 execfunction 被调用一次，传递给原始输入元组。它的输出是一个包含部分结果的元组。Intermed 类的 exec 函数可以被调用零次或更多次，并将包含由初始类或 Intermed 类的先前调用产生的部分结果的元组作为其输入，并产生具有另一部分结果的元组。最后，调用最后一个类的 exec 函数，并以标量类型给出最终结果。

## **过滤功能:**

过滤函数是返回布尔值的评估函数。它可以用在布尔表达式适用的任何地方，包括过滤运算符或 Bincond 表达式。Apache Pig 不完全支持 Boolean，因此过滤函数不能出现在诸如“Foreach”之类的语句中，在这些语句中，结果被输出到另一个操作符。但是，筛选函数可以在筛选语句中使用。

下面的示例实现了 IsEmpty 函数:

```
import java.io.IOException;
import java.util.Map;
import org.apache.pig.FilterFunc;
import org.apache.pig.PigException;
import org.apache.pig.backend.executionengine.ExecException;
import org.apache.pig.data.DataBag;
import org.apache.pig.data.Tuple;
import org.apache.pig.data.DataType;
/**
* Determine whether a bag or map is empty.
*/
public class IsEmpty extends FilterFunc {
@Override
public Boolean exec(Tuple input) throws IOException {
try {
Object values = input.get(0);
if (values instanceof DataBag)
return ((DataBag)values).size() == 0;
else if (values instanceof Map)
return ((Map)values).size() == 0;
else {
int errCode = 2102;
String msg = "Cannot test a " +
DataType.findTypeName(values) + " for emptiness.";
throw new ExecException(msg, errCode, PigException.BUG);
}
} catch (ExecException ee) {
throw ee;
}
}
}
```