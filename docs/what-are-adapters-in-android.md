# Android 适配器教程:Android 中的适配器是什么

> 原文：<https://www.edureka.co/blog/what-are-adapters-in-android/>

Android 中的适配器是适配器视图(例如 ListView)和该视图的底层数据之间的桥梁。这是 Android 架构中至关重要的概念，也是 ***[Android 认证](https://www.edureka.co/android-development-certification-course)*** 所需要的。想象一下，如果没有 Android 适配器，这个世界会是什么样子！

## 为什么是安卓适配器？

如果没有 Android 适配器，要实现 *ListView* 功能，您需要:

*   在 ScrollView 组中创建 TextView。

*   然后，您必须为 TextView 的内容实现分页概念。

*   您还必须编写额外的代码来标识 TextView 中特定行上的单击事件。

相当繁琐的工作！不是吗？

#### 你可能会问为什么我们需要分页？

假设您正在创建一个应用程序，该应用程序需要显示您所有的电子邮件，并且用户能够滚动浏览它们。我每天收到大约 100 封电子邮件，即使我们每天考虑 10 封电子邮件，电子邮件数据也会非常庞大。如果您不实现分页，那么在检索所有数据并将其显示在移动屏幕上时，您会遇到很大的性能问题。感谢上帝，我们在 Android 和适配器视图中有适配器！

#### 下面是一个概念图，显示了 Android 适配器的高级工作:

#### [![How Android Adapter works](img/5454ccbd32687deed1be9243a5634430.png "How Android Adapter works")](https://cdn.edureka.co/blog/wp-content/uploads/2013/03/adapters-1.png)

现在让我们了解 Android 适配器的内部工作，以及它如何充当适配器视图的数据泵。

适配器调用 **getView()** 方法，该方法为适配器视图中的每个项目返回一个视图。适配器视图中项目的布局格式和相应的数据在 **getView()** 方法中设置。现在，如果 **getView()** 每次被调用时都返回一个新视图，这将是一场性能噩梦。在 Android 中创建一个新的视图是非常昂贵的，因为你需要遍历视图层次结构(使用 find **ViewbyID ()** 方法)，然后放大视图，最终在屏幕上显示它。这也给垃圾收集器带来了很大的压力。这是因为当用户滚动列表时，如果创建了新视图；旧视图(因为它没有被回收)不会被引用，而是成为垃圾收集器要拾取的候选对象。所以 Android 所做的就是回收视图，并重用焦点之外的视图。

#### 以下是这一回收过程的直观表示:

[![Working-of-an-Android-adapter-Android-adapter](img/d71a4a7629e1000c6b028d5c669862c6.png "Working of an Android adapter")](https://cdn.edureka.co/blog/wp-content/uploads/2013/03/021-1.png)

在上图中，假设我们在 ListView 中显示一年中的月份。首先，一月到五月显示在屏幕上。当您滚动视图时，一月份会超出手机屏幕的显示区域。一月视图一离开屏幕，适配器视图(在本例中是 ListView)就将视图发送给一个叫做回收器的东西。因此，当您向上滚动时，getView()方法被调用来获取下一个视图(即 June)。这个方法 getView()有一个名为 convertview 的参数，它指向回收器中未使用的视图。通过 convertview，适配器试图获取未使用的视图并重用它来显示新视图(在本例中是 June)。

**所以，当你创建一个定制的适配器视图时，你应该如下所述编写你的****getView:**

```
@Override

publicView getView(intitempos, View convertView, ViewGroup parent) {

//Check if the convertview is null, if it is null it probably means that this //is the first time the view has been displayed

if (convertView == null)

{

convertView = View.inflate (context,R.layout.list_content_layout, null);

}

//If it is not null, you can just reuse it from the recycler

TextView txtcontent = (TextView) convertView.findViewById(R.id.textView1);

<code>ImageView imgcontent = (ImageView) </code>convertView<code>.findViewById(R.id.imageView1); </code> <code>&nbsp;</code> <code>Paintings paintingcontent = content [itempos]; </code> txtcontent.setText (paintingcontent.imagetitle); imgcontent.setImageResource(paintingcontent.drawableresid); // return the view for a single item in the listview returnconvertView; 
```

[![Android-Adapter](img/0aa3a790d97385941409f1e74e8b682a.png "Android Adapter")](https://cdn.edureka.co/blog/wp-content/uploads/2013/03/android-adapters-1.png)

我们希望，这个 Android 适配器 tutoria  对你有用！  敬请关注安卓更多教程！快乐学习！

*以下资源用于创建此帖子:**[](https://www.edureka.co/android-development-certification-course "get started with Android Development")*[](http://developer.android.com/guide/topics/ui/layout/listview.html)

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[Android 开发入门](https://www.edureka.co/android-development-certification-course "get started with Android Development")

[用帧动画播放声音](https://www.edureka.co/blog/android-tutorial-on-playing-sound-with-frame-animation/ "Playing sound with frame animation")

[Android Widgets:自定义 Listview](https://www.edureka.co/blog/custom-spinner-in-android "Custom spinner in Android")

[安卓](https://www.edureka.co/blog/frame-animation-in-android/ "Frame animation in Android")帧动画