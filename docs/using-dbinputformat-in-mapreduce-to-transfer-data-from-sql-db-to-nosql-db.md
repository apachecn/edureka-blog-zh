# 将数据从 SQL 转移到 NoSQL 数据库的 DBInputFormat

> 原文：<https://www.edureka.co/blog/using-dbinputformat-in-mapreduce-to-transfer-data-from-sql-db-to-nosql-db/>

在这篇博客中，我们将探索 Hadoop 技术中最重要的组件之一 MapReduce 的功能和可能性。

如今，许多公司都将 Hadoop 框架作为数据存储的首选，因为它能够有效地处理大量数据。但是我们也知道数据是多用途的，并且以各种结构和格式存在。为了控制如此多种多样的数据及其不同的格式，应该有一种机制来适应所有的种类，并产生有效和一致的结果。

Hadoop 框架中最强大的组件是 MapReduce，它可以比其他组件更好地控制数据及其结构。虽然这需要额外的学习曲线和编程复杂性，但是如果你能处理这些复杂性，你肯定可以用 Hadoop 处理任何类型的数据。

MapReduce 框架将其所有处理任务分为两个基本阶段:映射和简化。

为这些阶段准备原始数据需要理解一些基本的类和接口。这些再处理的超类是 ***InputFormat。***

***InputFormat*** 类是 Hadoop MapReduce API 中的核心类之一。这个类负责定义两件主要的事情:

*   数据分割
*   唱片阅读器

*数据分割*是 Hadoop MapReduce 框架中的一个基本概念，它定义了单个地图任务的大小及其潜在的执行服务器。*记录阅读器*负责从输入文件中实际读取记录，并将它们(作为键/值对)提交给映射器。

映射器的数量是根据拆分的数量决定的。创建拆分是 InputFormat 的工作。大多数情况下，拆分大小等同于数据块大小，但并不总是根据 HDFS 数据块大小创建拆分。这完全取决于如何覆盖 InputFormat 的 getSplits()方法。

斯普利特和 HDFS·布洛克之间有一个根本的区别。块是数据的物理区块，而分割只是映射器读取的逻辑区块。split 不包含输入数据，它只保存数据的引用或地址。一个 split 基本上有两个东西:以字节为单位的长度和一组存储位置，它们只是字符串。

为了更好地理解这一点，让我们举一个例子:使用 MR 处理存储在 MySQL 中的数据。因为在这种情况下没有块的概念，所以理论:“分割总是基于 HDFS 块创建的”，失败。一种可能是基于 MySQL 表中的行范围创建拆分(这就是 DBInputFormat 所做的，它是一种从关系数据库读取数据的输入格式)。我们可能有 k 个由 n 行组成的拆分。

只有基于 FileInputFormat(一种用于处理存储在文件中的数据的输入格式)的输入格式，才会根据输入文件的总大小(以字节为单位)创建拆分。但是，输入文件的文件系统块大小被视为输入拆分的上限。如果您的文件小于 HDFS 数据块大小，您将只能获得该文件的 1 个映射器。如果你想有一些不同的行为，你可以使用 mapred.min.split.size。但是它同样只取决于你的 InputFormat 的 getSplits()。

我们在包 org . Apache . Hadoop . MapReduce . lib . input 下已经有了很多现成的输入格式。

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineFileInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineFileRecordReader.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineFileRecordReaderWrapper.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineFileSplit.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineSequenceFileInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/CombineTextInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/FileInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/FileInputFormatCounter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/FileSplit.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/FixedLengthInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/InvalidInputException.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/KeyValueLineRecordReader.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/KeyValueTextInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/MultipleInputs.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/NLineInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileAsBinaryInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileAsTextInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileAsTextRecordReader.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileInputFilter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileInputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/SequenceFileRecordReader.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/input/TextInputFormat.html)

**默认为 TextInputFormat。**

同样，我们有许多输出格式，可以从减速器读取数据并将其存储到 HDFS 中:

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/FileOutputCommitter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/FileOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/FileOutputFormatCounter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/FilterOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/LazyOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/MapFileOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/MultipleOutputs.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/NullOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/PartialFileOutputCommitter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/PartialOutputCommitter.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/SequenceFileAsBinaryOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/SequenceFileOutputFormat.html)

