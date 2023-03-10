# 2023 年你必须准备的春季面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/top-spring-interview-questions-2016/>

Spring 是当今用 Java 开发企业应用程序最广泛使用的框架。当然，Java 是编程语言中的佼佼者，年复一年地为创造新的和创新的工作机会做出了巨大贡献。成为 ***Spring 认证专家*** 将帮助你获得与 Java 相关的最佳高薪工作。如果你打算在不久的将来参加春季面试，这里有一个明确的春季面试问题和答案列表，你可以为此做准备。如果你已经参加了春季面试，我们鼓励你在下面的评论标签中粘贴更多的问题。万事如意！

# 1。列出 Spring 框架的重要特性。

 <caption>#### **弹簧框架的特点**</caption> 
| **特色** | **描述** |
| *轻量级* | 就尺寸和透明度而言，Spring 框架是轻量级的。 |
| *控制反转* | 在 Spring 中，松散耦合是使用控制反转实现的，其中对象给出它们自己的依赖关系，而不是创建或寻找依赖对象。 |
| *面向方面编程* | Spring 框架将应用业务逻辑与系统服务分离，支持面向方面的编程，并支持内聚开发。 |
| *集装箱* | Spring Framework 创建并管理应用对象的生命周期和配置。 |
| *MVC 框架* | Spring Framework 是一个 MVC web 应用框架，可通过接口配置，支持多种视图技术。 |
| *交易管理* | 对于事务管理， Spring 框架提供了一个通用的抽象层。 |
| *JDBC 异常处理* | Spring 框架的 JDBC 抽象层提供了一个异常层次，简化了错误处理策略 。 |

# 2。说出 Spring 框架的不同模块。

Spring 框架有以下模块:

*   JDBC 模块
*   ORM 模块
*   OXM 模块
*   Java 消息服务(JMS)模块
*   交易模块
*   Web 模块
*   Web-Servlet 模块
*   Web-Struts 模块
*   门户网站模块

# 3。什么是 Spring 配置文件？

Spring 配置文件本质上是一个 XML 文件，它包含了关于类的信息，并描述了它们是如何配置和相互介绍的。

# 4。解释 Spring 框架上下文中的依赖注入。

依赖注入是一种设计模式，它允许用户移除硬编码的依赖，并确保应用程序是松散耦合的、可扩展的和可维护的。依赖注入设计模式用于将依赖解析从编译转移到运行时。

# 5。哪两种类型的依赖注入？

*   基于构造函数的依赖注入
*   基于 Setter 的依赖注入

# 6。如何在 Spring 应用中实现依赖注入？

Spring 中有三种配置依赖注入的方式:基于 XML 的配置、基于 Java 的配置和基于注释的配置。

# 7。列出基于注释的 Spring 配置中的一些重要注释。

重要的注释是:

*   @必填
*   @自动连线
*   @限定符
*   @资源
*   @PostConstruct
*   @PreDestroy

# 8。在 Spring 框架的上下文中，解释面向方面的编程。

面向方面编程基本上将程序逻辑分解成更小的块，称为“关注点”。跨应用程序多个点的功能被称为横切关注点，它们独立于应用程序的核心业务逻辑运行。Spring 框架上下文中的一些重要方面是:日志记录、审计、缓存和声明性事务。

# 9。解释春天的豆子。

Beans 是构成 Spring 应用程序主干的对象。它们由 Spring IoC 容器管理。换句话说，bean 是由 Spring IoC 容器实例化、组装和管理的对象。

# 10。列出 Spring bean 的不同作用域。

Spring beans 中定义了五个作用域。它们是:

*   一个
*   原型
*   请求
*   会议
*   全局会话

# 11。Spring bean 配置文件的作用是什么？

Spring bean 配置文件定义了将由 Spring 上下文初始化的所有 bean。当创建 Spring ApplicationContext 的实例时，它读取 spring bean xml 文件并初始化所有这些文件。一旦初始化了上下文，就可以用它来获取不同的 bean 实例。

# 12。解释 Spring bean 的生命周期。

