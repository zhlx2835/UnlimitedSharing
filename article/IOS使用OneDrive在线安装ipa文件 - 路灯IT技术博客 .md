这里说的是实现在线安装，ipa安装包首先要有准备好。-

使用到的文件：1.ipa安装包；2.plist描述文件；3.制作安装页面

-
第一步、首先是是要把ipa文件放到外网上可以访问下载到，我这里选择的是[onedrive](https://onedrive.live.com/)网盘。-
上传后共享出外链地址。如下图。链接如：[https://onedrive.live.com/redir?resid=75381495E1C2A8F%21108](https://www.eqishare.com/technology/170.html)-
-
第二步、然后通过[OneDrive外链提取工具](http://www.hiadmin.org/onedrive)拿到真实下载地址。-
其实不用工具也可以自己拿到地址比如上面的那个链接。拿到resid之后的字符串，在用文件类型就可以拼接出来。-
\[code\]http://storage.live.com/items/+resid字符串+?hiadmin.+文件类型 //得到下面的真实地址-
http://storage.live.com/items/75381495E1C2A8F%21108?hiadmin.ipa\[/code\]-
第三步、修改plist文件，将plist文件上传。-
\[code\]<?xml version="1.0" encoding="UTF-8"?>-
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">-
<plist version="1.0">-
<dict>-
 <key>items</key>-
 <array>-
 <dict>-
 <key>assets</key>-
 <array>-
 <dict>-
 <key>kind</key>-
 <string>software-package</string>-
 <key>url</key>-
 <string>程序ipa的URL</string> //这里是以上得到的ipa真实地址-
 </dict>-
 <dict>-
 <key>kind</key>-
 <string>display-image</string>-
 <key>url</key>-
 <string>小ICON图标的URL</string> //这里将图片上传后的真实地址-
 </dict>-
 </array>-
 <key>metadata</key>-
 <dict>-
 <key>bundle-identifier</key>-
 <string>com.xxxxxxx.xxxxxxx</string>-
 <key>kind</key>-
 <string>software</string>-
 <key>title</key>-
 <string>赵一诺</string>-
 </dict>-
 </dict>-
 </array>-
</dict>-
</plist>\[/code\]-
第四步、创建下载的页面。-
<a href="itms-services://?action=download-manifest&url=https://storage.live.com/items/75381495E1C2A8F%21114?hiadmin.plist">赵一诺</a>-
其中url就上刚刚上传的plist的真实地址，并且url必须是https的。-
\[code\]<html>-
<head>-
<meta http-equiv="Content-Type" content="text/html;charset=utf-8"/>-
<meta name="viewport" content="target-densitydpi=device-dpi,width=device-width, initial-scale=1, user-scalable=no" /></head>-
<body>-
<a href="itms-services://?action=download-manifest&url=https://storage.live.com/items/75381495E1C2A8F%21114?hiadmin.plist">赵一诺</a>-
</body>-
</html>\[/code\]-
-
扫码测试：[赵一诺成长记IOS手机客户端](http://www.zhaoyinuo.cn/)-
-
-

-

本文转自 [https://www.eqishare.com/technology/170.html](https://www.eqishare.com/technology/170.html)，如有侵权，请联系删除。