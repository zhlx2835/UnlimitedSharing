![](https://www.xshell.com/wp-content/uploads/2020/11/p-xshell7-main-zh.png)

解决办法：

1.将日期调整到2017年即可

将下方的保存成bat，其中的路径改成自己的路径。然后点bat启动，xshell和xftp都适用。

##################################begin#################### @echo off %1 mshta vbscript:CreateObject("Shell.Application").ShellExecute("cmd.exe","/c%~s0::","","runas",1)(window.close) title Xshell启动器 set atime=%date:~0,4%-%date:~5,2%-%date:~8,2% #设置系统时间 date 2018-12-31 #改成你的xshell启动路径 start "" "D:\\Program Files (x86)\\NetSarang\\Xshell 7\\Xshell.exe" echo 启动软件中... ping 0.0.0.0 -n 10> null echo 同步时间中，完成后自动关闭窗口... date %atime% exit

-

2.直接下载免费版

[https://www.xshell.com/zh/free-for-home-school/](https://www.xshell.com/zh/free-for-home-school/)

-

-

-

-

-

本文转自 [https://www.eqishare.com/programming/1114.html](https://www.eqishare.com/programming/1114.html)，如有侵权，请联系删除。