![[TXT]](img/09ce9b1f704ec6bc81025a3b9c95a6a7.png)[](https://hadoop.apache.org/docs/current/api/org/apache/hadoop/mapreduce/lib/output/TextOutputFormat.html)

**默认的输入文本输出格式。**

当你读完这篇博客的时候，你应该已经学会了:

*   如何编写一个 map reduce 程序
*   关于 Mapreduce 中可用的不同类型的输入格式
*   输入格式的需求是什么
*   如何编写自定义输入格式
*   如何将数据从 SQL 数据库传输到 HDFS
*   如何将数据从 SQL(这里是 MySQL)数据库转移到 NoSQL 数据库(这里是 Hbase)
*   如何将数据从一个 SQL 数据库转移到另一个 SQL 数据库的表中(如果我们在同一个 SQL 数据库中这样做，这可能不是很重要。然而，拥有相同的知识并没有错。你永远不知道它会怎样派上用场)

**先决条件:**

*   预装 Hadoop
*   预装 SQL
*   预装 Hbase
*   Java 基本理解
*   MapReduce 知识
*   Hadoop 框架基础知识

**让我们来理解一下我们这里要解决的问题陈述:**

我们在关系数据库 Edureka 的 MySQL DB 中有一个雇员表。现在，根据业务要求，我们必须将关系数据库中的所有可用数据转移到 Hadoop 文件系统，即 NoSQL HDFS 数据库，也称为 Hbase。

我们有许多选择来完成这项任务:

*   Sqoop
*   水道
*   MapReduce

现在，您不想为该操作安装和配置任何其他工具。你只剩下一个选择，那就是 Hadoop 的处理框架 MapReduce。MapReduce 框架可以让你在传输的时候完全控制数据。您可以操作这些列，并将其直接放在两个目标位置中的任何一个。

**注:**

*   我们需要下载 MySQL 连接器并将其放在 Hadoop 的类路径中，以便从 MySQL 表中获取表。为此，下载连接器 com.mysql.jdbc_5.1.5.jar 并将其保存在 Hadoop _ home/share/Hadoop/MaPreduce/lib 目录下。

```
cp Downloads/com.mysql.jdbc_5.1.5.jar$HADOOP_HOME/share/hadoop/mapreduce/lib/
```

*   此外，将所有 Hbase jars 放在 Hadoop 类路径下，以便让您的 MR 程序访问 Hbase。为此，执行以下命令 **:**

```
cp $HBASE_HOME/lib/* $HADOOP_HOME/share/hadoop/mapreduce/lib/
```

我在执行该任务时使用的软件版本是:

*   Hadooop-2.3.0
*   HBase 0.98.9-Hadoop2
*   月食月神

为了避免程序出现任何兼容性问题，我规定我的读者在类似的环境下运行该命令。

## 自定义 DBInputWritable:

```
package com.inputFormat.copy;
import java.io.DataInput;
import java.io.DataOutput;
import java.io.IOException;
import java.sql.ResultSet;
import java.sql.PreparedStatement;
import java.sql.SQLException;
import org.apache.hadoop.io.Writable;
import org.apache.hadoop.mapreduce.lib.db.DBWritable;
public class DBInputWritable implements Writable, DBWritable
{
 private int id;
 private String name,dept;
public void readFields(DataInput in) throws IOException { }
public void readFields(ResultSet rs) throws SQLException
 //Resultset object represents the data returned from a SQL statement
 {
 id = rs.getInt(1);
 name = rs.getString(2);
 dept = rs.getString(3);
 }
public void write(DataOutput out) throws IOException { }
public void write(PreparedStatement ps) throws SQLException
 {
 ps.setInt(1, id);
 ps.setString(2, name);
 ps.setString(3, dept);
 }
public int getId()
 {
 return id;
 }
public String getName()
 {
 return name;
 }

 public String getDept()
 {
 return dept;
 }
}
```

## 自定义 DBOutputWritable:

```
package com.inputFormat.copy;
import java.io.DataInput;
import java.io.DataOutput;
import java.io.IOException;
import java.sql.ResultSet;
import java.sql.PreparedStatement;
import java.sql.SQLException;
import org.apache.hadoop.io.Writable;
import org.apache.hadoop.mapreduce.lib.db.DBWritable;
public class DBOutputWritable implements Writable, DBWritable
{
 private String name;
 private int id;
 private String dept;
public DBOutputWritable(String name, int id,String dept )
 {
 this.name = name;
 this.id = id;
 this.dept = dept;
 }
public void readFields(DataInput in) throws IOException { }
public void readFields(ResultSet rs) throws SQLException
 {
 }
public void write(DataOutput out) throws IOException { }
public void write(PreparedStatement ps) throws SQLException
 {
 ps.setString(1, name);
 ps.setInt(2, id);
 ps.setString(3, dept);
 }
}
```

## 输入表格:

```
create database edureka;
```

```
create table emp(empid int not null,name varchar(30),dept varchar(20),primary key(empid));
```

```
insert into emp values(1,"abhay","developement"),(2,"brundesh","test");
```

```
select * from emp;
```

## 案例 1:从 MySQL 转移到 HDFS

```
package com.inputFormat.copy;
import java.net.URI;
import org.apache.hadoop.conf.Configuration;
import org.apache.hadoop.fs.FileSystem;
import org.apache.hadoop.fs.Path;
import org.apache.hadoop.mapreduce.Job;
import org.apache.hadoop.mapreduce.lib.db.DBConfiguration;
import org.apache.hadoop.mapreduce.lib.db.DBInputFormat;
import org.apache.hadoop.mapreduce.lib.output.FileOutputFormat;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.io.IntWritable;

public class MainDbtohdfs
{
 public static void main(String[] args) throws Exception
 {
 Configuration conf = new Configuration();
 DBConfiguration.configureDB(conf,
 "com.mysql.jdbc.Driver", // driver class
 "jdbc:mysql://localhost:3306/edureka", // db url
 "root", // user name
 "root"); //password
Job job = new Job(conf);
 job.setJarByClass(MainDbtohdfs.class);
 job.setMapperClass(Map.class);

 job.setMapOutputKeyClass(Text.class);
 job.setMapOutputValueClass(IntWritable.class);

 job.setInputFormatClass(DBInputFormat.class);

 FileOutputFormat.setOutputPath(job, new Path(args[0]));

 DBInputFormat.setInput(
 job,
 DBInputWritable.class,
 "emp", //input table name
 null,
 null,
 new String[] { "empid", "name" ,"dept"} // table columns
 );

 Path p=new Path(args[0]);
 FileSystem fs= FileSystem.get(new URI(args[0]), conf);
 fs.delete(p);

 System.exit(job.waitForCompletion(true) ? 0 : 1);
 }
}
```

这段代码让我们准备或配置 inputformat 来访问我们的源 SQL DB。参数包括驱动程序类，URL 包含 SQL 数据库的地址、用户名和密码。

```
DBConfiguration.configureDB(conf,
 "com.mysql.jdbc.Driver", // driver class
 "jdbc:mysql://localhost:3306/edureka", // db url
 "root", // user name
 "root"); //password
```

这段代码让我们传递数据库中表的详细信息，并在 job 对象中设置它。参数当然包括作业实例、必须实现 DBWritable 接口的自定义可写类、源表名、条件(如果有的话)else null、任何排序参数 else null、表列列表。

```
DBInputFormat.setInput(
 job,
 DBInputWritable.class,
 "emp", //input table name
 null,
 null,
 new String[] { "empid", "name" ,"dept"} // table columns
 );
```

## Mapper

```
package com.inputFormat.copy;
import java.io.IOException;
import org.apache.hadoop.mapreduce.Mapper;
import org.apache.hadoop.io.LongWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.io.IntWritable;
public class Map extends Mapper<LongWritable, DBInputWritable, Text, IntWritable>
{
```

```
protected void map(LongWritable key, DBInputWritable value, Context ctx)
 {
 try
 {
 String name = value.getName();
 IntWritable id = new IntWritable(value.getId());
 String dept = value.getDept();
```

```
ctx.write(new Text(name+"	"+id+"	"+dept),id);
```

```
} catch(IOException e)
 {
 e.printStackTrace();
 } catch(InterruptedException e)
 {
 e.printStackTrace();
 }
 }
 }
```

## 减速器:标识使用的减速器

**运行命令:**

```
hadoop jar dbhdfs.jar com.inputFormat.copy.MainDbtohdfs /dbtohdfs
```

## 输出:MySQL 表转移到 HDFS

```
hadoop dfs -ls /dbtohdfs/*
```

## 案例 2:从 MySQL 中的一个表转移到 MySQL 中的另一个表

在 MySQL 中创建输出表

创建表 employee1(name varchar(20)，id int，dept varchar(20))；

```
package com.inputFormat.copy;
import org.apache.hadoop.conf.Configuration;
import org.apache.hadoop.mapreduce.Job;
import org.apache.hadoop.mapreduce.lib.db.DBConfiguration;
import org.apache.hadoop.mapreduce.lib.db.DBInputFormat;
import org.apache.hadoop.mapreduce.lib.db.DBOutputFormat;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.NullWritable;
public class Mainonetable_to_other_table
{
 public static void main(String[] args) throws Exception
 {
 Configuration conf = new Configuration();
 DBConfiguration.configureDB(conf,
 "com.mysql.jdbc.Driver", // driver class
 "jdbc:mysql://localhost:3306/edureka", // db url
 "root", // user name
 "root"); //password
Job job = new Job(conf);
 job.setJarByClass(Mainonetable_to_other_table.class);
 job.setMapperClass(Map.class);
 job.setReducerClass(Reduce.class);
 job.setMapOutputKeyClass(Text.class);
 job.setMapOutputValueClass(IntWritable.class);
 job.setOutputKeyClass(DBOutputWritable.class);
 job.setOutputValueClass(NullWritable.class);
 job.setInputFormatClass(DBInputFormat.class);
 job.setOutputFormatClass(DBOutputFormat.class);

 DBInputFormat.setInput(
 job,
 DBInputWritable.class,
 "emp", //input table name
 null,
 null,
 new String[] { "empid", "name" ,"dept"} // table columns
 );
DBOutputFormat.setOutput(
 job,
 "employee1", // output table name
 new String[] { "name", "id","dept" } //table columns
 );
 System.exit(job.waitForCompletion(true) ? 0 : 1);
 }
}
```

这段代码让我们在 SQL DB 中配置输出表名。这些参数分别是作业实例、输出表名和输出列名。

```
DBOutputFormat.setOutput(
 job,
 "employee1", // output table name
 new String[] { "name", "id","dept" } //table columns
 );
```

## 映射器:与情况 1 相同

**减速器:**

```
package com.inputFormat.copy;
import java.io.IOException;
import org.apache.hadoop.mapreduce.Reducer;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.NullWritable;
public class Reduce extends Reducer<Text, IntWritable, DBOutputWritable, NullWritable>
{
 protected void reduce(Text key, Iterable<IntWritable> values, Context ctx)
 {
 int sum = 0;
String line[] = key.toString().split("	");
try
 {
 ctx.write(new DBOutputWritable(line[0].toString(),Integer.parseInt(line[1].toString()),line[2].toString()), NullWritable.get());
 } catch(IOException e)
 {
 e.printStackTrace();
 } catch(InterruptedException e)
 {
 e.printStackTrace();
 }
 }
}
```

## 运行命令:

```
hadoop jar dbhdfs.jar com.inputFormat.copy.Mainonetable_to_other_table
```

## 输出:将数据从 MySQL 中的 EMP 表传输到 MySQL 中的另一个 Employee1 表

## 案例 3:从 MySQL 中的表转移到 NoSQL (Hbase)表

**创建 Hbase 表以容纳 SQL 表的输出:**

```
create 'employee','official_info'
```

## 驱动程序类别:

```
package Dbtohbase;
import org.apache.hadoop.conf.Configuration;
import org.apache.hadoop.mapreduce.Job;
import org.apache.hadoop.mapreduce.lib.db.DBConfiguration;
import org.apache.hadoop.mapreduce.lib.db.DBInputFormat;
import org.apache.hadoop.hbase.mapreduce.TableOutputFormat;
import org.apache.hadoop.hbase.HBaseConfiguration;
import org.apache.hadoop.hbase.client.HTable;
import org.apache.hadoop.hbase.client.HTableInterface;
import org.apache.hadoop.hbase.io.ImmutableBytesWritable;
import org.apache.hadoop.hbase.mapreduce.TableMapReduceUtil;
import org.apache.hadoop.io.Text;

public class MainDbToHbase
{
 public static void main(String[] args) throws Exception
 {
 Configuration conf = HBaseConfiguration.create();
 HTableInterface mytable=new HTable(conf,"emp");
 DBConfiguration.configureDB(conf,
 "com.mysql.jdbc.Driver", // driver class
 "jdbc:mysql://localhost:3306/edureka", // db url
 "root", // user name
 "root"); //password

 Job job = new Job(conf,"dbtohbase");
 job.setJarByClass(MainDbToHbase.class);
 job.setMapperClass(Map.class);

 job.setMapOutputKeyClass(ImmutableBytesWritable.class);
 job.setMapOutputValueClass(Text.class);

 TableMapReduceUtil.initTableReducerJob("employee",Reduce.class, job);
job.setInputFormatClass(DBInputFormat.class);
 job.setOutputFormatClass(TableOutputFormat.class);

 DBInputFormat.setInput(
 job,
 DBInputWritable.class,
 "emp", //input table name
 null,
 null,
 new String[] { "empid", "name" ,"dept" } // table columns
 );
System.exit(job.waitForCompletion(true) ? 0 : 1);
 }
}
```

这段代码允许您配置输出键类，在 hbase 的情况下，它是 ImmutableBytesWritable

```
job.setMapOutputKeyClass(ImmutableBytesWritable.class);
 job.setMapOutputValueClass(Text.class);
```

这里我们传递 hbase 表名和 reducer 来作用于表。

```
 TableMapReduceUtil.initTableReducerJob("employee",Reduce.class, job);
```

## Mapper:

```
package Dbtohbase;
import java.io.IOException;

import org.apache.hadoop.mapreduce.Mapper;
import org.apache.hadoop.hbase.io.ImmutableBytesWritable;
import org.apache.hadoop.hbase.util.Bytes;
import org.apache.hadoop.io.LongWritable;
import org.apache.hadoop.io.Text;
import org.apache.hadoop.io.IntWritable;

public class Map extends Mapper<LongWritable, DBInputWritable, ImmutableBytesWritable, Text>
{
 private IntWritable one = new IntWritable(1);
protected void map(LongWritable id, DBInputWritable value, Context context)
 {
 try
 {
 String line = value.getName();
 String cd = value.getId()+"";
 String dept = value.getDept();
 context.write(new ImmutableBytesWritable(Bytes.toBytes(cd)),new Text(line+" "+dept));

 } catch(IOException e)
 {
 e.printStackTrace();
 } catch(InterruptedException e)
 {
 e.printStackTrace();
 }
 }
}
```

在这段代码中，我们从 DBinputwritable 类的 getters 中获取值，然后在 ImmutableBytesWritable 中传递它们，以便它们以 Hbase 理解的 bytewriatble 形式到达 reducer。

```
 String line = value.getName();
 String cd = value.getId()+"";
 String dept = value.getDept();
 context.write(new ImmutableBytesWritable(Bytes.toBytes(cd)),new Text(line+" "+dept));
```

## 减速器:

```
package Dbtohbase;
import java.io.IOException;
import org.apache.hadoop.hbase.client.Put;
import org.apache.hadoop.hbase.io.ImmutableBytesWritable;
import org.apache.hadoop.hbase.mapreduce.TableReducer;
import org.apache.hadoop.hbase.util.Bytes;
import org.apache.hadoop.io.Text;

public class Reduce extends TableReducer<
ImmutableBytesWritable, Text, ImmutableBytesWritable> {
public void reduce(ImmutableBytesWritable key, Iterable<Text> values, 
 Context context) throws IOException, InterruptedException {

 String[] cause=null;

 // Loop values
 for(Text val : values)
 {
 cause=val.toString().split(" ");

 }
 // Put to HBase
 Put put = new Put(key.get());
 put.add(Bytes.toBytes("official_info"), Bytes.toBytes("name"),Bytes.toBytes(cause[0]));
 put.add(Bytes.toBytes("official_info"), Bytes.toBytes("department"), Bytes.toBytes(cause[1]));
 context.write(key, put);
 }
 }
```

这段代码让我们决定存储来自 reducer 的值的确切行和列。这里，我们将每个 empid 存储在单独的行中，因为我们将 empid 作为唯一的行键。在每一行中，我们将雇员的官方信息分别存储在“姓名”和“部门”列下的“官方信息”列中。

```
 Put put = new Put(key.get());
 put.add(Bytes.toBytes("official_info"), Bytes.toBytes("name"),Bytes.toBytes(cause[0]));
 put.add(Bytes.toBytes("official_info"), Bytes.toBytes("department"), Bytes.toBytes(cause[1]));
 context.write(key, put);
```

## h base 中传输的数据:

扫描员工

正如我们所看到的，我们成功地完成了将业务数据从关系 SQL 数据库迁移到 NoSQL 数据库的任务。

在下一篇博客中，我们将学习如何为其他输入和输出格式编写和执行代码。

请继续发表您的评论、问题或任何反馈。我很想收到你的来信。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[在银行领域实施 Hadoop 和 R 解析技巧](https://www.edureka.co/blog/implementing-hadoop-and-r-analytic-skills-in-banking-domain/)

[对银行数据实施 K-means 聚类](https://www.edureka.co/blog/clustering-on-bank-data-using-r/)

[大数据和 Hadoop 入门](https://www.edureka.co/big-data-and-hadoop?%20to%20transfer%20data%20from%20SQL%20to%20NoSQL%20DB)