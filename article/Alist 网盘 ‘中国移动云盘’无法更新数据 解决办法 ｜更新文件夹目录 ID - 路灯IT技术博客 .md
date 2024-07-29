> **问题**

使用 alist网盘，最近中国移动云盘，可以加载出来数据，只是前几天的，昨天今天的都不更新。

> **排查问题**

查看官方文档

[https://alist.nn.ci/zh/guide/drivers/139.html](https://alist.nn.ci/zh/guide/drivers/139.html)

可以看到有一个说明：![更新.png](https://www.eqishare.com/zb_users/upload/2024/07/202407111720665471777773.png)

类型 个人云：选择个人云 家庭云：选择家庭云 新个人云：新版API 新注册的账号才有，可以通过在请求搜索 getDisk 来区分，如果能搜到就是旧版的，不能搜到就是新版的 如果是新API无法使用 个人云类型，虽然没有错误信息，但是文件不会被加载 有getDisk请求的无法使用新个人云类型，否则会提示用户不存在

> 解决思路-

根据说明查下现在的请求中没有 getDisk 请求，所以属于新版。

新版按照官方的方法如图：-

![](https://www.eqishare.com/zb_users/upload/2024/07/202407111720665481541638.png)

按照此方法无法获取到目录文件夹 ID，分析应该是官方有更新，所以分析新的请求，

目前只有一个 list 请求，看到请求参数中有个“parentFileId”参数，很有可能是。

![WX20240711-103939@2x_(1) (1).png](https://www.eqishare.com/zb_users/upload/2024/07/202407111720665828864594.png)

**所以更新下配置：**

**Authorization还是原来的；**

**（只需要填写Basic空格后面开始的内容）**

**目录文件夹 id 更新为“parentFileId”；**

**类型选择“新的个人盘”。**

-

配置上原来的问题就修复了，刷新可以显示最新的数据了。

-

![后台.png](https://www.eqishare.com/zb_users/upload/2024/07/202407111720665471439136.png)

-

-

-

-

-

本文转自 [https://www.eqishare.com/technology/1223.html](https://www.eqishare.com/technology/1223.html)，如有侵权，请联系删除。