-
**一、****安装****猎豹浏览器****，并注册****gmail****邮箱**-
-
注册一个gmail邮箱（这一步很关键，后续会多次用到你的gmail邮箱账号）。-
https://mail.google.com/mail?hl=zh-CN-
-
-
-
**二、运行****“hosts****自动更新程序****”**-
-
1、用安装好的猎豹打开网址，下载脚本文件（这一步需要gmail账号）：-
https://sandbox.google.com/storage/fgqi/hosts/fgqi.bat-
-
2、运行程序-
双击下载好的脚本文件“fgqi.bat”-
-
-
-
由于下述步骤要使用到被和谐掉的google服务，这里需要先更改对应服务的hosts地址。这一步我们需要更新google服务地址，输入数字“1”并回车。-
-
-
**三、在****GAE****里创建****app**-
-
GoogleApp Engine是一个开发、托管网络应用程序的平台，使用Google管理的数据中心。-
-
登陆申请网址（这一步需要gmail账号）：https://appengine.google.com/start/createapp-
-
如果上述步骤需要验证手机，输入+86前缀的大陆手机号码后会收到短信，在“MobileNumber”栏里输入你收到短信里的验证码code即可完成验证步骤。（注：如我的手机为18612345678，在其中填写 “+8618612345678”，不带引号，空格必须有）-
-
-
在Application Identifier栏输入你要创建的app名称（不支持中文），点击“CheckAvailability”以确认你要的名称还未被注册过。-
为了方便起见，这里用“Baron”借代你创建的app名称。**（请自行创建，勿对号入座）**-
-
下一栏“ApplicationTitle”里面可以随便填，后期也可以随便改。-
-
完成后点击页面下方的“Create Application”，如果前面有出现“Terms ofService”即使用条款，则需要在点击“Create Application”前，把使用条款下方的“I accept theseterms”打钩。至此，app创建成功，得到的AppID即Baron （借代用）。-
-
-
**四、下载goagent**-
-
goagent是一个使用Python和Google AppengineSDK编写的代理软件。-
-
登陆goagent官网：https://code.google.com/p/goagent/ 主页最上方即给出了下载链接-
-
下载解压后会得到两个文件夹：“local”和“server”。-
-
-
**五、上传goagent服务端并配置客户端**-
-
1、上传服务端双击打开之前解压后的“server”文件夹，找到并双击运行“uploader.bat”这时界面提示“AppID:”，输入之前你在ApplicationIdentifier栏创建的app名称，如我刚刚示例的Baron。-
-
出现Email提示后输入你的gmail账号，然后是密码。（注意：输入密码时，屏幕上不会出现任何符号，请不用担心，完整正确地输入密码后按回车即可。上传完毕后按任意键关闭。）-
-
2、配置客户端双击打开之前解压后的“local”文件夹，找到并双击打开“proxy.ini”文件，修改\[gae\]栏下的appid，将等号后面的“goagent”换成你的AppID，如将原来的“appid= goagent”换成“appid = “baron”，其余保持不变。-
至此，绝大部分工作已经完成。-
-
-
**六、配置浏览器**-
-
在猎豹下安装Proxy SwitchySharp插件：https://chrome.google.com/webstore/detail/dpplabbmogkhghncfbfdeeokoefdjegm-
安装后打开ProxySwitchySharp插件的选项：-
-
-
-
在“导入/导出”栏目的最下行，“在线恢复备份”栏输入：-
https://raw.github.com/phus/phus-config/master/SwitchyOptions.bak-
最后点击“在线恢复备份” 。-
-
**若以上地址不可以使用，也可在网上搜索导入SwitchyOptions.bak文件**-
**推荐一个地址：****http://pan.baidu.com/s/1mgwRKso**-
-
-
至此，大功告成。-
-
-
**七、开始翻-墙！**-
-
1、运行goagent.exe位于之前解压后的“local”文件夹下注意：第一次运行可能需要管理员权限。**（fan时要一直打开着goagent.exe）**题外话：我们还可以设置goagent程序开机自启动，运行“local”文件夹下的“addto-startup.vbs”文件即可。2、代理翻-墙打开猎豹，在右上角ProxySwitchySharp插件上点击选择GoAgent，如下：-
\[attachment=635\]-
至此，已经挂上代理，可以随意浏览墙外世界。要想换回自己的ip，只需选择上图中的“直接连接”，即不用代理，回归墙内。-
-
-
**八、结束语**-
-
Google AppEngine并非毫无限制，每个开发者只能拥有10个应用程序，即你最多只能创建并得到10个AppID。对于创建过的AppID，可以手动删除（72小时后生效，期间随时可以反悔），AppID一旦删除，同名的账号就不能再申请。GoogleAppEngine提供给免费用户的流量是每天1GB.一般应用绝对够了。且，每天的流量重新清零的时间好像是北京时间下午16点整，而非0点。-
-
登陆 [https://appengine.google.com/](https://www.eqishare.com/technology/521.html) 点击你创建的AppID，可以看到你的流量图，以及每天免费配额还剩多少.-
-
（注：原文转自互联网，非本人原创。此教程原针对于谷歌Chrome浏览器，经本人测试后在猎豹上面可以正常运行，而后加以润色，使其通俗简练，更加适应所在环境。）\[attachment=634\]-
-
-
-
-
-
-
-
-

-

本文转自 [https://www.eqishare.com/technology/521.html](https://www.eqishare.com/technology/521.html)，如有侵权，请联系删除。