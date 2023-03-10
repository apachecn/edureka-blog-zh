# 阿帕奇猪 UDF:第 2 部分-加载函数

> 原文：<https://www.edureka.co/blog/apache-pig-udf-part-2-load-functions/>

今天的帖子是关于 Apache Pig 中的加载函数。这是 [第一帖](https://www.edureka.co/blog/apache-pig-udf-part-1-eval-aggregate-filter-functions/) 的续篇，其中涵盖了 UDF 函数，如 Eval、Filter 和 Aggregate。有关猪 UDF 的其他功能的更多信息，请参考他们。

Pig 的 load 函数建立在 Hadoop 的 InputFormat 之上，这是 Hadoop 用来读取数据的类。InputFormat 有两个用途:它确定如何在地图任务之间对输入进行分段，并提供一个 RecordReader，该 record reader 生成键值对作为这些地图任务的输入。load 函数的基类是 LoadFunc。

## **加载功能-分类:**

LoadFunc 抽象类有三个加载数据的主要方法，在大多数用例中，扩展它就足够了。还有另外三个可选接口可以实现扩展功能:

*   #### **Loading metadata:**

LoadMetadata 有处理元数据的方法。大多数加载器的执行不需要实现这一点，除非它们与元数据系统交互。该接口中的 getSchema()方法为加载器实现提供了一种将数据模式反馈给 Pig 的方式。如果加载器实现返回由实类型字段组成的数据，它应该提供描述通过 getSchema()方法返回的数据的模式。其他方法处理其他类型的元数据，如分区键和统计数据。如果这些方法对其他实现无效，实现可以为这些方法返回 null 返回值。

*   #### **Load and push down:**

LoadPushDown 有不同的方法将操作从 Pig 运行时推入加载器实现。目前，Pig 只调用 pushProjection()方法来与加载程序通信，这正是 Pig 脚本中需要的字段。加载器实现可以选择接受或不接受请求。如果加载器实现决定接受请求，它应该实现 LoadPushDown 来提高查询性能。

*   #### **push projection():**

该方法通知 LoadFunc，Pig 脚本中需要哪些字段。从而使 LoadFunc 能够通过只加载所需的字段来提高性能。pushProjection()采用“requiredFieldList”“requiredFieldList”是只读的，不能由 LoadFunc 更改。“requiredFieldList”包括一个“requiredField”列表，其中每个“requiredField”表示 Pig 脚本所需的一个字段，由索引、别名、类型和子字段组成。Pig 使用列索引 requiredField.index 与 LoadFunc 就 Pig 脚本所需的字段进行通信。如果必填字段是映射，Pig 将传递“requiredField.subFields ”,其中包含 Pig 脚本对映射所需的键列表。

*   #### **Truck casters:**

LoadCaster 拥有将字节数组转换成特定类型的技术。当需要支持从 DataByteArray 字段到其他类型的隐式或显式转换时，加载器实现应该实现这一点。

LoadFunc 抽象类是为实现加载程序而扩展的主要类。需要被覆盖的方法解释如下:

*   #### **输入格式()**

    Pig 调用此方法来获取加载程序使用的 InputFormat。Pig 以与 MapReduce Java 程序中 Hadoop 相同的方式调用 InputFormat 中的方法。如果 InputFormat 是 Hadoop 打包的格式，实现应该使用基于新 API 的格式，在 org.apache.hadoop.mapreduce 下。如果是自定义的 InputFormat，最好使用 org.apache.hadoop.mapreduce 中的新 API 来实现。

*   #### **setLocation():**

    Pig 调用该方法将装载位置通知给装载器。加载程序需要使用这个方法将相同的信息传递给核心 InputFormat。这个方法被猪多次调用。

*   #### **prepareToRead():**

    在这个方法中，与 LoadFunc 提供的 InputFormat 相关的 RecordReader 被传递给 LoadFunc。现在，getNext()中的实现可以使用 RecordReader 将表示数据记录的元组返回给 Pig。

*   #### **getnext():t1**

    getNext()的含义没有改变，由 Pig 运行时调用以获取数据中的下一个元组。在此方法中，实现应使用基础 RecordReader 并构造要返回的元组。

## **load func 中默认实现:**

请注意，LoadFunc 中的默认实现应该仅在需要时被覆盖。

*   #### **setudfccontext signature():**

    Pig 将在前端和后端调用该方法，以将唯一的签名传递给加载程序。签名可用于将加载程序需要在前端和后端的各种方法调用之间存储的任何信息存储到 UDFContext 中。一个用例是在 getNext()中返回元组之前，在 loadpushdown . push projection(RequiredFieldList)中存储传递给它的 RequiredFieldList，供后端使用。LoadFunc 中的默认实现有一个空体。此方法将在其他方法之前被调用。

*   #### **相对绝对路径():**

    Pig 运行时将调用此方法，以允许加载程序将相对加载位置转换为绝对位置。LoadFunc 中提供的默认实现为文件系统位置处理这个问题。如果加载源是其他东西，加载器实现可以选择覆盖它。

示例中的加载器实现是一个文本数据加载器，行分隔符为''，默认字段分隔符为' '，类似于 Pig 中的当前 PigStorage 加载器。该实现使用现有的 Hadoop 支持的 Inputformat–TextInputFormat–作为底层 input format。

```
public class SimpleTextLoader extends LoadFunc {
protected RecordReader in = null;
private byte fieldDel = '	';
private ArrayList<Object> mProtoTuple = null;
private TupleFactory mTupleFactory = TupleFactory.getInstance();
private static final int BUFFER_SIZE = 1024;
public SimpleTextLoader() {
}
/**
* Constructs a Pig loader that uses specified character as a field delimiter.
*
* @param delimiter
*            the single byte character that is used to separate fields.
*            ("	" is the default.)
*/
public SimpleTextLoader(String delimiter) {
this();
if (delimiter.length() == 1) {
this.fieldDel = (byte)delimiter.charAt(0);
} else if (delimiter.length() >  1 & & delimiter.charAt(0) == '') {
switch (delimiter.charAt(1)) {
case 't':
this.fieldDel = (byte)'	';
break;
case 'x':
fieldDel =
Integer.valueOf(delimiter.substring(2), 16).byteValue();
break;
case 'u':
this.fieldDel =
Integer.valueOf(delimiter.substring(2)).byteValue();
break;
default:
throw new RuntimeException("Unknown delimiter " + delimiter);
}
} else {
throw new RuntimeException("PigStorage delimeter must be a single character");
}
}
@Override
public Tuple getNext() throws IOException {
try {
boolean notDone = in.nextKeyValue();
if (notDone) {
return null;
}
Text value = (Text) in.getCurrentValue();
byte[] buf = value.getBytes();
int len = value.getLength();
int start = 0;
for (int i = 0; i < len; i++) {
if (buf[i] == fieldDel) {
readField(buf, start, i);
start = i + 1;
}
}
// pick up the last field
readField(buf, start, len);
Tuple t =  mTupleFactory.newTupleNoCopy(mProtoTuple);
mProtoTuple = null;
return t;
} catch (InterruptedException e) {
int errCode = 6018;
String errMsg = "Error while reading input";
throw new ExecException(errMsg, errCode,
PigException.REMOTE_ENVIRONMENT, e);
}
}
private void readField(byte[] buf, int start, int end) {
if (mProtoTuple == null) {
mProtoTuple = new ArrayList<Object>();
}
if (start == end) {
// NULL value
mProtoTuple.add(null);
} else {
mProtoTuple.add(new DataByteArray(buf, start, end));
}
}
@Override
public InputFormat getInputFormat() {
return new TextInputFormat();
}
@Override
public void prepareToRead(RecordReader reader, PigSplit split) {
in = reader;
}
@Override
public void setLocation(String location, Job job)
throws IOException {
FileInputFormat.setInputPaths(job, location);
}
}
*Got a question for us? Please mention it in the comments section and we will get back to you.*
```

**相关帖子:**

[关于 Hadoop 你需要知道的一切](https://www.edureka.co/blog/hadoop-tutorial/ "All you need to know about Hadoop")

[大数据入门& Hadoop](https://www.edureka.co/big-data-and-hadoop)