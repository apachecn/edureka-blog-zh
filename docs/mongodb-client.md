# 关于 MongoDB 客户端您需要知道的一切

> 原文：<https://www.edureka.co/blog/mongodb-client/>

如果您已经使用任何形式的关系数据库管理系统有一段时间了，那么您可能已经听说过 [MongoDB](https://www.edureka.co/blog/node-js-mongodb-tutorial/) 这个名字。mongoDb 于 2009 年首次推出，现在是业内最流行的关系数据库管理系统之一。尽管市场上出现了 MySql 等较老的关系数据库软件管理器，但其疯狂流行背后的主要原因是它带来的广泛的数量和巨大的多功能性。MongoDB 的使用消除了许多需求，其中之一是需要创建一个数据库，并在每次启动新项目时定义数据类型。MongoDB 客户端文章的议程:

*   【MongoDB 客户端的先决条件
*   [在 Maven 上创建项目](#Creating%20the%20project%20on%20Maven)
*   [添加您的第一个 JSON rest 服务](#Adding%20your%20very%20first%20JSON%20rest%20service)
*   [配置 MongoDB 数据库](#Configuring%20the%20mongoDb%20database)
*   [运行已配置的 MongoDB 数据库](#RunningtheconfiguredMongoDbdatabase)
*   [制作前端](#Making%20the%20front%20end)
*   [使用 BSON 编解码器简化 MongoDB 客户端](#Simplifying%20the%20mongoDb%20client%20using%20BSON%20codec)
*   [最终代码](#Final%20Code)

但是要实现 MongoDB 的最大功能，需要熟悉 MongoDB 客户端，在本文中，我们将讨论这一点。

## 【MongoDB 客户端的先决条件

为了全面理解本文，您需要首先满足以下先决条件。

您的系统中已经有一个 IDE。安装 Java 开发工具包或 1.8 及以上版本，并正确配置 JAVA_HOME。安装了 Docker 或 MongoDB。阿帕奇 Maven 版本 3.5.3 及以上。

我们在本指南中创建和使用的架构是最简单的架构之一。当执行时，用户可以轻松地在列表中添加数据和元素，之后它会自动在数据库中更新。

![MongoDB Client Logo](img/c4d085b1810d60b2ab1e49983c42751e.png)

除此之外，我们还确保数据和服务器之间的所有通信都在 JSON 中进行，并且所有数据都存储在 MongoDB 中。

**入门**

为了开始这个项目，遵循以下步骤。

#### **步骤#1:在 Maven 上创建项目**

第一步总是创建一个新项目，为了做到这一点，使用下面的代码。

```

mvn io.quarkus:quarkus-maven-plugin:0.22.0:create 
-DprojectGroupId=org.acme 
-DprojectArtifactId=using-mongodb-client 
-DclassName="org.acme.rest.json.FruitResource" 
-Dpath="/fruits" 
-Dextensions="resteasy-jsonb,mongodb-client"

```

运行上述命令时，IDE 会将 JSON-B、MongoDb 以及 RESTEasy/JAX-RS 客户端导入到您的系统中。

继续第二步。

#### **步骤#2:添加您的第一个 JSON rest 服务**

```

In order to do this, use the code below.

package org.acme.rest.json;

import java.util.Objects;

public class Fruit {

private String name;
private String description;

public Fruit() {
}

public Fruit(String name, String description) {
this.name = name;
this.description = description;
}

public String getName() {
return name;
}

public void setName(String name) {
this.name = name;
}

public String getDescription() {
return description;
}

public void setDescription(String description) {
this.description = description;
}

@Override
public boolean equals(Object obj) {
if (!(obj instanceof Fruit)) {
return false;
}

Fruit other = (Fruit) obj;

return Objects.equals(other.name, this.name);
}

@Override
public int hashCode() {
return Objects.hash(this.name);
}
}

```

在上面的例子中，我们首先创建了水果，稍后将在程序中使用。

接下来，我们需要创建 org . acme . rest . JSON . fruit service 文件，这将是我们的应用程序的用户层。为此，请使用下面的代码。

```

package org.acme.rest.json;

import com.mongodb.client.MongoClient;
import com.mongodb.client.MongoCollection;
import com.mongodb.client.MongoCursor;
import org.bson.Document;

import javax.enterprise.context.ApplicationScoped;
import javax.inject.Inject;
import java.util.ArrayList;
import java.util.List;

@ApplicationScoped
public class FruitService {

@Inject MongoClient mongoClient;

public List list(){
List list = new ArrayList<>();
MongoCursor cursor = getCollection().find().iterator();

try {
while (cursor.hasNext()) {
Document document = cursor.next();
Fruit fruit = new Fruit();
fruit.setName(document.getString("name"));
fruit.setDescription(document.getString("description"));
list.add(fruit);
}
} finally {
cursor.close();
}
return list;
}

public void add(Fruit fruit){
Document document = new Document()
.append("name", fruit.getName())
.append("description", fruit.getDescription());
getCollection().insertOne(document);
}

private MongoCollection getCollection(){
return mongoClient.getDatabase("fruit").getCollection("fruit");
}
}

Now we need to edit the org.acme.rest.json.FruitResource class to suit our needs. In order to do this, use the code below.

@Path("/fruits")
@Produces(MediaType.APPLICATION_JSON)
@Consumes(MediaType.APPLICATION_JSON)
public class FruitResource {

@Inject FruitService fruitService;

@GET
public List list() {
return fruitService.list();
}

@POST
public List add(Fruit fruit) {
fruitService.add(fruit);
return list();
}
}

```

继续第三步。

#### **步骤#3:配置 mongoDb 数据库**

下面给出了配置 mongoDb 数据库的语法和标准代码。

```

# configure the mongoDB client for a replica set of two nodes
quarkus.mongodb.connection-string = mongodb://mongo1:27017,mongo2:27017

```

在我们的例子中，我们将利用下面的代码来配置数据库。

```

# configure the mongoDB client for a replica set of two nodes
quarkus.mongodb.connection-string = mongodb://localhost:27017

```

继续第 4 步。

#### **步骤#4:运行配置好的 MongoDB 数据库**

下一步是运行我们刚刚创建的 MongoDB 数据库。为此，请使用下面的代码。

```

docker run -ti --rm -p 27017:27017 mongo:4.0

```

继续第 5 步。

#### **步骤#5:制作前端**

现在，应用程序后端的所有工作都已完成，让我们来看看用于编写应用程序前端的代码。

```

package org.acme.rest.json;

import io.quarkus.mongodb.ReactiveMongoClient;
import io.quarkus.mongodb.ReactiveMongoCollection;
import org.bson.Document;

import javax.enterprise.context.ApplicationScoped;
import javax.inject.Inject;
import java.util.List;
import java.util.concurrent.CompletionStage;

@ApplicationScoped
public class ReactiveFruitService {

@Inject
ReactiveMongoClient mongoClient;

public CompletionStage<List> list(){
return getCollection().find().map(doc -> {
Fruit fruit = new Fruit();
fruit.setName(doc.getString("name"));
fruit.setDescription(doc.getString("description"));
return fruit;
}).toList().run();
}

public CompletionStage add(Fruit fruit){
Document document = new Document()
.append("name", fruit.getName())
.append("description", fruit.getDescription());
return getCollection().insertOne(document);
}

private ReactiveMongoCollection getCollection(){
return mongoClient.getDatabase("fruit").getCollection("fruit");
}
}

package org.acme.rest.json;

import javax.inject.Inject;
import javax.ws.rs.*;
import javax.ws.rs.core.MediaType;
import java.util.List;
import java.util.concurrent.CompletionStage;

@Path("/reactive_fruits")
@Produces(MediaType.APPLICATION_JSON)
@Consumes(MediaType.APPLICATION_JSON)
public class ReactiveFruitResource {

@Inject ReactiveFruitService fruitService;

@GET
public CompletionStage<List> list() {
return fruitService.list();
}

@POST
public CompletionStage<List> add(Fruit fruit) {
fruitService.add(fruit);
return list();
}
}

```

在上面的例子中，我们利用一个反应式 mongoDb 客户端来促进前端的形成。

继续第 6 步。

#### **步骤 6:使用 BSON 编解码器简化 mongoDb 客户端**

为此，请使用下面的代码。

```

package org.acme.rest.json.codec;

import com.mongodb.MongoClient;
import org.acme.rest.json.Fruit;
import org.bson.*;
import org.bson.codecs.Codec;
import org.bson.codecs.CollectibleCodec;
import org.bson.codecs.DecoderContext;
import org.bson.codecs.EncoderContext;

import java.util.UUID;

public class FruitCodec implements CollectibleCodec {

private final Codec documentCodec;

public FruitCodec() {
this.documentCodec = MongoClient.getDefaultCodecRegistry().get(Document.class);
}

@Override
public void encode(BsonWriter writer, Fruit fruit, EncoderContext encoderContext) {
Document doc = new Document();
doc.put("name", fruit.getName());
doc.put("description", fruit.getDescription());
documentCodec.encode(writer, doc, encoderContext);
}

@Override
public Class getEncoderClass() {
return Fruit.class;
}

@Override
public Fruit generateIdIfAbsentFromDocument(Fruit document) {
if (!documentHasId(document)) {
document.setId(UUID.randomUUID().toString());
}
return document;
}

@Override
public boolean documentHasId(Fruit document) {
return document.getId() != null;
}

@Override
public BsonValue getDocumentId(Fruit document) {
return new BsonString(document.getId());
}

@Override
public Fruit decode(BsonReader reader, DecoderContext decoderContext) {
Document document = documentCodec.decode(reader, decoderContext);
Fruit fruit = new Fruit();
if (document.getString("id") != null) {
fruit.setId(document.getString("id"));
}
fruit.setName(document.getString("name"));
fruit.setDescription(document.getString("description"));
return fruit;
}
}

```

现在我们将利用 CodecProvider 将它链接到已经存在的 Fruit 类。

```

package org.acme.rest.json.codec;

import org.acme.rest.json.Fruit;
import org.bson.codecs.Codec;
import org.bson.codecs.configuration.CodecProvider;
import org.bson.codecs.configuration.CodecRegistry;

public class FruitCodecProvider implements CodecProvider {
@Override
public Codec get(Class clazz, CodecRegistry registry) {
if (clazz == Fruit.class) {
return (Codec) new FruitCodec();
}
return null;
}

}

```

继续第 7 步。

#### **步骤#7:最终代码**

这个应用程序的最终代码看起来会像这样。

```

package org.acme.rest.json;

import com.mongodb.client.MongoClient;
import com.mongodb.client.MongoCollection;
import com.mongodb.client.MongoCursor;

import javax.enterprise.context.ApplicationScoped;
import javax.inject.Inject;
import java.util.ArrayList;
import java.util.List;

@ApplicationScoped
public class CodecFruitService {

@Inject MongoClient mongoClient;

public List list(){
List list = new ArrayList<>();
MongoCursor cursor = getCollection().find().iterator();

try {
while (cursor.hasNext()) {
list.add(cursor.next());
}
} finally {
cursor.close();
}
return list;
}

public void add(Fruit fruit){
getCollection().insertOne(fruit);
}

private MongoCollection getCollection(){
return mongoClient.getDatabase("fruit").getCollection("fruit", Fruit.class);
}
}

```

**结论**

现在您知道了如何在您的系统中配置和使用 MongoDB 客户机。继续在您的系统中尝试这些代码，并让我们知道您的体验。

**文章摘要**

了解关于 MongoDB 客户机的所有内容，以及如何在您的系统中为各种用途配置相同的客户机。请继续阅读，了解更多信息。

到此，我们来结束 MongoDB 客户端的文章。