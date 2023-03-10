# 如何创建 Android 小部件:自定义吐司

> 原文：<https://www.edureka.co/blog/android-tutorial-custom-toast/>

在这个“ [如何创建 Android Widgets](https://www.edureka.co/blog/category/android/ "Android Widgets") 的主题中，我们将学习如何定制一个祝酒词。在我们之前的帖子中，我们提到了[RatingBar](https://www.edureka.co/blog/tag/how-to-create-android-widgets/ "Android Widgets : Rating Bar")和 SeekBar ，它们的用法非常相似。

如果你不清楚 Android 的基本概念，请参加本次 [Android 课程](https://www.edureka.co/android-development-certification-course? "Android training") 。

**![android](img/ec9a27372d875b471670c11da624b380.png)一直用同一个吐司你烦吗？**

这个博客将告诉你如何制作你自己定制的吐司。很酷不是吗？；)

使用定制吐司，您可以真正重新定义吐司的外观。你甚至可以在你的吐司里放上图片。在上面的图片中，文本“没有互联网连接”旁边，放置了一个图像，使这个烤面包看起来很棒。改变文本的颜色、大小非常容易。所以让我们开始吧！

### 如何创建 Android Widgets:

#### 自定义吐司:

创建一个 XML 文件，将所有想要显示在 Toast 中的 android 小部件拖放到其中。

重要的关键点:

*   布局 id 是必需的，因为它将在活动中使用。
*   布局的宽度和高度应该设置为“ match_parent ”，以便覆盖完整的 Toast。

### 创建一个名为 custom_toast.xml 的 xml 文件:

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:id="@+id/toast_custom" android:layout_width="match_parent" android:layout_height="match_parent" android:background="@drawable/custom_textview" >

    <ImageView android:layout_width="match_parent" android:layout_height="match_parent" android:layout_margin="4dp" android:contentDescription="@string/android" android:src="@drawable/img2" />

    <TextView android:id="@+id/tvtoast" android:layout_width="match_parent" android:layout_height="match_parent" android:paddingRight="6dp" android:paddingTop="6dp" />

</LinearLayout>

```

创建另一个 XML 文件来设置文本视图的外观，该文本视图将在上面的布局中用作背景。这个文件应该放在 drawable 文件夹中。

### 创建另一个名为 custom_textview.xml: 的 xml 文件

```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android" android:shape="rectangle" >

    <solid android:color="#98E8F9" />

    <stroke android:width="1dip" android:color="#4fa5d5" />

    <corners android:radius="4dp" />

</shape>

```

### 在 onCreate() 方法内:

我们创建的自定义布局在这个方法中是膨胀的，使用它我们可以创建自定义的 Toast。

```
		// Inflating the layout for the toast
		LayoutInflater inflater = getLayoutInflater();
		View layout = inflater.inflate(R.layout.custom_toast,
				(ViewGroup) findViewById(R.id.toast_custom));

		// Typecasting and finding the view in the inflated layout
		TextView text = (TextView) layout.findViewById(R.id.tvtoast);

		// Setting the text to be displayed in the Toast
		text.setText("No internet connection");

		// Setting the color of the Text to be displayed in the toast
		text.setTextColor(Color.rgb(0, 132, 219));

		// Creating the Toast
		Toast toast = new Toast(getApplicationContext());

		// Setting the position of the Toast to centre
		toast.setGravity(Gravity.CENTER_VERTICAL, 0, 0);

		// Setting the duration of the Toast
		toast.setDuration(Toast.LENGTH_LONG);

		// Setting the Inflated Layout to the Toast
		toast.setView(layout);

		// Showing the Toast
		toast.show();

```

[dl URL = " # " class = ' e model e model-11 ' title = "下载代码" desc = " " type = " " align = " " for = " Download "]

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[Android SDK 安装](https://www.edureka.co/blog/android-sdk-installation/)

[开始你的安卓开发历程](https://www.edureka.co/android-development-certification-course)