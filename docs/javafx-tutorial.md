# JavaFX 教程:如何创建应用程序？

> 原文：<https://www.edureka.co/blog/javafx-tutorial/>

JavaFX 是一个 Java 平台，用于创建可以在多种设备上运行的富互联网应用程序(RIA)。它旨在取代 Java 应用中的 [Swing 作为 GUI 框架。此外，它提供了比 Swing 更多的功能。JavaFX 是用于 Java 平台](https://www.edureka.co/blog/java-swing/)的下一代 GUI 工具包。听起来很有趣？在这篇 JavaFX 教程中，让我们详细探讨一下这个概念。

*   [什么是 JavaFX？](#javafx)
*   [JavaFX 架构](#architecture)
*   [Java FX 应用的剖析](#application-anatomy)
*   [创建 JavaFX 应用程序](#javafx-application)

## **什么是 JavaFX？s**

JavaFX 是一个 Java 库，用于设计、创建、测试和部署跨平台 GUI 应用程序和富互联网应用程序(RIA ),它们可以在各种设备上运行。

*   创建 JavaFX 的一个动机是取代 Swing。此外，JavaFX 在设计上比 Swing 更加一致。
*   它有更多的功能，也更现代，使你能够使用布局文件(XML)设计 GUI，并用 [CSS](https://www.edureka.co/blog/what-is-css/) 设计它们。
*   JavaFX 还将 2D + 3D 图形、图表、音频、视频和嵌入式 web 应用集成到一个连贯的 GUI 工具包中。

***注:**富互联网应用是那些提供与桌面应用相似的功能和体验的网络应用。与普通的 web 应用程序相比，它们为用户提供了更好的视觉体验。*

现在您已经知道 JavaFX 到底是什么了，请在本 JavaFX 教程的下一部分中查看它的体系结构部分。

## **JavaFX 架构**

JavaFX 有各种内置组件，这些组件相互连接。它包含了一组丰富的 API，这些 API 对于开发在许多平台上一致运行的富互联网应用程序来说绰绰有余。下图显示了 JavaFX API 的体系结构。

![Architecture - JavaFX Tutorial - Edureka](img/40e28443661fc414ebb87ca23f140950.png)

让我们详细探讨一下这些组件。

### **场景图**

场景图是构建 JavaFX 应用的起点。这是一个层次化的[树](https://www.edureka.co/blog/java-binary-tree)，它代表了应用程序用户界面的所有可视元素。场景图中的单个元素称为节点。每个节点要么是分支节点，要么是叶节点。分支节点可以包含其他节点，就像它们的子节点一样，但是叶节点不包含其他节点。树中的第一个节点称为*根节点。*根节点没有父节点。

***javafx.scene*** 包中有各种类，用于在节点上创建、修改和应用一些变换。

### **图形引擎**

JavaFX 图形引擎为场景图形组件提供图形支持。它通常支持 2D 和 3D 图形。当系统上的图形硬件不支持硬件加速渲染时，也提供软件渲染。

JavaFX 中的两个图形加速管道是:

*   prism–It是一款经过硬件加速的高性能显卡，可以渲染 2D 和 3D 图形。
*   quantum Toolkit–用于将 prism 和 glass windowing tool kit 绑定在一起，并使它们可用于堆栈中的以上层。

### **玻璃开窗工具包**

它是一个平台相关层，将 JavaFX 平台连接到本机操作系统。它提供本机操作系统服务，如管理窗口、事件、计时器和表面。

### **媒体和网络引擎**

*   Web Engine–It是一个 web 浏览器引擎，用于将 [HTML](https://www.edureka.co/blog/what-is-html/) 内容嵌入到 JavaFX 场景图中。支持 HTML5、CSS、[、JavaScript](https://www.edureka.co/blog/what-is-javascript/) 、DOM、SVG。
*   媒体引擎——It提供了创建媒体应用程序的工具，这些应用程序可以在支持平台的桌面窗口或网页中播放媒体。JavaFX **媒体引擎**基于一个被称为**流媒体工具**的开源引擎。它支持视频和音频内容的播放。

这些是支持 JavaFX API 的组件。本 JavaFX 教程的下一部分是关于 JavaFX 应用程序结构的。

## **Java FX 应用的剖析**

JavaFX 应用程序按层次划分为三个主要组件:舞台、场景和节点。

![Application Structure - JavaFX Tutorial - Edureka](img/0af6fa8b727a2a7e1b22c73c4b4cd6a0.png)

### **阶段**

它是应用程序的主容器和入口点。它代表主窗口，创建的 stage 对象作为参数传递给***start()***方法的 ***Application*** 类。一个载物台有两个参数，**宽度，**和**高度，**决定了位置，即 。

有五种类型的阶段可用

*   盛饰建筑的
*   未加装饰的
*   透明的
*   统一的
*   效用

你要调用**【show()】**方法来显示一个阶段的内容。

### **场景**

*场景*是舞台视觉内容的容器。它包含 UI 元素，比如图像视图、按钮、网格、文本框。 **Javafx.scene.Scene** 包 **的类 javafx.scene** 提供了所有处理场景对象的方法。您可以通过创建**场景**类对象并将布局对象传递到场景类构造函数来创建场景。

### **场景图&节点**

它存在于层次结构的最低级别。**场景图**是代表场景内容的树状数据结构(分层)。你可以把它想象成各种节点的集合。基本上。**节点**是场景图形的可视/图形对象。 包 **javafx.scene** 的 **节点** 类表示 javafx 中的单个节点，该类是所有节点的超类。

现在您已经详细了解了 JavaFX 应用程序的结构，让我们在本 JavaFX 教程中通过一个示例来学习如何创建一个 JavaFX 应用程序。

## **创建 JavaFX 应用程序**

让我们看看如何在 IDE Eclipse 上执行 J **avaFX** 编程。你需要做的第一件事是为 Eclipse IDE 安装 ***e(fx)clipse*** 插件。e(fx)clipse 是一套工具和必要的库，可以帮助你执行 JavaFX 编程。

在这里，我们创建了一个简单的 JavaFX 应用程序，它打印了**欢迎来到 Edureka！控制台上的** 点击了舞台上显示的按钮。

```
package application;
import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        Button btn = new Button();
        btn.setText("Say 'Welcome to Edureka!'");
        btn.setOnAction(new EventHandler<ActionEvent>() {

            @Override
            public void handle(ActionEvent event) {
                System.out.println("Welcome to Edureka!");
            }
        });

        StackPane root = new StackPane();
        root.getChildren().add(btn);
        Scene scene = new Scene(root, 300, 250);
        primaryStage.setTitle("Hello World!");
        primaryStage.setScene(scene);  
        primaryStage.show();
    }
    public static void main(String[] args) {
        launch(args);
    }

}
```

**输出:**

![Botton - JavaFX Tutorial - Edureka](img/9214d53f37e19d494ef1607445d542dc.png)

```
Welcome to Edureka!
```

### **JavaFX 应用示例程序说明**

让我们试着用简单的步骤来理解这个示例程序是如何工作的。

**步骤 1:** 扩展 javafx.application.Application 并覆盖 start()方法

正如我们前面讨论的， *start()* 方法是 JavaFX 应用程序的起点。导入**Java FX . application . application**来覆盖 start()方法。覆盖 start()方法并传递给它一个类 **javafx.stage.Stage.** 的 o 对象

```
@Override
    public void start(Stage primaryStage)
```

第二步:创建一个按钮

可以通过实例化**Java FX . scene . control . button**类来创建按钮。因此，将相关的类导入代码。在按钮类构造函数中传递按钮标签文本。

```
 Button btn = new Button();
```

第三步:为按钮创建一个事件

这个示例应用程序在按钮上打印事件的文本。因此，您需要为按钮创建一个事件。为此，调用按钮上的**【setOnAction()**，并定义一个匿名类事件处理程序作为该方法的参数。在这个匿名类中，定义一个方法句柄()。查看 handle()方法的代码。

```
btn.setText("Say 'Welcome to Edureka!'");
        btn.setOnAction(new EventHandler<ActionEvent>() {

            @Override
            public void handle(ActionEvent event) {
                System.out.println("Welcome to Edureka!");
            }
```

**步骤 4:** 创建一个布局并将按钮添加到其中

JavaFX 通常提供多种布局。实现其中的一个，以便正确地可视化小部件。你需要添加按钮，文本等其他节点。到这个布局。

```
StackPane root = new StackPane();
        root.getChildren().add(btn);
```

第五步:创建场景

场景在 JavaFx 应用程序结构的层次中处于较高的级别。因此，您需要将您的布局添加到场景中。您可以创建它的实例化 **javafx.scene.Scene** 类，并将布局对象传递给场景类构造函数。

```
Scene scene = new Scene(root, 300, 250);
```

第五步:准备舞台

舞台是应用程序的主要容器和入口点。使用 **javafx.stage.Stage** 类提供的方法为 stage 设置一些属性。使用 show()方法显示舞台。这是代码。

```
 primaryStage.setTitle("Hello World!");
        primaryStage.setScene(scene);  
        primaryStage.show();
```

**步骤 6:** 创建主方法

最后一步，创建一个 main 方法，您将在其中启动应用程序，即调用 launch()方法，并向其传递命令行参数(args)。

```
public static void main(String[] args) {
        launch(args);
    }
```

**Step7:** 运行应用程序，查看输出。

为了使它更有趣，您可以通过应用自定义设计(如 HTML 和 CSS)来更改 JavaFX 应用程序的 UI。

本 JavaFX 教程到此结束。我们研究了 JavaFX 应用程序的内部结构，了解了其架构、生命周期和组件的关键功能。我们还了解了如何创建一个简单的 GUI 应用程序。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这个 JavaFX 教程*T3 的评论部分提到它，我们会尽快回复你。