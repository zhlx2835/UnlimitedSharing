-
执行ant编译时，总会出现如下的警告：-
\[javac\] E:\\workspace\\HelloAntWorld\\build.xml:26: warning: 'includeantruntime' was not set, defaulting to build.sysclasspath=last; set to false for repeatable builds-
其实解决方法也很简单，只需要根据提示在javac任务中添加includeAntRuntime="false"属性即可。-
例如：-
-
-
修改前：-
 <javac srcdir="${srcDir}" destdir="${binDir}" />-
修改后：-
 <javac srcdir="${srcDir}" destdir="${binDir}" includeAntRuntime="false" />-
-
-
添加上红色标记的属性即可-
-
-
\[attachment=1046\]-
-
-
\[attachment=1047\]-
-
-
-
不再出现警告

-

本文转自 [https://www.eqishare.com/programming/366.html](https://www.eqishare.com/programming/366.html)，如有侵权，请联系删除。