在创建AVD时，在DOS下输入android list targets 会出现android不是内部或外部命令。这主要是没有配置好android sdk环境变量所致的。\[attachment=667\]-
-
-
解决的办法有两种：-
（1）.配置android sdk的环境变量；-
（2）.直接进入android sdk所在的目录执行（其实可以不配置环境变量而直接进入目录执行文件的）-
**方法一：配置android sdk环境变量，以我安装的android sdk为例（E:\\android-sdk）。**-
在设置系统环境变量的地方新建ANDROID\_HOME（右键点击我的电脑–>属性–>高级–>环境变量–>系统变量–>新建，注意是“系统变量”而不是“Administrator的用户变量”）-
1）. **ANDROID\_HOME=E:\\android-sdk**（android sdk所在目录）；-
2）. 在 path 中加入 **%ANDROID\_HOME%\\tools** ，注意不要改变其他文件路径，只需在分号后面加入。-
如果是2.3版本,想在任意命令行上执行adb命令,还需要在path中加入%ANDROID\_HOME%\\platform-tools,即%ANDROID\_HOME%\\tools与%ANDROID\_HOME%\\platform-tools同时加入path中，tools目录运行android命令,platform-tools目录运行adb命令.-
\[attachment=668\]-
-
-
**方法二：直接在进入安装目录中执行文件**-
android命令是在android sdk的tools下，android.bat，相关的命令还有ddms.bat，traceview.bat等。-
\[attachment=669\]-
-
不是所有的命令都在tools目录，如常用的adb命令则在E:\\android-sdk\\platform-tools目录下，而且需要进入该目录才能执行。例如查看android应用程序日志的命令 需要进入E:\\android-sdk\\platform-tools目录下，执行adb logcat。

-

本文转自 [https://www.eqishare.com/programming/508.html](https://www.eqishare.com/programming/508.html)，如有侵权，请联系删除。