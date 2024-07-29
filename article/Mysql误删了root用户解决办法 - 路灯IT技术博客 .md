-
1、停止mysql服务；在mysql安装目录下找到my.ini；在my.ini中找到以下片段\[**mysqld**\]；另起一行加入代码：**skip-grant-tables** 并保存-
-
2、启动mysql服务，并登录mysql(无用户名和密码)；找到user表加入root用户-
。切换表：use mysql 使用mysql表 执行添加用户-
insert into user(user,host,password,ssl\_type,ssl\_cipher,x509\_issuer,x509\_subject) values('root','localhost',PASSWORD('root'),'','','','');-
-
-
3、root用户设置权限-
update user set Host='localhost',select\_priv='y', insert\_priv='y',update\_priv='y',Alter\_priv='y',delete\_priv='y',create\_priv='y',drop\_priv='y',reload\_priv='y',shutdown\_priv='y',Process\_priv='y',file\_priv='y',grant\_priv='y',References\_priv='y',index\_priv='y',create\_user\_priv='y',show\_db\_priv='y',super\_priv='y',create\_tmp\_table\_priv='y',Lock\_tables\_priv='y',execute\_priv='y',repl\_slave\_priv='y',repl\_client\_priv='y',create\_view\_priv='y',show\_view\_priv='y',create\_routine\_priv='y',alter\_routine\_priv='y',create\_user\_priv='y'where user='root';commit;-
-
-
4、把my.ini刚才加入的那行删除并重启服务。-
-
用root用户登录，OK！-
-

-

本文转自 [https://www.eqishare.com/db/90.html](https://www.eqishare.com/db/90.html)，如有侵权，请联系删除。