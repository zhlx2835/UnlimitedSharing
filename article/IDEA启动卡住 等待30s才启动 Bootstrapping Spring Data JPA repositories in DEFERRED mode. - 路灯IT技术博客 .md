2021-09-01 11:05:37.636 INFO 7096 --- \[ main\] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 204ms. Found 0 JDBC repository interfaces.-
2021-09-01 11:05:37.643 INFO 7096 --- \[ main\] .s.d.r.c.RepositoryConfigurationDelegate : Multiple Spring Data modules found, entering strict repository configuration mode!-
2021-09-01 11:05:37.644 INFO 7096 --- \[ main\] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFERRED mode.-
2021-09-01 11:06:59.355 INFO 7096 --- \[ main\] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 81707ms. Found 128 JPA repository interfaces.-
\[attachment=1616\]-
启动使用了22s，平常7,8秒都启动完成的。-

![](https://www.eqishare.com/zb_users/upload/2022/05/202205171652771392433471.png "微信截图_20220517150849.png")

解决方案：DEBUG里去掉菱形的断点。

![](https://www.eqishare.com/zb_users/upload/2022/05/202205171652771392729554.png "微信截图_20220517150839.png")

扩展：[https://blog.csdn.net/festone000/article/details/104005559](https://www.eqishare.com/tools/8.html)-

-

本文转自 [https://www.eqishare.com/tools/8.html](https://www.eqishare.com/tools/8.html)，如有侵权，请联系删除。