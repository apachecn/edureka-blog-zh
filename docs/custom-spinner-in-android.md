# Android Widgets:Android 中的自定义微调器

> 原文：<https://www.edureka.co/blog/custom-spinner-in-android>

## 让我们来看看 Android 中的自定义微调器

在本主题的 如何创建 Android Widgets 中，我们将学习如何在 Android 中创建自定义微调器。 **Spinners 是 Android 中的一个小工具，允许用户从物品列表中选择一个物品。微调器中的项目来自于 *[适配器](http://developer.android.com/reference/android/widget/Adapter.html)* 的关联。**

如果你对 Android 的基本概念不清楚，可以追寻这个 ***[Android 在线培训](https://www.edureka.co/android-development-certification-course/ "Android training")*** 去了解每一个&技术的每一个细微之处。

**微调器提供了从集合中选择一个值的快速方法。在默认状态下，微调器显示其当前选定的值。触摸微调器会显示一个包含所有其他可用值的下拉菜单，用户可以从中选择一个新值。**

**示例:**显示一周中各天的列表，当选择一个项目时，它会在一个 Toast 中显示该项目。

#### **1)** **全局声明微调器，即在 onCreate 方法之外**

```
// Declare the variable outside onCreate
Spinner spin;
```

#### **2)** **内 onCreate 方法:**

*   **铅字旋转器**
*   **创建数据泵**
*   **声明一个数组适配器**

```
// Typecasting the variable here
spin = (Spinner) findViewById(R.id.spn1);

// Array of Months acting as a data pump
String[] objects = { "January", "Feburary", "March", "April", "May",
"June", "July", "August", "September", "October", "November","December" };

// Declaring an Adapter and initializing it to the data pump
ArrayAdapter adapter = new ArrayAdapter(
getApplicationContext(),android.R.layout.simple_list_item_1 ,objects);

// Setting Adapter to the Spinner
spin.setAdapter(adapter);

// Setting OnItemClickListener to the Spinner
spin.setOnItemSelectedListener(this);

```

#### **3)****onCreate 方法之外:需要用 OnItemSelectedListener 实现的回调方法。**

**有两种回调方法:**

1.  **onItemSelected**
2.  **onNothingSelected**

```
// Defining the Callback methods here
public void onItemSelected(AdapterView parent, View view, int pos,
long id) {
Toast.makeText(getApplicationContext(),
spin.getItemAtPosition(pos).toString(), Toast.LENGTH_LONG)
.show();
}

// Defining the Callback methods here
@Override
public void onNothingSelected(AdapterView arg0) {
// TODO Auto-generated method stub

}

```

[![2](img/2ba2d07c57335d830a265840359c024d.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/2.png)[![3](img/1032d161e3054f37c1de6bc869aa4455.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/3.png)[![4](img/9e7fa90a52c392a478a84c22ff0edae7.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/4.png)

现在你知道如何实现 Spinner 了，它是 Android 中的一个小部件。

### 现在我们将在 Android 中创建一个自定义微调器:

那么为什么要等呢，让我们看看如何实现一个定制的微调器，它将显示一个图像，后面跟着一些文本作为微调器的元素。

看看我们想要创造的东西:

[![5](img/6a89985aac1aa21dc9060d53dda3a260.png) ](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/5.png) [ ![6](img/a2fc2cb811e97278947f838c39a63202.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/6.png)

这更像是一个“**真实而实用的**旋转器。

#### 创建自定义微调器的步骤:

#### **1)****onCreate 之前的方法:**

*   **声明要在微调器中显示的项目数组**
*   **用必须与项目一起显示的相应图像的资源 id 声明一个数组。**

```
// Declaring the String Array with the Text Data for the Spinners
String[] Languages = { "Select a Language", "C# Language", "HTML Language",
"XML Language", "PHP Language" };
// Declaring the Integer Array with resourse Id's of Images for the Spinners
Integer[] images = { 0, R.drawable.image_1, R.drawable.image_2,
R.drawable.image_3, R.drawable.image_4 };

```

#### **2)** **内 onCreate 方法:**

*   **铅字旋转器**
*   **创建数据泵**
*   **声明和分配自定义适配器**

```
// Declaring and typecasting a Spinner
Spinner mySpinner = (Spinner) findViewById(R.id.spinner1);

// Setting a Custom Adapter to the Spinner
mySpinner.setAdapter(new MyAdapter(MainActivity.this, R.layout.custom,
Languages));

```

#### **3)****onCreate 后的方法:**

*   **定义自定义适配器，即 MyAdapter**

```
// Creating an Adapter Class
public class MyAdapter extends ArrayAdapter {

public MyAdapter(Context context, int textViewResourceId,
String[] objects) {
super(context, textViewResourceId, objects);
}

public View getCustomView(int position, View convertView,
ViewGroup parent) {

// Inflating the layout for the custom Spinner
LayoutInflater inflater = getLayoutInflater();
View layout = inflater.inflate(R.layout.custom, parent, false);

// Declaring and Typecasting the textview in the inflated layout
TextView tvLanguage = (TextView) layout
.findViewById(R.id.tvLanguage);

// Setting the text using the array
tvLanguage.setText(Languages[position]);

// Setting the color of the text
tvLanguage.setTextColor(Color.rgb(75, 180, 225));

// Declaring and Typecasting the imageView in the inflated layout
ImageView img = (ImageView) layout.findViewById(R.id.imgLanguage);

// Setting an image using the id's in the array
img.setImageResource(images[position]);

// Setting Special atrributes for 1st element
if (position == 0) {
// Removing the image view
img.setVisibility(View.GONE);
// Setting the size of the text
tvLanguage.setTextSize(20f);
// Setting the text Color
tvLanguage.setTextColor(Color.BLACK);

}

return layout;
}

// It gets a View that displays in the drop down popup the data at the specified position
@Override
public View getDropDownView(int position, View convertView,
ViewGroup parent) {
return getCustomView(position, convertView, parent);
}

// It gets a View that displays the data at the specified position
@Override
public View getView(int position, View convertView, ViewGroup parent) {
return getCustomView(position, convertView, parent);
}
}

```

#### **4)** **创建一个名为 activity_mail.xml 的 XML 文件**

*   **它包括一个旋转器**

```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:orientation="vertical" android:layout_width="fill_parent" android:layout_height="fill_parent">
    <Spinner android:drawSelectorOnTop="true" android:id="@+id/spinner1" android:layout_width="match_parent" android:layout_height="wrap_content" android:prompt="@string/select">
</LinearLayout>

```

#### [![7](img/40341dc058135e5504639955af7e37c0.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/7.png)

#### **5)** **创建一个 XML 文件，命名为 custom.xml :**

**包括**

*   **一个图像视图**
*   **一个文本视图**

```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="wrap_content" android:padding="3dip">
    <ImageView android:id="@+id/imgLanguage" android:layout_width="wrap_content" android:layout_height="wrap_content" android:src="@drawable/ic_launcher">
    </ImageView>
    <TextView android:id="@+id/tvLanguage" android:layout_width="wrap_content" android:layout_height="wrap_content" android:layout_marginLeft="10dp" android:layout_marginTop="8dp" android:text="Text Here">
    </TextView>
</LinearLayout>

```

[![8](img/c69e00861e0c6eb4e2a0203363142bbe.png)](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/8.png)

[button leads form _ title = " Download Code " redirect _ URL = https://edu reka . wistia . com/medias/sl 63 rjlcfc/Download？media _ file _ id = 64011904 course _ id = 318 button _ text = "下载代码"]

***对所讨论的概念有疑问？请在评论区提到它，我们会给你回复。***

请继续关注更多教程，学习如何创建 Android 小部件！

**Related Posts:**

[如何创建 Android Widgets:自定义吐司](https://www.edureka.co/blog/android-tutorial-custom-toast/ "How to create Android Widgets:Custom Toast")

*[如何创建 Android Widgets:Android 中的 rating bar](https://www.edureka.co/blog/tag/how-to-create-android-widgets/ "How to create Android widgets: RatingBar in Android")*

**[大一新生前 5 名安卓面试问题](https://www.edureka.co/blog/interview-questions/top-5-android-interview-questions-for-freshers/ "Top 5 Android Interview Questions for freshers")**