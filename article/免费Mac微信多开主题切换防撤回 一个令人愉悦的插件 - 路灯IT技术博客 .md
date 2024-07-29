**Mac微信功能拓展/微信插件/微信小助手(A plugin for Mac WeChat)**

**视频教程**

**迷离/黑夜/上帝/少女 皮肤模式**

少量细节没有做适配，主题模式-关闭皮肤可以关掉这个功能。

群聊中每个发言人的昵称颜色都会有所区别。

在皮肤模式下，未读消息头像会轻微可爱摇动，未读数超过99条的会话有彩蛋。

如果你的迷离模式未生效，打开系统偏好设置 -> 辅助功能 -> 显示，不要勾选减少透明度或提供对比度。

上帝模式可选一张图片做背景。

![皮肤模式.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600538636063.png)

切换模式

![切换模式.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600615153334.png)

**僵尸粉检测**

无感检测！（发布的第三天就有XX公众号公布了检测漏洞，已被封，切勿再使用。）

**手机端也能收到被撤回的消息**

如果Mac拦截到A发送来的消息，手机也会同步收到的这条已经拦截的消息(自己发送给自己)。目前只支持同步文字消息与图片消息。

可以对同步的消息进行勾选，以免群消息打扰。

![手机端也能收到被撤回的消息 .png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600932261049.png)

**消息转发**

Mac可实现多开，出门在外手机却不能，怎样在同一台手机上实现多个微信号消息的监听？

iPhone上可安装自签的微信包，实现多开，但是Bundle Id的改变导致APNS消息推送异常，无法收到消息推送？

目前只能转发文字消息。选择转发所有好友消息时，只转发单聊消息，不转发群聊消息。

![消息转发.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600707557680.png)

**免认证登录与多开**

可以同时登录多个微信号。

![免认证登录与多开.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600727566821.png)

**同时支持自定义回复和AI自动撩妹**

腾讯AI人工智能自动回复，能理解上下文语义。大量临床试验和大家反馈，腾讯这个AI接口回复不够完善，慎用。

自定义自动回复。

![同时支持自定义回复和AI自动撩妹.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600744814874.png)

**显示小程序详情**

即便Mac微信现在可以打开小程序，暂时还不支持游戏小程序，所以保留了此功能。

![显示小程序详情 .png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600760684965.png)

**Alfred**

确保你电脑中有安装Alfred，双击此文件进行安装。

![Alfred.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600774225462.png)

依次点击 小助手 -> 开启Alfred功能

打开你的Alfred搜索框，输入 wx (wx后面接一个空格)，即可开启Alfred控制微信之旅

**退群监控**

退群提醒，同一人在同一群里的退出提醒7天内不再重复提示。

![退群监控.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600788730012.png)

**群员监控**

微信版本>=2.4.2（15650）才支持此功能。

群员监控Window中，鼠标右键单击左侧Session列表某行出现拒收消息，可以在Mac上完全拒收此群消息，避免打扰。

右侧列表是依次是昵称、相关发言时间与条数、违规言论、拼多多砍一刀。

此功能暂时属于实验性质。

![群员监控.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682600804205064.png)

**怎么安装?**

**安装方式一：普通安装(clone最新版本并安装)**

sudo rm -r -f WeChatExtension-ForMac && git clone --depth=1 https://github.com/MustangYM/WeChatExtension-ForMac && cd WeChatExtension-ForMac/WeChatExtension/Rely && ./Install.sh && cd ~

**安装方式二：懒癌版安装**

打开应用程序-实用工具-Terminal(终端)，执行下面的命令安装 Oh My WeChat：（Oh My WeChat只需安一次，以后就只需执行 omw或omw -n即可）

curl -o- -L https://omw.limingkai.cn/install.sh | bash -s

Oh My WeChat一键命令

omw

跳过检查更新的步骤，优先使用下载过的安装包安装小助手。

omw -n

omw 会从 GitHub 仓库检查更新及下载安装包，但由于网络不稳定，下载可能会失败，但你还可以使用 omw load 命令安装小助手。

安装完成后会自动安装微信插件，可以访问 Oh My WeChat 的项目主页查看更多用法。

**安装方式三：手动安装**

3.1.确保你的Mac上已经安装了微信App。

3.2.下载本项目到你的电脑里， 并双击打开。

![3.2.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682601921158536.png)

3.3.依次打开文件夹WeChatExtension/Rely/Install.sh。

3.4.将Install.sh拖入终端工具中按回车执行安装。

![3.4.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682601945845426.png)

3.5.重启微信，安装完成。

**怎么卸载?**

**卸载方式一：自动卸载（推荐）**

bash <(curl -sL https://git.io/JUO6r)

**卸载方式二：手动卸载**

将Uninstall.sh拖到终端工具中，回车执行即可。

![uninstall.png](https://www.eqishare.com/zb_users/upload/2023/04/202304271682601964510076.png)

**卸载方式三：使用 Oh My Wechat 卸载**

如果你安装了 Oh My WeChat，那么运行下面的命令即可：

omw un

**下载地址及官网：**

此处为隐藏内容，请评论后查看隐藏内容，谢谢！评论后看不到请[再刷新网页](javascript:location.reload();)

-

-

本文转自 [https://www.eqishare.com/technology/1069.html](https://www.eqishare.com/technology/1069.html)，如有侵权，请联系删除。