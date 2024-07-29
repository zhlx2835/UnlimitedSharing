重点：安装前你的空间、vps、服务器需要提前安装ionCube插件，才可以进行安装
=========================================

![iMobiTrax追踪统计程序的安装教程](https://i4userve.com/wp-content/uploads/2019/08/imobiTrax-300x73.jpg)-
iMobiTrax是一个流量追踪统计程序，可以同时追踪mobile和desktop广告，有了它我们就能跟踪每一个clicks，根据转化情况，我们就可以科学的优化我们的广告。和iMobiTrax类似的追踪工具还有Prosper202、AdsBridge和Voluum等等，后2者提供的是订阅服务，按流量多少付费，如果你流量比较多或者是跑Pop，采用后2者作为追踪工具的成本将会很大。Prosper202跟iMobiTrax类似，都是购买版权，然后安装在你自己的服务器，相对来说成本要低。本文将向你讲述iMobiTrax追踪系统的安装过程。

![iMobiTrax追踪统计程序的安装教程](https://i4userve.com/wp-content/uploads/2019/08/im-1-300x146.jpg)

前提条件：首先你肯定要有一个服务器或者空间，还要有一个域名。

准备工作：先去服务器上绑定域名，然后域名解析到服务器。在服务器上建立一个新的MYSQL数据库，并记录下数据库名，用户名以及密码。

首先，就是配置IM参数。将IM压缩包解压到本地，依次找到”\\account\\mt”文件夹下”mt\_config.php”文件。然后右键编辑（建议使用NotePad++打开，很方便，推荐给大家）。

![iMobiTrax追踪统计程序的安装教程](https://i4userve.com/wp-content/uploads/2019/08/im-2-300x46.jpg)

其次，输入数据库信息后保存，然后上传到空间（可以先打包上传，然后在空间直接解压。）。

最后，等你的域名解析生效之后，在浏览器输入http://XXX.com/account/install.php按照步骤进行设置就行了。这时整个IM就算搭建完成了。

程序安装完成之后，我们就可以登录iMobiTrax了，在浏览器访问www.XXX.com/account/login.php，输入安装时所创建账户的用户名和用户密码即可。

注意：我们在完成iMobiTrax安装之后，强烈建议你删除以下3个文件：-
./account/install.php-
./account/mt/mt\_dbinstall.php-
./xxx.zip （你上传的那个压缩包）-
要执行删除操作，你可以在FTP工具中找到相应文件，然后点击右键选择删除即可。

-

-

本文转自 [https://www.eqishare.com/technology/926.html](https://www.eqishare.com/technology/926.html)，如有侵权，请联系删除。