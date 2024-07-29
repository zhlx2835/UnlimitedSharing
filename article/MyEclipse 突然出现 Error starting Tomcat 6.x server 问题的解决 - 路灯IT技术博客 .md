-
原因：可能是哪个软件给MyEclipse访问jvm的链接给阻止了！-
打开MyEclipse 的Tomcat的时候突然出现 Error starting Tomcat 6.x server 错误。-
-
**修改方案：运行cmd，netsh winsock reset，这个是重置winsock，可能是那个软件篡改了winsock**-
 **但是在修改 cmd的过程中又总是出现 “请求的操作需要提升(作为管理员运行)。”，接着就是具体步骤：在C:\\Windows\\System32下找到cmd.exe程序，右击“以管理员身份运行” 这样再输入上面的修改命令即可；**-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/180.html](https://www.eqishare.com/programming/180.html)，如有侵权，请联系删除。