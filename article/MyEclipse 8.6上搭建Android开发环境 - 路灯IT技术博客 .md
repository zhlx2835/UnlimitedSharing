**1，基本环境准备：**-
安装JDK1.5以上,Eclipse3.3以上版本.（MyEclipse也可以），笔者安装了JDK1.6和MyEclipse 8.6。-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035280.png)-
**JDK1.6**

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035281.jpg)-
**MyEclipse 8.6**-
**2，下载Android SDK**-
非常不幸的是，Android.com 被我们强大的GFW 给墙了，但是我们又不得不去官网下载（当然，你能从朋友手中拿到SDK也很不错哦），让我们不得不翻墙。当然翻——墙的方法很多，点这里看：http://www.eqishare.com/read.php?tid-768.html-
地址：[http://developer.android.com/sdk/index.html](http://developer.android.com/sdk/index.html)-
下载成功后：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035282.png)-
**Android SDK文件**解压到某目录下：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035283.png)-
**解压文件**

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035284.png)-
**解压目录**双击SDK Setup.exe 安装SDK，安装完成后，文件夹入下图所示：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035285.png)-
**安装SDK**-
****3，配置SDK环境变量：****-
主要是在path 中加入SDK 下的tools目录：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035286.png)-
**在path 中加入SDK 下的tools目录**环境变量：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035287.png)

**环境变量**完成以后SDK就算配置完成。-
-
**4，给MyEclipse安装ADT插件**-
打开eclipse的help菜单->MyEclipse Configuration Center-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035288.png)

**打开eclipse的help菜单**进入后点击 Software 标签-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/1035289.png)-
**Software 标签**在Browser Software后面的 add site-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352810.png)-
**Browser Software**在对话框中填写如图所示：（name 自己取）-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352811.png)-
**在对话框中填写名称后点击ok**然后在左边会出现 如下的-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352812.png)

**点击Add to Profile**选中目标，右键点击Add to Profile，于是在右边的Software Updates Available 就会有所反应，-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352813.png)-
**Software Updates Available** 然后点击下面的Apply 2 changes 来开始安装-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352814.png)-
**点击下面的Apply 2 changes**

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352815.png)-
**开始安装**点击接受下面的许可，继续。-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352816.png)-
**点击接受**接着点击Update开始安装。这个过程可能有点慢，耐心等待他的完成。-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352817.png)-
**Update开始安装**

**5，配置MyEclipse**-
-
点击window –>preferences-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352818.png)

**点击window –>preferences**在Android选项，填写好SDK location，点击Apply后出现以下内容。-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352819.png)-
**点击Apply后出现的内容**-

-
**6，AVD的管理**-
点击window-> Android SDK and AVD Manager-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352820.png)-
**Android SDK and AVD Manager**然后选择 Available Package-
因为需要兼容性测试，如果条件允许，最好 多装些版本。-
然后，点击Install Selected 开始安装。这又是一个漫长的过程，可能非常漫长。呵呵-
安装好了后。我们开始建立一个虚拟机-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352821.png)**点击new**-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352822.png)-
**创建**创建成功后，可以启动试试-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352823.png)-
**启动，点击Start**

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352824.png)-
**开始启动模拟器**点击Start ，然后点击launch，开始启动模拟器。-
-
**7,创建Hello World程序**-
创建一个Android 项目-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352825.png)-
**点击next**

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352826.png)-
**点击finish**右键点击项目->Run As –> Android Application-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352827.png)

**点击右键**即可看到效果：-

![](http://p_w_picpath.51cto.com/files/uploadimg/20100831/10352828.png)-
**搭建成功**现在，你可以开始研究这个Hello Word 程序了，祝你好运。谢谢-
-
本文地址：[http://www.eqishare.com/read.php?tid=342](http://www.eqishare.com/read.php?tid=342)-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/653.html](https://www.eqishare.com/programming/653.html)，如有侵权，请联系删除。