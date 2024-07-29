Google翻译正式退出中国。目前，这款App已经关闭了这一地区的访问权限，用户被定向到一个普通的搜索栏，并建议将该App的中国香港版本加入书签。

![WX20221010-213022@2x (1).png](https://www.eqishare.com/zb_users/upload/2022/10/202210101665408660223336.png "WX20221010-213022@2x (1).png")

谷歌Chrome谷歌浏览器是目前国内使用率最高的浏览器之一。这次暂停服务直接影响了浏览器内置的“网页自动翻译”功能，给无数国内用户浏览外文网站和查阅英文资料带来了极大的不便！如果你经常使用谷歌Chrome的网页翻译功能办公和学习,那无疑是非常不便，那如何才能解决呢？

![谷歌翻译.png](https://www.eqishare.com/zb_users/upload/2022/10/202210111665456003523974.png)

1.找到 Hosts 文件所在路径：

Windows 系统 Hosts 文件路径：C:\\Windows\\System32\\drivers\\etc\\hosts Mac 或 Linux 系统 Hosts 文件路径：sudo vim /etc/hosts Android 系统 Hosts 文件路径：/system/etc/hosts

2.找到可用的地址

去站长工具[ping.chinaz.com](http://ping.chinaz.com/)，查找[translate.google.cn](http://translate.google.cn/)的响应ip，找一个国内地址，响应时间和TTL比较短的。

![](https://www.eqishare.com/zb_users/upload/2022/10/202210101665408824539070.png "WX20221010-213144@2x (1).png")

![](https://www.eqishare.com/zb_users/upload/2022/10/202210101665408824393287.png "WX20221010-213230@2x (1).png")

3.修改hosts,保存测试，如不行刷新DNS，ipconfig /flushdns

113.108.239.162 translate.google.com 113.108.239.162 translate.googleapis.com

最新更新地址(更新时间20230705)：

64.233.189.191 108.177.97.100 216.239.32.40 142.251.175.90 142.251.171.90 74.125.196.113 142.251.176.90 142.250.195.242 172.217.218.90 142.251.168.90 142.250.192.121

-

小工具：[https://abpyu.lanzoul.com/i9bBC0duph8j](https://abpyu.lanzoul.com/i9bBC0duph8j)

github工程：[https://github.com/Ponderfly/GoogleTranslateIpCheck](https://github.com/Ponderfly/GoogleTranslateIpCheck)

-

-

本文转自 [https://www.eqishare.com/technology/1002.html](https://www.eqishare.com/technology/1002.html)，如有侵权，请联系删除。