Spring Beans 和所有依赖项都由 Spring 容器初始化。当“上下文”被销毁时，它也会销毁所有相应的已初始化的 beans。在极少数情况下，beans 在使用之前需要某种级别的验证。Spring 框架还支持 spring beans 中的后初始化和预销毁方法。

# 13。Spring bean 自动布线有哪些不同的类型？

*   自动连线名称
*   自动连线类型
*   由构造函数自动点火
*   自动点火

# 14。解释 DispatcherServlet 和 ContextLoaderListener 的作用。

DispatcherServlet 基本上是 Spring MVC 应用程序中的前端控制器，因为它加载 spring bean 配置文件并初始化所有已配置的 bean。如果启用了注释，它还会扫描包来配置任何用@Component、@Controller、@Repository 或@Service 注释注释的 bean。

另一方面，ContextLoaderListener 是在 Spring root 中启动和关闭 WebApplicationContext 的监听器。它的一些重要功能包括将 ApplicationContext 的生命周期与 ServletContext 的生命周期捆绑在一起，以及自动创建 ApplicationContext。

# 15。解释 InternalResourceViewResolver 和 MultipartResolver 的作用。

InternalResourceViewResolver 是 ViewResolver 接口的实现之一，它允许您通过 bean 属性查看页面目录和后缀位置。

另一方面，MultipartResolver 是用于上传文件的接口。–CommonsMultipartResolver 和 standardservletmultipartresolver 是 Spring 框架为文件上传提供的两个实现。

# 16。如何在独立的 Java 程序中创建 ApplicationContext？

我们可以通过三种方式做到这一点:

*   **AnnotationConfigApplicationContext:**如果我们使用注释进行配置，那么我们可以用它来初始化容器并获得 bean 对象。
*   **classpathmlaplicationcontext:**如果我们在 Java 应用程序中有 spring bean 配置 xml 文件，那么我们可以使用这个类来加载文件和检索容器对象。
*   **file systemxmlaplicationcontext:**这与 ClassPathXmlApplicationContext 非常相似，只是 xml 配置文件可以从文件系统中的任何位置加载。

# 17。解释 JDBC 模板在 Spring 中的用法。

Spring 通过 Spring JDBC 模板简化了数据库访问处理。

与标准 JDBC 相比，春季 JDBC 模板有许多优势:

*   Spring JDBC 模板自动清理资源；比如释放数据库连接。
*   Spring JDBC 模板将标准的 JDBC SQLExceptions 转换成 RuntimeExceptions。这确保了更快的响应时间来识别和消除错误。

# 18。Spring 提供了哪些类型的事务管理支持？

*   **程序化交易管理**:交易量较小的操作
*   **声明式事务管理**:针对大量事务。

# 19。解释 Spring AOP 中关注点和横切关注点的区别。

简而言之，关注点是应用程序模块中期望的行为。这是程序员想要实现的核心功能。

另一方面，横切关注点是适用于整个应用程序的关注点。安全、数据传输、日志记录等都是跨领域关注的例子。

# 20。解释建议，在春天的背景下。

建议是方面的实现。它在连接点被插入到应用程序中。有不同类型的建议，包括“周围”、“之前”和“之后”。

# 21。在 Spring 的上下文中，什么是连接点？

连接点是代码中我们可以应用方面的一个机会。在 Spring 编程中，连接点总是代表一个方法的执行。

# 22。Spring 支持哪种连接点？

Spring 框架支持方法执行连接点。

# 23。什么是切入点？

切入点是匹配连接点的谓词。点切割定义了应该在哪些连接点应用建议。

# 24。什么是目标对象？

目标对象是由一个或多个方面建议的代理对象。

# 25。什么是编织？

它是将方面与其他应用程序链接起来的过程。

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[入门弹簧框架](https://www.edureka.co/blog/videos/building-web-application-using-spring-framework/ "Building web application using Spring Framework")

[使用 Spring 框架构建 Web 应用](https://www.edureka.co/blog/videos/building-web-application-using-spring-framework/ "Building web application using Spring Framework")

加入[春季框架课程](https://www.edureka.co/spring-certification-course)