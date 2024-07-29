 ![](https://www.zaixue.net/pic/1_6129.jpg)

Arthas 是一款线上监控诊断产品，通过全局视角实时查看应用 load、内存、gc、线程的状态信息，并能在不修改应用代码的情况下，对业务问题进行诊断，包括查看方法调用的出入参、异常，监测方法执行耗时，类加载信息等，大大提升线上问题排查效率。

[#](https://arthas.aliyun.com/doc/#%E8%83%8C%E6%99%AF)背景
--------------------------------------------------------

通常，本地开发环境无法访问生产环境。如果在生产环境中遇到问题，则无法使用 IDE 远程调试。更糟糕的是，在生产环境中调试是不可接受的，因为它会暂停所有线程，导致服务暂停。

开发人员可以尝试在测试环境或者预发环境中复现生产环境中的问题。但是，某些问题无法在不同的环境中轻松复现，甚至在重新启动后就消失了。

如果您正在考虑在代码中添加一些日志以帮助解决问题，您将必须经历以下阶段：测试、预发，然后生产。这种方法效率低下，更糟糕的是，该问题可能无法解决，因为一旦 JVM 重新启动，它可能无法复现，如上文所述。

Arthas 旨在解决这些问题。开发人员可以在线解决生产问题。无需 JVM 重启，无需代码更改。 Arthas 作为观察者永远不会暂停正在运行的线程。

[#](https://arthas.aliyun.com/doc/#arthas-%E9%98%BF%E5%B0%94%E8%90%A8%E6%96%AF-%E8%83%BD%E4%B8%BA%E4%BD%A0%E5%81%9A%E4%BB%80%E4%B9%88)Arthas（阿尔萨斯）能为你做什么？
---------------------------------------------------------------------------------------------------------------------------------------------------------

`Arthas` 是 Alibaba 开源的 Java 诊断工具，深受开发者喜爱。

当你遇到以下类似问题而束手无策时，`Arthas`可以帮助你解决：

0.  这个类从哪个 jar 包加载的？为什么会报各种类相关的 Exception？
    
1.  我改的代码为什么没有执行到？难道是我没 commit？分支搞错了？
    
2.  遇到问题无法在线上 debug，难道只能通过加日志再重新发布吗？
    
3.  线上遇到某个用户的数据处理有问题，但线上同样无法 debug，线下无法重现！
    
4.  是否有一个全局视角来查看系统的运行状况？
    
5.  有什么办法可以监控到 JVM 的实时运行状态？
    
6.  怎么快速定位应用的热点，生成火焰图？
    
7.  怎样直接从 JVM 内查找某个类的实例？
    

`Arthas` 支持 JDK 6+，支持 Linux/Mac/Windows，采用命令行交互模式，同时提供丰富的 `Tab` 自动补全功能，进一步方便进行问题的定位和诊断。

**快速安装**

[https://arthas.aliyun.com/doc/quick-start.html](https://arthas.aliyun.com/doc/quick-start.html)

面板命令dashboard

[https://arthas.aliyun.com/doc/dashboard.html](https://arthas.aliyun.com/doc/dashboard.html)

查看线程

thread 15

thread -b 找出当前阻塞其他线程的线程

thread -n 3 指定最忙的前 N 个线程并打印堆栈

jad反编译 [https://arthas.aliyun.com/doc/jad.html](https://arthas.aliyun.com/doc/jad.html)

jad com.xurui.app.task.EveryDayRedisTask

watch函数执行数据观测

[https://arthas.aliyun.com/doc/watch.html](https://arthas.aliyun.com/doc/watch.html)

watch com.xurui.app.api.admin.controller.GradeController gradeList '{params,returnObj,throwExp}' -n 5 -x 3

memory查看 JVM 内存信息。[](https://arthas.aliyun.com/doc/memory.html#%E4%BD%BF%E7%94%A8%E5%8F%82%E8%80%83)

trace方法内部调用路径，并输出方法路径上的每个节点上耗时

trace com.xurui.app.service.impl.SaasGradeServiceImpl getAllByType

tt方法执行数据的时空隧道，记录下指定方法每次调用的入参和返回信息，并能对这些不同的时间下调用进行观测

tt -t com.xurui.app.api.admin.controller.GradeController gradeList

tt -i 1002

profiler生成火焰图

[https://arthas.aliyun.com/doc/profiler.html](https://arthas.aliyun.com/doc/profiler.html)

profiler start start

profiler status

profiler stop --format html

quit

退出当前 Arthas 客户端，其他 Arthas 客户端不受影响。等同于exit、logout、q三个指令。

IDEA插件

-

图文笔记：

[https://note.youdao.com/s/LMoWxCxY](https://note.youdao.com/s/LMoWxCxY)

官方文档：-

[https://arthas.aliyun.com/doc/commands.html](https://arthas.aliyun.com/doc/commands.html)

-

-

本文转自 [https://www.eqishare.com/programming/1107.html](https://www.eqishare.com/programming/1107.html)，如有侵权，请联系删除。