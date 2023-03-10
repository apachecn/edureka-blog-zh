# 如何用亚马逊 Lex 开发一个聊天机器人？

> 原文：<https://www.edureka.co/blog/how-to-develop-a-chat-bot-using-amazon-lex/>

人类一直在试图寻找越来越多的方法来利用科技让生活变得更轻松。随着各种应用软件处理日常生活，聊天机器人很快成为日常生活不可或缺的一部分。这是最新的流行语。 ***亚马逊 Lex*** 是最流行的构建聊天机器人的平台之一。他的教程将指导你使用亚马逊 Lex 制作聊天机器人的整个过程。

我们来看看这篇亚马逊 Lex 教程涉及的话题:

*   [什么是聊天机器人技术？](#whatarechatbots)
*   [机器人是做什么的？](#whychatbots)
*   [亚马逊 Lex Bot 是什么？](#AmazonLexBot)
*   [演示:如何使用亚马逊 Lex 构建聊天机器人？](#LexBotDemo)

## **什么是聊天机器人技术？**

![chatbotex - Amazon Lex - edureka](img/b0a576f2a5ad0160bdff72df38ef6fe8.png)

*“聊天机器人是一种计算机程序，它通过听觉或文本方式用自然语言进行对话，理解用户的意图，并根据业务规则和组织的数据发送响应。”*

简单来说，聊天机器人(chatbot)是一种你可以通过聊天界面与之交流的服务或工具。聊天机器人理解你试图暗示什么，并回复相关信息或直接为你完成所需任务。

### **聊天机器人的进化是如何以及何时开始的？**

如果你认为聊天机器人是新技术，那你就错了。事实上，第一个聊天机器人**伊莱扎**是 1966 年由约瑟夫·韦岑鲍姆在麻省理工学院人工智能实验室建造的，它只用了 200 行代码就模仿了心理治疗师。然后在 1988 年，当罗洛·卡彭特开始 Jabberwacky 项目时，一个语音操作的娱乐 AI 聊天机器人。以下是聊天机器人从那时起的演变:

![Bot Evolution -Amazon Lex - Edureka](img/5589c7ded4311572346c195f0d68c7d6.png)

## **机器人是做什么的？**

聊天机器人之所以相关是因为以下原因:

*   他们在正确的时间、正确的地点，最重要的是只在人们需要的时候，向他们提供正确的信息。
*   我们在移动设备上大约 90%的时间花在电子邮件和信息平台上。因此，使用聊天机器人吸引客户，而不是将他们转移到网站或移动应用程序是有意义的。
*   人工智能、[机器学习](https://www.edureka.co/blog/scikit-learn-machine-learning/)、[自然语言处理](https://www.youtube.com/watch?v=05ONoGfmKvA)的进步，让机器人越来越像真人一样对话。

现代聊天机器人不仅仅依赖文本，还会显示有用的卡片、图像、链接和表格，提供类似应用程序的体验。 根据机器人的编程方式，我们可以将它们分为两种聊天机器人:基于规则的(哑机器人)&自我学习的(智能机器人)。

1.  基于规则的聊天机器人:这种机器人根据一些简单的规则来回答问题，这些规则是他们接受训练的。
2.  **自学习聊天机器人**:这类机器人依靠[人工智能](https://www.edureka.co/blog/what-is-artificial-intelligence) (AI) & [机器学习](https://www.edureka.co/blog/machine-learning-tutorial/) (MI)技术与用户进行对话。

有些平台采用了所有复杂的技术，让你只需简单的几步就能创建聊天机器人&根据你的喜好定制它们。亚马逊 lex 就是这样一个平台。

Want To Take Your 'Cloud' Knowledge To Next Level? [<button>Get Cloud Certified Today!</button>](https://www.edureka.co/masters-program/cloud-architect-training)

## **亚马逊 Lex Bot 是什么？**

Amazon Lex 是一项全面管理的服务，用于在任何使用语音和文本的应用程序中构建对话界面。它提供深度学习功能，如:

*   [自动语音识别](https://www.edureka.co/blog/what-is-deep-learning) (ASR)，用于将语音转换为文本
*   [自然语言理解](https://www.edureka.co/blog/what-is-deep-learning) (NLU)识别文本的意图

Amazon Lex 使您能够快速&轻松构建聊天机器人，提供高度吸引人的用户体验和逼真的对话互动。现在你可能想知道，

**亚马逊 Lex 免费吗？**

是的，的确如此，你可以在 AWS 免费层下使用它的大部分功能。

### **使用亚马逊 Lex 的好处:**

*   简单:它提供了一个易于使用的控制台，可以在几分钟内创建你自己的聊天机器人&预定义的机器人帮助你开始。
*   **内置技术:**你只需提供几个示例短语，亚马逊 Lex 就会构建一个完整的自然语言模型，通过这个模型，机器人可以使用语音和文本进行交互。
*   **无缝部署和扩展:**随着用户参与度的提高，您无需担心配置硬件和管理基础设施来增强您的 bot 体验。
*   **与 AWS 的内置集成:**亚马逊 Lex 允许与 AWS 平台上的许多其他服务集成，包括 [AWS Lambda](https://www.edureka.co/blog/aws-lambda-tutorial) 、[亚马逊 CloudWatch](https://www.edureka.co/blog/amazon-cloudwatch-monitoring-tool/) 、亚马逊 Cognito 和亚马逊 DynamoDB &许多其他服务。
*   **性价比高:**有了亚马逊 Lex，没有前期费用，也没有最低费用。您只需为您发出的文本或语音请求付费

让我们考虑一个用例来理解 Amazon Lex 的功能。

### **用例**:通过亚马逊 Lex 聊天机器人获取银行信息。

使用 Amazon Chatbot，您可以构建强大的界面来使用移动应用程序。您可以添加语音或文本聊天界面，在移动设备上创建机器人，帮助客户完成基本任务。

假设你想获得你的银行账户余额&你正在使用*亚马逊 Lex 聊天机器人。* Amazon Lex 理解你的请求并执行必要的后台任务。它与 Amazon Polly 协调，并以语音形式要求您进一步输入。一旦它收到信息，它就调用[AWSλ](https://www.edureka.co/blog/aws-lambda-tutorial)。Lambda 检索请求的信息或执行其他类型的操作。比如它可能会触发亚马逊 SNS 服务向您发送通知，或者与 AWS CloudWatch 集成以存储日志&事件。

![usecase - Amazon Lex - Edureka](img/9927559644baf757ce7e1b50dfa9478a.png)

现在你知道 Amazon Lex 如何满足你的要求了。让我们看看其他一些有趣的用例:

*   美国宇航局星际机器人大使“Rov-E”是真实的美国宇航局火星探测器的复制品。通过亚马逊 Lex，美国宇航局的工作人员可以通过语音命令轻松导航 Rov-E。
*   **OhioHealth** 使用 Amazon Lex 在正确的时间和正确的地点为我们的患者提供正确的护理。
*   **【HubSpot’**growth bot 是一款一体化聊天机器人，通过使用对话界面提供对相关数据和服务的访问，帮助营销人员和销售人员提高工作效率。

这些用例看起来非常有趣。

所以，如果这激起了你的兴趣&如果你渴望在亚马逊 Lex 上创建一个自己的聊天机器人，那就去看看下面提供的视频吧。这段视频将带你一步步了解如何在 Amazon Lex 上创建聊天机器人。

## **演示:如何使用亚马逊 Lex** 创建聊天机器人

由于聊天机器人是建立在亚马逊网络服务上的，你需要创建一个账户。一旦你建立了你的账户，我们就可以开始创建聊天机器人了。这个视频演示了如何使用一些简单的响应来构建聊天机器人。

## **亚马逊 Lex 聊天机器人教程|在亚马逊 Lex 上创建聊天机器人| Edureka**



[//www.youtube.com/embed/KTa1T14nkbw?rel=0&showinfo=0](//www.youtube.com/embed/KTa1T14nkbw?rel=0&showinfo=0)

这段视频将帮助你了解什么是聊天机器人&如何使用 Aws Lex 服务构建出色的聊天机器人。

我希望你看过视频&成功创建了自己的聊天机器人。 最后，如果你想知道机器人是否会蹂躏人类。不，我不这么认为。机器人是并将永远是机器人，本质上是机器人的性质和互动。总而言之，它们被开发出来是为了倾听和服从，为人类执行任务，让我们的生活更轻松。

*原来如此！我希望这篇文章内容丰富，增加了你的知识。如果你有兴趣将你在亚马逊网络服务方面的知识提升到一个新的水平，那么就报名参加 Edureka 的 [AWS 架构师认证培训](https://www.edureka.co/aws-certification-training)课程。*

*有问题吗？请在“Amazon Lex”的评论部分提到它，我们会给你回复。*