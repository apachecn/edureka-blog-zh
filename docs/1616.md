# 如何在 HTML 中最好地利用音频标签？

> 原文：<https://www.edureka.co/blog/audio-tag-in-html/>

这篇文章提出了一个关于 web 开发的有趣话题，即 HTML 中的音频标签。本文将通过实际演示帮助您探索这个 [HTML](https://www.edureka.co/blog/what-is-html/) 主题。本文将涉及以下几点:

*   [HTML 中的音频标签](#AudioTagInHTML)
*   [音频标签](#AudioTag)
*   [音频标签属性](#AudioTagAttributes)

那么让我们开始吧，

## **HTML 中的音频标签**

很明显，听到 Www 这个术语后，人们首先想到的是 HTML。基本上，它是你今天访问的每一个网站背后的东西。

单靠 HTML 无法公正地处理我们今天看到的一些最受欢迎的设计。它需要帮助，这是由 **CSS** 或 **级联样式表** 提供的。HTML & CSS 可以一起使用，创建一些有吸引力的网页。

**标签【HTML 中的 属性**

这两者都是 HTML 的基础，它们一起工作，但执行不同的功能。

**标签:**标签用来标记 HTML 元素的开始，用尖括号括起来。

**举例:** < h1 >

上面的标签是 HTML 中的 heading 标签。

属性:这些是关于标签的附加信息，在标签中指定。

**举例:**

<imgsrc=" hello _ world . jpg "alt="我的 第一个 程序 >

上面的标签是图片标签< img >，alt 是标签的属性，提供图片 hello_world.jpg 的描述

我们已经讨论了我们需要的基础知识，所以现在我们可以继续讨论这篇文章的主题，一些高级的 HTML 和 CSS 标签。

继续这个 HTML 文章中的音频标签，

## **音频标签**

顾名思义，这个标签绝对是网页上声音的来源。这可用于向网页提供音乐或任何其他流。当前支持的可用于<音频>标签的格式有 MP3、WAV 和 OGG。

**举例:**

```
<audio controls>
<source src="welcome_tune.ogg" type="audio/ogg">
<source src="welcome_tune.mp3" type="audio/mpeg" >
Your browser does not support the audio tag.
</audio>

```

GitHub Gist 链接:<script src = " https://Gist . GitHub . com/snehs eel/6605 e 463 ff 17 e 3886 a 52 a2 e 9 D1 f 26125 . js "></script>

![Output - Audio Tag In HTML - Edureka](img/1bfe5bc234b0cf5eeed1e62bd4eae340.png)

这是音频在网页上的显示方式。

如果用户使用的浏览器不支持音频标签，则显示包含不支持音频标签消息的行。HTML 5 中引入了音频标签。因此，不支持 HTML 5 的浏览器不会支持音频标签。

继续这个 HTML 文章中的音频标签，

## **音频标签属性**

音频标签的属性有:

*   **自动播放:**确保音频一加载到网页上就开始播放。
*   **控件:**指定在网页上显示播放和暂停按钮等音频控件。
*   **循环:**指定循环播放网页上的音频，即反复播放。
*   **静音:**确保音频标签的音频输出静音，即没有声音。
*   **预加载:**指定作者端的 if 和 how，即网页加载时作者希望音频如何加载。
*   **Src:** 指定文件的来源，即要使用的音频文件的地址。

**注意:**音频标签还支持 HTML 中的 accesskey、class、dir、dropzone、hidden、id、lang、style 等全局属性。

这就把我们带到了这篇关于 HTML 中的音频标签的文章的结尾。

*既然你知道了什么是 HTML，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这篇文章的评论部分提到它，我们会给你回复。*