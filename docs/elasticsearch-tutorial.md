# 弹性搜索教程——增强你的搜索能力

> 原文：<https://www.edureka.co/blog/elasticsearch-tutorial/>

在我之前关于[什么是 Elasticsearch](https://www.edureka.co/blog/what-is-elasticsearch/) 的博客中，我已经介绍了 Elasticsearch，谈到了它的优势，并在 windows 上做了安装。我还讨论了 Elasticsearch 中的基本概念和不同的 API 约定。但是让我告诉你一些有趣的事情，无论我在之前的博客中讨论了什么，都只是冰山一角。在这篇 Elasticsearch 教程博客中，我将介绍所有使 Elasticsearch 在其竞争对手中最快和最受欢迎的特性。另外 ，我将通过这个 Elasticsearch 教程博客向你介绍 Elasticsearch 中的不同 API，以及你如何使用它们进行不同的搜索。

以下是我将在这篇 Elasticsearch 教程博客中讨论的主题:

*   [elastic search API](#1)
*   [查询 DSL](#2)
*   [映射](#3)
*   [分析](#4)
*   [模块](#5)

那么，让我们从这篇 Elasticsearch 教程博客的第一个话题开始吧。

## **elastic search API—****elastic search 教程**

Elasticsearch 教程博客的这一部分讨论了 Elasticsearch 支持的各种 API。下面我们来详细了解一下其中的每一个。

### **文档 API**

Elasticsearch 提供单文档 API 和多文档 API。

1.  **单文档 API**
    *   *指标 API*
    *   *获取 API*
    *   *更新 API*
    *   *删除 API*
2.  **多单据 API**
    *   *多获取 API*
    *   *批量 API*
    *   *通过查询 API 删除*
    *   *通过查询 API 更新*
    *   *重新索引 API*

现在你已经知道了不同类型的文档 API，让我们试着实现它们的 CRUD 操作。

#### **指数 API**

index API 负责在特定索引中添加和更新类型化的 JSON 文档，然后使其可搜索。下面的示例将 JSON 文档插入到“playlist”索引中，其类型为“kpop”，id 为 1:

```
PUT /playlist/kpop/1
{
 "title" : "Beautiful Life",
 "artist" : "Crush",
 "album" : "Goblin",
 "year" : 2017
}
```

#### **获取 API**

get API 负责根据惟一的 id 从索引中获取一个 类型的 JSON 文档。下面的示例从“playlist”索引中获取一个 JSON 文档，该文档的类型为“kpop”，id 值为 2:

```
GET /playlist/kpop/2
```

#### **更新 API**

更新的 API 负责根据提供的脚本更新文档。该操作从索引中获取文档，运行脚本，然后索引回结果。为了确保在“获取”和“重新索引”期间不会发生更新，它使用了版本控制。下面的示例通过添加一个名为“time”的新字段，从“playlist”索引中更新一个名为“kpop”的 JSON 文档:

```
PUT /playlist/kpop/1
{
 "title" : "Beautiful Life",
 "artist" : "Crush",
 "album" : "Goblin",
 "year" : 2017,
 "time" : 5
}
```

#### **删除 API**

delete API 负责根据特定索引的惟一 id 删除一个类型化的 JSON 文档。下面的示例从“playlist”索引中获取一个 JSON 文档，该文档的类型为“kpop”，id 值为 3:

```
DELETE /playlist/kpop/3
```

### **搜索 API**

搜索 API 负责搜索 Elasticsearch 中的内容。您可以通过发送带有字符串参数的查询的 get 请求进行搜索，也可以在 post 请求的消息正文中发送查询。通常，搜索 API 是多索引或多类型的。

在具有统一资源标识符(URI)的搜索操作中可以传递各种参数:

| **参数** | **描述** |
| **q** | 该参数指定查询字符串 |
| **网开一面** | 通过将该参数的值设置为真，基于格式的错误可被忽略 |
| **字段** | 该参数从选择字段获取响应 |
| **排序** | 该参数对结果进行排序 |
| **超时** | 该参数有助于限制搜索时间 |
| 后终止 _  | 该参数将响应限制在每个分片中特定数量的文档 |
| **出自** | 该参数指定开始索引 |
| **大小** | 该参数指定返回的命中次数 |

现在您已经熟悉了搜索参数，让我们看看如何通过多个索引和类型执行搜索。

1.  #### **多指标**

    在 Elasticsearch 中，您可以搜索所有索引或某些特定索引中的文档。以下示例从所有索引中搜索 JSON 文档，其中年份为 2014:

    ```
    GET playlist,my_playlist/_search?q=2014
    {
     "title" : "MAMACITA",
     "artist" : "SuJu",
     "album" : "MAMACITA",
     "year" : 2014,
     "time" : 4
    }
    ```

2.  #### **多型**

    您还可以搜索所有类型或某个指定类型的特定索引中的所有文档。以下示例在所有类型下从“playlist”索引中搜索 JSON 文档，其中年份是 2017:

    ```
    GET playlist/_search?q=2017
    ```

Elasticsearch 教程的下一节将讨论 elastic search 支持的聚合及其类型。

### **聚合**

在 Elasticsearch 中，聚合框架负责提供基于搜索查询的聚合数据。可以将聚合组合在一起，以构建复杂的数据汇总。为了更好的理解，把它看作一个 *工作单元。*它通过 Elasticsearch 中的一组文档开发分析信息。有各种类型的聚合可用，每种都有自己的目的和输出。为了简化，它们被归纳为 4 个主要家族:

1.  这里每个桶都关联着一个 *键* 和一个文档。每当执行聚合时，都会对每个文档评估所有存储桶标准。每当一个标准匹配时，该文档被认为“落入”相关的桶中。

2.  #### **公制**

    度量是负责跟踪和计算一组文档的度量的集合。

3.  #### **矩阵**

    矩阵是负责对多个字段进行操作的集合。它们根据从请求的文档字段中提取的值生成一个矩阵结果。Matrix 不支持脚本。

4.  #### **管道**

    管道是负责将其他聚合的输出及其相关度量聚合在一起的聚合。

以下示例显示了基本聚合的结构:

```
"aggregations" : {
 "<aggregation_name>" : {
 "<aggregation_type>" : {
 <aggregation_body>
 }
 [,"meta" : { [<meta_data_body>] } ]?
 [,"aggregations" : { [<sub_aggregation>]+ } ]?
 }
 [,"<aggregation_name_2>" : { ... } ]*
}
```

### **指标 API**

在 Elasticsearch 中，索引 API 或索引 API 负责管理单个索引、索引设置、别名、映射和索引模板。下面是我们可以在索引 API 上执行的一些操作:

*   #### **创建指标**

    创建索引 API 负责实例化一个索引。每当用户传递一个 JSON 对象时，就会自动创建一个索引。以下示例创建了一个名为“courses”的索引，其中包含一些设置:

    ```
    PUT courses
    {
     "settings" : {
     "index" : {
     "number_of_shards" : 3, 
     "number_of_replicas" : 2 
     }
     }
    }
    ```

*   #### **获取指标**

    get API 负责获取关于索引的信息。通过向一个或多个索引发送 get 请求，可以调用它。以下示例检索名为“courses”的索引:

    ```
    GET /courses
    ```

*   #### **删除指标**

    删除索引 API 负责删除现有的索引。以下示例删除名为“courses”的索引:

    ```
    DELETE /courses
    ```

*   #### **开/闭指数 API**

    打开和关闭索引 API 负责关闭一个索引，然后打开它。对于任何读/写操作，关闭的索引都被阻止。但是您仍然可以打开它，这将通过正常的恢复过程。以下示例关闭并打开名为“courses”的索引:

    ```
    POST /courses/_close

    POST /courses/_open

    ```

*   #### **指标别名**

    在需要时，Elasticsearch 中的 API 可以在处理特定索引时接受索引名。index aliases API 允许用一个名称作为索引的别名，所有 API 都会自动将别名转换为实际的索引名称。以下示例添加和删除一个索引别名:

    ```
    POST /_aliases
    {
     "actions" : [
     { "add" : { "index" : "courses", "alias" : "subjects" } }
     ]
    }

    POST /_aliases
    {
     "actions" : [
     { "remove" : { "index" : "courses", "alias" : "subjects" } }
     ]
    }
    ```

*   #### **析**

    在 Elasticsearch 中，它对文本执行分析过程，并返回文本的记号分解。您可以在不指定任何索引的情况下执行分析。下面的例子执行一个简单的分析:

    ```
    GET _analyze
    {
     "analyzer" : "standard",
     "text" : "this is a demo"
    }
    ```

*   #### **指标模板**

    索引模板负责定义创建新索引时自动应用的模板。下面的例子显示了一个模板格式:

    ```
    PUT _template/template_1
    {
     "template": "te*",
     "settings": {
     "number_of_shards": 1
     },
     "mappings": {
     "type1": {
     "_source": {
     "enabled": false
     },
     "properties": {
     "host_name": {
     "type": "keyword"
     },
     "created_at": {
     "type": "date",
     "format": "EEE MMM dd HH:mm:ss Z YYYY"
     }
     }
     }
     }
    }
    ```

*   #### **指数统计**

    在 Elasticsearch 中，indices level stats 负责提供发生在索引上的不同操作的统计数据。API 通常提供索引级别的统计信息。以下示例显示了所有索引的索引级别统计信息以及特定的索引统计信息:

    ```
    GET /_stats

    GET /playlist/_stats

    ```

*   #### **同花顺**

    刷新 API 负责通过 API 刷新一个或多个索引。基本上，这是一个通过将数据推送到索引存储并清除内部事务日志来从索引中释放内存的过程。以下示例显示了一个正在刷新的索引:

    ```
    POST playlist/_flush
    ```

*   #### **刷新**

    刷新 API 负责显式刷新一个或多个索引。这使得自上次刷新以来执行的所有操作都可用于搜索。以下示例显示了一个正在刷新的索引:

    ```
    POST /courses/_refresh

    POST /playlist,courses/_refresh

    ```

### **集群 API**

Elasticsearch 中的集群 API 负责获取关于集群及其节点的信息，并在其中进行进一步的更改。

*   #### **集群健康**

    这个 API 负责通过附加 health 关键字来检索集群的健康状态。 以下示例显示了集群的运行状况:

    ```
    GET _cluster/health
    ```

*   #### **集群状态**

    这个集群状态 API 负责通过附加“State”关键字 URL 来检索关于集群的状态信息。状态包含各种信息，如版本、主节点、其他节点、路由表、元数据和块。以下示例显示了集群状态:

    ```
    GET /_cluster/state
    ```

*   #### **集群统计**

    集群统计 API 负责从集群范围的角度检索统计数据。它返回一个基本的索引指标和关于构成集群的当前节点的信息。以下示例显示了集群统计信息:

    ```
    GET /_cluster/stats
    ```

*   #### **待定集群任务**

    这个 API 负责监控任何集群中的未决任务。任务可能包括创建索引、更新、映射、分配碎片、失败碎片等。 下面的例子显示了集群的统计数据:

    ```
    GET /_cluster/pending_tasks
    ```

*   #### **节点统计**

    这个集群节点统计 API 负责检索一个或多个集群节点统计信息。以下示例显示了集群节点统计信息:

    ```
    GET /_nodes/stats
    ```

*   #### **节点热点 _ 线程**

    这个 API 负责检索集群中每个节点上的当前热线程。以下示例显示了集群的热线程:

    ```
    GET /_nodes/hot_threads
    ```

本 Elasticsearch 教程博客的下一节将讨论 Elasticsearch 提供的查询 DSL。

## **查询 DSL—****弹性搜索教程**

Elasticsearch 提供了基于 JSON 的全查询 DSL，负责定义查询。查询 DSL 由两类子句组成:

1.  ### **叶查询子句**

    在 Elasticsearch 中，叶查询子句搜索特定字段中的特定值，如匹配、术语或范围查询。这些查询也可以单独使用。

2.  ### **复合查询子句**

    在 Elasticsearch 中，复合查询子句包装其他叶 **或** 复合查询。这些查询用于以逻辑方式组合多个查询或改变它们的行为。

*   ### **匹配所有查询**

    这是最简单的查询，它匹配所有文档，并为每个对象返回 1.0 分。以下示例显示了匹配查询:

    ```
    GET /_search
    {
     "query": {
     "match_all": {}
     }
    }
    ```

*   ### **全文查询**

    这些查询用于在全文字段上运行全文查询。这些基本上是高级查询，它们理解如何分析被查询的字段。然后，在执行之前，它将每个字段的分析器应用于查询字符串。以下示例显示了一个简单的全文查询:

    ```
    POST /playlist*/_search
    {
    "query":{
    "match" : {
    "title":"Beautiful Life"
    }
    }
    }
    ```

    一些全文查询是:

    | **查询** | **描述** |
    | **匹配** | 该查询用于执行全文查询。 |
    | **匹配 _ 短语** | 此查询用于匹配精确的短语或单词近似匹配。 |
    | **匹配 _ 短语 _ 前缀** | 这个查询用于对最后一个单词进行通配符搜索。 |
    | **多 _ 赛** | 该查询用于匹配多字段版本。 |
    | **常用术语** | 此查询用于提供对不常用单词的更多偏好。 |
    | **查询 _ 字符串** | 该查询用于在单个查询字符串中指定 AND&#124;OR&#124;NOT 条件和多字段搜索。 |
    | **简单 _ 查询 _ 字符串** | 这个查询是 **query_string 的健壮版本。** |

*   ### **任期级别查询**

    这些类型的查询用于结构化数据，如数字、日期和枚举，而不是全文字段。您还可以使用它们创建低级查询。以下示例显示术语级别查询:

    ```
    POST /playlist/_search
    {
     "query":{
     "term":{"title":"Silence"}
     }
    }
    ```

    一些全文查询是:

    | **查询** | **描述** |
    | **任期** | 该查询用于查找包含指定精确术语的文档。 |
    | **条款** | 此查询用于查找包含任何指定精确术语的文档。 |
    | **范围** | 该查询用于查找指定范围必须包含在指定字段中的文档。 |
    | **退出** | 该查询用于查找指定字段包含任何非空值的文档。 |
    | **前缀** | 该查询用于查找包含以指定前缀开头的术语的文档。 |
    | **通配符** | 该查询用于查找包含与指定模式匹配的术语的文档。 |
    | **正则表达式** | 该查询用于查找包含与正则表达式匹配的术语的文档。 |
    | **模糊** | 该查询用于查找包含与指定术语模糊相似的术语的文档。 |
    | **式** | 该查询用于查找指定类型的文档。 |
    | **ids** | 该查询用于查找具有指定类型和 id 的文档。 |

*   ### **复合查询**

    Elasticsearch 中的复合查询负责将其他复合查询或叶查询打包在一起。这样做是为了组合他们的结果和分数，改变他们的行为，或者从查询切换到过滤上下文。下面的例子展示了一个简单的全文查询:

    ```
    POST /playlist/_search
    {
     "query": {
     "match": {
     "title": "Lucifer"
     }
     }
    }
    ```

    一些全文查询有:

    | **查询** | **描述** |
    | **常数 _ 分数** | 该查询用于包装另一个查询，并在过滤器上下文中执行。 |
    | **布尔** | 默认情况下，此查询用于组合多个叶查询子句或复合查询子句。 |
    | **dis _ max** | 该查询接受多个查询，然后返回匹配任何查询子句的文档。 |
    | **函数 _ 分数** | 该查询用于通过函数修改主查询返回的分数，以考虑流行度、新近度、距离或脚本实现的自定义算法等因素。 |
    | **助推** | 该查询用于返回匹配肯定查询的文档，但是降低匹配否定查询的文档的分数。 |
    | **指数** | 该查询用于对指定的索引执行一个查询，对其他索引执行另一个查询。 |

*   ### **加盟查询**

    在像 Elasticsearch 这样的分布式系统中，执行完全 SQL 风格的连接是非常昂贵的。因此，Elasticsearch 提供了两种旨在水平扩展的连接形式。

    1.  #### **嵌套查询**

        该查询用于包含 **嵌套** 类型字段的单据。使用此查询，您可以将每个对象作为独立的文档进行查询。

    2.  #### **已 _ 子** & **已 _ 父** 查询

        该查询用于检索单个索引中两个文档类型之间的父子关系。has_child 查询返回匹配的父文档，而 has_parent 查询返回匹配的子文档。

下面的例子显示了一个简单的连接查询:

```
POST /my_playlist/_search
{
 "query":
 {
 "has_child" : {
 "type" : "kpop", "query" : {
 "match" : {
 "artist" : "EXO"
 }
 }
 }
 }
}
```

*   ### **地理查询**

    在 Elasticsearch 中，支持两种类型的地理数据:

1.  **地理点:**这些是支持纬度/经度对的字段
2.  **geo_shape:** 这些是支持点、线、圆、多边形、多重多边形等的字段。

```
{
 "query":{
 "filtered":{
 "filter":{
 "geo_distance":{
 "distance":"150km",
 "location":[42.056098, 86.674299]
 }
 }
 }
 }
}
```

这篇 Elasticsearch 教程博客的下一部分将讨论 Elasticsearch 中可用的不同映射。

## **贴图-弹性搜索教程**

在 Elasticsearch 中，映射负责定义文档及其字段的存储和索引方式。下面的例子展示了一个简单的映射查询:

```
POST /playlist
POST /playlist
{
 "mappings": {
 "report": {
 "_all": {
 "enabled": true
 },
 "properties":{
 "title":{ "type":"string"}, "artist":{ "type":"string"},
 "album":{ "type":"string"}, "year":{ "type":"integer"}
 }
 }
}
```

*   ### **字段类型**

    Elasticsearch 支持文档中字段的各种数据类型，如:

    |  | **描述** |
    | **核心** | 这些是几乎所有系统都支持的基本数据类型。基本数据类型有整型、长整型、双精度型、短整型、字节型、双精度型、浮点型、字符串型、日期型、布尔型和二进制型。 |
    | **复杂** | 这些数据类型是核心数据类型的组合。例如数组、JSON 对象和嵌套数据类型。 |
    | **地理** | 这些是用于定义地理属性的数据类型。 |
    | **专门** | 这些是用于特殊目的的数据类型。 |

*   ### **映射类型**

    在 Elasticsearch 中，每个索引都有一个或多个映射类型。这些映射类型用于将索引的文档分成逻辑组/单元。映射可以基于以下参数进行区分:

    1.  **元字段:**m元字段负责定制如何处理文档的关联元数据。Elasticsearch 中的元字段包括文档的**_ index****、_type、_id** 和 **_source** 字段。
    2.  **字段或属性:** 在 Elasticsearch 中，e ach 映射类型有一个字段或属性的列表这些字段或属性只是特定的 it。在索引中，名称相同但映射类型不同的字段应该具有相同的映射。
    3.  **动态映射:** Elasticsearch 允许自动创建的映射称为动态映射。使用动态映射，用户可以将数据发送到任何未定义的映射。

本 Elasticsearch 教程博客的下一节将向您介绍 Elasticsearch 的分析过程。

## **分析——弹性搜索教程**

在 Elasticsearch 中，解析是将文本转换成令牌或项的过程。这些标记然后被添加到倒排索引中用于搜索。该分析过程由分析仪执行。分析仪有两种类型:

1.  内置分析仪
2.  **自定义** 分析仪定义的每项指标。

因此，如果没有定义分析器，那么默认情况下内置分析器将执行分析。以下示例显示了一个简单的分析查询:

```
PUT cities
{
 "mappings": {
 "metropolitan": {
 "properties": {
 "title": {
 "type": "text",
 "analyzer": "standard"
 }
 }
 }
 }
}
```

*   ### **分析仪**

    在 Elasticsearch 中，一个标记器和可选的标记过滤器组成了一个分析器。在分析模块内部，这些分析仪以逻辑名称注册。使用名称，可以在映射定义或一些 API 中引用分析器。以下是一些默认的分析器

    | **分析器** | **描述** |
    | ***标准***T7 | 使用该分析器，您可以设置停用词和最大令牌长度。 |
    | ***简单*** | 小写的记号赋予器组成了这个分析器。 |
    | ***空白*** | 空白标记器组成了这个分析器。 |
    | ***停止*** | 使用该分析器，可以配置停用词和停用词 _ 路径。 |
    | ***关键词*** | 使用这个分析器，整个流可以被标记为单个标记。 |
    | ***图案*** | 使用这个分析器，你可以配置像小写、模式、标志、停用词等正则表达式。 |
    | ***语言*** | 使用此分析仪，您可以分析不同的语言，如印地语、阿拉伯语、荷兰语等。 |
    |  | 该分析器利用标准记号赋予器，具有标准过滤器、小写过滤器、停止过滤器和雪球过滤器。 |
    | ***自定义*** | 使用这个分析器，可以创建一个定制的分析器和一个带有可选令牌过滤器和字符过滤器的令牌化器。 |

*   在 Elasticsearch 中，标记器负责从文本中生成标记。使用空格或其他标点符号，文本可以被分解成记号。Elasticsearch 提供了一个内置标记化器的列表，这些标记化器在定制分析器中使用。以下是在 Elasticsearch 中使用的一些标记符:

    | 记号标记 | **描述** |
    | ***标准*** | 在基于语法的标记器上开发，也可以配置 max_token_length。 |
    | ***边缘 NGram*** | 可以为这个记号赋予器设置不同的配置，如 min_gram、max_gram、token_chars。 |
    | ***关键词*** | 这个记号赋予器负责生成整个输入作为输出，并设置 buffer_size。 |
    | ***字母*** | 这个分词器负责捕获整个单词，除非遇到非字母。 |
    | ***小写*** | 这个记号赋予器的工作原理类似于字母记号赋予器。一旦标记被创建，它就把它们变成小写。 |
    |  | 您可以设置最小语法、最大语法和令牌字符等。，对于这个记号赋予器。 |
    | ***空白*** | 在空格的基础上，这个标记器对文本进行划分。 |
    | ***图案*** | 这个记号赋予器使用正则表达式作为记号分隔符。 |
    | ***UAX 邮箱网址*** | 这类似于标准的令牌化器，但是将电子邮件和 URL 作为一个令牌。 |
    | ***路径层次*** | 这个记号赋予器负责生成输入目录路径中所有可能的路径。 |
    |  | 这个记号赋予器使用基于语法的记号来实现它的功能。 |
    | ***泰国*** | 这用于使用内置泰语分割算法进行处理的泰语。 |

*   ### **令牌过滤器**

    在 Elasticsearch 中，标记化器将输入发送到标记过滤器。这些令牌过滤器可以进一步修改、删除或添加文本到输入中。

*   ### **字符过滤器**

    在分词器之前，文本由字符过滤器处理。字符过滤器搜索特殊字符或 HTML 标签或指定的模式。之后它或者删除它们或者将它们改变成适当的单词。

这篇 Elasticsearch 教程博客的下一部分讲述了 Elasticsearch 提供的不同模块。

## **模块****——弹性搜索教程**

Elasticsearch 由不同的模块组成，这些模块负责其功能的各个方面。这些模块中的每一个都可以有以下任何一种设置:

1.  ***静态***–这些设置必须在节点级别完成，并且必须在每个相关节点上设置。
2.  ***动态***–这些设置可以在实时集群上动态更新。

| **模块** | **描述** |
| ***集群级路由和分片分配*** | 负责控制碎片分配到节点的位置、时间和方式的设置。 |
|  | 负责发现一个集群并维护其中所有节点的状态。 |
| ***网关*** | 负责在重启期间维护整个集群的集群状态和分片数据。 |
| ***HTTP*** | 负责管理 HTTP 客户端和 Elasticsearch APIs 之间的通信。 |
| ***指数*** | 负责维护为每个指标全局设置的设置。 |
|  | 负责控制默认网络设置。 |
| ***节点客户端*** | 负责启动集群中的一个节点。 |
|  | 负责安全使用内联和存储脚本的默认脚本语言。 |
|  | 负责以定制方式增强基本的 elasticsearch 功能。 |
|  | 允许用户使用脚本来评估自定义表达式。 |
| 快照/恢复 | 负责将单个索引或整个集群的快照创建到远程存储库中。 |
| ***线程池*** | 负责保持几个线程池，以便改进如何在一个节点内管理线程内存消耗。 |
| ***运输*** | 负责配置传输网络层。 |
| ***部落节点*** | 负责加入一个或多个集群，并充当它们之间的联合客户端。 |
| ***跨簇搜索*** | 负责跨多个集群执行搜索请求，而不加入它们，并作为跨它们的联合客户端。 |

elastic search 教程的博客到此结束。我希望通过这篇关于 Elasticsearch 教程的博客，我能够清楚地解释不同的 Elasticsearch APIs 以及如何使用它们。

[https://www.youtube.com/embed/1EnvkPf7t6Y?rel=0&showinfo=0](https://www.youtube.com/embed/1EnvkPf7t6Y?rel=0&showinfo=0)

## **弹性搜索教程|弹性搜索入门**

*如果你想接受 Elasticsearch 的培训，并希望轻松搜索和分析大型数据集，那么就去看看 Edureka 的 [**ELK Stack Training**](https://www.edureka.co/elk-stack-training-sp) ，这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

*有问题吗？请在评论区提到它，我们会给你回复。*