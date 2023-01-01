# 前 20 个 Git 命令及示例

> 原文：<https://www.edureka.co/blog/git-commands-with-example/>

[***Git&GitHub 认证***](https://www.edureka.co/git-github-sp) 如今已经从仅仅是一项首选技能稳步上升为多种工作角色的必备技能。在这篇博客中，我将谈论您在使用 Git 时经常使用的前 20 个 Git 命令。

以下是所涉及的 Git 命令:

*   **[【git 配置】](#git%20config)**
*   **[git init](#git%20init)**
*   **[【git 克隆】](#git%20clone)**
*   **[去添加](#git%20add)**
*   **[去委员会](#git%20commit)**
*   **[【git diff】](#git%20diff)**
*   **[去复位](#git%20reset)**
*   **[git 状态](#git%20status)**
*   **[git RM](#git%20rm)**
*   **[git 日志](#git%20log)**
*   **[git 显示](#git%20show)**
*   **[git 标签](#git%20tag)**
*   **[吉特科](#git%20branch)**
*   **[吉特结账](#git%20checkout)**
*   **[git merge](#git%20merge)t5**
*   **[走远点](#git%20remote)**
*   **[饭桶推](#git%20push)**
*   **[吉特拉](#git%20pull)**
*   **[git stash](#git%20stash)**

那么，现在就开始吧！！

## **Git 命令**

### **【git 配置】**

**用法:git config–global user . name "[name]"**

**用法:git config–global user . email "【电子邮件地址】"**

该命令分别设置提交时使用的作者姓名和电子邮件地址。

![Git Config Command - Git Commands - Edureka](img/1ebf5229577ffe0c89cac83343a9b347.png)

### **git init**

**用法:git init【库名】**

该命令用于启动一个新的存储库。

![GitInit Command - Git Commands - Edureka](img/c6f3203b9f3f873b333fc201b9ab7f32.png)

### **【git 克隆】**

**用法:git 克隆[URL]**T3]

该命令用于从现有的 URL 获取存储库。

![Git Clone Command - Git Commands - Edureka](img/3133bccd533c39ae7c8bb8c0ff0c8c3d.png)

### **去添加**

**用法:git 添加**

该命令向暂存区添加一个文件。

![Git Add Command - Git Commands - Edureka](img/63afc6571a1b0914ba0f8495ebd8ad38.png)

**用法:git add ***

该命令向暂存区添加一个或多个。

![Git Add Command - Git Commands - Edureka](img/98b8b3d58e0bfde2e77e3a481b639150.png)

### **去委员会**

**用法:git commit -m "[键入提交消息]"**

该命令在版本历史中永久记录或快照文件。

![Git Commit Command - Git Commands - Edureka](img/fbd5639fc084da05a9773fde4b14ee63.png)

**用法:git commit-a**

这个命令提交你用 git add 命令添加的任何文件，也提交你从那以后修改过的任何文件。

![Git Commit Command - Git Commands - Edureka](img/9b58b74472333d1be0068b070f1b14a4.png)

### **【git diff】**

**用法:git diff**

该命令显示尚未暂存的文件差异。

![Git Diff Command - Git Commands - Edureka](img/1d2072f0d961e2b45da54cf54aa78e36.png)

**用法:git diff–staged**

该命令显示暂存区中的文件与当前最新版本之间的差异。

![Git Diff Command - Git Commands - Edureka](img/9e3be2f25b5142936103067e190179dc.png)

**用法:git diff【第一分支】【第二分支】**

该命令显示了上述两个分支之间的差异。

![Git Diff Command - Git Commands - Edureka](img/1356ff638e853b42c5a485ce2b97e799.png)

## **Git 命令示例| Edureka**

### **去复位**

**用法:git 重置【文件】**

该命令将文件拆分，但保留文件内容。

![Git Reset Command - Git Commands - Edureka](img/ebdacb1c5c25a324a6fbdff6902fc533.png)

**用法:git reset【提交】**

该命令撤销指定提交后的所有提交，并在本地保存更改。

![Git Reset Command - Git Commands - Edureka](img/f23390b3336318e6d5718a6257ef5030.png)

**用法:git reset-hard**

该命令丢弃所有历史记录，并返回到指定的提交。

![Git Reset Command - Git Commands - Edureka](img/12608396f60930d5a3901365a178e1e2.png)

### t1【去状态】T2

**用法:git 状态**

该命令列出了所有必须提交的文件。

![Git Status Command - Git Commands - Edureka](img/c0887795eeeab66f8383e1e91e97751f.png)

### **git RM**

**用法:git RM[文件]**T3]

这个命令从你的工作目录中删除文件，并分阶段删除。

![Git Rm Command - Git Commands - Edureka](img/41cf3a76214019247c6a104842a2cd76.png)

### **去日志**

**用法:git 日志**

该命令用于列出当前分支的版本历史。

![Git Log Command - Git Commands - Edureka](img/2bdcee0393cc36de2deb6f29a8ddee25.png)

**用法:git log–follow【文件】**

该命令列出了文件的版本历史，包括文件的重命名。

![Git Log Command - Git Commands - Edureka](img/8562adb49a3e9974fcbfdceacc045ab8.png)

### **上节目**

**用法:git show**

该命令显示指定提交的元数据和内容变化。

![Git Show Command - Git Commands - Edureka](img/082395bbd611fa8051bebd8c2d28a00a.png)

### **git 标签**

**用法:git 标记[commitid]**T3]

该命令用于给指定的提交赋予标签。

![Git Tag Command - Git Commands - Edureka](img/16aeb4982d88a89438c116350d50ee68.png)

### **去分支机构**

**用法:git 分支**

该命令列出了当前存储库中的所有本地分支。

![Git Branch Command - Git Commands - Edureka](img/36ee6731f6523a55e4d1f8d20a457d61.png)

**用法:git 分支【分支名称】**

该命令创建一个新的分支。

![Git Branch Command - Git Commands - Edureka](img/5da8e29a07ca01d8bc4c0ed003c18004.png)

**用法:git branch -d【分支名称】**

该命令删除特征分支。

![Git Branch Command - Git Commands - Edureka](img/9a7efaace50ba74485d65e94d7d18ace.png)

### **git 结账**

**用法:git 结帐【分行名称】**

该命令用于从一个分支切换到另一个分支。

![Git Checkout Command - Git Commands - Edureka](img/1c45ba630b638682587b72a57180bba0.png)

**用法:git checkout -b【分行名称】**

该命令创建一个新分支并切换到该分支。

![Git Checkout Command - Git Commands - Edureka](img/2865f48784f280af193850a48c8f0944.png)

### **去髓** 去髓

**用法:git merge【分支名称】**

该命令将指定分支的历史合并到当前分支。

![Git Merge Command - Git Commands - Edureka](img/eda9297368145683eebea624e5d41d55.png)

### **去远端**

**用法:git 远程添加【变量名】【远程服务器链接】**

该命令用于将您的本地存储库连接到远程服务器。

![Git Remote Command - Git Commands - Edureka](img/53bc517f3a68f7117b976e734d22eb63.png)

### **git 推送**

**用法:git push【变量名】master**

该命令将主分支提交的更改发送到您的远程存储库。

![Git Push Command - Git Commands - Edureka](img/a3420cb73cdb8d10d9e2c8022a4eda21.png)

**用法:git 推送【变量名】【分支】**

这个命令将分支提交发送到您的远程存储库。

![Git Push Command - Git Commands - Edureka](img/8b666812c1f1a668e72ba31a6ca5e3db.png)

**用法:git push–all【变量名】**

该命令将所有分支推送到您的远程存储库。

![Git Push Command - Git Commands - Edureka](img/764e2e7fb76a2f792c54bfbc6b6d64cc.png)

**用法:git push【变量名】:【分支名】**

该命令删除远程存储库上的一个分支。

![Git Push Command - Git Commands - Edureka](img/916b7e3fa914ff2b5a55102b72cd5193.png)

### **吉特拉**

**用法:git pull【资源库链接】**

这个命令获取并合并远程服务器上的更改到你的工作目录。

![Git Pull Command - Git Commands - Edureka](img/c89b4137faa27ac4958a37d364f460cb.png)

### **git stash**

**用法:git sta save**

该命令临时存储所有修改过的跟踪文件。

![Git Stash Command - Git Commands - Edureka](img/e0af699ce21d657947e6e033ccfc7487.png)

**用法:git stash pop**

该命令恢复最近隐藏的文件。

![Git Stash Command - Git Commands - Edureka](img/4f1fefd03b4df24ecc4ddffe7ce63395.png)

**用法:git stash list**

这个命令列出了所有隐藏的变更集。

![Git Stash Command - Git Commands - Edureka](img/d5d064af1376f10a224a5f045f5f20a4.png)

**用法:git stash drop**

这个命令丢弃最近隐藏的变更集。

![Git Stash Command - Git Commands - Edureka](img/43df6277fe630e1f2415c8ece3145af4.png)

想要了解更多关于 git 命令的信息吗？这里有一个 [**Git 教程**](https://www.edureka.co/blog/git-tutorial/) 让你入门。或者，你可以采取自上而下的方法，从这篇 **[DevOps 教程开始。](https://www.edureka.co/blog/devops-tutorial)**