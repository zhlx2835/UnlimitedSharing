-
**代码如下：**-
**Set a=WScript.CreateObject("WScript.shell")-
a.run "http://newreg.qq.com/" '打开QQ号码申请页面-
WScript.Sleep 3000 '延时10秒，等待页面载入-
a.SendKeys "123" '这里填写昵称-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{DOWN}"-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{DOWN}"-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{DOWN}"-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "tonghua" '这里是密码-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "tonghua" '再次输入密码-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
WScript.Sleep 200-
a.SendKeys "{TAB}"-
\-----------------------------------------------------------------------**-
**其实这个最主要的是可以自定义名称和密码。况且免去了用工具被留后门的危险。希望拿到代码的回复下帖子哈，让更多的人看到这个帖子-
-
-
代码使用方法：-
-
新建TXT记事本-
复制进去-
另存为VBS即可-
使用的过程中记得把输入法切换到英文输入状态！-
运行 即可自动填写资料 大家都试试吧！ 绝对可行！-
-
自动申请QQ代码！只需一个记事本！超快.稳定.绿色.安全-
**

-

本文转自 [https://www.eqishare.com/qqwx/871.html](https://www.eqishare.com/qqwx/871.html)，如有侵权，请联系删除。