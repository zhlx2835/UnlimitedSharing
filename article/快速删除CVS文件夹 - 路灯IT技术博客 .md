**@echo On-
@Rem d:/GZRAIL/-
@PROMPT \[Com\]#-
@for /r . %%a in (.) do @if exist "%%a\\CVS" rd /s /q "%%a\\CVS"-
@Rem for /r . %%a in (.) do @if exist "%%a\\CVS" @echo "%%a\\CVS"-
@echo Mission Completed.-
@pause**

-
复制以上代码。粘贴到txt中，保存成bat文件。-
把文件放到项目内，执行。-
把d:/GZRAIL/ 换成 你的项目路径。-
-
-
**删除文件夹的.svn工具[http://www.eqishare.com/read.php?tid=48](http://www.eqishare.com/read.php?tid=48)**-
-

-

本文转自 [https://www.eqishare.com/programming/550.html](https://www.eqishare.com/programming/550.html)，如有侵权，请联系删除。