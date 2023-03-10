# Salesforce 教程:学习创建自己的 Salesforce 应用程序

> 原文：<https://www.edureka.co/blog/salesforce-tutorial>

在之前的博客中，你学习了[什么是 Salesforce](https://www.edureka.co/blog/what-is-salesforce/) 以及不同的 [Salesforce 认证](https://www.edureka.co/blog/salesforce-certifications/)。在这篇 Salesforce 教程博客中，我将向您展示如何创建自定义 Salesforce 应用程序。我将创建一个名为*student force*的应用程序，可用于维护学生记录。

这个 app 会包含三个不同的对象(表格)来存储数据。第一个名为*学生数据*的对象将包含学生的姓名和他们的个人信息，如电子邮件 id、电话号码和籍贯。学生所属的学院将被存储在名为*学院*的第二个对象中，名为*分数*的第三个对象将包含学生在各个科目中获得的分数。

## **Salesforce 教程**

在这篇 Salesforce 教程博客中，我已经用分步说明和截图讲述了以下主题:

*   如何创建 app 环境？
*   什么是选项卡，如何在你的应用中创建选项卡？
*   什么是简档，如何定制用户简档？
*   如何在 app 中创建对象？
*   如何在对象中创建字段并定义其数据类型？
*   如何在这些对象中添加条目(字段)？
*   如何链接两个不同的对象(在它们之间创建关系)？

在我开始创建应用程序之前，让我向您介绍构建 Salesforce 应用程序的云环境。

## **Salesforce 组织**

Force.com 为您或您的组织提供的云计算空间称为 Salesforce org。它也称为 Salesforce 环境。开发人员可以在 Salesforce Org 上创建自定义 Salesforce 应用程序、对象、工作流、数据共享规则、Visualforce 页面和 Apex 编码。立即获取您的 [Salesforce 销售云认证](https://www.edureka.co/masters-program/salesforce-architect-certification-course)以获得认证。

现在让我们深入了解 Salesforce 应用程序，并了解它的工作原理。

## **Salesforce Apps**

Salesforce 应用程序的主要功能是管理客户数据。Salesforce 应用程序提供了一个简单的 UI 来访问存储在对象(表)中的客户记录。应用程序还通过链接字段来帮助建立对象之间的关系。

应用包含一组最终用户可见的相关选项卡和对象。下面的截图展示了 *StudentForce* 应用的样子。

![salesforce app - salesforce tutorial - edureka](img/5e1427b6fdca109aa33779176b2ae3f7.png)

截图右上角高亮部分显示的是 app 名称:*student force*。个人资料图片旁边高亮显示的文字是我的用户名:*vard Han NS*。

在创建对象和输入记录之前，您需要设置应用程序的框架。您可以按照以下说明来设置应用程序。

### **设置 App 的步骤**

1.  点击右上角 app 名称旁边的 *设置* 按钮。
2.  在左侧的 栏中，进入 *构建* →选择 *创建* →从下拉菜单中选择 *应用* 。 ![create salesforce app - salesforce tutorial - edureka](img/b5ae272f22a9b4a68e7bffd8d5bff7c3.png) 
3.  点击 *新建* 如下图截图所示。 ![new salesforce app - salesforce tutorial - edureka](img/bbbe4b1acdcdd2340916bb2817d8aae5.png) 
4.  选择 *自定义 App* 。
5.  进入 *App 标签* 。 *StudentForce* 是我的 app *的标签。* 点击 *下一个* 。![custom app - salesforce tutorial - edureka](img/8c41bfcee0ded0ebab6688b02916f50f.png) 
6.  为你的 app 选择一张个人资料图片。点击 *下一个* 。
7.  选择你认为必要的标签。点击 *下一个* 。
8.  选择您希望 *app* 分配到的不同情景模式。点击 *保存* 。

在第 7 步和第 8 步中，要求您选择相关的选项卡和配置文件。选项卡和简档是 Salesforce 应用程序不可或缺的一部分，因为它们帮助您管理 Salesforce 中的对象和记录。

在本 salesforce 教程中，我将向您详细解释选项卡、简档，然后向您展示如何创建对象并向其添加记录。

## **Salesforce 选项卡**

选项卡用于访问 Salesforce 应用程序中的对象(表格)。它们出现在屏幕顶部，类似于工具栏。它包含多个对象的快捷链接。单击选项卡中的对象名称，将显示该对象中的记录。选项卡还包含指向外部 web 内容、自定义页面和其他 URL 的链接。以下屏幕截图中突出显示的部分是 Salesforce 选项卡。

![salesforce tabs - salesforce tutorial - edureka](img/d9f9117772217c33f36b55eabc89d94c.png)

所有应用都会有一个 *首页* 标签页默认设置。点击选项卡菜单中的“ *+* ”可选择标准选项卡。客户、联系人、组、潜在客户、简档是 Salesforce 提供的标准选项卡。例如， *账户* 选项卡将显示 SFDC 组织中的账户列表，而 *联系人* 选项卡将显示 SFDC 组织中的联系人列表。

### **添加标签页的步骤**

1.  点击标签菜单中的“+”。
2.  点击 *自定义标签页，右侧出现* 。
3.  选择您选择的选项卡，点击 *保存* 。![custom tabs - salesforce tutorial - edureka](img/65ad07a7f989602107b14a309f320f5b.png) 

除了标准标签页，您还可以创建自定义标签页。您在上面的截图中看到的 *学生* 选项卡是我创建的自定义选项卡。这是到达自定义对象的捷径: *学生* 。

### **创建自定义标签页的步骤**

1.  导航至设置→构建→创建→选项卡。
2.  点击 *新建* 。
3.  选择正在创建标签的对象名称。我的情况是 *学生数据* 。这是我创建的一个自定义对象(创建该对象的说明将在本博客后面介绍)。
4.  选择您喜欢的标签样式并输入描述。
5.  点击下一步→保存。新增的 *学生数据* 页签会出现如下所示。![students data object - salesforce tutorial - edureka](img/d14347ea5283f6ff6dc11f14d84f67d2.png) 

## **Salesforce 个人资料**

需要访问数据或 SFDC 组织的每个用户都将被链接到一个配置文件。简档是设置和权限的集合，控制用户在 Salesforce 中可以查看、访问和修改的内容。

简档控制用户权限、对象权限、字段权限、应用程序设置、选项卡设置、apex 类访问、Visualforce 页面访问、页面布局、记录类型、登录时间和登录 IP 地址。

您可以根据用户的背景定义个人资料。例如，可以为不同的用户设置不同的访问级别，如系统管理员、开发人员和销售代表。

与选项卡类似，我们可以使用任何标准配置文件或创建自定义配置文件。默认情况下，可用的标准配置文件包括:只读、标准用户、市场营销用户、合同经理、解决方案经理和系统管理员。如果您想要创建自定义配置文件，您必须首先克隆标准配置文件，然后编辑该配置文件。请注意，一个配置文件可以分配给多个用户，但一个用户不能分配多个配置文件。

### **创建概要文件的步骤**

1.  点击设置→管理→管理用户→个人资料
2.  然后，您可以点击*编辑*来克隆任何现有的档案。 ![salesforce profiles - salesforce tutorial - edureka](img/2f8e837f9ddf8f026d21c88badfd46e9.png)

为您的应用程序设置标签和档案后，您就可以将数据加载到其中。因此，本 Salesforce 教程的下一节将介绍如何以记录和字段的形式将数据添加到对象中。

*报名参加 [Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training)，快速推进您的职业生涯。*

## **sales force 中的对象、字段和记录**

对象、字段和记录是 Salesforce 的组成部分。因此，了解它们是什么以及它们在构建应用程序中扮演什么角色非常重要。

对象是存储数据的 Salesforce 中的数据库表。Salesforce 中有两种类型的对象:

*   **标准对象:**sales force 提供的对象称为标准对象。例如，客户、联系人、潜在客户、业务机会、活动、产品、报告、仪表板等。
*   **自定义对象:**用户创建的对象称为自定义对象。

对象是记录的集合，记录是字段的集合。

对象中的每一行都由许多字段组成。因此，对象中的记录是相关字段的组合。请看下面的 excel 图表。

![sample excel - salesforce tutorial - edureka](img/2eeb8bdb69c9e0242aef8778ab2f14ce.png)

我将创建一个名为 *的学生数据对象* ，其中 将包含学生的个人详细信息。

创建自定义对象的步骤:

1.  导航至设置→构建→创建→对象
2.  点击 *新建自定义对象* 。
3.  填写 *对象名称* 和 *描述* 。从下图可以看出，对象名为 *学生数据* 。![custom object - salesforce tutotial - edureka](img/7c9d4bb557e4289f395271269eded8c4.png) 
4.  点击 *保存* 。

如果您想将此自定义对象添加到选项卡菜单，那么您可以遵循本 Salesforce 教程博客中前面提到的说明。

创建对象后，您需要在该对象中定义各种字段。例如，学生记录中的字段将是学生姓名、学生电话号码、学生电子邮件 ID、学生所属的系和他的家乡城市。

只有在定义了字段后，您才能向对象添加记录。

### **添加自定义字段的步骤**

1.  导航至设置→构建→创建→对象
2.  选择要添加字段的对象。我的情况是 *学生数据* 。
3.  向下滚动至该对象的自定义字段&关系，点击*新建*，如下图 所示。![new objects - salesforce tutorial - edureka](img/5824659999bb1cc677dc3501d47aa094.png) 
4.  你需要选择那个特定字段的数据类型，然后点击 *下一步* 。我选择了 *文本* 格式，因为我将在该字段中存储字母。 *本博客的下一节将详细解释不同数据类型的字段。*
5.  然后会提示您输入字段的名称、字段的最大长度和描述。
6.  您也可以使其成为可选/必填字段，并通过选中复选框来允许/禁止不同记录的重复值。请看下面的截图，以便更好地理解。![new fields - salesforce tutotial - edureka](img/7f54aab99cfb38401537ac281b1c4565.png)
7.  点击 *下一个* 。
8.  选择可以在以后编辑该文本字段的各种配置文件。点击 *下一个* 。
9.  选择应包含该字段的页面布局。
10.  点击 *保存* 。

从下面的截图可以看出，有两种类型的字段。默认情况下为每个对象创建的标准字段和我自己创建的自定义字段。我为 *学生数据* 创建的四个字段是城市、部门、电子邮件 ID 和电话号码。您会注意到所有自定义字段都带有后缀“__C ”,这表示您有权编辑和删除这些字段。而有些标准字段可以编辑，但不能删除。

![fields - salesforce tutotial - edureka](img/8f4c96c497f3c03e8baa498316b7ae19.png)

现在您可以将学生记录(完整的一行)添加到您的对象中。

### **添加一条记录的步骤**

1.  从选项卡菜单进入对象表。 *学生数据* 是我要添加记录的对象。
2.  从下图可以看出，没有现存的记录。点击 *【新增】* 添加新的学生记录。![new record - salesforce tutotial - edureka](img/7f4318f7a01c14c2bfb3b8a451304dbe.png) 
3.  将学生详细信息添加到不同的字段，如下图所示。点击 *保存* 。![custom record - salesforce tutotial - edureka](img/fcc9ab6eb6c05c45efbee45b645824c6.png) 
4.  您可以创建任意数量的学生记录。我已经创建了 4 个学生记录，如下图所示。![students - salesforce tutotial - edureka](img/ca659c0f483788706c2329f346055703.png)
5.  如果您想编辑学生的详细信息，可以点击 *编辑* ，如下图截图所示。![student - salesforce tutotial - edureka](img/0401588110e4ff690b46c01aa5670f03.png) 

## **数据类型字段**

数据类型控制哪种类型的数据可以存储在一个字段中。记录中的字段可以有不同的数据类型。比如:

*   如果是电话号码字段，可以选择 *电话* 。
*   如果是名称或者文本字段，可以选择 *文本* 。
*   如果是日期/时间字段，可以选择 *日期/时间* 。
*   通过选择 *选项列表* 作为字段的数据类型，您可以在该字段中写入预定义值并创建下拉列表。

您可以为自定义字段选择任何一种数据类型。下面是列出不同数据类型的屏幕截图。

![data types - salesforce tutorial - edureka](img/d6a0bf8107be1b5322fe1e405f0b7e4c.png)

数据类型如 *查找关系、主从关系和外部查找关系* 用于创建一个或多个对象之间的链接/关系。对象之间的关系是本 Salesforce 教程博客的下一个讨论主题。

## **sales force 中的对象关系**

顾名思义，对象关系在 Salesforce 中用于创建两个对象之间的链接。你脑海中的问题是，为什么需要它？我用一个例子来说一下需要。

在我的*student force*app 中，有一个 *学生数据* 对象，里面包含了学生的个人信息。关于学生的分数和他们以前的大学的详细信息呈现在不同的对象中。我们可以使用关系来链接这些使用相关字段的对象。学生和学院的标志可以与 *学生数据* 对象 的 *学生姓名* 字段相联系。

选择数据类型时可以定义关系。它们总是在子对象中定义，并引用主对象中的公共字段。当所需的数据存在于不同的对象中时，创建这样的链接将帮助您轻松地搜索和查询数据。对象之间可以存在三种不同类型的关系。他们是:

*   主-详细信息
*   查找
*   接合处

让我们逐一看看:

**了解我们在顶级城市的销售队伍培训课程**

| 印度 | 美国 | 其他国家 |
| [海得拉巴的销售队伍培训](https://www.edureka.co/salesforce-administrator-and-developer-training-hyderabad) | [达拉斯的 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-dallas) | [墨尔本的 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-melbourne) |
| [班加罗尔的销售队伍培训](https://www.edureka.co/salesforce-administrator-and-developer-training-bangalore) | [夏洛特 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-charlotte) | [伦敦的 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-london) |
| [金奈的 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-chennai) | [纽约的销售人员培训](https://www.edureka.co/salesforce-administrator-and-developer-training-new-york-city) | [悉尼的 Salesforce 培训](https://www.edureka.co/salesforce-administrator-and-developer-training-sydney) |

### **【1:n】主从关系**

主从关系是一种父子关系，其中主对象控制从属对象的行为。这是一个 1:n 的关系，父母只能有一个，但孩子可以有很多。在我的例子中， *学生数据* 是主对象， *标记* 是子对象。

让我给你举一个主从关系的例子。 *学生数据* 对象包含学生记录。每个记录都包含学生的个人信息。但是，学生获得的分数却存在于另一个名为 *的记录中* 。看下面 *标记* 对象的截图。

![master detail relationship - salesforce tutotial - edureka](img/6bb6dfe86691c2bff63aa4f55d9b486c.png)

我用学生的名字在这两个对象之间创建了一个链接。以下是在建立主从关系时你必须记住的几点。

*   作为控制对象，主字段不能为空。
*   如果主对象中的记录/字段被删除，相关对象中的相应字段也被删除。这称为级联删除。
*   从属字段将从其主字段继承所有者、共享和安全设置。

您可以定义两个自定义对象之间的主从关系，或者自定义对象和标准对象之间的主从关系，只要标准对象是关系中的主对象。

### 查找关系(1:n)

当您想要在两个对象之间创建一个链接，但不依赖于父对象时，使用查找关系。你可以认为这是一种亲子关系，只有一个父母，但有许多孩子，即 1:n 关系。以下是在建立查找关系时您必须记住的几点。

*   子对象上的查找字段不是必需的。
*   子对象中的字段/记录不能通过删除父对象中的记录来删除。因此，子对象中的记录不会受到影响。
*   子字段不会继承其父字段的所有者、共享和安全设置。

在我的例子中，查找关系的一个例子是一个 *学院* 对象。您可以在下面的截图中看到子对象: *学生数据* 。您会注意到第一条记录有一个空的 *学院* 字段。这表明依赖性不是必需的。

![lookup relationship - salesforce tutotial - edureka](img/0ce282a5c6f7ab039299a559a0d4ab35.png)

下面是两种关系的模式图截图。*学院-学生数据*形成查找关系，*学生数据-分数*形成主从关系。

![schema builder 1 - salesforce tutotial - edureka](img/a283e283d99387a5173e5fb4e100f934.png)

这是一种查找关系的形式，这种关系不是两个表/对象，而是在同一个表/对象中。因此得名自我关系。这里，查找引用了同一个表。这种关系也叫层级关系。

### **【多对多】结关系**

当需要创建两个主-细节关系时，这种关系可以存在。通过链接 3 个自定义对象，可以创建两个主-详细信息关系。这里，两个对象将是主对象，第三个对象将依赖于这两个对象。简单地说，它将是两个主对象的子对象。

为了举例说明这种关系，我创建了两个新对象。

*   一个大师的对象叫做。里面有教授的名单。
*   一个子对象叫做 *课程* 。它包含了可供选择的课程列表。
*   我将使用 *学生数据* 对象作为另一个主对象。

我创建了一个多对多的关系，使得*课程*对象中的每条记录必须至少有一个学生和一个教授。这是因为每门课程都是学生和教授的结合。事实上，一门课程可以有一个或多个学生和教授与之相关联。

依赖于 *学生* 和 *教授* 对象使得 *课程* 成为子对象。 *学生* 和 *教授* 都是由此而来的主人对象。下面是 *课程* 对象的截图。

![many to many relationship - salesforce tutotial - edureka](img/0e93d4bdbe516e7752295acf51cc9867.png)

你会注意到这些学科有不同的教授和学生组合。例如，Kate 与两门课程相关联，并且这两门课程中的每一门都有两位不同的教授。Mike 只与一门课程相关联，但是该课程有两个不同的教授。乔和凯特都与同一个课程和同一个教授有联系。在下面的截图中，你会发现这种关系的示意图。

![schema builder 2 - salesforce tutotial - edureka](img/a8db0a633f1dc680d3e74403aa0690ca.png)

祝贺你！成功构建了 *StudentForce* 应用。上面给出的两个架构图显示了不同对象在我的 Salesforce 应用程序中是如何链接的。

本 Salesforce 教程到此结束。我希望您理解在 Salesforce 教程博客中解释的各种概念，如应用程序、选项卡、简档、字段、对象和关系。如果你有任何疑问或疑问，请在下面的评论区留下，我会尽快回复你。

我强烈建议您观看这段解释 Salesforce 学生应用程序创建的 Salesforce 教程视频。继续，欣赏视频，告诉我你的想法。

**Salesforce 新手教程|学习创建 Salesforce App | Salesforce 培训| Edureka**

[//www.youtube.com/embed/IvhQKT48JcM?rel=0&showinfo=0](//www.youtube.com/embed/IvhQKT48JcM?rel=0&showinfo=0)

本 Salesforce 教程视频将帮助您学习如何从头开始创建 Salesforce 应用程序。这是关于创建 Salesforce 应用程序的一步一步的教程，非常适合初学者。

请继续阅读我们的 Salesforce 教程系列的下一篇博客。与此同时，我建议您创建一个 Salesforce 帐户，并试用 Salesforce 应用程序。你可以尝试按照上面提到的说明来构建自己的应用程序。

*如果您想成为销售队伍中的专业人员，请查看我们在哥伦布的 [销售队伍培训，该培训带有讲师指导的现场培训和真实项目体验。](https://www.edureka.co/salesforce-administrator-and-developer-training-columbus)*