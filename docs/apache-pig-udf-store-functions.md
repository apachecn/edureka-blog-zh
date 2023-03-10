# 阿帕奇猪 UDF:第 3 部分-商店功能

> 原文：<https://www.edureka.co/blog/apache-pig-udf-store-functions/>

StoreFunc 抽象类有存储数据的主要方法，对于大多数用例来说，扩展它就足够了。有一个可选的接口，可以实现扩展功能:

## **存储元数据**

该接口具有与元数据系统交互的方法，以存储模式和统计数据。这个接口是可选的，只有在需要存储元数据时才应该实现。

需要在 StoreFunc 中覆盖的方法解释如下:

*   #### **getoutput format():t1**

    Pig 将调用这个方法来获取 Storer 使用的 OutputFormat。OutputFormat 中的方法将由 Pig 以与 map-reduce Java 程序中 Hadoop 相同的方式和在相同的上下文中调用。如果 OutputFormat 是 Hadoop 打包格式，则应使用 org.apache.hadoop.mapreduce 下基于新 API 的实现。如果是自定义 OutputFormat，则应使用 org.apache.hadoop.mapreduce 下的新 API 实现。OutputFormat 的 checkOutputSpecs()方法将由 pig 调用，以预先检查输出位置。当作业启动时，该方法也将作为 Hadoop 调用序列的一部分被调用。所以实现应该确保这个方法可以被多次调用而不会产生不一致的副作用。

*   #### **setStoreLocation():**

    Pig 调用此方法将商店位置传达给商店。storer 应该使用这个方法将相同的信息传递给底层 OutputFormat。这个方法被猪多次调用。实现应该注意到这个方法被多次调用，并且应该确保不会因为多次调用而产生不一致的副作用。

*   #### **prepareToWrite():**

    在新的 API 中，数据的写入是通过 StoreFunc 提供的 OutputFormat 完成的。在 prepareToWrite()中，与 StoreFunc 提供的 OutputFormat 关联的 RecordWriter 被传递给 StoreFunc。然后，putNext()中的实现可以使用 RecordWriter 来以 RecordWriter 所期望的方式编写表示数据记录的元组。

*   #### putnext():

    putNext()的含义没有改变，由 Pig 运行时调用以写入下一个数据元组——在新的 API 中，这是实现将使用底层 RecordWriter 写出元组的方法。

## **store func 中默认实现:**

*   #### **setStoreFuncUDFContextSignature():**

    Pig 将在前端和后端调用该方法，以将唯一的签名传递给 Storer。签名可用于将任何信息存储到 UDFContext 中，存储者需要在前端和后端的各种方法调用之间存储这些信息。StoreFunc 中的默认实现有一个空体。此方法将在任何其他方法之前被调用。

*   #### **relToAbsPathForStoreLocation(): **

    Pig 运行时将调用此方法，以允许存储程序将相对存储位置转换为绝对位置。StoreFunc 中提供了一个实现，它为基于文件系统的位置处理这个问题。

*   #### **检查方案():T1**

    存储函数应该实现这个函数，以检查描述要写入的数据的给定模式对它来说是可接受的。StoreFunc 中的默认实现有一个空体。在调用 setStoreLocation()之前，将调用此方法。

## **示例实现:**

示例中的 storer 实现是一个文本数据的 storer，行分隔符为''，默认字段分隔符为' '(可以通过在构造函数中传递不同的字段分隔符来覆盖)–这类似于 Pig 中的当前 PigStorage storer。该实现使用现有的 Hadoop 支持的 OutputFormat–text output format 作为底层 output format。

