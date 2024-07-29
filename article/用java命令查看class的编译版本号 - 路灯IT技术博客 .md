最近遇到个老项目用jdk1.8编译有问题，不知道当时是用什么编译的。-
可以使用java自带的工具，查看 class的编译器版本号-
\[code\]$ javap -v ServiceImpl.class\[/code\]或-
\[code\]$ javap -verbose ServiceImpl.class\[/code\]-
\[attachment=1505\]-
可以查看jdk和major version对应关系：-
\[code\]J2SE 8 = 52,-
J2SE 7 = 51,-
J2SE 6.0 = 50,-
J2SE 5.0 = 49,-
JDK 1.4 = 48,-
JDK 1.3 = 47,-
JDK 1.2 = 46,-
JDK 1.1 = 45\[/code\]

-

本文转自 [https://www.eqishare.com/programming/100.html](https://www.eqishare.com/programming/100.html)，如有侵权，请联系删除。