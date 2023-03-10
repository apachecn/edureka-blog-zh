# 如何用 AWS WAF 保护 Web 应用？

> 原文：<https://www.edureka.co/blog/secure-web-applications-with-aws-waf/>

这篇文章将告诉你如何使用 [AWS](https://www.edureka.co/blog/what-is-aws/) WAF 来保护 Web 应用程序，并通过一个实际的演示来跟进。本文将涉及以下几点:

*   [开始学习一些基础知识](#GettingStartedWithSomeFundamentals)
*   [开始使用 AWS WAF 的步骤顺序](#SequenceofstepstogetstartedwithAWSWAF)

那么让我们开始吧，

继续这篇文章“如何用 AWS WAF 保护 Web 应用程序？”

## **开始学习一些基础知识**

AWS 提供 EC2、ELB(弹性负载均衡器)、S3(简单存储服务)、EBS(弹性块存储)等服务，以更少的资本支出快速创建有用且精美的应用。在创建这些应用程序时，保护应用程序和数据同样重要。如果保护不当，应用程序数据可能会落入坏人之手，就像最近发生的 [Capital One 事件](https://krebsonsecurity.com/2019/07/capital-one-data-theft-impacts-106m-people/)一样。

Capital One 在 EC2 上托管了一个 Web 应用程序，它没有得到适当的保护。一名前 AWS 员工能够利用该漏洞从 S3 下载大量客户数据。后来发现其他 30 个组织的数据也是从 AWS 下载的。因此，再次强调，仅仅设计和架构应用程序是不够的，保护应用程序的安全也同样重要。

Capital One 使用了 [AWS WAF (Web 应用防火墙)](https://aws.amazon.com/waf/faq/)来保护 Web 应用，但由于配置不当，黑客得以访问 S3 的数据并下载。在本文中，我们将探讨如何使用和配置 AWS WAF 来防范常见的 web 攻击，如 SQL 注入、XSS(跨站脚本)等。AWS WAF 必须与[应用负载平衡器](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html)、CloudFront 或 API Gateway 一起配置。在这个场景中，我们将使用应用程序负载平衡器。客户通过浏览器发出的任何请求都将通过 AWS WAF，然后到达应用程序负载平衡器，最后到达 EC2 上的 Web 应用程序。AWS WAF 可用于[利用一套规则和条件阻止黑客的恶意请求](https://docs.aws.amazon.com/waf/latest/developerguide/how-aws-waf-works.html)。

## ![Image - Secure Web Applications With AWS WAF - Edureka](img/ace91161cdfe2ad0a931328082923b59.png)

继续这篇关于“如何用 AWS WAF 保护 Web 应用程序安全？”的文章

## **开始使用 AWS WAF 的步骤顺序**

**步骤 1:** 创建易受攻击的 web 应用程序，

第一步是创建一个易受 SSRF(服务器端请求伪造)攻击的 web 应用程序，正如这篇关于 Capital One 攻击如何发生的博客中所提到的。本博客包含以下一系列步骤:

1.  创建 EC2
2.  安装创建具有 SSRF 漏洞的 web 应用程序所需的软件
3.  创建具有 S3 只读权限的 IAM 角色
4.  将 IAM 角色附加到 EC2
5.  最后，利用 SSRF 漏洞获取与 IAM 角色相关的安全凭证。

一旦在提到的博客中完成了一系列步骤，在下面的 URL 中用 EC2 的公共 IP 地址替换 5.6.7.8，并在浏览器中打开它。与 IAM 角色相关联的安全凭据应该显示在浏览器中，如下所示。这就是 Capital One 被黑的基本过程。有了安全凭证，黑客就能够访问 S3 等其他 AWS 服务来下载数据。你甚至可以通过 [AWS 云迁移课程](https://www.edureka.co/migrating-to-aws)了解迁移到 AWS 的细节。

**查看我们在顶级城市的 AWS 认证培训**

| 印度 | 美国 | 其他国家 |
| [在海德拉巴的 AWS 培训](https://www.edureka.co/aws-certification-training-hyderabad) | [亚特兰大 AWS 培训](https://www.edureka.co/aws-certification-training-atlanta) | [AWS 伦敦培训](https://www.edureka.co/aws-certification-training-london) |
| [班加罗尔的 AWS 培训](https://www.edureka.co/aws-certification-training-bangalore) | [波士顿 AWS 培训](https://www.edureka.co/aws-certification-training-boston) | [阿德莱德的 AWS 培训](https://www.edureka.co/aws-certification-training-adelaide) |
| [钦奈的 AWS 培训](https://www.edureka.co/aws-certification-training-chennai) | [纽约市的 AWS 培训](https://www.edureka.co/aws-certification-training-new-york-city) | [新加坡 AWS 培训](https://www.edureka.co/aws-certification-training-singapore) |

http://5.6.7.8:80？URL = http://169 . 254 . 169 . 254/latest/meta-data/iam/security-credentials/role 4c 2-S3RO

**![Image - Secure Web Applications With AWS WAF - Edureka](img/aa7b53534d7ea4dd22ab2f16e5cf601b.png)**

**步骤 2:** 创建应用负载平衡器

AWS WAF 不能与 Web 应用程序直接关联。但是，只能与应用负载平衡器、CloudFront 和 API 网关相关联。在本教程中，我们将创建[应用程序负载平衡器，并将 AWS WAF](https://aws.amazon.com/blogs/aws/aws-web-application-firewall-waf-for-application-load-balancers/) 与之相关联。

**步骤 2a:** 目标组是 EC2 实例的集合，必须在创建应用程序负载平衡器之前创建。在 EC2 管理控制台中，单击左侧窗格中的目标组，然后单击“创建目标组”。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/842adf9342b77018d5bff70e39addb0b.png)**

**步骤 2b:** 输入目标组名称并点击“创建”。将成功创建目标组。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/def3bd24a1f7ce8c96bf01f00957f8d7.png)**

**![Image - Secure Web Applications With AWS WAF - Edureka](img/b9bb8630b674e692c2ceda8c5d895cc5.png)**

**步骤 2c:** 确保选择了目标组，单击 Targets 选项卡，然后单击 edit 向目标组注册 EC2 实例。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/48333d42aa32a22e05a478c57fe7b88e.png)**

**步骤 2d:** 选择 EC2 实例并点击“添加到已注册”并点击“保存”。

![Image - Secure Web Applications With AWS WAF - Edureka](img/4fb7652585176bdcf137f4a2ac46942f.png)

![Image - Secure Web Applications With AWS WAF - Edureka](img/06aae03d9ed76b6169b4d72504694932.png)

应该为目标组注册如下所示的实例。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/54eba45175fc196f59fbb39d7726dc80.png)**

**步骤 2e:** 创建应用负载平衡器的时间。单击 EC2 管理控制台左侧窗格中的负载平衡器，然后单击“创建负载平衡器”。

![Image - Secure Web Applications With AWS WAF - Edureka](img/bc055f30e4b75d2610a59bb4f189cc53.png)

单击“应用程序负载平衡器”的“创建”。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/47a68842b4c1abe990b230944db5e18f.png)**

继续这篇文章“如何用 AWS WAF 保护 Web 应用程序？”

**步骤 2f:** 输入应用负载平衡器的名称。确保选择了所有可用区域，然后单击“Next”。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/4e994d51a721471b13f0c04cdd389095.png)**

**步骤 2g:** 在“配置安全设置”中点击下一步。

![Image - Secure Web Applications With AWS WAF - Edureka](img/441f39e5d00e9bba5b276cd7414c0360.png)

在“配置安全组”中创建新的安全组或选择一个现有的安全组。确保端口 80 已打开，可以访问 EC2 上的网页。点击下一步。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/aa49c20bdac4351d3467f7e979c0d8a8.png)**

**步骤 2h:** 在“配置路由”中选择“现有目标组”，并选择在之前步骤中已经创建的目标组。点击下一步。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/8a018fd58ad6aeabf24a98b9ca61911d.png)**

**步骤 2i:** 目标 EC2 实例已经注册为目标组的一部分。因此，在“注册目标”选项卡中，不做任何更改，单击“下一步”。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/66aba72793699a91575af38f3f4545da.png)**

**步骤 2j:** 最后，查看应用程序负载平衡器的所有详细信息，并单击 Create。应用程序负载平衡器的创建如下所示。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/f56bc4d1a40c0626f0978d71114211e4.png)![Image - Secure Web Applications With AWS WAF - Edureka](img/28275e6b1ff3579e57d86c77fe820957.png)**

