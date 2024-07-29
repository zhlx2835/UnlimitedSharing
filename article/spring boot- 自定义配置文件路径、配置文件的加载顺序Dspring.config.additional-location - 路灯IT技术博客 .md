-
-
**一、spring boot常用配置文件目录**-
-
SpringBoot配置文件存放位置以及读取顺序-
参考URL: [https://www.jianshu.com/p/780f83a40a90](https://www.eqishare.com/programming/35.html)-
配置文件目录-
SpringBoot配置文件可以放置在多种路径下，不同路径下的配置优先级有所不同。-
可放置目录(优先级从高到低)-

1.  file:./config/ (当前项目路径config目录下);-
    ![](https://img-blog.csdnimg.cn/20200401112754192.png)
2.  file:./ (当前项目路径下);-
    ![](https://img-blog.csdnimg.cn/20200401113031357.png)
3.  classpath:/config/ (类路径config目录下);
4.  classpath:/ (类路径config下).
3和4 都是打包进jar包的，1和2相当于外部配置。-
\[blockquote\]SpringBoot会从这四个位置全部加载配置文件并互补配置。注意是互补配置！优先级高的配置会覆盖优先级低的配置！-
\[/blockquote\]-
-
**springboot配置文件的加载顺序**-
-
官网参考： [https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-external-config](https://www.eqishare.com/programming/35.html)-
为了能让应用在不同的环境下运行，Spring Boot允许自定义配置文件，如properties文件、yaml文件、系统环境变量参数、命令行参数。-
Spring Boot使用一个非常特殊的PropertySource顺序，该顺序被设计为允许对值进行合理的重写。属性按以下顺序考虑：-
![](https://img-blog.csdnimg.cn/202004011110177.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ludGhhdA==,size_16,color_FFFFFF,t_70)-
可以参考，覆盖的点很多，图中 标红的是我们常用的。-
-
-
**二、spring boot自定义配置文件路径**-
-

1.  –spring.config.location
–spring.config.location=“D:/xxx/system.properties”-
要特别注意的是，该命令指定的配置文件会使项目默认的application.properties或application.yml文件失效，换句话说该命令会用指定的配置文件替换application.properties或application.yml文件。-
\[blockquote\]总结：该命令指定的配置文件，会使默认互补覆盖配置失效，一般不推荐使用！-
\[/blockquote\]

1.  –spring.config.additional-location
–spring.config.additional-location=“D:/xxx/conf/”-
顾名思义，该命令用于追加配置文件。原有的application.properties或application.yml文件均有效。-
注意，使用双引号可以支持带空格的路径，路径是斜杠，而不是Windows默认的反斜杠。-
\[blockquote\]注意：经过测试,如下：–spring.config.additional-location后面接的必须是一个目录，不是一个文件，你直接接配置文件，发现配置文件不生效。-
\[/blockquote\] --spring.profiles.active\=dev --spring.config.additional-location\=/home/xxx/conf/ \>nohup.output 2\>&1 &

*   1

-
-
**三、参考**-
-
springboot配置文件的加载先后顺序-
参考URL: [https://www.cnblogs.com/ghc520/p/11213741.html](https://www.eqishare.com/programming/35.html)-
Spring Boot 2 启动时加载properties文件-
参考URL: [https://www.cnblogs.com/eagle6688/p/10061739.html](https://www.eqishare.com/programming/35.html)-

-

本文转自 [https://www.eqishare.com/programming/35.html](https://www.eqishare.com/programming/35.html)，如有侵权，请联系删除。