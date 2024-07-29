谷歌浏览器设置中“提示保存密码”已经打开，“自动登录”也已经打开。-

但是访问网站未登录时都不自动填充密码。

-

解决方案：

1.设置-自动填充-密码中，找到密码提醒，进行忽略警告（这步可忽略）

-

2.打开目录：C:\\Users\\你的用户名\\AppData\\Local\\Google\\Chrome\\User Data\\Default

删除 Login Data 和 Login Data-journal 两个文件。

![image.png](https://www.eqishare.com/zb_users/upload/2022/02/202202241645668679640805.png)

然后重新启动浏览器，再试就可以自动填充了。

-

-

本文转自 [https://www.eqishare.com/technology/916.html](https://www.eqishare.com/technology/916.html)，如有侵权，请联系删除。