**步骤 2k:** 获取应用程序负载平衡器的域名，替换下面 URL 中突出显示的文本，并在浏览器中打开。请注意，我们通过应用程序负载平衡器访问 Web 应用程序，安全凭证如下所示。可以使用 AWS WAF 阻止下面的 URL，如后续步骤所示，以阻止安全凭证的泄漏。

**MyALB-1929899948.us-east-1.elb.amazonaws.com**？URL = http://169 . 254 . 169 . 254/latest/meta-data/iam/security-credentials/role 4c 2-S3RO

**![Image - Secure Web Applications With AWS WAF - Edureka](img/675035f42f4a4498ec2589935a0dc4f1.png)**

从 [AWS 开发人员培训](https://www.edureka.co/aws-developer-certification-training)中了解更多关于 AWS 开发人员及其框架的信息。

**步骤 3:** 创建 AWS WAF(网络应用防火墙)

**步骤 3a:** 进入 AWS WAF 管理控制台，点击“配置 web ACL”。显示了 AWS 晶片概况。这里是 AWS WAF 的层次结构。Web ACL 有许多规则，而规则又有许多条件，我们将在后续步骤中创建这些条件。点击下一步。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/6c6d9ca16c8703d5e83ccc91e9e552b8.png)**

**![Image - Secure Web Applications With AWS WAF - Edureka](img/3d8de8ba4729ee260136855e15ca844d.png)**

