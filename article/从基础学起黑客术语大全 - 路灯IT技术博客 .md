-
 **1.肉鸡：所谓“肉鸡”是一种很形象的比喻，比喻那些可以随意被我们控制的电脑，对方可以是WINDOWS系统，也可以是UNIX/LINUX系统，可以是普通的个人电脑，也可以是大型的服务器，我们可以象操作自己的电脑那样来操作它们，而不被对方所发觉。**-
**　　2.木马：就是那些表面上伪装成了正常的程序，但是当这些被程序运行时，就会获取系统的整个控制权限。有很多黑客就是 热中与使用木马程序来控制别人的电脑，比如灰鸽子，黑洞，PcShare等等。**-
**　　3.网页木马：表面上伪装成普通的网页文件或是将而已的代码直接插入到正常的网页文件中，当有人访问时，网页木马就会利用对方系统或者浏览器的漏洞自动将配置好的木马的服务端下载到访问者的电脑上来自动执行。**-
**　　4.挂马：就是在别人的网站文件里面放入网页木马或者是将代码潜入到对方正常的网页文件里，以使浏览者中马。**-
**　　5.后门：这是一种形象的比喻，入侵者在利用某些方法成功的控制了目标主机后，可以在对方的系统中植入特定的程序，或者是修改某些设置。这些改动表面上是很难被察觉的，但是入侵者却可以使用相应的程序或者方法来轻易的与这台电脑建立连接，重新控制这台电脑，就好象是入侵者偷偷的配了一把主人房间的要是，可以随时进出而不被主人发现一样。**-
**　　通常大多数的特洛伊木马（Trojan Horse）程序都可以被入侵者用语制作后门（BackDoor）**-
**　　6.rootkit：rootkit是攻击者用来隐藏自己的行踪和保留root（根权限，可以理解成WINDOWS下的system或者管理员权限）访问权限的工具。通常，攻击者通过远程攻击的方式获得root访问权限，或者是先使用密码猜解（破解）的方式获得对系统的普通访问权限，进入系统后，再通过，对方系统内存在的安全漏洞获得系统的root权限。然后，攻击者就会在对方的系统中安装rootkit，以达到自己长久控制对方的目的，rootkit与我们前边提到的木马和后门很类似，但远比它们要隐蔽，黑客守卫者就是很典型的rootkit，还有国内的ntroorkit等都是不错的rootkit工具。**-
**　　7.IPC$：是共享“命名管道”的资源，它是为了让进程间通信而开放的饿命名管道，可以通过验证用户名和密码获得相应的权限，在远程管理计算机和查看计算机的共享资源时使用。**-
**　　8.弱口令：指那些强度不够，容易被猜解的，类似123，abc这样的口令（密码）**-
**　　9.默认共享：默认共享是WINDOWS2000/XP/2003系统开启共享服务时自动开启所有硬盘的共享，因为加了"$"符号，所以看不到共享的托手图表，也成为隐藏共享。**-
**　　10.shell：指的是一种命令指行环境，比如我们按下键盘上的“开始键+R”时出现“运行”对话框，在里面输入“cmd”会出现一个用于执行命令的黑窗口，这个就是WINDOWS的Shell执行环境。通常我们使用远程溢出程序成功溢出远程电脑后得到的那个用于执行系统命令的环境就是对方的shell**-
**　　11.WebShell：WebShell就是以asp、php、jsp或者cgi等网页文件形式存在的一种命令执行环境，也可以将其称做是一种网页后门。黑客在入侵了一个网站后，通常会将这些asp或php后门文件与网站服务器WEB目录下正常的网页文件混在一起，好后就可以使用浏览器来访问这些asp 或者php后门，得到一个命令执行环境，以达到控制网站服务器的目的。可以上传下载文件，查看数据库，执行任意程序命令等。国内常用的WebShell有海阳ASP木马，Phpspy，c99shell等**-
**　　12.溢出：确切的讲，应该是“缓冲区溢出”。简单的解释就是程序对接受的输入数据没有执行有效的检测而导致错误，后果可能是造成程序崩溃或者是执行攻击者的命令。大致可以分为两类：（1）堆溢出；（2）栈溢出。**-
**　　13.注入：随着B/S模式应用开发的发展，使用这种模式编写程序的程序员越来越来越多，但是由于程序员的水平参差不齐相当大一部分应用程序存在安全隐患。用户可以提交一段数据库查询代码，根据程序返回的结果，获得某些他想要知的数据，这个就是所谓的SQLinjection，即：SQL注意入。**-
**　　14.注入点：是可以实行注入的地方，通常是一个访问数据库的连接。根据注入点数据库的运行帐号的权限的不同，你所得到的权限也不同。**-
**　　15.内网：通俗的讲就是局域网，比如网吧，校园网，公司内部网等都属于此类。查看IP地址如果是在以下三个范围之内的话，就说明我们是处于内网之中的：10.0.0.0—10.255.255.255，172.16.0.0—172.31.255.255，192.168.0.0—192.168.255.255**-
**　　16.外网：直接连入INTERNET（互连网），可以与互连网上的任意一台电脑互相访问，IP地址不是保留IP（内网）IP地址。**-
**　　17.端口：（Port）相当于一种数据的传输通道。用于接受某些数据，然后传输给相应的服务，而电脑将这些数据处理后，再将相应的恢复通过开启的端口传给对方。一般每一个端口的开放的偶对应了相应的服务，要关闭这些端口只需要将对应的服务关闭就可以了。**-
**　　18.3389、4899肉鸡：3389是Windows终端服务（Terminal Services）所默认使用的端口号，该服务是微软为了方便网络管理员远程管理及维护服务器而推出的，网络管理员可以使用远程桌面连接到网络上任意一台开启了终端服务的计算机上，成功登陆后就会象操作自己的电脑一样来操作主机了。这和远程控制软件甚至是木马程序实现的功能很相似，终端服务的连接非常稳定，而且任何杀毒软件都不会查杀，所以也深受黑客喜爱。黑客在入侵了一台主机后，通常都会想办法先添加一个属于自己的后门帐号，然后再开启对方的终端服务，这样，自己就随时可以使用终端服务来控制对方了，这样的主机，通常就会被叫做3389肉鸡。Radmin是一款非常优秀的远程控制软件，4899就是Radmin默认使以也经常被黑客当作木马来使用（正是这个原因，目前的杀毒软件也对Radmin查杀了）。有的人在使用的服务端口号。因为Radmin的控制功能非常强大，传输速度也比大多数木马快，而且又不被杀毒软件所查杀，所用Radmin管理远程电脑时使用的是空口令或者是弱口令，黑客就可以使用一些软件扫描网络上存在Radmin空口令或者弱口令的主机，然后就可以登陆上去远程控制对恶劣，这样被控制的主机通常就被成做4899肉鸡。**-
**　　19.免杀：就是通过加壳、加密、修改特征码、加花指令等等技术来修改程序，使其逃过杀毒软件的查杀。**-
**　　20.加壳：就是利用特殊的酸法，将EXE可执行程序或者DLL动态连接库文件的编码进行改变（比如实现压缩、加密），以达到缩小文件体积或者加密程序编码，甚至是躲过杀毒软件查杀的目的。目前较常用的壳有UPX，ASPack、PePack、PECompact、UPack、免疫007、木马彩衣等等。**-
**　　21.花指令：就是几句汇编指令，让汇编语句进行一些跳转，使得杀毒软件不能正常的判断病毒文件的构造。说通俗点就是”杀毒软件是从头到脚按顺序来查找病毒。如果我们把病毒的头和脚颠倒位置，杀毒软件就找不到病毒了**

-

本文转自 [https://www.eqishare.com/other/803.html](https://www.eqishare.com/other/803.html)，如有侵权，请联系删除。