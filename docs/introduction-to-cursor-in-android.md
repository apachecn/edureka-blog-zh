# Android 中的光标介绍

> 原文：<https://www.edureka.co/blog/introduction-to-cursor-in-android/>

[//www.youtube.com/embed/vMw8Clvx4Uo](//www.youtube.com/embed/vMw8Clvx4Uo)

游标的基本用途是指向查询获取的结果中的一行。我们加载光标对象指向的行。通过使用光标，我们可以节省大量的内存和内存。

![Android logo-Edureka](img/0683366de853b8f305eeffbd5f1c4498.png)光标在下面的代码中定义:

```
Public Cursor getString(String[] columnNames}{
```

```
Cursor cursor = database.query(table_name, columnName, null, null,
```

```
Null,null,null);
```

```
Return cursor;
```

```
}
```

```
}
```

在这里，我们只传递表名、列名，然后我们接收光标。

为了得到列和行，我们使用语句:

```
Int col = cursor.getColumnCount();
```

```
Int row =  cursor.getCount();
```

```
In order to get the column names, we use:
```

```
String[] columnNames = cursor.getColumnNames();
```

然后我们通过语句显示结果:

```
Result += “No of Columns: “+col + “
”;
```

```
Result += “No of Rows: “+row + “
”;
```

```
Result += “Name of Columns” “+”
”;
```

SQLite 数据库中的任何查询都返回一个游标对象，游标指向一行。让我们以下面的代码为例:

```
Cursor cursor = database.query(*TABLE_NAME*, columnNames, null, null, null, null, null);
```

```
Return cursor;
```

```
}
```

```
}
```

当我们定义光标时，它将指向第一行。使用光标，我们定义一个代码为的‘for row’

```
for( cursor.moveTofirst(); !cursor.isAfterLast(); cursor</pre>
<pre style="text-align: justify;">moveToNext()) {</pre>
<pre style="text-align: justify;">Result += cursor.getString(0) + “		”</pre>
<pre style="text-align: justify;">+ cursor.getString(1) + “		”</pre>
<pre style="text-align: justify;">+ cursor.getString(2) + “
”;</pre>
<pre style="text-align: justify;">}

```

当我们调用“Movetonext”方法时，它会一直转到下一行。如果方法是“afterlast ”,它将变为 NULL。

为了检查数据库，我们转到文件浏览选项卡并单击数据文件夹。文件夹“com . edu reka . sqlitexample”将包含 db 文件。然后，我们使用 SQLite 管理器，通过加载存储在桌面上的 db 文件来连接数据库。这将依次显示数据库表。它将包含行 ID、名称和编号等元素。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

**[Android 架构入门](https://www.edureka.co/blog/beginners-guide-android-architecture/)**

**[安卓开发历程](https://www.edureka.co/android-development-certification-course)**