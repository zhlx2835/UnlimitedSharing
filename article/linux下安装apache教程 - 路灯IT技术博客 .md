http-2.2.6.tar.gz-
-
下载地址：[http://www.filewatcher.com/m/httpd-2.2.6.tar.gz.6028951-0.html](https://www.eqishare.com/programming/343.html)-
-
下面是linux下安装apache的完整代码，系统是redhat5.5-
下载httpd-2.2.6.tar.gz-
把httpd-2.2.6.tar.gz放到/soft 下-
\[root@localhost-
~\]#cd /soft-
\[root@localhost-
soft\]#gzip –d httpd-2.2.6.tar.gz-
 //解压apache的压缩包-
\[root@localhost-
soft\]#cd httpd-2.2.6 //定位到httpd-2.2.6-
文件夹下-
\[root@localhost-
httpd-2.2.6\]#ls //查看显示httpd-2.2.6 文件夹下内容-
\[root@localhost-
httpd-2.2.6\]#./configure --help |-
more //查看安装apache配置参数-
\[root@localhost-
httpd-2.2.6\]#./configure --prefix=/usr/local/apache-
\--enable-so // 配置apache路径-
\[root@localhost-
httpd-2.2.6\]#make //编译apache-
\[root@localhost-
httpd-2.2.6\]#make install //安装apache-
\[root@localhost-
httpd-2.2.6\]#cd /usr/local/apache //进入apache的目录-
-
\[root@localhost-
apache\]# cd conf/-
\[root@localhost-
conf\]#cp -a httpd.conf httpd.conf--
//备份apache配置文件-
\[root@localhost-
conf\]#chkconfig --list-
httpd //查看httpd服务是否已存在-
\[root@localhost-
conf\]#chkconfig httpd off //关闭系统自带了httpd的服务，如果存在httpd服务-
-
\[root@localhost-
conf\]#service httpd status //查看自带httpd服务状态-
\[root@localhost-
conf\]#/usr/local/apache/bin/apachectl -k-
start //linux启动apache命令-
-
\[root@localhost-
conf\]#netstat -an | grep :80 //查看linux80端口是否开启-
\[root@localhost-
conf\]#ps -aux | grep-
httpd //linux下查看apache进程-
\[root@localhost-
conf\]#cd ../..-
\[root@localhost-
local\]#cp /usr/local/apache/bin/apachectl /etc/rc.d/init.d/apache-
//拷贝apache启动脚本-
\[root@localhost-
local\]#vi /etc/rc.d/init.d/apache //-
这里是编辑apache启动脚本-
-
在开头的#！/bin/sh 下面加上-
-
#chkconfig: 2345 85 15-
\[root@localhost-
local\]#chkconfig --add apache //添加apache服务-
\[root@localhost-
local\]#chkconfig --list apache //列出apache服务-
\[root@localhost-
local\]#service apache stop //停止apache服务-
\[root@localhost-
local\]#netstat -an | grep :80-
//查看linux的80端口是否关闭-
\[root@localhost-
local\]#ps -aux | grep-
httpd //查看是否存在httpd服务，若果之前自带httpd服务启动的话会导致新添加的apache服务启动失败-
\[root@localhost-
local\]#service apache start //启动apache服务-
打开你的服务器ip地址，看看是否出现了tomcat的默认首页，如果出现的话，那么恭喜你-
linux下安装apache已经成功了

-

本文转自 [https://www.eqishare.com/programming/343.html](https://www.eqishare.com/programming/343.html)，如有侵权，请联系删除。