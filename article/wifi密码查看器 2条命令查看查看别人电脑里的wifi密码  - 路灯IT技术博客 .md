![037 获取电脑wifi密码-封面.jpg](https://www.eqishare.com/zb_users/upload/2022/09/202209021662089961745740.jpg)

有无线网卡，并且wifi链接过的才可以查看。

工具查看：

![wifi密码查看器.png](https://www.eqishare.com/zb_users/upload/2022/08/202208301661826147243902.png)

工具地址：[http://download0.eqishare.com/f/37298141-660705647-e37b00](http://download0.eqishare.com/f/37298141-660705647-e37b00)

易语言源码：[https://fan67.lanzouw.com/iyjmi09jq57c](https://fan67.lanzouw.com/iyjmi09jq57c)

-

命令查看：-

一、运行CMD（命令提示符） （确保无线网卡启用状态）-
二、输入命令：-

netsh wlan show profiles

三、然后CMD就列出所有连接过的WiFi的配置名-
四、输入命令：-

netsh wlan show profiles name="wifi名称" key=clear

就可以查看到某个具体WiFi的配置详情，包括密码。-
如果自己知道WiFi名称就可以直接执行这个命令！就不需要执行上一个命令了。上个命令行的作用主要用来查看和确认WiFi名称的。-
参数:-
 标记 值-
 name - 所要显示配置文件的名称。-
 interface - 已配置此配置文件的接口的名称。-
 key - 以纯文件显示密钥，设置密钥=clear-

![cmd命令查看wifi密码.png](https://www.eqishare.com/zb_users/upload/2022/08/202208301661826196259389.png)

-

本文转自 [https://www.eqishare.com/technology/987.html](https://www.eqishare.com/technology/987.html)，如有侵权，请联系删除。