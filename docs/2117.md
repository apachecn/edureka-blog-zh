# 什么是基本的 MongoDB 命令，如何使用它们？

> 原文：<https://www.edureka.co/blog/mongodb-commands/>

MongoDB 现在很流行。从小规模的创业公司开始，一直到大组织，每个人都开始使用它，因此这个平台值得探索。如果你是第一次接触 [MongoDB](https://www.edureka.co/blog/sql-vs-nosql-db/#What%20is%20MongoDB?) 的世界，并且还在掌握使用它的窍门，那么这篇文章就是为你准备的。 在本文中，我们将分享您可以在这个平台上使用的最流行的 MongoDB 命令，让您的生活更加轻松，编码过程更加高效。

*   [什么是 MongoDB？](#whatismongodb)
*   [MongoDB 的基本命令](#basiccommands)
*   [显示命令](#showcommands)
*   [积垢操作](#crud)

在我们分享 MongoDB 最流行的命令之前，这里先做一个平台的小介绍。

## **什么是 MongoDB？**

MongoDB 是一个开源的[关系数据库管理系统](https://www.edureka.co/blog/what-is-dbms#typesofdbms)，于 2009 年首次推出。它与 [MySQL](https://www.edureka.co/blog/what-is-mysql/) 共享许多功能，并带来了新的增强和额外的功能，这有助于它的广泛流行。

使用 MongoDb 作为主要资源的一些公司包括 HootSuite、Sony 和 Zendesk 等。

## **MongoDB 的基本命令**

1.  **Mongo** :这是 MongoDB 中最常用的命令之一。使用时，您要求平台在默认端口 27017 上连接到本地主机。

2.  **Mongo<host>/<database>**:当你希望平台连接到一个特定的数据库时，使用这个命令。这个命令的一个例子是，mongo 10.121.65.58/mydb。

3.  **Mongo–host<主机名或 ip 地址>–port<port no>**:如果你想使用指定的端口连接到远程主机，那么你需要使用这个命令。这个命令的一个例子是，mongo–host 10 . 121 . 65 . 23–port 23020。

4.  **使用<数据库名称>** :如果在任何时间点，需要在现有数据库之间切换，使用该命令。例如，使用 mydb。

5.  **Db** :如果需要查看当前正在使用的数据库，使用该命令。

6.  **Help** :和其他平台类似，MongoDB 也有一个内置的帮助窗口，为了使用它，运行这个命令。示例，帮助

7.  **load(<filename>)**:如果您需要在任意时间点执行或运行 [JavaScript 文件](https://www.edureka.co/blog/javascript-tutorial/)，使用该命令。例如，load (myscript.js)。

8.  **db.help()** :如果你需要使用 db 方法的帮助，那么你可以使用这个命令。例如，db.help()。

9.  **db.mycol.help()** :如果你需要帮助使用一个集合，那么你使用这个命令。例如，db.mycol.help()。

## **显示命令**

现在您已经知道了可以在 MongoDB 中使用的基本命令，下面是一些最流行的 show 命令。

1.  **显示收藏库**:如果需要查看当前数据库中的所有收藏库，则使用该命令。示例:显示收藏。

2.  **显示数据库**:在编程过程中，如果需要查看当前正在使用的数据库，则使用该命令。示例:显示数据库。

3.  **显示角色**:在每个数据库中，都有不同的角色。为了查看所有这些角色，请使用以下命令。示例:显示角色。

4.  j **显示用户** :在任何时间点，任何数据库上都可以有多个用户。为了查看所有这些用户，请使用以下命令。例如:显示用户。

## **积垢操作**

MongoDB 中的 CRUD 是业界公认的创建、读取、更新和删除的缩写。如您所知，在 MongoDB 平台中可以同时执行读和写操作，为了实现这一点，可以使用以下命令。

1.  **db . collection . insert many([<document 1>，< document2 >，… ])** :如果需要在一个已经存在的集合中插入多个文档，那么就使用这个命令。例如，db . books . insert many([{ " ISBN ":9780198321668，"书名":"罗密欧与朱丽叶"，"作者":"威廉·莎士比亚"，"类别:":"悲剧"，"年份":2008}，{"isbn": 9781505297409，"书名":"金银岛"，"作者:" "罗伯特·路易斯·史蒂文森"，"类别:":"小说"，"年份":2014})))。

2.  **db . collection . insert(<document>)**:如果你需要将一个单独的新文档插入到一个已经存在的集合中，那么就使用这个命令。例如，db . books . insert({ " ISBN ":9780060859749，"书名":"爱丽丝之后:一部小说"，"作者":"格莱葛利·马奎尔"，"类别:" "小说"，"年份":2016})。

3.  **db . collection . find(<query>)**:如果需要使用字段值条件在集合中查找特定的文档，则使用该命令。比如 db.books.find({"title ":"金银岛" })。

4.  **db.collection.find()** :如果需要查找一个已经存在的集合中的所有文档，那么就使用这个命令。例如 db.books.find()。

5.  **db . collection . findone(<query>，< projection > )** :如果你需要找到第一个与你给定的查询相匹配的文档，那么就使用这个命令。例如:db.books.findOne({}，{_id:false})。

6.  **db . collection . find(<query>，< projection > )** :如果需要查找某个集合中某个文档的某些特定字段，那么可以使用这个命令。例如:db.books.find({"title ":"金银岛" }，{title:true，category:true，_id:false})。

7.  **db . collection . update(<query>，< update > )** :如果需要删除某个已有文档中的某个，那么通过匹配查询就可以使用这个命令。例如:db.books.update({title:“金银岛”}，{$unset : {category:""}})。

8.  **db . collection . update(<query>，< update > )** :如果你需要更新一个文档中某些特定的字段来匹配给定的查询，那么就使用这个命令。例如:db.books.update({title:“金银岛”}，{$set : {category:“冒险小说”})。

9.  **db . collection . remove(<query>，{justOne:true})** :如果在某种情况下，你需要删除一个符合你的查询的单个文档，那么使用这个命令。例如:db.books.remove({title:“金银岛”}，{justOne:true})。

10.  **db . collection . update(<query>，< update >，{multi:true} )** :如果你需要删除所有符合你的查询的文档的某些字段，那么使用这个命令。例如:db . books . update({ category:" Fiction " }，{$unset : {category:""}}，{multi:true})。

11.  **db . collection . remove({ })**:如果你需要删除一个集合中的所有文档，不管它们是否匹配你的查询，那么使用这个命令。例如:db.books.remove({})。

12.  **db . collection . remove(<查询> )** :如果需要删除所有符合某个查询的文档，那么就使用这个命令。例如:db . books . remove({ " category ":" Fiction " })。

**结论**

与其他关系数据库管理系统类似，MongoDB 也包含许多在日常使用中很方便的命令。根据您的使用情况，使用上面共享的任何或所有命令。

有问题要问我们吗？在评论区提到他们，我们会回复你或者在线参加 [Mongodb 认证](https://www.edureka.co/mongodb-certification-training)课程。