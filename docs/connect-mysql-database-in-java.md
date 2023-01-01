# 如何用 Java 连接数据库？–JDBC 教程

> 原文：<https://www.edureka.co/blog/connect-mysql-database-in-java>

Java 作为最著名的编程语言之一，为数据库提供了广泛的支持。它帮助我们通过 [JDBC](https://www.edureka.co/blog/advanced-java-tutorial/#JDBC) (Java 数据库连接)连接到各种数据库。在本文中，我将告诉您如何使用 JDBC 连接到数据库并执行查询。

本文涵盖了以下主题:

*   [JDBC 简介](#IntroductiontoJDBC)
*   [常见 JDBC 组件](#CommonJDBCComponents)
*   [创建 JDBC 应用程序的步骤](#StepstocreateJDBCApplication)
*   [JDBC 连接](#JDBCConnections)

## **JDBC 简介**

JDBC 是标准的 Java API 之一，用于在 Java 编程语言和各种数据库之间建立独立于数据库的连接。这个 API 让你用[结构化查询语言](https://www.edureka.co/blog/what-is-mysql/) ( SQL )对访问请求语句进行编码。这个主要涉及到打开一个连接，创建一个 SQL 数据库，执行 SQL 查询，然后到达输出。

JDBC API 可以用来访问存储在任何关系数据库中的表格数据。有了这个，你可以更新，保存，获取和删除数据库中的数据。它类似于微软提供的开放式数据库连接(ODBC)。

为了更好地理解 JDBC 的工作方式，让我们更深入地研究这个主题，理解 Java 数据库连接背后的架构。

## **常见的 JDBC 组件**

JDBC API 提供了以下接口和类

*   ***驱动管理器:*** 这主要是用来管理数据库驱动的列表。识别某个子协议的驱动程序将用于建立数据库连接。

*   ***驱动*** 是处理与数据库服务器通信的接口。它还抽象了与驱动对象相关的细节。

*   ***连接*** 是一个接口，由连接数据库所需的所有方法组成。连接对象处理数据库的通信功能。语境。

现在让我们进入下一个主题，看看创建 JDBC 应用程序所需的步骤。

## **创建 JDBC 应用程序的步骤**

为了创建一个 JDBC 应用程序，您需要遵循几个步骤。让我们看看它们是什么。

![Steps to create JDBC Application - Advanced Java tutorial - Edureka](img/1a28cc1ec175b502ca0e9a7830097100.png)

1.  **导入包:**你需要包含所有包含[数据库编程](https://www.edureka.co/blog/what-is-mysql/)所需的 JDBC 类的包。大多数情况下，使用*导入 java.sql.** 就足够了。

2.  **注册 JDBC 驱动:**这里你要初始化一个驱动，这样你就可以打开与数据库的通信通道。

3.  **打开一个连接:**这里可以使用 *getConnection()* 方法创建一个连接对象，表示与数据库的物理连接。

4.  **执行查询:**这实际上需要使用一个语句类型的对象来构建 SQL 语句并提交给数据库。

5.  **从结果集中提取数据:** 建议您使用合适的 *getXXX()* 方法从结果集中提取数据。

6.  **清理环境:** 在这里，显式关闭所有数据库资源，而不是依赖 JVM 的垃圾收集是很重要的。

现在，您已经看到了创建 JDBC 应用程序的各个步骤，让我们看看创建数据库和建立连接的示例代码。

```
package Edureka;
import java.sql.*;
import java.sql.DriverManager;
public class Example {
// JDBC driver name and database URL
static final String JDBC_DRIVER = "com.mysql.jdbc.Driver";
static final String DB_URL = "jdbc:mysql://localhost/emp";
// Database credentials
static final String USER = "root";
static final String PASS = "";
public static void main(String[] args) {
Connection conn = null;
Statement stmt = null;
try{
//STEP 2: Register JDBC driver
Class.forName("com.mysql.cj.jdbc.Driver");
//STEP 3: Open a connection
System.out.println("Connecting to database...");
conn = DriverManager.getConnection(DB_URL,"root","");
//STEP 4: Execute a query
System.out.println("Creating statement...");
stmt = conn.createStatement();
String sql;
sql = "SELECT id, first, last, age FROM Employees";
ResultSet rs = stmt.executeQuery(sql);
//STEP 5: Extract data from result set
while(rs.next()){
//Retrieve by column name
int id = rs.getInt("id");
int age = rs.getInt("age");
String first = rs.getString("first");
String last = rs.getString("last");
//Display values
System.out.print("ID: " + id);
System.out.print(", Age: " + age);
System.out.print(", First: " + first);
System.out.println(", Last: " + last);
}
//STEP 6: Clean-up environment
rs.close();
stmt.close();
conn.close();
}catch(SQLException se){
//Handle errors for JDBC
se.printStackTrace();
}catch(Exception e){
//Handle errors for Class.forName
e.printStackTrace();
}finally{
//finally block used to close resources
try{
if(stmt!=null)
stmt.close()
}catch(SQLException se2){
}// nothing can be done
try{
if(conn!=null)
conn.close();
}catch(SQLException se){
se.printStackTrace();
}//end finally try
}//end try
System.out.println("Goodbye!");
}//end main
} // end Example
```

上面的代码在本地主机数据库中创建了一个表。要在创建的数据库中插入值，可以参考下面的代码。我将只为第 4 步编写代码。代码的其余部分与上面相同。

```
//STEP 4: Execute a query
System.out.println("Creating table in given database...");
stmt = conn.createStatement();
String sql = "CREATE TABLE EMPLOYEES " +
"(id INTEGER not NULL, " +
" first VARCHAR(255), " +
" last VARCHAR(255), " +
" age INTEGER, " +
" PRIMARY KEY ( id ))";
stmt.executeUpdate(sql);
System.out.println("Created table in given database...");
System.out.println("Inserting records into the table...");
stmt =conn.createStatement();
String sql ="INSERT INTO Employees VALUES (100, 'Kriss', 'Kurian', 18)";
stmt.executeUpdate(sql);
sql = "INSERT INTO Employees VALUES (101, 'Enrique', 'John', 25)";
stmt.executeUpdate(sql);
sql= "INSERT INTO Employees (102, 'Taylor', 'Swift', 30)";
stmt.executeUpdate(sql);
sql= "INSERT INTO Employees VALUES(103, 'Linkin', 'Park', 28)";
stmt.executeUpdate(sql);
System.out.println("Inserted records into the table...");
```

这就是如何建立到数据库的连接并在表中插入值的方法。现在，让我们进一步了解各种 JDBC 驱动程序类型

### **JDBC 司机类型**

JDBC 驱动程序用于实现 JDBC API 中定义的接口，以便与数据库服务器进行交互。本质上，一个 **JDBC 司机** 做三件事，它们是: 1。建立与数据源的连接。 2。它将向数据源发送查询和更新语句。 3。最后，它处理结果。

例如，JDBC 驱动程序通过发送 [SQL 或数据库命令](https://www.edureka.co/blog/sql-commands)来帮助你打开一个数据库连接并与之交互。如果你想了解更多关于 JDBC 司机的类型，你可以参考这篇关于 [JDBC 司机](https://www.edureka.co/blog/advanced-java-tutorial#JDBCDriver)的文章。

现在，让我们进一步了解 JDBC 连接。

## **JDBC人脉**

*   **导入 JDBC 包:**将**导入**语句添加到您的 [Java 程序](https://www.edureka.co/blog/java-programs/)中，以导入您的 Java 代码中所需的类。

*   注册 JDBC 驱动程序:在这个步骤中， [JVM](https://www.edureka.co/blog/what-is-java/#ComponentsinJava) 将所需的驱动程序实现加载到内存中，这样它就可以满足 JDBC 的请求。注册驾驶员有两种方法。

    *   注册驱动程序最合适的方法是使用 Java 的 **forName()** 方法将驱动程序的类文件动态加载到内存 *中，由内存自动注册。* 这种方法很合适，因为它允许您使驱动程序注册可配置和可移植。看看下面的代码:

        ```
        try {
        Class.forName("oracle.jdbc.driver.OracleDriver");
        }
        catch(ClassNotFoundException ex) 
        System.out.println("Error: unable to load driver class!");
        System.exit(1);
        }
        ```

    *   第二种注册驱动程序的方法是使用静态的 **registerDriver()** 方法。

        ```
        try {
        Driver myDriver = new oracle.jdbc.driver.OracleDriver();
        DriverManager.registerDriver( myDriver );
        }
        catch(ClassNotFoundException ex)
        {
        System.out.println("Error: unable to load driver class!");
        System.exit(1);
        }
        ```

*   如果您使用的是不符合 JDK 标准的 JVM，比如微软提供的 JVM，那么您应该使用 *registerDriver()* 方法。这里每个表单都需要一个数据库 **URL** 。

*   **数据库 URL 格式:** URL 格式是创建指向您想要连接的数据库的正确格式化地址所必需的。一旦加载了驱动程序，就可以使用**driver manager . getconnection()**方法建立连接。DriverManager.getConnection()方法是

    *   getConnection(字符串 url)

    *   getConnection(字符串 url，属性属性)

    *   getConnection(字符串 url，字符串用户，字符串密码)

*   **创建连接对象**

您可以使用数据库 URL、用户名和密码以及 properties 对象来创建连接。

*   **关闭**

最后，要结束数据库会话，您需要关闭所有数据库连接。但是，如果您忘记了，Java 的垃圾收集器会在清理过时对象时关闭连接。

```
conn.close(); // Used to close the connection
```

这就是 Java 数据库连接的全部内容。如果你想了解 JDBC 更多，可以参考这篇关于[高级 Java 教程](https://www.edureka.co/blog/advanced-java-tutorial)的文章。这就把我们带到了“如何连接到数据库”这篇文章的结尾。我希望我已经阐明了你对 JDBC 的了解。

查看 Edureka 提供的 [Java 在线培训](https://www.edureka.co/java-j2ee-training-course)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。

有问题吗？请在这篇“如何连接到数据库”文章的评论部分提到它，我们会尽快回复您。