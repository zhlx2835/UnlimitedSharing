问题：使用的人人开源的框架，linux下部署java程序验证码显示不了提示2个错误：-
-
**错误1：./usr/java/jdk1.7.0\_67/bin/unpack200: error while loading shared libraries: libgcc\_s.so.1: cannot open shared object file: No such file or directory**-
**错误2：.could not initialise class sun.awt.X11FontManager**-
-
\[attachment=1549\]-
\[attachment=1550\]-
-
2019-03-26 19:01:08.230 ERROR 49781 --- \[nio-8081-exec-1\] i.r.common.exception.RRExceptionHandler : Handler dispatch failed; nested exception is java.lang.UnsatisfiedLinkError: /app/jgyapp/java/jdk1.8.0\_191/jre/lib/i386/libfontmanager.so: libgcc\_s.so.1: cannot open shared object file: No such file or directory-
-
org.springframework.web.util.NestedServletException: Handler dispatch failed; nested exception is java.lang.UnsatisfiedLinkError: /app/jgyapp/java/jdk1.8.0\_191/jre/lib/i386/libfontmanager.so: libgcc\_s.so.1: cannot open shared object file: No such file or directory-
 at org.springframework.web.servlet.DispatcherServlet.doDispatch(DispatcherServlet.java:1006)-
 at org.springframework.web.servlet.DispatcherServlet.doService(DispatcherServlet.java:925)-
 at org.springframework.web.servlet.FrameworkServlet.processRequest(FrameworkServlet.java:974)-
 at org.springframework.web.servlet.FrameworkServlet.doGet(FrameworkServlet.java:866)-
 at javax.servlet.http.HttpServlet.service(HttpServlet.java:687)-
 at org.springframework.web.servlet.FrameworkServlet.service(FrameworkServlet.java:851)-
 at javax.servlet.http.HttpServlet.service(HttpServlet.java:790)-
 at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:231)-
 at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:166)-
 at org.apache.tomcat.websocket.server.WsFilter.doFilter(WsFilter.java:52)-
 at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:193)-
 at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:166)-
 at org.apache.shiro.web.servlet.OncePerRequestFilter.doFilter(OncePerRequestFilter.java:112)-
 at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:193)-
 at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterCh-
-
解决办法：-
**1.安装so缺少的库**-
安装缺失的文件: yum install libgcc\_s.so.1-
参考：https://blog.csdn.net/fly0496/article/details/38559545-
**2.安装字体**-
解决方案：-

yum grouplist

然后找到 Fonts-

yum groupinstall Fonts

装完后，再重启一下刷新，结果还是没有解决，其中提示一个JDK中的目录下没有一个 \*\*.so的东西，这时候直接再次装这个东西-

yum install \*\*.so

最后重启服务，验证码出现了！-
-

-

本文转自 [https://www.eqishare.com/programming/81.html](https://www.eqishare.com/programming/81.html)，如有侵权，请联系删除。