记一次调错，SSM项目JDK10，mysql8.0启动报错问题。花了我大概4个小时才搞定。-
-
问题：-
1.maven配置问题，重新配置了maven-
2.mysql版本使用太高，修改了pom中的坐标和application中的驱动-
3.jdk版本过高，pom中引入相应的坐标[https://blog.csdn.net/simba1949/article/details/79899431](https://www.eqishare.com/programming/88.html)-
4.启动报错：springboot java.lang.IllegalStateException: Restarter has not been initialized，原因是jar包冲突。（验证失败）-
5.错误：java.lang.ClassCastException: java.base/jdk.internal.loader.ClassLoaders$AppClassLoader cannot be cast to java.base/java.net.URLClassLoader。解决办法：jdk更换为1.8-
\[attachment=1541\]\[attachment=1542\]-
-
**总结：最好和教程里的版本一致。建议使用jdk1.8 mysql5.x**-
-

-

本文转自 [https://www.eqishare.com/programming/88.html](https://www.eqishare.com/programming/88.html)，如有侵权，请联系删除。