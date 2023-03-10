# 什么是 Bootstrap 证明幻灯片，如何设计它？

> 原文：<https://www.edureka.co/blog/bootstrap-testimonial/>

人们根据评论购买产品。如今，网上评论无所不在，有助于促进产品的销售。这就是 自举证明幻灯片 的用武之地。在这篇博客中，你将学习如何在网站上创建一个 自举推荐滑块 。此外，这个[引导](https://www.edureka.co/blog/bootstrap-pagination/) 证明滑块 也可以用作报价滑块。

在这篇博客中，你将学习如何使用 [HTML](https://www.edureka.co/blog/what-is-html/) 创建一个 自举证明滑块 ，并使用 [CSS](https://www.edureka.co/blog/what-is-css/) 对其进行样式化。

*   [HTML 代码](#htmlcode)
*   [CSS 代码](#csscode)

让我们开始吧。

## **理解使用 HTML 代码**

```
<div class = "container">
        <div class = "row">
            <div class = "col-md-12">
                <div class = "carousel slide" data-ride = "carousel" id = "quote-carousel">

                    <!-- Carousel Slides / Quotes -->
                    <div class = "carousel-inner text-center">

                        <!-- Quote 1 -->
                        <div class = "item active">
                            <blockquote>
                                <div class = "row">
                                    <div class = "col-sm-8 col-sm-offset-2">
                                        <p> Edureka has the best online courses! </p>
                                        <small> Reviewer's Name </small>
                                    </div>
                                </div>
                            </blockquote>
                        </div>
                        <!-- Quote 2 -->
                        <div class = "item">
                            <blockquote>
                                <div class = "row">
                                    <div class = "col-sm-8 col-sm-offset-2">
                                        <p> Edureka has the best online courses!  </p>
                                        <small> Reviewer's Name </small>
                                    </div>
                                </div>
                            </blockquote>
                        </div>
                        <!-- Quote 3 -->
                        <div class = "item">
                            <blockquote>
                                <div class = "row">
                                    <div class = "col-sm-8 col-sm-offset-2">
                                        <p> Edureka has the best online courses! </p>
                                        <small> Someone famous </small>
                                    </div>
                                </div>
                            </blockquote>
                        </div>
                    </div>
                    <!-- Bottom Carousel Indicators -->
                    <ol class = "carousel-indicators">
                        <li data-target = "#quote-carousel" data-slide-to = "0" class = "active"> <img class = "img-responsive " src = "https://s3.amazonaws.com/uifaces/faces/twitter/mantia/128.jpg" alt="">
                        </li>
                        <li data-target = "#quote-carousel" data-slide-to= "1"> <img class = "img-responsive" src = "https://s3.amazonaws.com/uifaces/faces/twitter/adhamdannaway/128.jpg" alt = "">
                        </li>
                        <li data-target = "#quote-carousel" data-slide-to = "2"><img class = "img-responsive" src = "https://s3.amazonaws.com/uifaces/faces/twitter/brad_frost/128.jpg" alt="">
                        </li>
                    </ol>

                    <!-- Carousel Buttons Next/Prev -->
                    <a data-slide = "prev" href = "#quote-carousel" class = "left carousel-control"><i class = "fa fa-chevron-left"> </i> </a>
                    <a data-slide = "next" href = "#quote-carousel" class = "right carousel-control"><i class = "fa fa-chevron-right"></i></a>
                </div>
            </div>
        </div>
        <a class = "btn btn-primary" href = "http://thecodeblock.com/create-a-quote-testimonial-slider-using-bootstrap-carousel"><i class = "fa fa-arrow-left"></i> Back to Article</a>
    </div>

```

**解说:**

这个”。carousel slide”类用于创建一个 carousel slider。要在中间创建一个文本。carouse-inner text-center”类。接下来，<块引用>用于指定被引用的部分。在这里，它被用来引用客户的评价。然后输入客户的证明。这是重复的，直到你添加了足够数量的证明。

## **了解 CSS**

```
#quote-carousel {
    padding: 0 10px 30px 10px;
    margin-top: 60px;
}
#quote-carousel .carousel-control {
    background: none;
    color: #CACACA;
    font-size: 2.3em;
    text-shadow: none;
    margin-top: 30px;
}
#quote-carousel .carousel-indicators {
    position: relative;
    right: 50%;
    top: auto;
    bottom: 0px;
    margin-top: 20px;
    margin-right: -19px;
}
#quote-carousel .carousel-indicators li {
    width: 50px;
    height: 50px;
    cursor: pointer;
    border: 1px solid #ccc;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
    border-radius: 50%;
    opacity: 0.4;
    overflow: hidden;
    transition: all .4s ease-in;
    vertical-align: middle;
}
#quote-carousel .carousel-indicators .active {
    width: 128px;
    height: 128px;
    opacity: 1;
    transition: all .2s;
}
.item blockquote {
    border-left: none;
    margin: 0;
}
.item blockquote p:before {
    content: "f10d";
    font-family: 'Fontawesome';
    float: left;
    margin-right: 10px;
}

```

**解释**

每一部分的 HTML 代码都可以根据你的需要进行定制。只需创建一个部分，复制粘贴上面的代码，并根据您的要求进行编辑。

你的代码的最终输出看起来像:

![Output- Boostrap Testimonial - Edureka](img/b071c876bf302874dc4af6f51e061e4d.png)

![Output css- Boostrap Testimonial - Edureka](img/115bd6fbb6486f13a3759a8333174c3c.png)

![Final Output- Boostrap Testimonial - Edureka](img/45a8dcc0cf9b02a2269f5f20f8596372.png)

希望这篇博客对你有所帮助！如果您对 自举证明幻灯片 有任何疑问，请在下面的评论区提出您的疑问！

就这样，我们来到了这篇文章的结尾。我希望你明白什么是自举证明滑块，以及如何使用 [HTML](https://www.edureka.co/blog/what-is-html/) 和 [CSS](https://www.edureka.co/blog/what-is-css/) 来设计它。

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这个博客的评论部分提到它，我们会给你回复。*