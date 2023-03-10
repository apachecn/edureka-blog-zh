# Android 中基于位置的服务——第 1 部分

> 原文：<https://www.edureka.co/blog/location-based-services-in-android/>

我相信，如果我们对某个特定主题的概念很清楚，那么不需要花太多时间就能理解如何玩弄这个概念。所以，让我们先从概念开始，然后我们将处理实际的代码开发。

### **Android 中基于位置的服务——概念**

在 Android 中，我们有一种叫做“T0”的基于位置的服务“T1”。Android 通过其位置框架提供基于位置的服务。该框架提供了一个位置 API，它由特定的类和接口组成。这些类和接口是允许我们在 Android 中开发基于位置的应用程序的关键组件。

**位置服务的类别和接口:**

**LocationManager** – This class helps to get access to the location service of the system. **LocationListener** – This interface acts as the listener which receives notification from the location manager when the location changes or the location provider is disabled or enabled. **Location** – This is the class which represents the geographic location returned at a particular time.

*这些 android 内置组件让我们更容易获得用户位置。在这篇博文中，我们将介绍检索用户位置需要遵循的步骤。*

### **第一步**

作为这个过程的第一步，需要创建 LocationManager 的一个实例。这是一个主类，应用程序通过它访问 Android 中的定位服务。对这个系统服务的引用可以通过调用 **getSystemService()** 方法获得。

location manager***location manager***=(location manager)getsystem service(Context。***LOCATION _ SERVICE***)；

### **第二步**

下一步是确定您希望用来检索位置详细信息的位置提供者。位置提供商实际上在 Android 中提供位置数据。Android 公开了两个主要的位置提供商:

#### 1.GPS 位置提供商:

*该位置提供商提供最高精度的位置数据(约 2 米–20 米)。位置更新通过卫星提供。然而，这个提供者有一些缺点，解释如下:*

A.它比网络提供商获得与卫星的初始连接设置慢得多。这种初始连接也称为首次定位时间(TTFF ),可能非常慢，但一旦连接建立，位置更新就非常快。

B.GPS 提供商也首先耗尽电池。因此，明智地使用这个提供程序非常重要。应特别注意确保在不使用时将其关闭。

C.第三个缺点是 GPS 使用的无线电信号会被固体物体阻挡。因此，如果你在建筑物内或地下室，GPS 提供者将无法工作。

#### 2.网络提供商:

*该提供商使用 Wi-Fi 热点和手机信号塔来估算位置。提供商通过使用 Wi-Fi 热点和蜂窝塔的 id 查询 Google 定位服务器来检索大概的位置。定位精度在 100-1000 米之间。定位精度与该地区可用的 Wi-Fi 热点和手机信号发射塔的数量成正比。*

您可以使用下面这段代码来检查提供程序的可用性:

**isGpsEnabled** = **mLocManager**.isProviderEnabled(LocationManager.***GPS_PROVIDER***); **isNetworkEnabled = mLocManager**.isProviderEnabled(LocationManager.***NETWORK_PROVIDER***);

### **第三步**

