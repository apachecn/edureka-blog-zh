# r 闪亮教程:你需要知道的一切

> 原文：<https://www.edureka.co/blog/r-shiny-tutorial/>

随着技术的发展，出现了更新的工具和框架来构建显示实时统计数据、地图和图表的 web 应用程序。由于这些功能需要高度的处理和同步，所以使用编程语言来减少服务器加载时间。在这篇 R 闪亮的教程中，我将解释如何在动态 web 应用程序中充分利用 R。T2T4

我们将涵盖并理解以下主题:

## **什么是 R 闪亮？**

Shiny 是一个 R 包，允许用户构建交互式网络应用。这个工具从闪亮的代码中创建一个相当于 HTML 的 web 应用程序。我们将原生 HTML 和 CSS 代码与 R Shiny 函数集成在一起，使应用程序变得可展示。Shiny 结合了 R 的计算能力和现代网络的交互性。 Shiny 使用您的服务器或 R Shiny 的托管服务创建部署在 web 上的 web 应用程序。

## **R 闪亮的特点:**

*   用基本的或没有 web 工具知识创建简单的应用程序
*   将 Shiny 与本地 web 工具集成，以提高灵活性和生产率
*   预建的 I/O 和渲染功能
*   无需多次重新加载即可轻松呈现应用内容
*   添加来自 R 脚本的计算(或处理)输出的特性
*   添加实时报告和可视化效果。

这就引出了一个问题:

## **Shiny 与传统应用有什么不同？**

让我们以一个天气应用程序为例，每当用户刷新/加载页面或更改任何输入时，它应该使用 JS 更新整个页面或部分页面。这增加了服务器端的处理负载。Shiny 允许用户隔离或渲染(或重新加载)应用程序中的元素，从而减少服务器负载。在传统的网络应用程序中滚动页面很容易，但在闪亮的应用程序中却很难。代码的结构在理解和调试代码中起主要作用。相对于其他应用程序，这一功能对于闪亮的应用程序至关重要。

让我们进入 R Shiny 教程的下一个主题，安装 R Shiny 包。

## **安装 R 闪亮**

安装 Shiny 就像在 R 中安装任何其他包一样。转到 **R 控制台**并运行下面的命令来安装 Shiny 包。

```
install.packages("shiny")
```

`![Install R Shiny - R shiny tutorial - Edureka](img/1b6f3be46aa65c73ecdcd6d30e46553f.png)`

安装完成后，加载闪亮的软件包来创建闪亮的应用程序。

```
library(shiny)
```

在我们继续学习 R shiny 教程之前，让我们先来看看并理解一个 shiny 应用程序的结构。

## **闪亮 app 的结构**

闪亮由 3 部分组成:

