首先启动模拟器。-
环境变量有问题的处理：[http://www.eqishare.com/read.php?tid=513](https://www.eqishare.com/programming/462.html)-
安装方法：-
直接 在CMD 里面运行-
-
C:\\Documents and Settings\\Administrator>d:-
D:\\>cd D:\\android-2.2\_r02-windows\\platform-tools-
D:\\android-2.2\_r02-windows\\platform-tools>adb install d:/Samsung\_release\_2012101901\_signed\_flash.ap-
177 KB/s (4687337 bytes in 25.765s)-
 pkg: /data/local/tmp/Samsung\_release\_2012101901\_signed\_flash.apk-
Success-
D:\\android-2.2\_r02-windows\\platform-tools>-
\[p\_w\_upload=776\]-
卸载：-
1.直接在模拟器中点击menu-->settings --> Applications --> Manage Applications 中点击你需要卸载的apk（就是你的应用软件）-->Uninstall。-
2.还有一种方法是进入内嵌的linux，去data/app目录下删除 apk文件，这种方法可以批量删除-
adb shell-
cd data-
cd app-
rm ApplicationName.apk-
\[p\_w\_upload=777\]

-

本文转自 [https://www.eqishare.com/programming/462.html](https://www.eqishare.com/programming/462.html)，如有侵权，请联系删除。