1、进入项目目录，找到.project文件，打开。-
2、找到…代码段。-
3、在第2步的代码段中加入如下标签内容并保存：-
org.eclipse.wst.common.project.facet.core.nature-
org.eclipse.wst.common.modulecore.ModuleCoreNature-
org.eclipse.jem.workbench.JavaEMFNature-
4、项目目录下的.classpath文件，把所有Webroot字符串改为WebContent，保存。-
5、把目录下webroot的文件夹改名为WebContent。-
6、在eclipse中Java Resources:src目录的Libraries里添加web服务器需要的包，选择BiuldPath—–>configure Build Path——>当前窗面下选择选择Add Library—–>server Runtime——>选择需要的web服务器-
7、在eclipse的项目上点右键，刷新项目。-
8、在项目上点右键，进入属性（properties）-
9、在左侧列表项目中点击选择“Project Facets”，在右侧选择“Dynamic Web Module”和”Java”，点击保存即可。-
这时应该可以在eclipse下正常启动项目了-

-

本文转自 [https://www.eqishare.com/programming/86.html](https://www.eqishare.com/programming/86.html)，如有侵权，请联系删除。