```
public class SimpleTextStorer extends StoreFunc {
protected RecordWriter writer = null;
private byte fieldDel = '	';
private static final int BUFFER_SIZE = 1024;
private static final String UTF8 = "UTF-8";
public PigStorage() {
}
public PigStorage(String delimiter) {
this();
if (delimiter.length() == 1) {
this.fieldDel = (byte)delimiter.charAt(0);
} else if (delimiter.length() > 1delimiter.charAt(0) == '') {
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
ByteArrayOutputStream mOut = new ByteArrayOutputStream(BUFFER_SIZE);
@Override
public void putNext(Tuple f) throws IOException {
int sz = f.size();
for (int i = 0; i < sz; i++) {
Object field;
try {
field = f.get(i);
} catch (ExecException ee) {
throw ee;
}
putField(field);
if (i != sz - 1) {
mOut.write(fieldDel);
}
}
Text text = new Text(mOut.toByteArray());
try {
writer.write(null, text);
mOut.reset();
} catch (InterruptedException e) {
throw new IOException(e);
}
}
@SuppressWarnings("unchecked")
private void putField(Object field) throws IOException {
//string constants for each delimiter
String tupleBeginDelim = "(";
String tupleEndDelim = ")";
String bagBeginDelim = "{";
String bagEndDelim = "}";
String mapBeginDelim = "[";
String mapEndDelim = "]";
String fieldDelim = ",";
String mapKeyValueDelim = "#";
switch (DataType.findType(field)) {
case DataType.NULL:
break; // just leave it empty
case DataType.BOOLEAN:
mOut.write(((Boolean)field).toString().getBytes());
break;
case DataType.INTEGER:
mOut.write(((Integer)field).toString().getBytes());
break;
case DataType.LONG:
mOut.write(((Long)field).toString().getBytes());
break;
case DataType.FLOAT:
mOut.write(((Float)field).toString().getBytes());
break;
case DataType.DOUBLE:
mOut.write(((Double)field).toString().getBytes());
break;
case DataType.BYTEARRAY: {
byte[] b = ((DataByteArray)field).get();
mOut.write(b, 0, b.length);
break;
}
case DataType.CHARARRAY:
// oddly enough, writeBytes writes a string
mOut.write(((String)field).getBytes(UTF8));
break;
case DataType.MAP:
boolean mapHasNext = false;
Map<String, Object> m = (Map<String, Object>)field;
mOut.write(mapBeginDelim.getBytes(UTF8));
for(Map.Entry<String, Object> e: m.entrySet()) {
if(mapHasNext) {
mOut.write(fieldDelim.getBytes(UTF8));
} else {
mapHasNext = true;
}
putField(e.getKey());
mOut.write(mapKeyValueDelim.getBytes(UTF8));
putField(e.getValue());
}
mOut.write(mapEndDelim.getBytes(UTF8));
break;
case DataType.TUPLE:
boolean tupleHasNext = false;
Tuple t = (Tuple)field;
mOut.write(tupleBeginDelim.getBytes(UTF8));
for(int i = 0; i < t.size(); ++i) {
if(tupleHasNext) {
mOut.write(fieldDelim.getBytes(UTF8));
} else {
tupleHasNext = true;
}
try {
putField(t.get(i));
} catch (ExecException ee) {
throw ee;
}
}
mOut.write(tupleEndDelim.getBytes(UTF8));
break;
case DataType.BAG:
boolean bagHasNext = false;
mOut.write(bagBeginDelim.getBytes(UTF8));
Iterator<Tuple> tupleIter = ((DataBag)field).iterator();
while(tupleIter.hasNext()) {
if(bagHasNext) {
mOut.write(fieldDelim.getBytes(UTF8));
} else {
bagHasNext = true;
}
putField((Object)tupleIter.next());
}
mOut.write(bagEndDelim.getBytes(UTF8));
break;
default: {
int errCode = 2108;
String msg = "Could not determine data type of field: " + field;
throw new ExecException(msg, errCode, PigException.BUG);
}
}
}
@Override
public OutputFormat getOutputFormat() {
return new TextOutputFormat<WritableComparable, Text>();
}
@Override
public void prepareToWrite(RecordWriter writer) {
this.writer = writer;
}
@Override
public void setStoreLocation(String location, Job job) throws IOException {
job.getConfiguration().set("mapred.textoutputformat.separator", "");
FileOutputFormat.setOutputPath(job, new Path(location));
if (location.endsWith(".bz2")) {
FileOutputFormat.setCompressOutput(job, true);
FileOutputFormat.setOutputCompressorClass(job,  BZip2Codec.class);
}  else if (location.endsWith(".gz")) {
FileOutputFormat.setCompressOutput(job, true);
FileOutputFormat.setOutputCompressorClass(job, GzipCodec.class);
}
}
}
```

有问题要问我们吗？请在评论区提及它们，我们将会回复您。

**相关帖子:**

[阿帕奇猪 UDF:第二部](https://www.edureka.co/blog/apache-pig-udf-part-2-load-functions/ "Apache Pig UDF: Part 2 – Load Functions") [阿帕奇猪 UDF:第一部](https://www.edureka.co/blog/apache-pig-udf-part-1-eval-aggregate-filter-functions/ "Apache Pig UDF: Part 1 – Eval, Aggregate & Filter Functions")[大数据与 Hadoop 训练](https://www.edureka.co/big-data-and-hadoop)