使用 Apple ID 签名 IPA 文件也就是常说的“个人签”，很多小伙伴在使用Apple ID签名时，有时候会出现证书申请失败，或者签名失败，这类报错信息。

-

以下汇总爱思助手 IPA 签名功能在使用时可能遇到的问题和解决办法。

-

**1.安装已签名的软件需要越狱吗？**-

-

不需要。不论是使用证书签名还是使用 Apple ID 签名，安装时都不要求设备越狱，和越狱并没有什么关系。

-

**2.用于签名的 Apple ID 需要关闭双重认证吗？**

-

不需要。不论 Apple ID 关闭或者开启双重认证，都可以用来签名 IPA 文件，只不过已开启双重认证的 Apple ID 在第一次使用时需要进行验证，之后使用时不需要再次验证。

-

**3.签名的有效期是多久？**

-

使用证书签名的 IPA 文件，安装后的使用时间取决于证书的有效期，如果在有效期内证书被吊销，软件将无法再次打开，也就是常说的“掉签”；使用 Apple ID 签名安装的应用有效期为 7 天。

-

**4.支持批量签名吗？**

-

支持。导入后勾选需要签名的文件，选择证书或者用于签名的 Apple ID，然后点击“开始签名”即可。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20200423/1587631653676008342.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

**5.使用 Apple ID 签名后的 IPA 文件可以安装到其他的设备上吗？**-

-

不可以。使用 Apple ID 签名的应用和设备标识绑定，签名时如果选择的是 A 设备的设备标识，就无法将签名后的 IPA 文件安装到 B 设备上。

-

**6.签名后的安装包为什么没有安装到设备上？**

-

IPA 签名工具目前没有自动安装功能，签名完成后需要手动“打开已签名 IPA 位置”，然后双击使用爱思助手安装。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20200424/1587699588808092103.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

**7.安装 IPA 文件失败提示“设备未越狱”是什么原因？**

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20200611/1591857957625062275.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

原因一：该 IPA 文件签名使用的设备标识和当前安装的设备不一致。使用 A 设备标识签名的 IPA 文件无法安装到 B 设备上。

-

原因二：IPA 文件签名成功后，安装到设备仍然提示“设备未越狱”，请检查设备上带云状图标的 App 并手动删除（或使用爱思助手工具箱的“删除顽固图标”进行删除），然后再重新安装即可。

-

**8.签名时报错怎么办？**

-

**第一种情况，**提示，证书申请失败！

（将鼠标移动至红色字体的位置。后面会出现一串这样的英文提示。)

get +XcodeToken+err+SRP\_Setp1+err:hsc=200+ec=-20101+au=+em=Your+account+information+was+entered+incorrectly.

-

这种情况是说明Apple ID账号有误，点击添加Apple ID，重新输入正确的账号和密码即可。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660791434539049884.jpg "爱思助手 IPA 签名功能常见问题汇总")

这里着重强调一下，如果Apple ID账号是手机号码，在签名输入ID账号时，手机号前面需要加86。

-

例如：8615012345678。

-

**第二种情况，**出现这类报错：

get +XcodeToken+err+GetGsldmsToken+err:hsc=401+ec=-22406+au=+em=Your+Apple+ID+or+password+is+incorrect.

这种情况是说明Apple ID账号或者密码有误，点击添加Apple ID，重新输入正确的账号和密码即可。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660791634506070804.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

同样，若账号是手机号前面也需要加86。

-

**第三种情况，**提示签名失败，错误码44。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792040541071513.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

这是因iPA包构架问题导致无法进行签名，可以尝试下载未被改动过的原始iPA包重新签名。

-

**第四种情况，**提示签名失败，错误码45。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792116143090644.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

这个也是iPA包有问题的原因，因为IPA包里面的文件可能存在非法字符比如中文字符这些，可以尝试下载未改动过的原始iPA包，然后重新签名。

-

**第五种情况，**出现这类签名失败的提示：get anisettedata failed.-

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660793227694066370.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

 这个有可能是电脑网络的原因：公司网络或校园网络。解决方法是：更换个人家庭网络或手机热点。

-

**第六种情况，**出现这类签名失败的提示：启动证书申请进程失败。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792454873052586.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

这个是杀毒软件拦截了证书申请的进程，重启电脑退出杀毒软件再重试。

-

**第七种情况，**出现这类证书申请失败的提示：get teams err Teams =0.

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792522999097953.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

原因是当前账号获取teams出错，更换Apple ID账号再去签名即可。

-

**第八种情况，**出现这类证书申请失败的提示：get XcodeToken err GetGsldmsToken err:hsc=434 ec=-22421 au=em=This action could not be completed. Try again.

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792633471028581.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

或者这种提示：get +teams+err+1100+Your+session+has+expired.+Please+log+in.

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792661744003802.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

然后这种提示：get +XcodeToken+err+RequestValidate+err;Http+Get+validate+vd+len;0+err;<nil>.

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792678781097209.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

**还有**这种提示：

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220823/1661237688790053492.png "爱思助手 IPA 签名功能常见问题汇总")

这四种情况的解决办法是一样的，按照这个文件路径 ：C:\\ProgramData\\i4\\i4tools\\ipasign，删除adi和cnf两个文件夹即可。-

-

**第九种情况，**这类证书申请失败的提示：get +XcodeToken+err+MakeCPD+err;anisette+null+err;The+operation+couldn\\U2019t+completed.+(AKAnisetteError+error+-8004.) .

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792932958040180.jpg "爱思助手 IPA 签名功能常见问题汇总")

-

这是电脑设置了代理服务器，关闭即可。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20220818/1660792988620000472.png "爱思助手 IPA 签名功能常见问题汇总")

-

**第十种情况，**签名数量已达上限。

-

根据苹果的规定，每个 Apple ID 在 7 天内只能为 10 个安装包进行签名，请更换 Apple ID 或 7 天后再试。

-

出现以上报错，首先检查 iTunes 是否为最新版本，确保为最新版后如果继续报错，请更换其他能正常登录使用的 Apple ID 来完成签名。-

-

**9.提示“不支持加密的ipa包”是什么意思？**

-

App Store 下载的或者其他已加密的 IPA 文件，无法再次签名安装。

-

![爱思助手 IPA 签名功能常见问题汇总](https://d-image.i4.cn/i4web/image/upload/20200423/1587633226112044579.jpg "爱思助手 IPA 签名功能常见问题汇总")

[](https://url.i4.cn/faIfqyaa "下载爱思助手")

-

-

本文转自 [https://www.eqishare.com/technology/1008.html](https://www.eqishare.com/technology/1008.html)，如有侵权，请联系删除。