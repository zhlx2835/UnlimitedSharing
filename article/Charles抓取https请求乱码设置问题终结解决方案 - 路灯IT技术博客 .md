问题出现了好久，找了好久。-
各种教程都试了都不行。-
问题出现在客户端安装证书时浏览器输入[http://charlesproxy.com/getssl](https://www.eqishare.com/programming/115.html)，但自动跳转到另外一个地址，无法安装证书。-
-
**最终发下了重要的一步：**-
**Charles设置Proxy**-
Proxy -> SSL Proxying Settings...-
\[attachment=1487\]-
勾选Enable SSL Proxying,点击Add-
-
-
Host设置要抓取的https接口，比如想抓这个-
-
-
Host填写：[https://api.weibo.cn](https://www.eqishare.com/programming/115.html)-
Port填写：443-
最终客户端也没安装上证书，https正常抓包了-
**Charles证书安装不了的，安装最新版的charles，手机上才能安装证书！**-
**IOS手机设置信任**-
设置->通用->关于本机->证书信任设置-> 找到charles proxy custom root certificate然后信任该证书即可.-
-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/115.html](https://www.eqishare.com/programming/115.html)，如有侵权，请联系删除。