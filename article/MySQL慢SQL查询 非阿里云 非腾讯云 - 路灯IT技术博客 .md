用阿里云，腾讯云习惯了，数据库都有完善的功能可以快速查询慢SQL，慢日志，SQL洞察和审计，可谓使用相当方便。-

![阿里云MySQL慢查询.png](https://www.eqishare.com/zb_users/upload/2022/07/202207221658453708652580.png)

但如果自己搭建的环境 或者 客户内部部署MySQL那就没法使用这样查询了。

那就需要手动配置，输入慢sql进行查询了。具体方法如下。

1.查询是否开启慢查询-

show variables like 'slow\_query\_log'; show variables like 'long\_query\_time';

2.若未开启，需开启，并设置时长

set global slow\_query\_log='ON'; set global long\_query\_time = 5; //设置慢sql时长

如果设置了，需要重启mysql-

3.查超过时长的慢SQL数量-

show global status like '%slow\_queries%';

4.查看具体SQL-

Linux：-

cd /www/server/mysql/bin //到mysql目录 ./mysqldumpslow --help //查看命令 ./mysqldumpslow -s r -t 3 /www/server/mysql/slowsql.log //获取返回记录最多的3个SQL mysqldumpslow 具体参数详情 参考：https://blog.csdn.net/achuDk/article/details/77869538

windows：

C:\\Program Files\\MySQL\\MySQL Server 5.5\\bin //来到安装目录 http://strawberryperl.com/ 安装perl perl -v //测试安装是否成功 perl mysqldumpslow.pl --help perl mysqldumpslow.pl -s r -t 3 "C:/Program Files/MySQL/MySQL Server 5.5/slow\_query\_log.log" //获取返回记录最多的3个SQL perl mysqldumpslow.pl -s c -t 3 "C:/Program Files/MySQL/MySQL Server 5.5/slow\_query\_log.log" //按照时间排序，前10条包含left join查询语句的SQL

出现错误：Died at mysqldumpslow.pl line 162. 有所是返回条数问题，把-t后数字改下小点。

-

本文转自 [https://www.eqishare.com/programming/971.html](https://www.eqishare.com/programming/971.html)，如有侵权，请联系删除。