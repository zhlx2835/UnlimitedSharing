1、order deny，allow-
allow from all-
全部可以通过-
2、order allow，deny-
deny from all-
全部不能通过-
3、order allow，deny-
deny from ip0-
-
-
**查找httpd进程**-
ps -ef|grep httpd-
-
-
**apahce启动命令：**-
**cd到目录下：**-
cd /app/apch/apache/bin/-
-
-
推荐/usr/local/apache2/bin/apachectl start apaceh启动-
./apachectl start 启动-
./apachectl start apaceh 启动-
apache停止命令-
/usr/local/apache2/bin/apachectl stop 停止-
./apachectl stop 停止-
apache重新启动命令：-
/usr/local/apache2/bin/apachectl restart 重启-
./apachectl restart 重启-
-
-
**配置文件目录：**-
cd /app/apch/apache/conf/-
-
-
**配置反向代理**-
<VirtualHost \*:81>-
ProxyRequests on-
<Proxy \*>-
 order deny,allow-
 Allow from all-
</Proxy>-
ProxyPass / [http://10.187.221.4/](https://www.eqishare.com/programming/80.html)-
ProxyPassReverse / [http://10.187.221.4/](https://www.eqishare.com/programming/80.html)-
</VirtualHost>-
-
-
错误1：-
E45: readonly option is set(add ! to override)-
原因：没有权限，查看当前用户是否是root-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/80.html](https://www.eqishare.com/programming/80.html)，如有侵权，请联系删除。