下一步是向位置管理器注册一个位置监听器。注册可以通过调用方法 **requestLocationUpdates 来完成((String provider，long minTime，float minDistance，LocationListener listener)。**

#### 以下是传递给此方法的参数:

**provider:** the name of the provider with which to register. This can be either GPS or Network provider.**minTime:** minimum time interval between location updates, in milliseconds.**minDistance:** minimum distance between location updates, in meters.**listener:** a LocationListener whose onLocationChanged(Location) method will be called for each location update.

当移动设备移动的距离大于 minDistance 或自上次位置更新以来的时间超过 minTime 时，位置管理器调用监听器的 onLocationChanged()。

**Android 中基于位置的服务——代码**

我们刚刚复习了一些基于 Android 定位服务的基本概念。现在让我们学习如何运用这些概念！

#### 1.先决条件:

*   应该了解如何在仿真器中测试基于位置的服务——通过仿真器；您可以通过模拟器控件设置模拟位置。为此，在模拟器控件中，键入纬度和经度，然后点击“**发送**按钮。这将设置模拟器的模拟位置。

[![Location based services](img/db99df37160a7599435af70138a623c9.png)](https://www.edureka.co/blog/location-based-services-in-android/)

*   Android 中基于位置的服务所需的权限——在 Android 清单文件中，您需要指定 **3 权限**,如下所述:

<uses-permissionandroid:name=”android.permission.ACCESS_COARSE_LOCATION”/> <uses-permissionandroid:name=”android.permission.ACCESS_FINE_LOCATION”/> <uses-permissionandroid:name=”android.permission.INTERNET”/>

对于**基于 GPS 的位置**，您只需要“**Android . permission . ACCESS _ FINE _ LOCATION**”对于**基于网络的位置**，您只需要“**Android . permission . ACCESS _ FINE _ LOCATION**”如果您同时使用两个提供者，您只需要请求 **ACCESS_FINE_LOCATION** 权限，它包括对两个提供者的权限。

#### 2.布局:

如果我们从应用程序项目的布局/用户界面开始，理解应用程序总是很容易的。该示例应用程序的布局如下所示:

[![Layout](img/3ad31ca2255299e29dec3d7bf1c7fb7f.png)](https://www.edureka.co/blog/location-based-services-in-android/)

**它有 4 个视图:**

1 – This is the label for the latitude. 2 – This text view will be populated with the latitude of the location. 3 – This is the label for the longitude. 4 – This text view will be populated with the longitude of the location. On click of this button the latitude and longitude will be retrieved and populated in their respective text views.

#### 3.代码:

***现在让我们来看看重要的代码片段:***

**MainActivity 类**实现位置监听器。这个类将被用作监听器，位置管理器将向这个监听器注册自己。

publicclassMainActivityextends 活动实现了 LocationListener，OnClickListener{

在 OnCreate()方法中，我做了两件重要的事情:

1.通过调用 sodystem 服务 metmloc manager =(location manager)getsystem service(Context)获取位置管理器的实例。位置 _ 服务)；

2.检查启用了哪个位置提供程序

isGpsEnabled = mLocManager.isProviderEnabled(LocationManager.GPS_PROVIDER); isNetworkEnabled = mLocManager.isProviderEnabled(LocationManager.NETWORK_PROVIDER);

下面是我在按钮视图的 OnClick 方法中的逻辑。当单击按钮时，我检查哪个提供者被启用。如果启用了 GPS，我使用 GPS provider 向位置监听器(这是 MainActivity 类的这个实例)注册位置管理器，否则我使用 Network Provider。这部分是关键。当调用 requestLocationUpdates 方法时，它将依次调用 onLocationChanged 方法，并将 location 对象传递给该方法。

```
</pre>

@Override
 publicvoidonClick(View v) {
 // TODO Auto-generated method stub
 int id = v.getId();

switch (id) {
 caseR.id.btGetLocation:
 if(isGpsEnabled)
 {
 mLocManager.requestLocationUpdates(LocationManager.GPS_PROVIDER, 30000, 10, MainActivity.this);
 } elseif(isNetworkEnabled)
 {

mLocManager.requestLocationUpdates(LocationManager.NETWORK_PROVIDER, 30000, 10, MainActivity.this);
 }
 break;

default:
 break;
 }

```

**onLocationChanged()方法中发生了什么？**

```
</pre>

latitude = loc.getLatitude();
 longitude = loc.getLongitude();
 tvLatitude.setText(String.valueOf(latitude));
 tvlongitude.setText(String.valueOf(longitude));
 mLocManager.removeUpdates(this);

```

我获取纬度和经度，然后从监听器中注销位置管理器。这样做是为了节省手机的电池电量。如果你不编码这个，这个方法将尝试访问 GPS 以获得更准确/精确的移动位置细节。但是对于我们的目的，我们满足于从卫星上获取第一个位置。

本文向您介绍了在 Android 中使用基于位置的服务的概念，并解释了如何获取您的移动位置的经度和纬度。在下一部分，我将解释如何使用纬度和经度检索地址。所以，请继续关注！

[![Location Based services in Android](img/2e473457cfc6101b7beeda5ff74c6fd8.png "Location Based services in Android")](https://www.edureka.co/blog/location-based-services-in-android/)

***对所讨论的概念有疑问？[问我们的专家！](# "Have a Doubt? Ask the experts!")***

请继续关注更多教程，学习如何创建 Android 小部件！快乐学习！

*以下资源用于创建此职位: [Edureka.in](http://edureka.in/ "Android courses") 。*[](http://developer.android.com/guide/topics/ui/layout/listview.html)

#### 你可能也会喜欢这些相关的帖子:

*   [了解 Android 中的适配器](https://www.edureka.co/blog/what-are-adapters-in-android/)
*   [安卓项目:21 点游戏](https://www.edureka.co/blog/android-tutorial-on-blackjack/ "Android Project : BlackJack Game")
*   [Android 初学者教程-5:广播接收机](https://www.edureka.co/blog/android-tutorials-broadcast-receivers/ "Android Tutorials for Beginners-5: Broadcast Receiver")