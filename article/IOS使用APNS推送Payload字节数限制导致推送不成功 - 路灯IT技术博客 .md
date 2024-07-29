\[attachment=1273\]-
这2天需要在推送上加上脚本，找到了badge方法可以加脚本。加上后但是怎么推送也不成功。郁闷了好久，在网上查找相关资料。-
终于被我找到原因：-
“**Payload--最多256bytes。**”-
-
原来是发送的payload字节超过规定字符。-
使用payload.getBytes().length得到字节数。查看了下字符个数240个字节，没有超过256，反复测试，得知，256bytes也不够准确。就把原payload中的某些值去掉了（loginUri登录，uri用于跳转），再次测试，推送成功。-
-
-
\========payload=========-
原来：-
-
{"loginUri":"http://192.168.1.8:8086/admin/msm/login","messageID":"580","aps":{"alert":"郑子宣向你发送了一个工作事项","sound":"default","badge":5},"uri":"http://192.168.1.8:8086/admin/msm/login?module=WEIBO&moduleId=93f7cf993df34d3dbc1681f08cced08c"}====字节数====250-
新：-
-
{"messageID":"608","aps":{"alert":"郑子宣向你发送了一个工作事项","sound":"default"},"uri":"http://192.168.1.8:8086/admin/msm/login?module=WEIBO&moduleId=caedadfd80f841538a3414ca737c2ab0"}====字节数====187-
\=======================-
-
-
-
更多文章：[http://blog.sina.com.cn/s/articlelist\_1238625327\_5\_1.html](https://www.eqishare.com/programming/197.html)-
-

-

本文转自 [https://www.eqishare.com/programming/197.html](https://www.eqishare.com/programming/197.html)，如有侵权，请联系删除。