**简介：**-
Lambda Probe（以前称为Tomcat Probe）是一款实时监控和管理的Apache Tomcat实例的基本工具。-
Lambda Probe 是基于 Web + AJAX 的强大的免费开源工具，可以用来实时管理一个单独的host。LambdaProbe拥有几乎所有Tomcat Manager的功能，可以说是一个增强版本的 Tomcat Manager。除此之外，Tomcat Probe 还拥有很多让开发者和系统管理者更方便的性能。从而使得Tomcat对开发者和管理者更加透明。包括应用程序、数据源、发布、日志、线程、集群、系统信息、状态、连接器状态这些功能。如配合 JDK 1.5 甚至可以实时的画出 Server 的详细内存占用状态。-
-
-
**下载：**-
Lambda Probe 的官方地址：http://code.google.com/p/psi-probe/，也可以呀通过附件下载probe-2.3.3.zip-
将下载后的war包部署到webapp下即可-
-
-
-
**配置：**-
配置conf/tomcat-users.xml，其实就是配置tomcat管理的用户-
可以参考：http://cuisuqiang.iteye.com/blog/2070357 中的Tomcat监控配置-
-
**汉化：**-
下载messages\_zh\_CN.zip，将其中的 **messages\_zh\_CN.properties** 放到 **webapps\\probe\\WEB-INF** 下-
改名为messages\_cn.properties-
最好是把国际化图标也配置到主页下面，工程布局使用的是**sitemesh-2.4**，修改probe\\WEB-INF\\jsp\\decorators下的probe.jsp来实现-
在最下面增加-
\[code\]<a href="?<probe:addQueryParam param='lang' value='cn'/>"><img src="<c:url value='/flags/cn.gif'/>" alt="BR" /></a>\[/code\]-
**访问：**-
通过http://localhost:8080/probe/?lang=cn 访问汉化的工程，因为默认是英文的-
也可以通过下面的国旗图标进行切换，页面如下-
\[attachment=1248\]

-

本文转自 [https://www.eqishare.com/technology/221.html](https://www.eqishare.com/technology/221.html)，如有侵权，请联系删除。