**步骤 3b:** 输入 Web ACL 名称，区域为 North Virginia(或创建 EC2 的地方)，资源类型为“应用负载平衡器”，最后选择在前面步骤中创建的应用负载平衡器。点击下一步。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/bae7eeb93a3b0daf89233962cee74c14.png)**

**步骤 3c:** 这里必须创建一个[条件来阻止一个特定的 web 应用请求](https://docs.aws.amazon.com/waf/latest/developerguide/web-acl-string-conditions.html)。向下滚动并单击“字符串和正则表达式匹配条件”的“创建条件”。

**步骤 3d:** 输入条件名称，类型为“字符串匹配”，过滤“所有查询参数”，其余参数如下图所示。点击“添加过滤器”，然后点击“创建”。这里我们试图创建一个条件，该条件匹配包含查询参数值 169.254.169.254 的 URL。该 IP 地址与 [EC2 元数据](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html#instance-metadata-security-credentials)相关。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/2a08e3e2ee9a83e959cbe8c8c591e714.png)![Image - Secure Web Applications With AWS WAF - Edureka](img/ea87f02d89ab03b5b4c3aa4c5689e57c.png)**

**步骤 3e:** 现在是创建规则的时候了，该规则是条件的集合。点击“创建规则”并如下所示指定参数。点击“添加条件”，创建和“审查和创建”。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/a2f15f64d0b1989d9fa35680dcc041e4.png)![Image - Secure Web Applications With AWS WAF - Edureka](img/061ac2343575131402795c8530733df4.png)**

继续这篇文章“如何用 AWS WAF 保护 Web 应用程序？”

**步骤 3f:** 最后查看所有细节，点击“确认并创建”。Web ACL(访问控制列表)将被创建并与应用程序负载平衡器相关联，如下所示。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/db2d36b645dbcbcba8aed9cf15bdfe96.png)![Image - Secure Web Applications With AWS WAF - Edureka](img/2965614bb293ff0977813a132e18d3f8.png)**

**步骤 3g:** 现在尝试通过浏览器访问应用负载平衡器 URL，如**步骤 2k** 中所执行的。这一次，我们将得到“403 禁止”，因为我们的网址匹配网络 ACL 条件，我们阻止它。请求永远不会到达 EC2 上的应用程序负载平衡器或 Web 应用程序。这里我们注意到，虽然应用程序允许访问安全凭证，但 WAF 阻止了同样的访问。

**![Image - Secure Web Applications With AWS WAF - Edureka](img/1f413b8b3cdb3ad2f1a5e190d965a669.png)**

**步骤 4:** 清理本教程中创建的 AWS 资源。必须按照下述完全相同的顺序进行清理。这是为了确保 AWS 停止对在本教程中创建的相关资源进行计费。

*   删除规则中的条件
*   删除 WebACL 中的规则
*   解除 WebACL 中 ALB 的关联
*   删除 WebACL
*   删除该规则
*   删除条件中的筛选器
*   删除条件
*   删除 ALB 和目标组
*   终止 EC2
*   删除 IAM 角色

**结论**

如前所述，使用 AWS 创建 Web 应用程序是非常容易和有趣的。但是我们也必须确保应用程序是安全的，数据不会泄露到坏人的手中。安全性可以应用于多个层。在本教程中，我们看到了如何使用 AWS WAF (Web 应用程序防火墙)来保护 Web 应用程序免受攻击，例如匹配 EC2 元数据的 IP 地址。我们还可以使用 WAF 来防范常见的攻击，如 SQL 注入和 XSS(跨站点脚本)。

使用 AWS WAF 或实际上任何其他安全产品都不能保证应用程序的安全，但是必须正确配置产品。如果配置不当，数据可能会落入他人之手，就像 Capital One 和其他组织所发生的那样。此外，要考虑的另一件重要事情是，安全性必须从第一天就考虑到，而不是在以后的阶段插入到应用程序中。

这就把我们带到了这篇关于如何用 AWS WAF 保护 Web 应用程序的文章的结尾。我们还推出了一套课程，涵盖了您通过解决方案架构师考试所需的全部内容！你可以看看 [AWS 解决方案架构师培训](https://www.edureka.co/aws-certification-training)的课程详情。

*有问题吗？请在“什么是 AWS”博客的评论部分提到它，我们会给你回复。*