1.  [用户界面](#userinterface)
2.  [服务器](#server)
3.  [ShinyApp](#shinyApp)

### **1。 用户界面功能**

**用户界面** (UI)函数定义了 app 的布局和外观。您可以在应用程序中添加 CSS 和 HTML 标签，使应用程序更加美观。该函数包含应用程序中显示的所有输入和输出。应用程序中的每个元素(部门、选项卡或菜单)都是使用函数定义的。像 HTML 元素一样，使用唯一的 id 来访问它们。让我们进一步了解一下应用中使用的各种 功能。

#### **闪亮的布局功能**

*   `headerPanel()` 给 app 添加标题。 **titlePanel()** 定义了 app 的副标题。为了更好地理解**标题面板**和**标题面板**，请参见下图。 **![](img/a0fec03ac2406a8e00e64abfc29b3abc.png)** 

*   `SidebarLayout()` 定义布局来容纳 **边栏**和  **主面板**元素。布局将 app 屏幕分为侧边栏面板和主面板 。例如，在下图中，红色矩形是**主面板**区域，黑色矩形垂直区域是**侧栏面板**区域。

**![](img/2f1e2659e316b49437185e8c869f698b.png)**

*   `wellPanel()` 定义一个容器，在同一个网格中保存多个对象 app 输入/输出对象。
*   `tabsetPanel()` 创建一个容器来保存标签。 **tabPanel()** 通过定义 tab 元素和组件将 tab 添加到 app 中。在下图中，黑色的矩形是 **tabsetPanel** 对象，红色的矩形是**tabspanel**对象。![](img/bcc934278e23d9232083dad09381309d.png)
*   `navlistPanel()` 提供了一个侧菜单，链接到不同的选项卡面板，类似于 **tabsetPanel()** ，就像屏幕左侧的垂直列表。在下图中，黑色矩形是 **navlistPanel** 对象，红色矩形是 **tabPanel** 对象。

![layout - R Shiny tutorial - Edureka](img/bae10ad668829f057e0f612209876ea7.png)

除了闪亮的布局功能，你还可以在应用程序的每个输入部件中添加内嵌 CSS。 闪亮的应用融合了网络技术的特点以及闪亮的特性和功能来丰富应用。在闪亮的应用程序中使用 HTML 标签，使用**标签$ <标签名称>。**

你的布局已经准备好了，是时候把小部件添加到应用程序中了。Shiny 为用户交互提供了各种用户输入和输出元素。让我们讨论几个输入和输出函数。

#### **闪亮的输入功能**

每个输入小部件都有一个标签、Id 和其他参数，如 choice、value、selected、min、max 等。

*   `selectInput()`–创建一个下拉 HTML 元素。

```
selectInput("select", h3("Select box"), choices = list("Choice 1" = 1,
 "Choice 2" = 2, "Choice 3" = 3), selected = 1)
```

![SelectInput - R Shiny tutorial - Edureka](img/878a9b3d773ba64ec4b766b27cd3e32b.png)

*   `numericInput()`–输入区域，用于输入数字或文本。

```
dateInput("num", "Date input", value = "2014-01-01")
numericInput("num", "Numeric input", value = 1)
textInput("num", "Numeric input", value = "Enter text...")
```

![Input widgets - R Shiny tutorial - Edureka](img/cf6abb64377e334ea1913a9e178507ce.png)

*   `radioButtons()`–为用户输入创建单选按钮。

```
radioButtons("radio", h3("Radio buttons"), choices = list("Choice 1" = 1,
"Choice 2" = 2,"Choice 3" = 3),selected = 1)
```

![RadioButon | R Shiny tutorial | Edureka](img/2ce8b986b5d36a300b00f171f6e2c23e.png)

#### **闪亮的输出功能**

Shiny 提供各种显示 **R** 输出的输出功能，如显示相应 **R** 对象的绘图、图像、表格等。

*   `plotOutput()`–显示 R 绘图对象。

```
plotOutput"top_batsman")
```

*   `tableOutput()`–将输出显示为表格。

```
tableOutput"player_table")
```

#### **2。服务器功能**

**服务器**功能 d 定义闪亮应用的服务器端逻辑。它包括创建使用输入产生各种输出的函数和输出。每个客户端(web 浏览器)在第一次加载闪亮的应用程序时都会调用服务器函数。每个输出存储渲染函数的返回值。

这些函数捕获一个 R 表达式，并对表达式进行计算和预处理。使用与正在定义的输出相对应的 render*函数。我们使用**input $【widget-id】**来访问输入小部件 。这些输入变量是反应值。使用输入变量创建的任何中间变量需要使用 **reactive({ })** 进行反应。使用( )访问变量。

**render** *函数在服务器函数内部执行计算，并存储在输出变量中。输出需要用 **output$【输出变量名】**保存。每个**渲染** *函数都有一个参数，即一个用大括号{ }括起来的 R 表达式。

### **3。ShinyApp 功能**

`shinyApp()`函数是应用的核心，它调用 **UI** 和**服务器**函数来创建一个闪亮的应用。

下图显示了闪亮应用的轮廓。

**![](img/c525aa75ba514cffa3a889f539d52a53.png)**

让我们进入 R Shiny 教程的下一部分，创建第一个 R Shiny 应用程序。

**创建一个闪亮的网络项目**

进入**文件**，在任意目录下创建**新项目**->-**闪亮 Web 应用** -【闪亮应用目录名称】。输入目录名，点击**确定**。

每个新的 shiny 应用程序项目都将包含一个直方图示例，以了解 Shiny 应用程序的基础知识。直方图应用程序包含一个滑块，后跟一个直方图，该直方图会根据滑块的变化更新输出。下面是直方图应用程序的输出。

![Histogram App | R shiny tutorial | Edureka](img/9f739958c55f734bafbdc9aba76ab873.png)

要运行闪亮的应用程序，点击源代码窗格右上角的 **运行应用程序** 按钮。闪亮的应用程序显示一个滑块小部件，它将 bin 的数量作为输入，并根据输入呈现直方图。

![R shiny totorial | Edureka](img/c6dd44db6e581cf9edfa227af51e79bb.png)

既然你已经了解了这个闪亮应用的结构和运行方式。让我们继续创建我们的第一个闪亮的应用程序。

## **打造第一款闪亮的应用**

您可以创建一个新项目，也可以在同一个工作目录中继续。在这个 R Shiny 教程中，我们将创建一个简单的 Shiny 应用程序来显示 IPL 统计数据。app 使用的数据集可以在这里 下载 [。数据集由两个文件组成， **deliveries.csv** 包含每个球(满场)击球手、投球手、跑垒手的得分交付详情，而 **matches.csv** 文件包含比赛详情，如比赛地点、掷球、场地&比赛详情。下面的 app 需要有 **dplyr** 和**gg plot**](https://www.kaggle.com/nowke9/ipldata)和的基础知识才能理解下面的教程。

按照以下步骤创建你的第一个闪亮应用。

**第一步** : **打造一个闪亮 app 的轮廓。**

清除除了**应用**中的函数定义之外的现有代码。 **R** 档。

![Outline | R shiny tutorial | Edureka](img/d2c9290503ddaf68d605b6da77cab6a2.png)

**第二步** : **加载库和数据。**

在这一步，我们加载所需的包和数据。然后，清理提取的数据并将其转换成所需的格式。在 **UI** 和**服务器**功能前添加以下代码。

#### **代码:**

```
library(shiny)
library(tidyverse)
# Loading Dataset-------------------------------------------------------
deliveries = read.csv("C:UsersCherukuri_SindhuDownloadsdeliveries.csv",
       stringsAsFactors = FALSE)
matches = read.csv("C:UsersCherukuri_SindhuDownloadsmatches.csv",
       stringsAsFactors = FALSE)
# Cleaning Dataset------------------------------------------------------
names(matches)[1] = "match_id"
IPL = dplyr::inner_join(matches,deliveries)
```

**说明**:

前 2 行装载 **tidyverse** 和**闪亮**包。接下来的两行加载数据集交付和匹配，并存储在变量`deliveries`和`matches`中。最后两行更新了`matches`数据集的列名，以执行与`deliveries`表的内部连接。我们将连接结果存储在`IPL`变量中。

**第三步** : **创建闪亮 app 的布局**。

如前所述， **UI** 函数定义了闪亮应用的外观、窗口小部件和对象。下面同样详细讨论。

**代码**

```
ui <- fluidPage(
   headerPanel("IPL - Indian Premier League"),
   tabsetPanel(
     tabPanel(title = "Season",
       mainPanel(width = 12,align = "center",
       selectInput("season_year","Select Season",choices=unique(sort(matches$season,
       decreasing=TRUE)), selected = 2019),
       submitButton("Go"),
       tags$h3("Players table"),
       div(style = "border:1px black solid;width:50%",tableOutput("player_table"))
)),
     tabPanel(
       title = "Team Wins & Points",
       mainPanel(width = 12,align = "center",
       tags$h3("Team Wins & Points"),
       div(style = "float:left;width:36%;",plotOutput("wins_bar_plot")),
       div(style = "float:right;width:64%;",plotOutput("points_bar_plot"))
)
)))
```

**UI** 函数包含一个 **headerPanel()** 或 **titlePanel()** ，后跟 **tabsetPanel** 来定义应用中的多个选项卡。 **tabPanel()** 分别为每个选项卡定义对象。每个 **tabPanel()** 由 title 和 **mainPanel()组成。mainPanel()** 创建一个宽度为 12 的容器，即整个窗口，并在中心对齐输入和输出对象。

#### **解释**

该应用程序由两个选项卡组成:**赛季**和**队赢得&积分。**

页签由**选择输入** ( **)** 、提交按钮和一个表格组成。season_year 用于从 l 值列表中读取输入。 **tableOutput()** 显示在服务器函数上计算的表格输出。 Table player_table 显示在服务器功能中定义的按钮下方，这将在下一步中讨论。**团队获胜&积分**选项卡在各自的条形图中显示团队获胜和积分。 **plotOutput()** 显示渲染 ***** 函数返回的输出。所有的输出、输入函数都包含在一个 div 标签中，以增加内联样式。

现在我们已经熟悉了 ui 函数，让我们在 R Shiny 教程中继续理解和使用服务器函数。

### **第四步:添加服务器函数语句**

**服务器**功能包括创建函数和 output，它们使用用户输入来产生各种输出。下面逐步解释服务器功能。

```
matches_year = reactive({ matches&nbsp;%>% filter(season == input$season_year) })
playoff = reactive({ nth(sort(matches_year()$match_id,decreasing = TRUE),4) })
matches_played = reactive({ matches_year()&nbsp;%>% filter(match_id < playoff()) }) t1 = reactive({ matches_played()&nbsp;%>% group_by(team1)&nbsp;%>% summarise(count = n()) })
t2 = reactive({ matches_played()&nbsp;%>% group_by(team2)&nbsp;%>% summarise(count = n()) })
wl = reactive({ matches_played()&nbsp;%>% filter(winner&nbsp;!= "")&nbsp;%>% group_by(winner)&nbsp;%>% 
summarise(no_of_wins = n()) })

wl1=reactive({ matches_played()&nbsp;%>% group_by(winner)&nbsp;%>% summarise(no_of_wins=n()) })
tied = reactive({ matches_played()&nbsp;%>% filter(winner == "")&nbsp;%>% select(team1,team2) })
playertable = reactive({data.frame(Teams = t1()$team1,Played=t1()$count+t2()$count,
Wins = wl()$no_of_wins,Points = wl()$no_of_wins*2)})
```

上面的代码过滤每年季后赛前的比赛，并将结果存储在 matches_played 变量中。表格包含全队比赛统计数据，即比赛次数、胜场数和积分。变量`matches_played`、`player_table`、`t1`、`tied`等都是中间**无功值**。这些变量需要使用( )来访问，如上面的代码所示。`player_table`使用 renderTable 函数显示。接下来，创建输出变量来存储 playertable。

```
output$player_table = renderTable({ playertable() })
```

现在，让我们创建条形图来显示每个团队在本赛季的胜场和得分。以下代码使用 ggplot 显示条形图。 **renderPlot()** 获取 ggplot 对象并将结果存储在变量`wins_bar_plot`中。ggplot 代码是不言自明的，它涉及基本的图形和映射功能，以编辑图例，标签和绘图。

```
output$wins_bar_plot = renderPlot({ ggplot(wl1()[2:9,],aes(winner,no_of_wins,fill=winner))+
geom_bar(stat = "identity")+ theme_classic()+xlab("Teams")+ ylab("Number Of Wins")+theme(
axis.text.x=element_text(color="white"),legend.position = "none",axis.title=element_text(
size=14),plot.background=element_rect(colour="white"))+geom_text(aes(x=winner,(no_of_wins+0.6),
label = no_of_wins,size = 7)) })

output$points_bar_plot = renderPlot({ ggplot(playertable(),aes(Teams,Points,fill=Teams))+
geom_bar(stat = "identity",size=3)+theme_classic()+theme(axis.text.x=element_text(
color = "white"),legend.text = element_text(size = 14),axis.title = element_text(size=14))+
geom_text(aes(Teams,(Points+1),label=Points,size = 7)) })
```

### **第五步:运行闪亮的 app。**

点击跑步应用程序。成功运行后，您闪亮的应用程序将如下所示。任何与应用程序相关的错误或警告都会显示在 R 控制台上。

**表 1–季节**

![R shiny App | R shiny Tutorial | Edureka](img/a8e3c138492f5256e59e128a29249cda.png)

**tab 2–团队赢得&积分**

![](img/b5df8f7076f6cf7974704870fedfa02d.png)

让我们看看如何设置 Shinyapps.io 帐户来部署您的闪亮应用。

**设置 Shinyapps.io 账户**

转到[Shinyapps . io](https://www.shinyapps.io/)用你的信息登录，然后给页面一个唯一的帐户名并保存。成功保存后，您将看到从 R 控制台部署应用程序的详细过程。按照以下步骤在 Rstudio 中配置您的帐户。

### 第一步。**安装 rsconnect**

```
install.packages('rsconnect')
```

### 第二步。**授权账户**

必须使用令牌和密码将 **rsconnect** 包授权到您的帐户。为此，在 **R** 控制台的仪表板页面中复制如下所示的整个命令。一旦您在 R 中成功地输入了命令，我现在授权您将应用程序部署到您的 Shinyapps.io 帐户。

```
rsconnect::setAccountInfo(name='account name',token='token',
              secret="secret")
```

#### 第三步。**部署应用**

使用下面的代码来部署闪亮的应用程序。

```
library(rsconnect)
rsconnect::deployApp('path/to/your/app')
```

设置完成后，您就可以开始部署闪亮的应用了。

现在你已经学会了如何创建和运行闪亮的应用程序，按照上面的解释将我们刚刚创建的应用程序部署到 Shinyapps.io 中，或者点击位于闪亮的应用程序窗口右上角的 **publish，**。

我希望这个 R 闪亮教程能帮助你学习如何创建和运行一个闪亮的应用程序。使用闪亮的 R 创建互动和美丽的网络应用程序很有趣。

*如果你希望学习 R 编程并在数据分析领域建立丰富多彩的职业生涯，那么就来看看我们的 [**【使用 R**](https://www.edureka.co/r-for-analytics) 进行数据分析，它附带有讲师指导的现场培训和真实的项目经验。本培训将帮助您理解数据分析，并帮助您掌握该主题。*