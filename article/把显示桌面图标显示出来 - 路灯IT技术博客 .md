-
安装了系统后，快速启动栏没了。-
而Free Launch Bar取代了快速启动栏。这个首先得现在任务栏右键属性工具栏里勾掉Free Launch Bar。-
把快速启动栏勾上。有的时候显示桌面图标没有了。-
需要通过以下方法把显示桌面图标显示出来。-
方法一：-
-
如果实在懒得往下看了，可以记住“win+d”快捷键，实现快速切换到桌面。（win键位于Ctrl与Alt之间）-
-
-
方法二：（我就是用的这个方法）-
-
-
也可以点击“开始→运行”，在弹出的“运行”对话框中输入“REGSVR32/n /i:u shell32”（不含双引号。注：32后面有个空格），然后回车，片刻后会弹出“shell32中的DllInstall成功”提示对话框，这样“显示桌面”按钮就可以完美归来了。-
-
-
方法三：-
-
可以自己做一个。-
打开记事本，输入以下内容：-
-
\[Shell\]-
Command=2-
IconFile=explorer.exe,3-
\[Taskbar\]-
Command=ToggleDesktop-
-
-
其中，第三行代码代表的是图标的位置，数字“3”显示的是，而当把数字“3”换成“4”，刷新，图标会变成；当数字换成“6”时，图标变成了回收站的图标。虽然图标的式样变了，但是同样是“显示桌面”的功能。因此，更改显示桌面图标的方法就是这样。其实，只要在“IconFile=”后输入你所中意的图标的路径就可以了。-
然后点“文件”——>“另存为”，在文件类型中选择"所有文件"，在文件名中打上“显示桌面.scf”（不包括双引号）就成了。-
接下来，用鼠标把保存好的文件拖到快速启动栏里就OK了。为了以后便于使用，还可以将该图标保存到以下路径：C:\\Documentsand Settings\\Administrator\\Application Data\\Microsoft\\Internet Explorer\\QuickLaunch。至此，“显示桌面”图标的新建工作，搞定！-
-
方法四：-
-
如果觉得这个麻烦，还有一个简单的方法，从另一台电脑上复制“显示桌面”快捷方式。首先到另一台电脑上找到这个快捷方式，按住ctrl把这个图标拖到电脑桌面上，然后把这个“显示桌面”复制到存储盘或者联网传给需要的电脑，传到后再用鼠标拖动到快速启动栏即可。-
-
-
方法五：-
-
-
或者运行“regedit”打开注册表，找到下面键值：HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Policies\\System，在右边的窗口中有一个DOWRD值：“NoDispCPL”，将其值设为“0”或者删除即可。-
-
-
-
-
在完成此操作后，有些电脑可能需要重启后才能生效-

-

本文转自 [https://www.eqishare.com/technology/664.html](https://www.eqishare.com/technology/664.html)，如有侵权，请联系删除。