错误：mysql 1213 deadlock found when trying to get lock try restarting transaction

![image.png](https://www.eqishare.com/zb_users/upload/2022/01/202201071641524679955908.png)

1.检查被占用的表：

show OPEN TABLES where In\_use > 0;

2.显示进程：

show processlist;

3.杀死挂起的进程即导致表锁死的进程：

kill 17909;---17909是进程的id

-

-

本文转自 [https://www.eqishare.com/db/905.html](https://www.eqishare.com/db/905.html)，如有侵权，请联系删除。