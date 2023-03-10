# 2023 年你需要知道的 50 大 Django 面试问答

> 原文：<https://www.edureka.co/blog/interview-questions/django-interview-questions/>

Django 和 Python 是最受欢迎的技能之一，当然也是最棘手的技能之一。因此，如果你想做好准备，在即将到来的 [Django](https://www.edureka.co/blog/django-tutorial/) 面试中表现最佳，这里有 50 个 Django 面试常见问题和答案。

## 十大 Django 面试问题 :

[Q1。Flask 和 Django 有什么区别？](#flaskvsdjango) [Q2。姜戈是什么？](#django) [Q3。你知道有使用 Django 的公司吗？](#companies) [Q4。Django 有什么特点？](#features) [Q5。如何检查系统上安装的 Django 版本？](#version) [Q6。使用 Django 有什么好处？](#advantages) [Q7。解释 Django 的架构。](#architecture) [Q8。简要介绍 Django 管理员。](#admin) [Q9。如何将 Django 项目连接到数据库？](#databaseconnection) [Q10。当你创建一个 Django 项目时，会创建哪些文件？简单解释一下。](#files)

让我们看看 Django 访谈问答文章中的第一个问题。

## **Q1。Flask 和 Django 有什么区别？**

| 比较因素 | 姜戈 | 瓶 |
| 项目类型 | 支持大型项目 | 专为小型项目打造 |
| 模板、管理和 ORM | 内置的 | 需要安装 |
| 易于学习 | 需要更多的学习和实践 | 简单易学 |
| 灵活性 | 允许完整的 web 开发，不需要第三方工具 | 更加灵活，因为用户可以根据自己的选择和要求选择任何第三方工具 |
| 可视化调试 | 不支持可视化调试 | 支持可视化调试 |
| 框架类型 | 含电池 | 简单、轻便 |
| 引导工具 | 内置 | 无法使用 |

## **Q2。姜戈是什么？**

Django 是一个在快节奏的新闻编辑室开发的网络开发框架。这是一个免费的开源框架，以 20 世纪 30 年代的爵士乐吉他手坦哥·雷恩哈特命名。Django 由一个名为 Django 软件基金会的非营利组织维护。Django 的主要目标是让 Web 开发变得快速而简单。

## **Q3。列举一些使用 Django 的公司？**

利用 ***Django*** 的公司有 [Instagram](https://instagram.com/edureka_learning/) 、DISCUS、Mozilla Firefox、YouTube、Pinterest、Reddit 等。

## **Q4。Django 有什么特点？**

*   SEO 优化
*   极快
*   完全加载的[框架](https://www.edureka.co/blog/python-frameworks/)伴随着认证、内容管理、RSS 提要等
*   非常安全，从而帮助开发人员避免常见的安全错误，如跨站点请求伪造(csrf)、点击劫持、跨站点脚本等
*   它具有出色的可扩展性，从而有助于满足最大的流量需求
*   非常多才多艺，允许你开发任何类型的网站

## **Q5。如何检查系统上安装的 Django 版本？**

要检查安装在您的系统上的 [Django 的版本，您可以打开命令提示符并输入以下命令:](https://docs.djangoproject.com/en/3.1/topics/install/)

*   python-m django–版本

您还可以尝试导入 Django 并使用 get_version()方法，如下所示:

```
import django
print(django.get_version())
```

## **Q6。使用 Django 有什么好处？**

*   Django 的堆栈是松散耦合的，具有紧密的内聚力
*   Django 应用程序使用的代码很少
*   允许快速开发网站
*   遵循枯燥或不重复的原则，这意味着一个概念或一段数据应该只存在于一个地方
*   在低水平和高水平上保持一致
*   行为不是隐式假设的，而是显式指定的
*   [SQL 语句](https://www.edureka.co/blog/what-is-sql/)不会执行太多次，会在内部进行优化
*   需要时可以很容易地放入原始 SQL
*   使用 URL 的灵活性

## **Q7。解释 Django 架构。**

Django 遵循 MVT 或[模型视图模板架构](https://www.edureka.co/blog/django-tutorial/#architecture)，它基于 MVC 或模型视图控制器架构。这两者的主要区别在于 Django 本身负责控制器部分。

![MVT-Django Interview Questions-Edureka](img/55c1fa97afd10f6d74d1f21e42fb2e3d.png)

Django 认为,“视图”基本上描述了呈现给用户的数据。它*不处理* *数据* *看起来*如何，而是处理*数据* *实际上是什么*。视图基本上是指定 URL 的回调函数，这些回调函数描述了呈现的数据。

另一方面，“模板”处理数据的表示，从而将内容与其表示分离。在 Django 中，视图委托模板来呈现数据。

这里的“控制器”是 Django 本身，它根据指定的 URL 将请求发送到适当的视图。这就是 Django 被称为 MTV 而不是 MVC 架构的原因。

## **Q8。简要介绍“django-admin”。**

django-admin 是 django 用于管理任务的命令行实用程序。使用 django-admin，您可以执行许多任务，下表列出了其中一些任务:

| 工作 | 命令 |
| 显示每个应用程序提供的使用信息和命令列表 | django-管理帮助 |
| 显示可用命令的列表 | django-管理帮助-命令 |
| 显示给定命令的描述及其可用选项的列表 | django-管理帮助 |
| 确定 Django 的版本 | django-管理版本 |
| 基于模型中的更改创建新的迁移 | django-管理 make 迁移 |
| 将数据库状态与当前的模型和迁移集同步 | django-管理迁移 |
| 启动开发服务器 | django-管理运行服务器 |
| 发送一封测试邮件，以确认通过 Django 发送的邮件正常工作 | django-admin sendtestemail |
| 要启动 Python 交互式解释器 | django-管理 shell |
| 显示项目中的所有迁移 | django-管理显示迁移 |

## **Q9。如何将 Django 项目连接到数据库？**

Django 有一个默认的数据库，它是 SQLite。若要将您的项目连接到此数据库，请使用以下命令:

1.  python manage.py migrate (migrate 命令查看 INSTALLED_APPS 设置并相应地创建数据库表)
2.  python manage.py 进行迁移(告诉 Django 您已经创建/更改了您的模型)
3.  python manage . py SQL migrate<name of="" the="" app="" followed="" by="" generated="" id="">(SQL migrate 获取迁移名称并返回它们的 SQL)</name>

## **Q10。当你创建一个 Django 项目时，会创建哪些文件？简单解释一下。**

当您使用 startproject 命令创建项目时，将会创建以下文件:

| 文件名 | 描述 |
| manage.py | 允许您与 Django 项目交互的命令行实用程序 |
| __init__.py | 一个空文件，告诉 Python 当前目录应该被认为是一个 Python 包 |
| settings.py | 由当前项目的设置组成 |
| urls.py | 包含当前项目的 URL |
| wsgi.py | 这是 web 服务器为您创建的项目服务的入口点 |

## **Django 面试问题**

## **Q11。什么是“模型”？**

模型是关于数据信息的唯一和确定的来源。它由您存储的数据的所有基本字段和行为组成。通常，每个模型都会映射到一个特定的数据库表。

在 Django 中，模型充当抽象层，用于结构化和操作数据。Django 模型是 django.db.models.Model 类的子类，模型中的属性表示数据库字段。

## **Q12。什么是“视图”？**

Django 视图服务于封装的目的。它们封装了负责处理用户请求并将响应返回给用户的逻辑。Django 中的视图要么返回一个 HttpResponse，要么引发一个异常，比如 Http404。HttpResponse 包含由要呈现给用户的内容组成的对象。视图也可以用于执行任务，例如从数据库中读取记录、委托给模板、生成 PDF 文件等。

## **Q13。什么是“模板”？**

Django 的模板层以一种设计者友好的格式将信息呈现给用户。使用模板，可以动态生成 [HTML](https://www.edureka.co/blog/what-is-html/) 。HTML 由内容的静态和动态部分组成。根据项目的需求，您可以拥有任意数量的模板。一个都没有也很好。

Django 有自己的模板系统，叫做 Django 模板语言(DTL)。不管后端如何，您也可以使用 Django 的标准管理来加载和呈现模板。

## **Q14。项目和 App 的区别？**

一个应用程序基本上是一个 Web 应用程序，创建它是为了做一些事情，例如，一个雇员记录的数据库。另一方面，项目是某个特定网站的应用程序的集合。因此，一个项目可以包含“n”个应用程序，一个应用程序可以在多个项目中。

## **Q15。Django 有哪些不同的传承风格？**

Django 有三种可能的继承方式:

| 继承风格 | 描述 |
| *抽象基类* | 当您希望使用父类来保存不想为每个子模型键入的信息时使用。在这里，父类永远不会被单独使用 |
| *多表继承* | 当您必须对现有模型进行子类化并希望每个模型拥有自己的数据库表 |
| *代理模型* | 如果您只想修改模型的 Python 级行为，而不想以任何方式更改“模型”字段，请使用此选项 |

## **Q16。什么是静态文件？**

Django 中的静态文件是那些为附加文件服务的文件，比如 [CSS](https://www.edureka.co/blog/what-is-css/) ，图像或者 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 文件。这些文件由 django.contrib.staticfiles 管理，通过创建一个名为 static 的子目录在项目 app 目录中创建。

## **Q17。什么是“信号”？**

Django 包含一个信号调度器，当框架中的其他地方发生动作时，它可以帮助解耦的应用程序得到通知。Django 提供了一组内置信号，基本上允许发送者在某个动作被执行时通知一组接收者。一些信号如下:

| 信号 | 描述 |
| django . db . models . signals . pre _ savedjango . db . models . signals . post _ save | 在调用模型的 save()方法之前或之后发送 |
| django . db . models . signals . pre _ deletedjango . db . models . signals . post _ delete | 在调用模型的 delete()方法或 queryset 的 delete()方法之前或之后发送 |
| django . db . models . signals . m2m _ changed | 当 Django 开始或完成 HTTP 请求时发送 |

## **Q18。简单解释 Django 字段类。**

“Field”基本上是一个抽象类，它实际上表示数据库表中的一列。Field 类又是 RegisterLookupMixin 的子类。在 Django 中，这些字段用于创建数据库表(db_type())，这些表用于使用 *get_prep_value()* 将 Python 类型映射到数据库，反之亦然，使用 *from_db_value()* 方法*。*因此，字段是不同 Django APIs 中的基础部分，比如模型和查询集。

## **Q19。如何创建 Django 项目？**

要创建 Django 项目，请使用 cd 进入您想要创建项目的目录，并键入以下命令:

*   django-管理开始项目 xyz

**注:**这里 xyz 是项目的名称。你可以给任何你想要的名字。

## **Django 面试问题**

## **Q20。什么是 mixin？**

Mixin 是一种多重继承类型，其中您可以组合多个父类的行为和属性。Mixins 提供了一种很好的方法来重用来自多个类的代码。例如，通用的基于类的视图由一个名为 TemplateResponseMixin 的 mixin 组成，其目的是定义 *render_to_response()* 方法。当它与视图中存在的类结合时，结果将是一个 TemplateView 类。

使用这些 mixins 的一个缺点是，很难分析一个子类正在做什么，以及在它的代码过于分散在多个类之间的情况下应该覆盖哪些方法。

## **Q21。什么是“会话”？**

Django 完全支持会议。使用会话框架，您可以根据每个站点的访问者轻松地存储和检索任意数据。这个框架基本上将数据存储在服务器端，并负责发送和接收 cookies。这些 cookie 由一个会话 ID 组成，而不是实际的数据本身，除非您明确使用基于 cookie 的后端。

## **Q22。上下文是什么意思？**

Django 中的 Context 是赋予 [Python 对象](https://www.edureka.co/blog/python-class/#Objects)的字典映射模板变量名。这是约定俗成的名字，但是如果你愿意的话，你也可以选择其他的名字。

## **Q23。什么时候可以在 Django ORM 中使用迭代器？**

Python 中的迭代器基本上是由可数个元素组成的容器。任何迭代器对象都会实现两个方法，即 __init__()和 __next__()方法。当您在 Django 中使用迭代器时，最好的情况是处理需要大量内存空间的结果。为此，您可以使用 iterator()方法，该方法基本上计算一个 QuerySet 并返回结果的相应迭代器。

## **Q24。解释 Django 的缓存策略？**

高速缓存基本上意味着保存昂贵计算的输出，以避免再次执行相同的计算。Django 提供了一个强大的缓存系统，反过来帮助你保存动态网页，这样就不必为每个请求反复评估它们。Django 的一些缓存策略如下表所示:

| 战略 | 描述 |
| Memcached | 哪种基于内存的缓存服务器速度最快、效率最高 |
| 文件系统缓存 | 缓存值按序列化顺序存储为单独的文件 |
| 本地内存缓存 | 这实际上是默认缓存，以防您没有指定任何其他缓存。这种类型的缓存是基于进程的，也是线程安全的 |
| 数据库缓存 | 缓存数据将被存储在数据库中，如果您有一个快速且索引良好的数据库服务器，缓存数据将非常有效 |

## **Q25。解释 Django 中中间件的使用。**

你可能会碰到无数 Django 的面试问题，在那里你会找到这个问题。中间件是一个轻量级的框架和底层插件系统，用于改变 Django 的全局输入和输出。它基本上是一个挂钩 Django 的请求/响应处理的框架。中间件中的每个组件都有特定的任务。例如， *AuthenticationMiddleware* 用于使用会话将用户与请求相关联。Django 提供了许多其他中间件，如支持站点范围缓存的缓存中间件、执行许多任务(如禁止访问用户代理、URL 重写等)的通用中间件、用于为浏览器压缩内容的 GZip 中间件等。

## **Q26。Django 中 manage.py 文件的意义是什么？**

每当您创建项目时，都会自动生成 manage.py 文件。这基本上是一个命令行实用程序，帮助您以各种方式与 Django 项目进行交互。它做的事情与 django-admin 相同，但除此之外，它还设置了 DJANGO_SETTINGS_MODULE 环境变量，以便指向您的项目设置。通常，如果您正在处理一个项目，最好使用 manage.py，而不是 django-admin。

## **Q27。解释 Django 中“migrate”命令的用法？**

在 Django 中，迁移用于传播对模型所做的更改。migrate 命令主要用于应用或取消应用对模型所做的迁移更改。这个命令基本上将当前的一组模型和迁移与数据库状态同步。您可以使用带参数或不带参数的命令。如果不指定任何参数，所有应用程序都将运行所有迁移。

## **Q28。如何查看和筛选数据库中的项目？**

为了查看数据库中的所有项目，您可以使用交互式 shell 中的“all()”函数，如下所示:

*   XYZ.objects.all()，其中 XYZ 是您在模型中创建的某个类

要从数据库中筛选出某些元素，可以使用 get()方法或 filter 方法，如下所示:

*   XYZ.objects.filter(pk=1)
*   XYZ.objects.get(id=1)

## **Q29。解释 Django 是如何处理请求的？**

如果某个用户从某个 Django 支持的网站请求页面，系统会遵循一种算法来确定需要执行哪个 Python 代码。以下是总结该算法的步骤:

1.  Django 首先决定使用哪个根 URLconf 或 URL 配置模块
2.  然后，加载特定的 Python 模块，然后 Django 寻找变量 urlpatterns
3.  然后 Django 运行这些 URL 模式，并在第一次匹配请求的 URL 时停止
4.  一旦完成，Django 就会导入并调用给定的视图
5.  如果没有一个 URL 匹配所请求的 URL，Django 会调用一个错误处理视图

## **Django 面试问题**

## **Q30。Django 是如何产生的？**

Django 基本上是从一个非常实际的需求发展起来的。世界在线的开发者 Adrian Holovaty 和 Simon Willison 开始使用 Python 开发网站。随着他们继续构建密集的、丰富的交互式网站，他们开始推出一个通用的 Web 开发框架，使他们能够越来越快地构建 Web 应用程序。在 2005 年夏天，世界在线决定开源由此产生的软件，也就是 Django。

## **Q31。如何使用基于文件的会话？**

为了利用基于文件的会话，您需要将 SESSION_ENGINE 设置为“django . contrib . sessions . backends .file”。

## **Q32。简要解释 Django URLs？**

Django 允许你随心所欲地设计自己的 URL。目的是维护一个没有任何框架限制的干净的 URL 方案。为了为您的应用程序创建 URL，您需要创建一个非正式的 Python 模块，称为 URLconf 或 URL 配置，它是纯 Python 代码，也是 URL 路径表达式到 Python 方法之间的映射。该映射的长度可以根据需要而定，也可以引用其他映射。处理请求时，请求的 URL 与 urls.py 文件中的 URL 匹配，并检索相应的视图。关于这个的更多细节，可以参考 Q29 的回答。

## **Q33。给出 Django 中存在的异常类。**

Django 使用自己的异常以及 Python 中的异常。Django 核心异常出现在 *django.core.exceptions* 类中，下表中提到了其中一些异常:

| 例外 | 描述 |
| AppRegistryNotReady | 当您试图在应用程序加载过程(初始化 ORM)完成之前使用您的模型时引发。 |
| ObjectDoesNotExist | 这是 DoesNotExist 异常的基类 |
| EmptyResultSet | 如果查询不返回任何结果，可能会引发此异常 |
| field does 不存在 | 如果请求的字段不存在，这个异常由模型的 _meta.get_field()函数引发 |
| 返回了多个对象 | 如果返回多个对象，而只需要一个对象，则查询会引发此问题 |

## **Q34。Django 稳定吗？**

是的，姜戈很稳定。像 Instagram、Discus、Pinterest 和 Mozilla 这样的公司已经使用 Django 很多年了。不仅如此，使用 Django 建立的网站经受住了每秒超过 5 万次点击的流量高峰。

## **Django 面试问题**

## **Q35。Django 框架可扩展吗？**

是的。与开发时间相比，硬件要便宜得多，这就是为什么 Django 被设计成充分利用你能提供的任何数量的硬件。Django 使用了“无共享”架构，这意味着您可以在任何级别添加硬件，如数据库服务器、缓存服务器或 Web/应用服务器。

## **Q36。Django 是 CMS 吗？**

Django 不是一个内容管理系统。它只是一个网络框架，一个让你建立网站的工具。

## **Q37。Django 应该使用哪个 Python 版本？**

下表给出了可用于 Django 的 Python 版本的详细信息:

![python version-django interview questions-Edureka](img/036739e6e0cc193951abba8ccab3f38d.png)

Python 3 实际上是最值得推荐的，因为它速度快，功能更多，支持更好。在 Python 2.7 的情况下，Django 1.1 可以和它一起使用，但只能使用到 2020 年。

## **Q38。姜戈支持 NoSQL 吗？**

[NoSQL](https://www.edureka.co/blog/sql-vs-nosql-db/#What%20is%20NoSQL?) 基本上代表“不只是 SQL”。这被认为是传统 RDBMS 或关系数据库的一种替代方案。Django 官方不支持 NoSQL 数据库。但是，有些第三方项目，比如 Django non-rel，允许在 Django 中使用 NoSQL 功能。目前可以使用 MongoDB 和 Google App Engine。

## **Q39。如何定制 Django 管理界面的功能？**

有许多方法可以做到这一点。您可以搭载在 Django 自动生成的添加/更改表单之上，您可以使用 *js 参数*添加 JavaScript 模块。这个参数基本上是指向 JavaScript 模块的 URL 列表，这些模块将包含在您的项目中的一个<脚本>标签中。如果您想做更多的事情，而不仅仅是摆弄 from，您可以专门为管理员编写视图。

## **Q40。Django 比 Flask 好吗？**

Django 是一个允许你构建大型项目的框架。另一方面， [Flask](https://www.youtube.com/watch?v=lj4I_CvBnt0) 用于构建较小的网站，但是 Flask 比 Django 更容易学习和使用。Django 是一个成熟的框架，不需要第三方包。Flask 更像是一个轻量级的框架，它允许你按照自己喜欢的方式安装第三方工具。所以，这个问题的答案基本上取决于用户的需求，如果需求非常大，答案肯定是，Django。

## **Django 面试问题**

## **Q41。举一个 Django 视图的例子。**

Django 中的视图要么返回一个 HttpResponse，要么引发一个异常，比如 Http404。HttpResponse 包含由要呈现给用户的内容组成的对象。

**举例:**

```
from django.http import HttpResponse
def hello_world(request):
    html = "
<h1>Hello World!</h1>

"
    return HttpResponse(html)

```

**Q42。如果在输入正确的详细信息登录管理部分后仍收到“请输入正确的用户名和密码”的消息，该怎么办？**

如果您输入了正确的详细信息，但仍然无法登录到管理站点，请交叉验证用户帐户是否将 *is_active* 和 *is_staff* 属性设置为 True。管理站点只允许这些值设置为 True 的用户。

## **Q43。** **如果输入正确的详细信息后仍无法登录，并且没有错误消息，该怎么办？**

在这种情况下，登录 cookie 设置不正确。如果 Django 发出的 cookie 的域与您的浏览器中的域不匹配，就会发生这种情况。为此，您必须更改 *SESSION_COOKIE_DOMAIN* 设置以匹配您的浏览器。

## **Q44。如何限制管理员访问权限，使对象只能由创建它们的用户编辑？**

Django 的 *ModelAdmin* 类提供了定制挂钩，使用这些挂钩，您可以控制管理器中对象的可见性和可编辑性。为此，可以使用*的 get_queryset()* 和*的 has_change_permission()。*

## **Q45。当您在管理站点上看不到所有对象时该怎么办？**

缺少外键值或外键字段设置为 null=False 会导致行数不一致。如果*外键*指向不存在的记录，并且如果该外键出现在 *list_display* 方法中，则该记录不会显示在管理变更列表中。

## **Q46。csrf _ token 是什么意思？**

csrf_token 用于防止跨站点请求伪造。当恶意网站包含一个链接、一些 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 或一个表单，其目的是通过使用真正用户的登录凭证在您的网站上执行一些操作时，就会发生这种攻击。

## **Q47。Django 支持多列主键吗？**

不可以。Django 只支持单列主键。

## **Q48。如何查看 Django 正在运行的原始 SQL 查询？**

首先，确保您的调试设置为 True。然后，键入以下命令:

```
from django.db import connection
connection.queries
```

## **Q49。必须使用模型/数据库层吗？**

不。模型/数据库层实际上与框架的其余部分是分离的。

## **Q50。如何使一个变量对所有模板都可用？**

如果你的所有模板都需要相同的对象，比如菜单，你可以使用 *RequestContext* 。这个方法将一个 HttpRequest 作为它的第一个参数，并根据引擎的 context_processors 配置选项，用一些变量自动填充上下文。

说到这里，我们就到了这篇关于 Django 面试问题的文章的结尾。我希望你清楚这篇文章中与你分享的所有内容。 ***确保你尽可能多的练习，恢复你的经验。***

*对这篇 Django 访谈问题文章有疑问？请在这个“Django 面试问题”博客的评论部分提到它，我们会尽快回复你。*

*要深入了解任何趋势技术及其各种应用，您可以注册参加实时 **[Edureka 在线培训](https://www.edureka.co/)** ，24/7 全天候支持和终身访问。*