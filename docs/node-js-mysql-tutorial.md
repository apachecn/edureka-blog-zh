# Node.js MySQL 教程:关于 CRUD 应用程序您需要知道的一切

> 原文：<https://www.edureka.co/blog/node-js-mysql-tutorial/>

MySQL 是开发者最喜欢的数据库之一，因为它是开源的，而且高效。这就是为什么像 [Java](https://www.edureka.co/blog/what-is-java/) 、 [Python](https://www.edureka.co/blog/python-tutorial/) 、 [Node.js](https://www.edureka.co/blog/nodejs-tutorial/) 等大多数著名编程语言都提供驱动程序来访问 MySQL 并执行事务。在这篇 Node.js MySQL 教程中，我将演示如何通过几个简单易行的步骤建立与 MySQL 的连接，并执行各种 CRUD 操作。

下面是 Node.js MySQL 教程将要讨论的主题的详细列表:

*   [为什么要用 MySQL 搭配 Node.js？](#nodemysql)
*   [MySQL 安装](#mysqlinstallation)
*   [使用 Node.js 和 MySQL 创建 CRUD 应用](#demo)

让我从解决最基本的问题开始这个 Node.js MySQL 教程，即我们为什么使用 MySQL。

## **为什么要用 MySQL 搭配 Node.js？**

简单来说， [MySQL](https://www.edureka.co/blog/what-is-mysql/) 是一个开源的关系数据库管理系统，可以在各种平台上运行。它是一种 Oracle 产品，提供多用户访问以支持许多存储引擎。不仅如此，MySQL 还有许多有趣的特性，这些特性将应用程序的性能提升了一个档次。下面我列出了其中的几个:

*   易于管理——非常容易下载，而且免费。它提供了一个事件调度器的功能，您可以使用它来自动调度任务。
*   *健壮的事务支持*–它拥有 ACID(原子性、一致性、隔离性、持久性)属性，并提供分布式多版本支持。
*   *高性能*–它还提供快速加载实用程序，具有独特的内存缓存和表索引分区。
*   *较低的总拥有成本*–它从整体上降低了许可成本和硬件支出。
*   *安全数据保护*–它通过实施强大的机制来提供高安全性，这些机制只允许授权用户访问数据库。
*   *高可用性*–它可以运行高速主/从复制配置，还提供集群服务器。
*   *可扩展性&灵活性*–它可用于运行深度嵌入式应用程序，并创建容纳海量数据的数据仓库。

我想现在你已经非常熟悉 MySQL 在市场上被大量使用的原因了。如果你想了解更多，可以参考这篇关于 [MySQL 教程](https://www.edureka.co/blog/mysql-tutorial/)的文章。接下来，让我们看看如何在您的本地系统中安装并开始使用 MySQL。

## **MySQL 安装**

有多种方法可以在你的系统中安装 MySQL。安装 MySQL 最简单的方法是使用 MySQL 安装程序。可以从 [**MySQL 官方网站**](https://dev.mysql.com/downloads/installer/) 下载。

现在，我为什么使用这个是因为 MySQL 安装程序 是一个独立的应用程序，它简化了安装和配置 MySQL 产品的复杂性。想了解更多，可以参考这篇关于 [MySQL 工作台](https://www.edureka.co/blog/mysql-workbench-tutorial)的文章。

现在我们已经完成了安装，让我们尝试将 MySQL 与 Node.js 应用程序集成起来。

## **使用 Node.js 和 MySQL 创建 CRUD 应用**

在这里，我将使用 Node.js 创建一个简单的 CRUD 应用程序，并将其与 [MySQL 数据库](https://www.edureka.co/blog/mysql-tutorial/)链接，以在其中存储学习者的数据。因为我的主要目的是演示来自数据库的数据事务，所以我将主要关注控制器。一旦您对控制器有了足够的了解，您就可以向它添加视图了。

现在，让我们专注于我们的项目。该项目将有以下项目结构:

*   **sample nodemysqlT3**
    *   package.json
    *   script.js

因此，让我们通过为项目创建一个目录来开始应用程序开发。完成后，打开命令提示符并导航到您的项目目录。现在您需要为此设置项目配置，键入下面的命令并提供必要的细节:

```
npm init
```

现在，您需要安装所需的软件包。在这个项目中，我使用以下软件包:

*   **express.js:** 它是一个 web 框架。
*   **MySQL:**MySQL 的 Node.js 驱动
*   **body-parser:** 帮助将 POST 数据转换成请求体。
*   **nodemon:** 每当代码改变时，帮助自动重启服务器。

为了安装这些软件包，请键入以下命令:

```
npm i --s express express-handlebars mongoose body-parser
```

因为我想安装 nodemon，以便它可以访问目录中的任何文件，所以我将使用全局命令:来安装它

```
npm i -g nodemon
```

一旦你完成了软件包的安装，你最终的 JSON 文件应该看起来像下面的文件:

**package . JSON**

```
{
"name": "samplenodemysql",
"version": "1.0.0",
"description": "Edureka Demo for creating a CRUD application using Node.js and MySQL",
"main": "script.js",
"scripts": {
"test": "echo "Error: no test specified" && exit 1"
},
"author": "Edureka",
"license": "ISC",
"dependencies": {
"body-parser": "^1.19.0",
"express": "^4.16.4",
"mysql": "^2.17.1"
}
}
```

如你所见，在 dependencies 部分，所有已安装的软件包都已成功列出。现在，让我们创建将在本演示中使用的数据库。为此，在 [MySQL Workbench](https://www.edureka.co/blog/mysql-workbench-tutorial) 发布了一个新的连接。进入后，创建一个名为“learners”的新数据库。现在，在这个数据库中，创建一个名为“learnerdetails”的新表，包含以下几列:

1.  learner _ id(INT)–主键
2.  学员姓名(VARCHAR)
3.  学习者电子邮件(VARCHAR)
4.  course_Id (INT)

![learnerdetails table - Node.js MySQL Tutorial - Edureka](img/efce5f0d81700b86b7421b1c89796ec0.png)

在表中添加一些值，以便我们可以从 Node.js 应用程序中访问和测试它们。

回到应用程序，下一步是创建 **script.js** 文件，这将有助于从新创建的数据库中检索数据。Script.js 是根文件，也是这个应用程序的入口点。它将包含所有的路由器和驱动程序。除此之外，它还负责调用服务器并建立连接。

要创建这个文件，你可以使用任何代码编辑器或 IDE。我正在使用 Webstorm IDE 开发这个应用程序。首先，您需要在您的应用程序中导入所需的包，为此，您需要键入下面的代码:

```
const mysql = require('mysql');
const express = require('express');
const bodyparser = require('body-parser');
var app = express();
//Configuring express server
app.use(bodyparser.json());
```

接下来，您需要与您的 MySQL 数据库建立连接。为此，您必须使用 createConnection()函数并提供所需的详细信息，如主机、用户、密码和数据库。输入详细信息时要非常小心，否则 MySQL 不会授权连接。

```
//MySQL details
var mysqlConnection = mysql.createConnection({
host: 'localhost',
user: 'root',
password: 'edu1234',
database: 'learner',
multipleStatements: true
});
```

之后，使用 connect()函数连接使用提供的凭证建立与数据库的连接。这里需要指定如果连接成功 Node.js 应该做什么，如果连接失败应该做什么。

```
mysqlConnection.connect((err)=> {
if(!err)
console.log('Connection Established Successfully');
else
console.log('Connection Failed!'+ JSON.stringify(err,undefined,2));
});
```

最后，您还需要指定端口，因为我们将通过 HTTP 向服务器发送请求。

```
//Establish the server connection
//PORT ENVIRONMENT VARIABLE
const port = process.env.PORT || 8080;
app.listen(port, () => console.log(`Listening on port ${port}..`));
```

现在，在终端键入下面的命令:

```
nodemon script.js
```

一旦你按下回车键并且你的连接成功，你将能够在终端中看到成功的信息，如下图所示: ![cmd successful - Node.js MySQL Tutorial - Edureka](img/3492e69575169441c130bf1148ce21ef.png)

现在让我们继续，尝试创建 GET 路由器，从数据库中获取完整的学员列表及其详细信息。参考以下代码:

```
//Creating GET Router to fetch all the learner details from the MySQL Database
app.get('/learners' , (req, res) => {
mysqlConnection.query('SELECT * FROM learnerdetails', (err, rows, fields) => {
if (!err)
res.send(rows);
else
console.log(err);
})
} );
```

我将使用另一个名为 Postman 的应用程序来提出我的请求。Postman 可以作为插件轻松添加到您的浏览器中。它有助于组织来自客户端的请求并存储请求历史。 所以，一旦你在系统中安装了 [POSTMAN for Node.js](https://www.edureka.co/blog/rest-api-with-node-js/) ，你就可以开始启动它了。 现在，从下拉列表中选择 GET，在下面输入 URL:http://localhost:8080/learners

![SQL GET ALL - Node.js MySQL Tutorial - Edureka](img/7deae16a767916820a93a51c2107cd87.png)它将在回复部分向您显示数据库中学员的完整列表。

接下来，让我们尝试创建一个路由器，通过传入学习者的 ID 来获取特定学习者的详细信息。键入以下代码来创建此路由器。

```
//Router to GET specific learner detail from the MySQL database
app.get('/learners/:id' , (req, res) => {
mysqlConnection.query('SELECT * FROM learnerdetails WHERE learner_id = ?',[req.params.id], (err, rows, fields) => {
if (!err)
res.send(rows);
else
console.log(err);
})
} );
```

让我们试着在 POSTMAN 中发送一个带有学习者特定 ID 的请求。

![SQL GET - Node.js MySQL Tutorial - Edureka](img/c44a60a418fdad02c71c01d7fa088ae4.png)

接下来，让我们创建一个路由器来添加新学员的详细信息。但是在此之前，您需要在数据库中创建一个存储过程来处理您的插入或更新请求。对于开放 MySQL 工作台。在您的学员数据库下，您会发现一个“存储过程”。右键单击以创建一个存储过程，并将其命名为' learnerAddOrEdit '。![Stored Procedure - Node.js MySQL Tutorial - Edureka](img/5067ca37f610c95e37bfbc5bfa48e8eb.png)

输入以下代码，定义所有需要的程序:

**学习过的学科**

```
CREATE DEFINER=`root`@`localhost` PROCEDURE `learnerAddOrEdit`(
IN _learner_id INT,
IN _learner_name VARCHAR(45),
IN _learner_email VARCHAR(45),
IN _course_Id INT
)
BEGIN
IF _learner_id = 0 THEN
INSERT INTO learnerdetails(learner_name,learner_email,course_Id)
VALUES (_learner_name,_learner_email,_course_Id);
SET _learner_id = last_insert_id();
ELSE
UPDATE learnerdetails
SET
learner_name = _learner_name,
learner_email = _learner_email,
course_Id = _course_Id
WHERE learner_id = _learner_id;
END IF;
SELECT _learner_id AS 'learner_id';
END
```

完成后，切换回 script.js 文件，并为 POST 请求键入以下代码。

```
//Router to INSERT/POST a learner's detail
app.post('/learners', (req, res) => {
let learner = req.body;
var sql = "SET @learner_id = ?;SET @learner_name = ?;SET @learner_email = ?;SET @course_Id = ?; 
CALL learnerAddOrEdit(@learner_id,@learner_name,@learner_email,@course_Id);";
mysqlConnection.query(sql, [learner.learner_id, learner.learner_name, learner.learner_email, learner.course_Id], (err, rows, fields) => {
if (!err)
rows.forEach(element => {
if(element.constructor == Array)
res.send('New Learner ID : '+ element[0].learner_id);
});
else
console.log(err);
})
});
```

根据我们的代码，值为 0 的学员 ID 表示该特定条目是数据库中的新条目。因此，无论何时发出插入请求，都要确保将 ID 作为 0 传递。现在打开 POSTMAN，从下拉列表中选择 POST，提供 URL 并在 body 部分输入学员的详细信息。

![SQL POST - Node.js MySQL Tutorial - Edureka](img/e455ca7a2cf4ac97f255bbe8f0d2cda9.png)

现在，当您尝试获取完整的学员列表时，您也会看到新插入的记录。为了进行交叉检查，您可以打开工作台并点击 refresh 按钮来查看表中的新记录。

![New Learner - Node.js MySQL Tutorial - Edureka](img/08b4dc7b48d27d6383a1e01ef345f86f.png)

接下来，您需要创建一个路由器来更新学员的详细信息。为此，键入以下代码:

```
//Router to UPDATE a learner's detail
app.put('/learners', (req, res) => {
let learner = req.body;
var sql = "SET @learner_id = ?;SET @learner_name = ?;SET @learner_email = ?;SET @course_Id = ?; 
CALL learnerAddOrEdit(@learner_id,@learner_name,@learner_email,@course_Id);";
mysqlConnection.query(sql, [learner.learner_id, learner.learner_name, learner.learner_email, learner.course_Id], (err, rows, fields) => {
if (!err)
res.send('Learner Details Updated Successfully');
else
console.log(err);
})
});
```

让我们尝试实现更新请求。为此，返回到 POSTMAN，从下拉列表中选择 PUT 并提供 URL。

![SQL PUT - Node.js MySQL Tutorial - Edureka](img/8355c978428cca55105973b2bc548866.png)

现在，如果您返回 MySQL 工作台并进行刷新，您会看到特定的记录已经更新。

![SQL UPDATE - Node.js MySQL Tutorial - Edureka](img/005e5e82999ea497c44d447af4e2b7e2.png)

最后，让我们创建删除路由器。为此，键入下面给出的代码。

```
//Router to DELETE a learner's detail
app.delete('/learners/:id', (req, res) => {
mysqlConnection.query('DELETE FROM learnerdetails WHERE learner_id = ?', [req.params.id], (err, rows, fields) => {
if (!err)
res.send('Learner Record deleted successfully.');
else
console.log(err);
})
});
```

完成后，到邮递员那里，从下拉列表中选择删除。在 URL 中，提供要删除其详细信息的特定学员 id。点击发送后，您可以在响应正文中看到成功消息。

![SQL DELETE - Node.js MySQL Tutorial - Edureka](img/3214a4d5d2b116600389548e77b6d761.png)为了交叉检查，您可以返回到您的工作台并点击刷新。您将看到具有所提供 id 的记录已经从表中删除。

![DELETE RECORD - Node.js MySQL Tutorial - Edureka](img/621b56336051cc045bd2b6159b7ec82f.png)

这就把我们带到了 Node.js MySQL 教程这篇文章的结尾。希望，它有助于增加你的知识价值。如果你想获得更多关于 Node.js 的见解，你也可以参考我在 Node.js 上的其他文章。

*如果您发现本“Node.js MySQL 教程* *”相关，* *请查看 Edureka 提供的 [**Node.js 课程**](https://www.edureka.co/nodejs-certification-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意学习者。在印度和美国的所有其他 [Web 开发人员认证](https://www.edureka.co/complete-web-developer)课程中，Node JS 的需求很高。*

*有问题吗？请在这个 *Node.js MySQL 教程*的评论部分提到它，我们会给你回复。*