-

![111-封面 (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718276287201713.png)

> **前言**

之前蒲公英支持上传证书查看证书有效期和包含设备

【干货】IOS苹果P12证书有效性检测 及查看证书是否包含自己的设备

[https://www.eqishare.com/technology/1076.html](https://www.eqishare.com/technology/1076.html)

![pgyer (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718243894424270.png)

如今蒲公英下架了该功能，已经没有证书检查功能。

![kefu (1) (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718243719464739.png)

今天教大家包含设备是否包含 udid 的办法-

**视频教程**

> **查看描述文件（.mobileprovision）包含的设备**

打开命令窗口：-

security cms -D -i embedded.mobileprovision

可以看到配置文件，其中ProvisionedDevices（已配置的设备），如下图，然后 array 里的就是包含的 udid 的，如果有多个，这里会显示多个。

![配置文件 (1) (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718243738448650.png)

> **IPA 查看包含的设备**

首先，将.ipa文件改名为.zip，并解压缩它。

在解压缩后的文件夹中，找到名为"embedded.mobileprovision"的证书文件。

打开终端（Terminal）应用程序，并使用cd命令进入包含"embedded.mobileprovision"文件的目录。

运行以下命令来查看描述文件中包含的设备UDID：

security cms -D -i embedded.mobileprovision

这将显示描述文件的详细信息，其中ProvisionedDevices的array就是 UDID

> **使用轻松签查看**

证书导入轻松签，然后点击证书，查看详情就可以看到包含 udid

![zs (1) (1) (1) (1) (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718244708547559.png)

![zsxq (1) (1) (1) (1) (1) (1).png](https://www.eqishare.com/zb_users/upload/2024/06/202406131718244708389376.png)

-

-

本文转自 [https://www.eqishare.com/technology/1204.html](https://www.eqishare.com/technology/1204.html)，如有侵权，请联系删除。