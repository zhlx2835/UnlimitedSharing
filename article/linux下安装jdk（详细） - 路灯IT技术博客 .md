jdk1.6 linux版本下载-
[http://www.oracle.com/technetwork/java/javase/downloads/jdk6downloads-1902814.html](https://www.eqishare.com/programming/344.html)-
-
1.首先安装jdk-
jdk-6u11-linux-i586.bin-
这个是自解压的文件，在linux上安装如下：-
\# chmod 755-
jdk-6u11-linux-i586.bin-
\# ./jdk-6u11-linux-i586.bin-
（注意，这个步骤一定要在jdk-6u11-linux-i586.bin所在目录下）-
在按提示输入yes后，jdk被解压。-
出现一行字：Do you aggree to the above license terms? \[yes or no\]-
安装程序在问您是否愿意遵守刚才看过的许可协议。当然要同意了，输入"y" 或 "yes" 回车。-
-
2.配置环境变量-
#vi /etc/profile-
在里面添加如下内容-
export JAVA\_HOME=/soft/jdk1.6.0\_45-
export JAVA\_BIN=/soft/jdk1.6.0\_45/bin-
export PATH=$PATH:$JAVA\_HOME/bin-
export CLASSPATH=.:$JAVA\_HOME/lib/dt.jar:$JAVA\_HOME/lib/tools.jar-
export JAVA\_HOME JAVA\_BIN PATH CLASSPATH-
重启linux-
-
**3.jdk测试**-
用文本编辑器新建一个Test.java文件，在其中输入以下代码并保存：-
public-
class test {-
public static void main(String args\[\])-
{-
System.out.println("A new jdk test !");-
}-
}-
2\. 编译：在shell终端执行命令-
javac Test.java-
3\. 运行：在shell终端执行命令 java Test-
当shell下出现“A new jdk test-
!”字样则jdk运行正常-

-

本文转自 [https://www.eqishare.com/programming/344.html](https://www.eqishare.com/programming/344.html)，如有侵权，请联系删除。