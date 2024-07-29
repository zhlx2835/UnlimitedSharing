**粘贴数据的时候遇到的这个问题。在这里记录下！**-
**“无法打开剪切板” 是你粘贴的数据过大.**-
**首先把，你打开的文件夹先关掉。粘贴的时候尽量不要打开文件夹，这样影响速度。(具体为啥我也不清楚，只知道这个很管用)关掉文件夹后，试试还弹框吗，如果弹框就试试下面的办法。**-
**cmd clipbrd可以打开剪切板。**-
**regsvr32 Shdocvw.dll-
regsvr32 Shell32.dll　-
regsvr32 Oleaut32.dll-
regsvr32 Actxprxy.dll-
regsvr32 Mshtml.dll-
regsvr32 Urlmon.dll**-
**然后重启机器。-
**-

-

本文转自 [https://www.eqishare.com/technology/868.html](https://www.eqishare.com/technology/868.html)，如有侵权，请联系删除。