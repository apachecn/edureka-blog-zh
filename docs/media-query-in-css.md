# 关于 CSS 中的媒体查询，您需要知道的一切

> 原文：<https://www.edureka.co/blog/media-query-in-css/>

本文将从 Web 开发的角度向您介绍一个重要的概念，即 [CSS](https://www.edureka.co/blog/what-is-css/) 中的媒体查询，并通过一个实际的演示来跟进。本文将涉及以下几点:

*   [CSS 中的媒体查询](#MediaQueryinCSS%20)
*   [识别的媒体类型类型](#TypesOfMediaTypesRecognized)
*   [定义行和列的媒体查询](#MediaQueryfordefiningrowsandcolumns)
*   [菜单媒体查询](#MediaQueryForMenus)
*   [媒体查询字体大小](#MediaQueryFontSize)
*   [画廊](#Gallery)
*   [ViewportSize](#ViewportSize)

继续这篇关于 CSS 中媒体查询的文章

随着技术的发展，我们遇到的是设备数量的指数增长。市场上充斥着各种不同属性的设备，比如设备类型和屏幕分辨率。对于不同的设备属性，也需要不同范围的代码来创建相同的响应式设计。

因此，使用 CSS3 的媒体查询，您可以为各种设备类型创建响应性设计，包括台式机、平板电脑、IOS 设备、Android 设备等等。这种查询通过明确提及设备类型和寻找特定媒体特征的零个或多个表达式来定义。通过定义颜色、宽度、高度等媒体查询，您可以根据设备类型定制需求。

在 CSS3 引入媒体查询之前，CSS2 已经定义了媒体规则，在这些规则中，您可以将各种媒体查询制成表格，以使布局对任何设备类型都有效且响应迅速。

但是使用 CSS3，你可以定义不完全依赖于设备的规则，而是根据它们的方向。喜欢定义规则为:

设备的宽度-设备支持的分辨率-设备的高度-设备的方向(纵向或横向)。 媒体查询是逻辑表达式，我们得到的回答要么是“真”，要么是“假”。如果提到的设备与打开文档的设备相匹配，则查询返回 true。

它让你更容易为不同的设备创建不同的布局。您只需为设备添加媒体类型和 条件，您的 CSS 设置将帮助您构建一个响应式设计布局。HTML4 中定义了媒体查询的语法。

**我们来举个例子:**

如果浏览器窗口为 500 像素或更小(最大宽度定义为 500 像素),则背景颜色为浅蓝色。

```
media only screen and (max-width: 500px) { 
body { 
background-color: lightblue; } 

```

媒体查询的条件应该为真才能应用。因此，如果你在一个宽度小于 500 像素的设备中打开一个文档，那么它的背景色将变成浅蓝色。

我们知道，在开发一个网站时，要让它在每种设备上都看起来不错，而不仅仅是在桌面上，这是一项相当大的努力。因此，通过 CSS3 的媒体查询属性，您可以使用@media type 做出令人惊叹的响应设计。

让我们举一个例子，在引入媒体类型之前它是什么样子。

左侧图像显示了我们未申请媒体类型属性时的文档视图。右边的图片显示了当我们在 CSS 文件中定义一个媒体查询时，视图发生了变化，变得更具可读性和视觉吸引力。您还可以使用“all”属性来提及隐含数据上的类似更改。您还可以为不同的设备使用不同的样式表。(.css)

继续这篇关于 CSS 中媒体查询的文章

## **识别的媒体类型类型**

1.  All:用于所有设备。
2.  盲文:用于盲文触觉设备
3.  手持式:适用于移动设备或具有较小屏幕的设备
4.  打印:用于在设备上以“打印预览”模式预览的文档。
5.  屏幕:用于彩色计算机屏幕
6.  投影:用于投影到屏幕上的演示文稿或文件。
7.  语音:对于支持语音的合成器
8.  电视:用于低分辨率的电视或设备

继续这篇关于 CSS 中媒体查询的文章

**那么，通过使用媒体查询，您还能做些什么呢？** 让我们使用简单的媒体查询规则来查看根据设备类型排列的各种属性:

**用于定义行和列**

在文档中创建行和列需要良好的格式。我们经常看到，当我们打开一个带有表格的文档时，当它在不同的设备上打开时会失真。因此，需要适当的格式来避免任何这种不匹配。因此，我们分配媒体查询规则，使其更好地定向。

```
media screen and (max-width: 767px){ 
.column { 
width: 100%; padding: 5px 20px; float: none; } .container .column:first-child{ 
margin-right: 0; margin-bottom: 20px; } 

```

当你这样做的时候，屏幕在不同的设备上看起来是不同的:

*添加断点:* 添加断点帮助你根据屏幕大小定义规则。添加断点时，可以更改断点两侧的规则。通过这种方式，您可以使它更好地适应不同的屏幕尺寸。

```
/* For desktop: */ .col-1 {width: 8.33%;} .col-2 {width: 16.66%;} .col-3 {width: 25%;} .col-4 {width: 33.33%;} .col-5 {width: 41.66%;} .col-6 {width: 50%;} .col-7 {width: 58.33%;} .col-8 {width: 66.66%;} .col-9 {width: 75%;} .col-10 {width: 83.33%;} .col-11 {width: 91.66%;} .col-12 {width: 100%;} 
@media only screen and (max-width: 768px) { 
/* For mobile phones: */ [class*="col-"] { width: 100%; } 

```

因此您可以使用上面的查询规则为各种设备定义 的行列模式。

继续这篇关于 CSS 中媒体查询的文章

**用于菜单**

即使是网站，我们也有一种菜单风格，需要在不同的设备中正确排列。比如桌面上的菜单样式是这样的:

然后，为了使它对移动设备友好，我们使用媒体查询来更好地浏览它。

```
/* The navbar container */ .topnav { 
overflow: hidden; background-color: #333; } /* Navbar links */ .topnav a { 
float: left; display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; } 
/* On screens that are 600px wide or less, make the menu links stack on top of each other instead of next to each other */ 
@media screen and (max-width: 600px) { 
.topnav a { 
float: none; 
width: 100%; } 

```

经过这次查询，移动设备中的导航栏从 变成了这样一个相当容易访问的导航栏:

继续这篇关于 CSS 中媒体查询的文章

**字体大小**

现在，随着屏幕尺寸的不同和变化，字体大小也会随之变化。在手机上看起来可读的字体大小在桌面上可能要小一些。因此，我们需要相应地改变字体大小。为了救急，通过定义媒体查询条件，还可以设置字体大小。

```
@media screen and (max-width: 780px) { 
div.example { 
font-size: 40px; }

```

现在，当在 条件成立的任意设备中打开文档时，字体大小变为 40 px。

继续这篇关于 CSS 中媒体查询的文章

**画廊**

即使图库中的图像结构也因屏幕尺寸、打印分辨率类型或方向而异。因此，使用 CSS3 的媒体类型，您还可以通过改变结构来管理图像库。

继续这篇关于 CSS 中媒体查询的文章

**Viewport Size**

视窗尺寸被定义为提供最佳的观看体验。因此，当您定义媒体查询规则时，您可以更改屏幕的宽度、分辨率或任何与设备相关的方向。例如，如果视窗宽度小于 768 像素，它将覆盖 100%的视窗宽度，但如果视窗宽度大于 768 像素且大于 1024 像素，它将是 750 像素，依此类推。

```
/* ##Device = Desktops ##Screen = 1281px to higher resolution desktops */ @media (min-width: 1281px) 
{ //CSS } /* ##Device = Laptops, Desktops ##Screen = B/w 1025px to 1280px */ @media (min-width: 1025px) and (max-width: 1280px) { //CSS }
 /* ##Device = Tablets, Ipads (portrait) ##Screen = B/w 768px to 1024px */
 @media (min-width: 768px) and (max-width: 1024px) 
{ //CSS } /* ##Device = Tablets, Ipads (landscape) ##Screen = B/w 768px to 1024px */ 
@media (min-width: 768px) and (max-width: 1024px) and(orientation: landscape) { //CSS } 
/* ##Device = Low Resolution Tablets, Mobiles (Landscape) ##Screen = B/w 481px to 767px 
*/ @media (min-width: 481px) and (max-width: 767px) { //CSS }
 /* ##Device = Most of the Smartphones Mobiles (Portrait) ##Screen = B/w 320px to 479px */ 
@media (min-width: 320px) and (max-width: 480px) { //CSS

```

最近，美国的 已经实现了自动化设计技术的极限水平。让你的品牌名称可以在任何设备上被访问是很好的。你不能仅仅因为你没有为一个设备很好地定位网站而失去一个客户。所以，试着使用 CSS3 的媒体 查询，让你的网站在所有设备上都有足够的响应能力，而不用改变任何代码或内容。