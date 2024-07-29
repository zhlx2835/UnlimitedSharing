易语言编辑后在别人机器上提示：“Not found the kernel library or the kernel library is invalid”-
\[attachment=1141\]-
打开tools文件夹里的link.ini配置文本，找到其中一句：ilnker="C:\\full\\path\\link.exe" 把它修改为：-
ilnker=" 这里是你易语言安装的路径 \\VC98linker\\bin\\link.exe"-
我的配置：ilnker=" C:\\Program Files (x86)\\易语言v5.11\\VC98linker\\bin\\link.exe" ， C:\\Program Files (x86)\\易语言v5.11 是我的易语言安装路径。-

-

本文转自 [https://www.eqishare.com/programming/304.html](https://www.eqishare.com/programming/304.html)，如有侵权，请联系删除。