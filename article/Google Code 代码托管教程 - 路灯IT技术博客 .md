一 创建托管账户-
1 首先应有一个 google 帐号(用你的gmail邮件地址可以注册)-
-
2 访问项目托管地址：[http://code.google.com/hosting/](https://www.eqishare.com/technology/877.html) 点击下面的 "Sign in to create a project" 链接-
-
3 点击 页面下方的 "Create a new project" 创建一个项目-
-
4 以此填写 项目名称、摘要、介绍、开源协议等等（除了项目名称不能更改之外其他选项在项目创建之后都可以更改）-
-
5 在注册完之后会自动跳转到项目主页了（我们注册的项目名称为 xxxx，随意项目主页的链接地址为[http://code.google.com/p/xxxx/](https://www.eqishare.com/technology/877.html)）注意(Note)：一个注册帐号最多只能创建10个项目。如果需要更多的项目，可以到google-code-hosting Google Group商议！-
-
\---------------------------------------------------------------------------------------------
-
二 添加项目成员-
-
1 使用项目创建者用户，访问项目主页。点击 administer 选项卡下的 Project Members 链接,在Project Member 文本框中添加成员的邮件地址()即可，成员之间用换行或空格分割。这样成员在登录之后就可以checkout 项目文件了。-
-
\-------------------------------------------------------------------------------------------
-
三 使用 svn 软件 checkout 项目文件-
-
1 使用你的成员帐号登录，访问项目主页（[http://code.google.com/p/xxxx/](https://www.eqishare.com/technology/877.html)）下的 Source 选项卡下的 Checkout 页面，这里会给出 checkout 项目的url (例如[https://jlufirefox.googlecode.com/svn/trunk/](https://www.eqishare.com/technology/877.html))，如下:-
-
2 获得密码，点击 “googlecode.com password”链接会自动跳转到含有密码的页面，例如这里密码为 wp5zm6tr6RN6，如果点击 Regenerate 按钮会重新生成新的密码。-
-
3 使用 svn 软件 checkout 项目文件(这里我们以 TortoiseSVN 为例)-
-
3.1 新建一个 目录，右键选择 “svn checkout..”-
-
3.2 输入checkout 链接地址，[https://jlufirefox.googlecode.com/svn/trunk/](https://www.eqishare.com/technology/877.html) ，然后输入用户名和密码（上面提到的，用户名就是你的项目用户名）。-
-

-

本文转自 [https://www.eqishare.com/technology/877.html](https://www.eqishare.com/technology/877.html)，如有侵权，请联系删除。