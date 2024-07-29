![logo.png](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318069347356.png)

LocSim，TrollStore 的守护进程经理、清洁工和主管

![115 巨魔天竺葵教程-封面 (1) (1) (1) (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/04/202404171713319483732133.png)

视频教程

-

> **关于**

LocSim、守护进程管理器、清理器、屏幕时间删除器和 TrollStore 监督器

![主页.PNG](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318179836932.png)

> **安装**

安装Geranium需要满足以下要求：使用TrollStore 1.3或更高版本，并在iOS 15或更高版本的设备上运行。您可以从Geranium的发布标签中下载最新版本，并在TrollStore中打开它进行安装。安装完成后，按照设置向导进行配置即可。

> **一、iPhone Daemons 进程**

具有后台进程管理功能，允许用户选择要优化的进程。如果用户不使用HomeKit或其他苹果相关功能，可以通过此功能优化设备性能，提升系统的响应速度。

**可删进程：**

com.apple.OTACrashCopier.plist - 在 Air software 中移动崩溃和上传到/var/mobile/Library/Logs. com.apple.OTATaskingAgent.plist - 定期告诉设备上的OTA更新 ReportCrash - 有5个带"ReportCrash"的".plist"文件, 都是用来收集系统或系统程序崩溃的信息, 没什么用处. com.apple.DumpPanic.plist - 这是苹果公司用来评估系统崩溃的, 完全没必要运行. com.apple.DumpBasebandCrash.plist - 这是苹果公司用来苹果基带崩溃的, 也没必要运行. com.apple.CrashHouseKeeping.plist - 也是和程序崩溃相关的, 可以删. com.apple.aslmanager.plist - 管理系统日志文件, 可以删. com.apple.syslogd.plist - 记录系统日志, 没必要. com.apple.powerlog.plist - 用来监测第三方不兼容的充电器, 可以删. com.apple.stackshot.server.plist - 具体功能暂不清楚, 但删除后对设备没有任何影响. com.apple.tcpdump.server.plist - 似乎是用来转存网络数据的, 具体不是很清楚, 但删除后不影响设备. com.apple.iqagent.plist - 不清楚具体功能, 但删除后不影响设备. com.apple.mobile.profile\_janitor.plist - 不清楚具体功能, 但删除后不影响设备. com.apple.chud.chum.plist - 这个进程应该和苹果的CHUD工具相关(计算机硬件协议开发/Computer Hardware Understanding Developer). 如果你不是一个软件开发者, 应该不用启动这个进程. com.apple.chud.pilotfish.plist - 着也是和苹果CHUD工具相关的一个进程. 如果你不开发苹果软件, 可以删除这个. com.apple.psctl.plist – 它的作用是连接外部存储设备. 它没有任何作用如果你不会使用相机连接套件(Camera Connection Kit). 移除它如果你会使用相机连接部件Camera Connection Kit. com.apple.apsd.tcpdump.en0.plist– 推送通知中心的错误日志. com.apple.apsd.tcpdump.pdp\_ip0.plist– 同样推送通知中心的错误日志.

**选择性删除进程：-
**

com.apple.AddressBook.plist - 如果不启动这个进程, 那么电话中的通讯录的载入速度会稍微变慢一些. 若不介意这一点, 则可以删除这个进程. com.apple.accessoryd.plist - 不启动这个进程就会禁用一些辅助设备功能, 例如: FM收音机, iPhone座充, AV数据线. 当然, 即便禁用了这个进程, 用iPhone座充还是能充电, 但也只能有充电的功能啦. com.apple.apsd.plist - 禁用这项功能, 就会禁用Push邮件通知功能. 不过iPhone中的Push在国内来说确实也只是一个鸡肋功能. com.apple.dataaccess.dataaccessd.plist - 禁用了这个进程, 就不能通过Exchange或者Google来同步了. com.apple.datamigrator.plist - 这个进程的作用是把联系人从你的SIM卡传到你的iPhone里. iPod用户就没必要启动它了. 尽管我是iPhone, 但我也没有启动它, 因为我从来不在SIM卡中存联系人. com.apple.racoon.plist - 这是\*\*需要的进程. 若你不用\*\*代理, 那就不需要启动了. com.apple.MobileInternetSharing.plist - 这是网络共享功能. iPod用户完全可以删除. iPhone用户就看你自己是否需要网络共享. 其实真没啥作用. com.apple.aggregated.plist - 这个应该和"音频输入"有关. 第一代的iPod完全不需要这个进程. 第二代iPod可以根据自己的需要来决定. iPhone用户需要这个进程. com.apple.AOSNotification.plist - 这是同步MobileMe用的. 不用MobileMe的人完全不需要它, 但我却少不了它, 用MobileMe已经N年啦. com.apple.AdminLite.plist - 这个进程的作用是: 当某个程序启动或反应时间过长, 则iPhone或iPod会自动终止这个程序(即: 让程序崩溃), 从而把控制权转交到你手中. 如果你不愿意经常看到程序崩溃, 那么你可以关闭这个进程, 但结果是, 当遇到某个程序启动或反应过慢时, 你得多等一会儿. 一般情况下不建议关闭这个进程. com.apple.iapd.plist-功能跟com.apple.accessoryd.plist差不多. 用来处理一些会运行特定配件的Apps. com.apple.graphicsservices.sample.plist– 当显示专辑插图时会运行的数据，小编在设备上移除了这个并所有程序正常，但有人曾遇到过问题. com.apple.UIKit.pasteboardd.plist– 复制和粘帖的功能 com.apple.scrod.plist– 用于语音控制(Voice Control). 移除如果你不使用这功能.

**不可删进程：**-

com.apple.mobile.Lockdown.plist - 和SIM卡授权及其他一些重要功能相关. com.apple.fairplayd.plist - 验证DRM的, 即你安装的程序和音乐的合法性. com.apple.installd.plist - 与app程序安装相关. com.apple.BTServer.plist - 若是禁用了这个进程, 就等着看你的iPhone或iPod变得像蜗牛一样慢的速度吧. com.apple.configd+pm.plist - 与系统设置相关. com.apple.configd-pm.plist - 与系统设置相关. com.apple.gmmd.plist - 设备调试功能.. com.apple.mDNSResponder.plist - 禁用了这个进程, 你就不能上网! com.apple.CommCenter.plist - 打出/打入电话. 即便是iPod用户也不要禁用这个进程! com.apple.locationd.plist - GPS及定位功能. com.apple.mediaserverd.plist - 播放音乐及视频. com.apple.graphicsservices.sample.plist - 展示相册功能. com.apple.usbptpd.plist - 允许设备连接电脑并充电. com.apple.mtmergeprops.plist – 配置给你的Touchscreen的文件，移除这个后，我的设备黑屏了，这也是为什么要备份! com.apple.SCHelper-embedded.plist– 似乎是系统结构框架的一部份，我不取尝试，但如果你有这勇气可以去尝试并PM我结果 (承受你个人的风险) com.apple.SpringBoard.plist– SpringBoard文件，移除这个你的SpringBoard就启用不了，然后就没有然后了 com.apple.mobile.lockbot.plist– 未知的文件，但移除这个后令我悲剧地重新刷机了 com.apple.mobile.Lockdown.plist– 配置给SIM卡和网络的文件，删除这个也得刷机。 com.apple.itdbprep.plist– 基础上的名字，用于同步音乐。 com.apple.itunesstored– 乱删这个，你的CPU就100%了，请远离它。

附完整 iPhone 进程：[https://www.eqishare.com/ios\_LaunchDaemons.html](https://www.eqishare.com/ios_LaunchDaemons.html)-

建议：操作要慎重，否则可能会导致死机，白苹果！

> **二、locsim 定位**

模拟虚假位置+并保存书签，Geranium允许用户模拟虚假的地理位置信息，并创建书签以保存特定位置。这对于需要在特定应用程序中模拟不同位置的用户非常有用，例如游戏或社交媒体应用。

![定位.PNG](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318359146095.png)

> **三、清洁工**

提供了一种强大的清理工具，可以帮助用户清理iOS设备上占用大量空间的"其他"类别文件。使用该工具，用户可以释放大量存储空间，使设备更加高效。

![清洁工界面.PNG](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318790655941.png)

> **四、设备监管**

允许用户监控自己的设备，并为设备设置自定义组织名称。这对于企业或教育机构管理设备非常有用。此外，Geranium还提供了一系列监视配置文件，用户可以选择使用。

![监管.PNG](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318893774219.png)

> **五、禁用**屏幕**使用时间**

如果用户忘记了屏幕使用时间的密码，Geranium可以帮助用户禁用设备上的屏幕使用时间功能。这对于不想受到屏幕使用时间限制的用户非常有用。需要注意的是，如果父母管理用户的屏幕使用时间，使用此功能可能会带来不良后果。在使用此功能时，请自行承担责任。

![禁用屏幕时间.PNG](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318979109126.png)![禁用屏幕时间-翻译.jpg](https://www.eqishare.com/zb_users/upload/2024/04/202404171713318998502787.jpg)

-

-

> **总结**

总之，Geranium是一款功能全面的应用程序，为巨魔商店用户提供了模拟位置、清理空间、管理后台进程、禁用屏幕使用时间和设备监控等实用功能。无论您是普通用户还是开发者，Geranium都可以为您带来更好的iOS设备使用体验。

**相关地址：**

**（防失效，下方回复可见）**

此处为隐藏内容，请评论后查看隐藏内容，谢谢！评论后看不到请[再刷新网页](javascript:location.reload();)

-

本文转自 [https://www.eqishare.com/technology/1181.html](https://www.eqishare.com/technology/1181.html)，如有侵权，请联系删除。