**![GitHub打不开-封面.jpg](https://www.eqishare.com/zb_users/upload/2022/06/202206151655256860780233.jpg)**

**FastGit 是一个对于 GitHub.com 的镜像加速器。我们使用开放资源为 GitHub 加速。**

![20220228140332.png](https://www.eqishare.com/zb_users/upload/2022/02/202202281646028527870968.png)

![20220228140345 (1).png](https://www.eqishare.com/zb_users/upload/2022/02/202202281646028538403804.png)

-

使用指南
====

请在同意我们服务条款和隐私协议后，再进行下一步。如若进行，我们将默认视为同意并遵守我们的服务条款和隐私协议。

WARNING

由于不可抗逆的因素，我们已经将我们的枢纽链接从 hub.fastgit.org 更新到 hub.fastgit.xyz。

关于 FastGit 的使用，本质上与 `git` 有关。常规的面向 GitHub 的 `clone` 命令可能如下：

git clone https://github.com/author/repo

使用 FastGit 时，可使用如下命令：

git clone https://hub.fastgit.xyz/author/repo

正如您所见， FastGit 仅仅是 GitHub 的代理，所以我们仅需要替换远程地址。

当然，您也可以直接修改 `git` 的配置，使用 FastGit 替换所有指向 GitHub 的链接：

git config --global url."https://hub.fastgit.xyz/".insteadOf "https://github.com/"git config protocol.https.allow always

注意

当您排查网络错误时别忘了看看 FastGit 是否宕机了，尽管我们提供高达 0% 可用性的 SLA 保障。

注意

我们暂时不支持超过 2GiB 的仓库的 `clone`，请参阅 [https://github.com/FastGitORG/nginx-conf/issues/14 (opens new window)](https://github.com/FastGitORG/nginx-conf/issues/14)与 [https://github.com/FastGitORG/nginx-conf/commit/61a41bc0bbb012fc9a6e54b198a10874eeaf9309 (opens new window)](https://github.com/FastGitORG/nginx-conf/commit/61a41bc0bbb012fc9a6e54b198a10874eeaf9309)。

我们并不反对对 git 配置的修改以方便您的工作。

随着 FastGit 的成长，我们会拥有更多资源用于加速，对于节点列表，请参阅 [节点](https://doc.fastgit.org/zh-cn/node.html) 章节。

[#](https://doc.fastgit.org/zh-cn/guide.html#web-%E7%9A%84%E4%BD%BF%E7%94%A8)Web 的使用
------------------------------------------------------------------------------------

对于常见的 GitHub Web 操作， FastGit 的基础节点也提供了最基本的支持。您可以直接访问包含有 Web 支持的节点。出于安全考虑，我们会禁用包括 `Cookie` 以及 `Session` 等敏感权限。这意味着您不能登录进行操作。

[#](https://doc.fastgit.org/zh-cn/guide.html#release-%E5%92%8C%E6%BA%90%E7%A0%81%E5%AD%98%E6%A1%A3%E7%9A%84%E4%B8%8B%E8%BD%BD)Release 和源码存档的下载
----------------------------------------------------------------------------------------------------------------------------------------------

对于正常的 `clone` ， `push` 操作，FastGit 已经提供了相当完善的操作。对于 Release 和源码存档的下载，我们可以使用如下方法进行操作。

\# Release# 假设下载链接为 https://github.com/A/A/releases/download/1.0/1.0.tar.gzwget https://download.fastgit.org/A/A/releases/download/1.0/1.0.tar.gz# Codeload# 假设下载链接为 https://hub.fastgit.xyz/A/A/archive/master.zip# 或者 https://codeload.github.com/A/A/zip/masterwget https://download.fastgit.org/A/A/archive/master.zip

[#](https://doc.fastgit.org/zh-cn/guide.html#ssh-%E6%93%8D%E4%BD%9C)SSH 操作
--------------------------------------------------------------------------

我们同样支持 SSH 克隆，您只需要把地址更换为 fastgit.org 即可。

由于不可抗逆因素，我们暂不支持 SSH 克隆。

26/06/2021 更新：由于 2FA 问题持续存在，所以我们很难以通过 HTTPS 的方法完成很多事。鉴于目前情况，我们继续开放了 SSH 操作入口。

与之前不同，我们拆分了 SSH 服务所在的域名，换句话说并不能通过替换地址为 FastGit.org 完成操作。

目前我们的 SSH 克隆地址为 ssh.fastgit.org。只需要修正地址即可完成加速。

[#](https://doc.fastgit.org/zh-cn/guide.html#%E5%AF%B9%E4%BA%8E-raw-%E7%9A%84%E4%BB%A3%E7%90%86)对于 raw 的代理
----------------------------------------------------------------------------------------------------------

我们同样对 [https://raw.githubusercontent.com/ (opens new window)](https://raw.githubusercontent.com/)进行了代理，地址为 [https://raw.fastgit.org/ (opens new window)](https://raw.fastgit.org/)。

-

**官网：**[**http://fastgit.org/**](http://fastgit.org/)

**加速github地址：**[**https://hub.fastgit.xyz/**](https://hub.fastgit.xyz/)

**测试项目：**[**https://hub.fastgit.xyz/zhaolu678**](https://hub.fastgit.xyz/zhaolu678)

-

-

本文转自 [https://www.eqishare.com/technology/917.html](https://www.eqishare.com/technology/917.html)，如有侵权，请联系删除。