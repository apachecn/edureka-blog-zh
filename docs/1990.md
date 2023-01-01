# 如何在 Power BI 中实现行级安全性

> 原文：<https://www.edureka.co/blog/row-level-security-in-power-bi/>

当涉及到任何数据的安全方面时，限制用户对任何数据的访问是使用的关键技术之一。在本文中，我们将了解如何在 [Power BI](https://www.edureka.co/blog/power-bi-tutorial/) 中实现行级安全性:

*   [Power BI 中的行级安全性是什么？](#what)
*   [在 Power BI Desktop 中定义角色和规则](#define)
*   [管理您的模型的安全性](#manage)
*   [与成员一起工作](#members)
*   [Power BI 中行级安全性的限制](#limitations)

## **Power BI 中的行级安全性是什么？**

Power BI 中的行级安全性可用于限制给定用户的数据访问。筛选器在行级别限制数据访问，您可以在角色中定义筛选器。请注意，在 Power BI 服务中，工作空间的成员可以访问工作空间中的数据集。RLS 不限制这种数据访问。

![Power BI Reports](img/1d0759fd228450eac6fd79977c536942.png)

您可以使用 Power BI Desktop 为导入到 Power BI 中的数据模型配置 RLS。还可以在使用 DirectQuery 的数据集(如 SQL Server)上配置 RLS。以前，您只能在 Power BI 之外的内部分析服务模型中实施 RLS。对于 Analysis Services 实时连接，您可以在内部模型上配置行级安全性。对于实时连接数据集，不会显示安全选项。

*您可以浏览一下微软 Power BI 录音，其中我们的* 专家 *已经用示例详细解释了这些主题，这将有助于您更好地理解这些概念。*

[https://www.youtube.com/embed/3u7MQz1EyPY](https://www.youtube.com/embed/3u7MQz1EyPY)

## **在 Power BI Desktop 中定义角色和规则**

您可以在 Power BI 桌面中定义角色和规则。当您发布到 Power BI 时，它还会发布角色定义。这是 Power BI 中行级安全性的一个重要方面。要定义安全角色，请按照下列步骤操作。

1.  将数据导入 Power BI Desktop 报告，或配置 DirectQuery 连接。

    **注意:**您不能在 Power BI Desktop 中为 Analysis Services 实时连接定义角色。您需要在 Analysis Services 模型中这样做。

2.  选择标签页。

3.  选择  **管理角色**。

    ![Row Level Security in Power BI](img/ca6e960b7641f69a004dfeef4beba3f8.png)

4.  选择  **创建**。![create- Row Level Security in Power BI](img/4cde57c6f3be2ebd0ab9c00f9e775755.png)
5.  提供角色的名称。

6.  选择要应用 DAX 规则的表。

7.  输入 DAX 表达式。该表达式应返回 true 或 false。例如:[实体 ID] = "值"。

    **注意:**可以在这个表达式内使用*用户名()* 。注意在 Power BI 桌面中*username()*的格式为*domain username*。在 Power BI 服务和 Power BI 报告服务器中，它采用用户的用户主体名称(UPN)的格式。或者，您可以使用*userprincipalname()*，它总是以用户主体名称、*username@contoso.com*的格式返回用户。

    ![manage- Row Level Security in Power BI](img/b7ae59b2379fd8abaed9ecb902fe7231.png)

8.  创建 DAX 表达式后，可以选择表达式框上方的复选标记来验证表达式。

    ![DAX Expression](img/6794bd1ddcc5ca01e91f18ea487ccf34.png)

    **注意:**在这个表达式框中，使用逗号分隔 DAX 函数参数，即使您使用的是通常使用分号分隔符的语言环境(例如法语或德语)。

9.  选择  **保存**。

您不能在 Power BI Desktop 中为用户分配角色。您可以在 Power BI 服务中分配它们。通过使用*username()*或*userprincipalname()*DAX 函数并配置适当的关系，您可以在 Power BI Desktop 中启用动态安全性。

默认情况下，无论关系设置为单向还是双向，行级安全筛选都使用单向筛选器。通过选择关系并选中  **在两个方向应用安全过滤器** 复选框，您可以手动启用具有行级安全性的双向交叉过滤器。当您还在服务器级实现了动态行级安全性时，您应该选中此框，其中行级安全性基于用户名或登录 ID。

![Apply Security Filter](img/d88e113b1824fec1b07fe3d0e7815bfd.png)

**验证 Power BI Desktop 中的角色**

创建角色后，在 Power BI Desktop 中测试角色的结果。

1.  选择  **查看角色**。![](img/017b5f0a4a9c6d39adb6910b35760e11.png)在  **角色视图**中，您可以看到您已经创建的角色。![](img/d20347f0ea585f828172f9bb03bca387.png)
2.  选择您创建的角色>  **确定** 来应用那个角色。该报告呈现了与该角色相关的数据。

3.  您也可以选择  **其他用户** 和供给给定用户。最好提供用户主体名称(UPN ),因为这是 Power BI 服务和 Power BI 报告服务器使用的名称。

    ![](img/f4049182abf151e984cd574c3f6160c9.png)

4.  选择  **确定** ，报表根据用户所能看到的内容进行渲染。

在 Power BI Desktop 中，**其他用户**仅在您使用基于 DAX 表达式的动态安全性时显示不同的结果。

## **管理您的模型的安全性**

要管理数据模型的安全性，您需要执行以下操作。

1.  选择  **【椭圆】(…)** 为一个数据集。

2.  选择  **安全**。

    ![Apply security filter in both directions](img/0f117f20a1511bc6a7fee28be4cd47ed.png)

这将带您进入 RLS 页面，您可以向在 Power BI Desktop 中创建的角色添加成员。只有数据集的所有者会看到可用的安全性。如果数据集在一个组中，则只有该组的管理员才能看到安全选项。

您只能在 Power BI Desktop 中创建或修改角色。

## **与成员一起工作**

### 添加成员

您可以通过键入要添加的用户、安全组或分发列表的电子邮件地址或名称来为角色添加成员。您不能添加在 Power BI 中创建的组。您可以添加组织外部的成员  。

![Add a member](img/f1245e48f445c3a7eeda300a0b8fd477.png)

您还可以通过角色名称旁边或成员旁边的括号中的数字来查看有多少成员是角色的一部分。

![Members in role - Row Level Security in Power BI](img/0b176f663f2e9822dfe330495fa4f2f6.png)

### 移除成员

您可以通过选择成员名称旁边的 X 来删除成员。

![Remove member](img/cfe38a1c95730f07251e2684f46d21fe.png)

**验证 Power BI 服务中的角色**

您可以通过测试角色来验证您定义的角色是否正常工作。

1.  选择角色旁边的(…)。

2.  选择  **测试数据作为角色**

![Test as role](img/3610aab41dc8a68920bb08852410be02.png)

然后，您将看到适用于该角色的报告。此视图中不显示仪表板。在上面的蓝色栏中，您将看到正在应用的内容。

![Now viewing as - Row Level Security in Power BI](img/98b92822b653db6f396be24a906f8dfe.png)

您可以通过选择  **来测试其他角色或角色组合，现在查看为**。

![Test other roles -Row Level Security in Power BI](img/af927b855e572c4aeed31f2aa814af70.png)

您可以选择以特定人员的身份查看数据，也可以选择可用角色的组合来验证他们正在工作。

要返回正常查看，选择  **回到行级安全**。

**使用 username()或 userprincipalname() DAX 函数**

您可以利用数据集内的 DAX 函数  *【用户名()* 或*userprincipalname()*。您可以在 Power BI Desktop 的表达式中使用它们。当您发布您的模型时，它将在 Power BI 服务中使用。

在 Power BI 桌面中，*username()*会以*domain user*和*userprincipalname()*会以*user@contoso.com*的格式返回一个用户。

在 Power BI 服务中，*username()*和*userprincipalname()*都将返回用户的用户主体名称(UPN)。这看起来像一个电子邮件地址。

**在 Power BI 的应用工作区中使用 RLS**

如果您将 Power BI Desktop 报告发布到 Power BI 服务中的应用工作区，这些角色将应用于只读成员。您需要指明成员只能在应用工作区设置中查看 Power BI 内容。

**警告:**如果您已将应用工作区配置为成员具有编辑权限，则 RLS 角色将不会应用于他们。用户将能够看到所有的数据。

![Group settings](img/04b80651f7f32e43998d99621a29a69e.png)

## **Power BI 中的限制行级安全性**

下面是云模型中行级安全性的当前限制列表。

*   如果您以前在 Power BI 服务中定义了角色和规则，则必须在 Power BI Desktop 中重新创建它们。

*   您只能在使用 Power BI Desktop 创建的数据集上定义 RLS。如果要为用 Excel 创建的数据集启用 RLS，必须先将文件转换为 Power BI Desktop (PBIX)文件。  了解更多

*   仅支持 ETL 和 DirectQuery 连接。与 Analysis Services 的实时连接是在内部模型中处理的。

*   RLS 目前不支持 Cortana。

至此，我们结束了 Power BI 中的这种行级安全性。我希望您对行级安全性有所了解。

*如果您希望学习 Power BI，并在数据可视化或 BI 方面建立职业生涯，请查看我们的 [**Power BI 培训认证**](https://www.edureka.co/power-bi-certification-training) ，它附带有讲师指导的现场培训和真实项目经验。本培训将帮助您深入了解 Power BI，并帮助您掌握该主题。*

此外，如果您希望在商业智能领域发展，我们的[商业智能课程](https://www.edureka.co/masters-program/business-intelligence-certification) 将帮助您挖掘这些数据，并增强整个组织的决策过程。

*有问题吗？请在“Power BI 中的行级安全性”的评论部分提到它，我们将会回复您。*