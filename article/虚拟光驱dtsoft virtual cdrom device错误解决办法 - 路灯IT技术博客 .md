控制面板—系统—硬件—设备管理器中，DVD/CD-ROM驱-
动器下dtsoft virtual cdrom device出现黄色感叹号，影响我网银的优盾识别，困扰我一天，终于坚决了，现将经验分享给大家。下面内容转。。。 现象：设备管理器光驱驱动提示错误信息为：由于dtsoft virtual cdrom device其配置信息不完整或已损坏，windows无法启动这个硬件设备。 解决方法：-
1\. 点击“开始”——运行regedit.exe,进入注册编辑器，到左边的项目栏里找到-
HKRY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4D36E965-E325-11CE-BFC1-08002BE10318}选定，在右面窗口找到upperfilters项和loweverfiters项。点右键将其逐个删除。 2. 在设备管理器中卸载有问题的光驱后，点击“操作”—“扫描检测硬件改动”，会自动更新光驱。这时光驱就恢复正常了，如果还不行就重启计算机就ok啦。

-

本文转自 [https://www.eqishare.com/technology/186.html](https://www.eqishare.com/technology/186.html)，如有侵权，请联系删除。