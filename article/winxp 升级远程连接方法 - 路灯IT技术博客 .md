今天在用windows xp连接 windows server 2008 R2 的时候报出了如下错误，处理方法如下：-
【问题描述】远程计算机，出现“远程计算机需要网络级别身份验证，而您的计算机不支持该验证，请联系您的系统管理员或者技术人员来获得帮助”。-
【问题分析】当使用Windows XP的“远程桌面连接”工具去连接Windows Vista或Windows Server 2008的远程桌面、终端服务时，出现上述故障。远程桌面连接工具6.0以下版本，或者Windows XP Profressional SP1、SP2、SP3-
【解决方法】

购买须知：本商品为虚拟物品，了解清楚再捐赠打赏。-
本部分为隐藏内容，捐赠打赏0.5元才能查看本内容-
[立即捐赠](javascript:;)或[查询订单](https://www.eqishare.com/buys_query.html)-
客服QQ:19571768 备注“咨询”。

2、如果是xp sp3，还是提示的话。运行“regedit”打开注册表编辑器，进入 “HKEY\_LOCAL\_MACHINE＼SYSTEM＼CurrentControlSet＼Control＼Lsa”，双击右边栏中的 “Security Packages”，打开“编辑多字符串”对话框，在列表框光标处增加“tspkg”字符。-
3、然后定位到 “HKEY\_LOCAL\_MACHINE＼SYSTEM＼CurrentControlSet＼Control＼SecurityProviders”，双击右侧“SecurityProviders”字符串，打开“编辑字符串”对话框，在数值末端中添加“, credssp.dll”，注意逗号后有一个英文的空格。编辑完注册表，一定要重启计算机，否则注册表修改的不会生效。-
重启系统后，再运行mstsc查看关于信息已经显示为支持网络级别身份验证了。-

知识点:什么是网络级身份验证？-
 网络级身份验证 (NLA) 是一种新的身份验证方法，在您建立所有远程桌面连接之前完成用户身份验证，-
并出现登录屏幕。 这是最安全的身份验证方法，有助于保护远程计算机避免黑客或恶意软件的攻击。NLA-
的优点是：

 最初需要较少的远程计算机资源。验证用户之前，远程计算机使用有限的资源，而不是像以前版本那样-
启动所有远程桌面连接。

 它通过降低拒绝服务攻击的风险帮助提供更好的安全性。（拒绝服务攻击试图限制或阻止访问Internet。）-
 使用远程计算机身份验证，从而帮助防止用户连接到设置为恶意目的的远程计算机。

-

-

本文转自 [https://www.eqishare.com/technology/360.html](https://www.eqishare.com/technology/360.html)，如有侵权，请联系删除。