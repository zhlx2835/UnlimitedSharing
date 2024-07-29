-
-
**1.适用于解压版Tomcat**-
windows 下 tomcat 虚拟内存配置-
 在tomcat的bin目录下,找到**catalina.bat** 文件,打开,在最上面添加这样一句:-
 **set JAVA\_OPTS=-Xms256m -Xmx512m**-
-
 Eclipse中设置tomcat 虚拟内存配置-
 Windows --> Preferences-->MyEclipse--->Tomcat-->Tomcate x.x --> JDK 中-
 Optional java vm arguments中加入 **\-Xms256m -Xmx512m**-
-
 注意：不同方式的tomcat启动，其虚拟内存取决于当前的配置，比如 tomcat中设置了，而Myeclipse中未设置，则在myeclipse启动tomcat 其虚拟内存还是未改变，仍然为默认值64M-
-
linux 下tomcat 虚拟内存配置-
 在tomcat的bin目录下,找到catalina.bat 文件,打开,在最上面添加这样一句:-
 **JAVA\_OPTS='-Xms256m -Xmx512m'**-
-
　 表示初始化内存为256MB，可以使用的最大内存为512MB。-
**2.适用于安装版Tomcat**-
适合将**tomcat**作为系统服务启动，这时候上面设置CATALINA\_OPTS 属性的方法就不适用了，因为作为系统服务的话，系统启动时调用的是 %tomcat\_home%"bin"tomcat5w.exe，他读取注册表中的值,而不是catalina.bat的设置，因此需要修改注册表：-
解决办法:-
修改注册表HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Apache Software Foundation\\Procrun 2.0\\Tomcat6\\Parameters\\Java-
原值为-
\-Dcatalina.home=C:\\Tomcat5\_5-
\-Dcatalina.base=C:\\Tomcat5\_5-
\-Djava.endorsed.dirs=C:\\Tomcat5\_5\\common\\endorsed-
\-Djava.io.tmpdir=C:\\Tomcat5\_5\\temp-
\-Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager-
\-Djava.util.logging.config.file=C:\\Tomcat5\_5\\conf\\logging.properties-
-
加入 -Xms300m -Xmx350m-
重起tomcat服务,设置生效-
-
**测试代码：**-
**新建个jsp放进去**-
<%-
double total = (Runtime.getRuntime().totalMemory()) / (1024.0 \* 1024);-
double max = (Runtime.getRuntime().maxMemory()) / (1024.0 \* 1024);-
double free = (Runtime.getRuntime().freeMemory()) / (1024.0 \* 1024);-
out.println("Java 虚拟机试图使用的最大内存量(当前JVM的最大可用内存)maxMemory(): " + max + "MB<br/>");-
out.println("Java 虚拟机中的内存总量(当前JVM占用的内存总数)totalMemory(): " + total + "MB<br/>");-
out.println("Java 虚拟机中的空闲内存量(当前JVM空闲内存)freeMemory(): " + free + "MB<br/>");-
out.println("因为JVM只有在需要内存时才占用物理内存使用，所以freeMemory()的值一般情况下都很小，<br/>" +-
"而JVM实际可用内存并不等于freeMemory()，而应该等于 maxMemory()-totalMemory()+freeMemory()。<br/>");-
out.println("JVM实际可用内存: " + (max - total + free) + "MB<br/>");-
out.println("jspcn");-
%>

-

本文转自 [https://www.eqishare.com/programming/860.html](https://www.eqishare.com/programming/860.html)，如有侵权，请联系删除。