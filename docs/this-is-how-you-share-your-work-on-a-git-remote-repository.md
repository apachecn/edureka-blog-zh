# 这就是如何在 git 远程存储库上共享您的工作

> 原文：<https://www.edureka.co/blog/this-is-how-you-share-your-work-on-a-git-remote-repository/>

*Your work adds more value when published and shared with the world(or your team) !!!*

## ****入门****

**[Git](https://git-scm.com/) ，如你所知，是当今最流行的版本化工具，用于*存储*、*轨道*和*版本*任何种类的*数据*。git 的一些关键特性是它的*速度*、*分布式*性质、*安全性*、无痛*分支和合并*以及多个贡献者之间的 ***协作*** 工作。从这里开始我们的讨论，让我们关注 git 如何帮助您与同行合作和共享您的工作，这样每个人都可以同时处理相同的代码，而不会破坏彼此的数据。这就是远程存储库概念出现的地方。我假设您已经掌握了编辑[的艺术，将您的数据](https://www.edureka.co/blog/how-to-use-github/)从您的*工作目录*(文件系统)添加并移动到*暂存区*，并最终提交到您的*本地存储库*(数据库)。 这激励我们将数据推送到下一个级别“远程回购”,以在远程存储库上发布数据。**

## **我的数据不是已经存储在 git 数据库中了吗？**

**是的，它是！然而，如下图所示，在您*提交*数据后，您的数据仍在*本地数据库*中，尚未与您的同事共享。 ![4-tier architecture](img/8a19e06be263673fc1282bf8867d79ea.png) 这篇文章填补了从您的*本地存储库*获取我们的数据并将其带到下一层*远程存储库*之间的空白。**

## ****什么是远程存储库****

**一个存储在某个位置的收集信息的数据库，通过给你的队友*访问权限*，你的队友就可以*共享*。理想情况下，它托管在互联网或本地网络上的*云*或*服务器*(本地或远程)上。远程存储库就像您的本地 git 存储库一样，除了它通常被声明为一个空存储库，以便没有像您的本地存储库一样的工作副本。这样做是为了限制对远程存储库的直接更改。**

**![Tip](img/3c7351afe70768b50f3c3ee3113c784c.png) <sub> *裸存储库*的概念对于远程存储库来说是一个额外的优势，可以使其*受到保护*，并用于在团队成员之间共享代码的唯一目的。</sub> 这是通过在将远程存储库初始化为 g it 存储库时使用“`--bare`”标志将远程存储库声明为空来实现的。通过这样做，你的 repo 是用 git 元数据创建的，或者换句话说，git 对象存储在 hidden '下。git '目录，没有工作副本可供任何人直接添加数据。命令:`git init --bare .` 记住这一点，接下来我们将看到更多管理远程回购的方法，以及如何将本地工作与远程同步。**

## ****创建远程存储库****

**首先也是最重要的，你需要决定一个你想要放置远程回购的位置。有很多流行的基于云的 git 托管库，比如——[git lab](https://about.gitlab.com/product/source-code-management/)、 [BitBucket](https://bitbucket.org/product?&aceid=&adposition=1t1&adgroup=55499712476&campaign=1407242849&creative=377552232607&device=c&keyword=bitbucket&matchtype=e&network=g&placement=&ds_kids=p33211115881&ds_e=GOOGLE&ds_eid=700000001551985&ds_e1=GOOGLE&gclid=CjwKCAjw1_PqBRBIEiwA71rmta6mJpXq5oxBBXrLk-XM7OI-lZe4gc5OzV15Rern_6NnHBa1xwpl4xoCEhoQAvD_BwE&gclsrc=aw.ds) 、 [GitHub](https://github.com/) 、 [Perforce](https://www.perforce.com/) 和 [CloudForge](http://www.cloudforge.com/) 等等。在这篇文章中，我考虑 GitHub，因为这是我第一次开始保存我的 git 库的地方。首先，你要做的就是登录 GitHub 账户，然后[创建一个新的存储库](https://git-scm.com/book/en/v2/GitHub-Maintaining-a-Project)，这将创建一个指向这个远程存储库的 URL。 ![GitHub remote repository](img/d7b278a0c3922dee2ca74e8b683d94f0.png) Git 支持 ssh、Git、http 和 https 协议来寻址存储库 URL。 或者，你也可以把你的项目放在其他地方，比如说一个 *Linux 服务器*遵循下面的命令-`cd $HOME``mkdir remote_repo``cd remote_repo``git init --bare .`![bare repo on Linux Server](img/28257db89dfd486c1c3322831e383f38.png)**

## ****将遥控器连接到您的本地机器上****

**将一个遥控器附加到你的工作副本仅仅意味着为该遥控器创建一个 ***指针引用处理程序*** ，或者简称为“*遥控器处理程序*”。让我们跳转到我要发布的项目- `cd learnRemotes` 语法:`git remote add <remote_name> <url>` 命令:`git remote add origin https://github.com/divyabhushan/learnRemotes.git` ***“原点*** 是*默认*远程处理程序的引用名。”(远程名称必须是一些相关的名称)让我们看看这是否有效，使用命令:`git remote` ![Show remote](img/5082ede0348b6f328835592ced7be2a3.png) 它做到了:) 打印远程 URL 以及名称: git remote -v ![show remote in verbose](img/2c3b0514430611d3a19cc3bf603957f9.png) 干得好！您已经准备好从本地工作目录建立到远程存储库的连接。**

## ****发布时间****

**语法:`git push --all --tags` `[-u | --set-upstream] <repository>` 命令:`git push origin master` ![first push from local to remote](img/2f8c32196186a2542ba00903125b314a.png) 所以，你把这个读成*“把提交的 diff 从本地主推送到原点”*。 如果您检查您的 GitHub 帐户，您的本地提交(数据)必须显示在那里- ![first push displayed on github](img/e7e5a8f17e80918ccb13f2164c86fffa.png)**

## ****跟踪分支机构****

**那么，您已经成功地在远程存储库上发布了您的作品。然而，重要的是您要建立本地分支来*自动跟踪*远程分支上的变化。使用“`--set-upstream`或`-u`”标志和“git push”命令命令:`git push -u origin master`![local master track origin/master](img/18b48228656dc6de7fed58e4cd186ba6.png)![color coded branches](img/03a5d26dc41f2e752527f535318de7fd.png)让我们进一步在“主”分支上创建一个新的提交，并验证 git 如何检测到它- 命令:`git status` ![local/master ahead of origin/master](img/eb03155270edfc3c0f70652dbb525c3e.png) 以详细模式显示跟踪分支命令:`git branch -vv` ![branch tracking](img/e1f0551d1174907d1df423647837073d.png) 因此每次  是不是很酷！！！**

## **其他人如何连接到您的遥控器？**

**当你用 ***克隆*** 一个远程储存库的时候简直易如反掌！！！ ![tip](img/4825eea85b76d65947b53b287080a339.png) 因此，从远程存储库克隆首先做两件事，你的*远程引用*被自动添加，第二个默认*分支*被自动设置为*跟踪* *远程分支*。 **步骤 1:** 将您的远程回购克隆为不同的用户- 命令:`git clone https://github.com/divyabhushan/learnRemotes.git developer2` `cd developer2` **步骤 2:** 显示远程及其 url 命令:`git remote -v` ![show remote verbose](img/f519833eefe945515abad7310e4c82ad.png) **步骤 3:** 列出跟踪分支命令:`git branch -vv` ![tracking branch](img/1574e96bcf894f09cbdb0272693b6bf8.png)  乐趣开始于 ![tip](img/4825eea85b76d65947b53b287080a339.png) 您可以从一个*单个项目*中连接并贡献给*多个远程*存储库。**

## ****查看远程分支机构****

**命令:`git branch -r` ![list remote branch](img/a50e8ac61545116fbb4e66ea47c08236.png) 使用“-a”选项打印本地和远程分支，在创建几个本地分支后，在您的本地回购中尝试一下。**

## ****别人如何促成你的远程？****

****初始设置** 开发者 2 决定改变几件事情，例如: **a.** *从“主”分支上的最新提交中创建*一个新的“特征”并在“特征”分支上进行*新的提交*命令:`git checkout -b feature``echo "feature enhancements">feature.txt``git add . && git commit -m 'feature enhancements'`**b .***创建*一个不同的“特征” 让我们将 developer2 机器上的分支与跟踪信息一起可视化: ![new feature branches](img/2f0b6aeddb6c0e3df5c771659f4c0d55.png) 您一定已经注意到，新分支并没有被设置为跟踪远程分支。 **将变更推至远程** 首先让我用“–set-upstream 或-u”标志将‘特征’分支推至远程命令:`git push -u origin feature`**

**![new feature branch pushed](img/febfc5ea235121e1482d4d73958d9250.png) ![tip](img/4825eea85b76d65947b53b287080a339.png) 将在远程上创建一个新分支，如果它不存在的话！！！ 此时，用命令列出远程分支:“git branch -r”**

**![remote 'feature' branch created](img/27449fb0d45ee294e6611eddee4b0752.png) **跟踪远程分支的另一种方式** 此外，让我们将“功能 2”分支也设置为指向远程命令上的相同“功能”分支:`git branch --set-upstream-to=origin/feature feature2`**

**![feature2 tracks origin/feature](img/0ce862e3eb735f997c5c1da8d6303563.png)![color coded branch](img/192294c2eb50690731030d1567d3da21.png)A quick tip: You may omit the local branch name if you are already on that branch, in other words, the local branch is already checked-out.List the branches in verbose mode yet again, command: `git branch -vv`**

**![2 local branches pointing to remote](img/212e7746b7f5d950d73d325de2d5e7ba.png) 注意，本地分支‘feature’和‘feature 2’都指向同一个远程分支‘feature’。**

## ****与遥控器保持同步——取、拉、推****

**让我们考虑你正在跟踪的*远程分支*已经更新的部分，然后呢？一个简单的“`git status`”或“`git checkout <branch_name>`”甚至“`git branch -vv`”命令警告我们这样的不匹配-**

**![local and remote diverged](img/8dff36de22e49b4ba09a0de23f673af8.png)“developer 2”必须首先更新本地引用和对象([git fetch](https://git-scm.com/docs/git-fetch)’)，然后合并远程和本地更改(“git merge”)。有趣的是，您可以用一个‘git pull’命令替换这两个命令。 语法:`git` `pull` `<options> <remote_repository> <local_refspec...>`–对于未被跟踪的分支语法:git pull<remote _ repository><remote _ branch>:<local _ branch>命令:`git pull origin feature:feature2`–对于被跟踪的分支语法:git pull<remote _ repository>命令:`git pull`**

**![git pull](img/2e11fcfb5c98cbf59a1eea96d302a0ab.png)=> In practice, there may be conflicts arising at this stage when you pull from remote for simplicity I have generated a no-conflict commit change.After ‘developer2’ pull (fetch and merge) the remote latest changes must now publish his own work-Command: `git push origin HEAD:feature` 注意:上游分支“特征”与本地分支“特征 2”名称不匹配，您必须明确提供**

**![](img/a97acb50cd6f63bd356bfdb9ab86696f.png) * **提醒***:‘HEAD’是本地‘feature 2’分支上的最新提交。**

**![tip](img/4825eea85b76d65947b53b287080a339.png) **什么时候用‘git fetch’？** 有时，您只需更新您的*参考头*，而无需从遥控器下载(拉取)。或者当远程分支在更新时被修改/删除时，您将必须运行带有“`--prune`”选项的获取命令。作为最佳实践，每次开始处理本地回购时，您都必须运行“git fetch”命令。**

## ****远程管理****

**最后，您可能希望执行一些日常工作，比如重命名或删除远程和分支。这些和前面的命令一样重要。**

### **重命名遥控器**

**语法:`git remote rename <old_name> <new_name>` 命令:`git remote rename snv_repo svn` 例如，考虑一个项目经理与 3 个项目相关联-**

**![rename remote](img/3c44b0c863a3a90584dba571c8741bc1.png)**

### **删除远程引用**

**假设您不再与远程存储库同步，您可能会删除指向它的指针。但是，这不会影响远程存储库和其他人的工作。 语法:`git remote remove <remote_ref_name>` 命令:`git remote remove proj1`**

****

**![tip](img/ddd93755e3fa3ed222981b7941f161a0.png)如果您设置了一个本地分支来跟踪已删除的“项目 1”存储库中的一个分支，会怎么样？好了，你的*本地分支*(因此工作)是*安全的*并且仍然存在，只是它的*远程跟踪参考*和*配置*设置将被*自动移除***

### **删除远程分支**

**假设你*不小心*将你*个人*在*分支上的粗糙工作推到了远程*上，但是还不想让其他人检查它-从远程“svn”中删除“未完成工作”分支- 命令:`git branch -vv`#列出远程跟踪分支**

**![remote urls](img/54dd630bb8db0e56c72ef7310f81fbea.png) 语法:`git push --delete <remote_repo> <branch_name>` 命令:`git push --delete svn unfinishedWork`**

****

## ****清盘****

**![Summary of commands used](img/989d0e6591dd25a30817ef9478915c59.png)**

**到此，我们来结束这篇文章。*如果你发现了这个* ***教程****相关，请查看 Edureka 的* [***DevOps 培训***](https://www.edureka.co/devops) *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 25 万多名满意的学习者。Edureka DevOps 认证培训课程可帮助学员获得各种 DevOps 流程和工具方面的专业知识，例如 Puppet、Jenkins、Nagios 和 GIT，用于自动化 SDLC 中的多个步骤。***