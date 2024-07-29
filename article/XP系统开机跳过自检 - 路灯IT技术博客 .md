**方法一、**-
开始----------cmd------Regedit，依次选择“HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Session Manager”子键，然后在右侧窗口中找到“BootExecute”键值项并将其数值清空或者0，最后按“F5”键刷新注册表即可-
\[attachment=319\]-
**方法二、**-
有时候电脑非正常关机，再开机时就会出现自检，要等它，，，还有的某个盘里出现损坏文件的话也会每次都自检的，，，，要想电脑久远不自检，很简单，如果是2000/XP系统的话，只要运行中运行：-
chkntfs /T:0-
chkntfs /X C:-
就OK了-
chkntfs /T:0 设定自检等待时间为"零",当然也可以自定义等待时间-
chkntfs /X C: 可以取消开机对C盘的自动扫描，也可以改成其它盘-
**类似方法**-
HKEY\_LOCAL\_MACHINESYSTEM\\CurrentControlSet\\Control\\Session Manager\\Memory ManagementPrefetchParameters，在右边找到EnablePrefetcher主键，把它的默认值3改为1， 它就只转一圈,你改成0试一试?-
-
开始--运行--cmd,输入:-
chkntfs /t:0。这样系统以后就不会再自动检测硬盘了-
自检是因为非正常关机引起的 每次关机的时候不要直接断电源 关掉正在运行的程序 然后再用开始的关机程序关机-
-
**原理**-
windows在遇到非法关机后，磁盘读写操作还没有完成，数据都保存在内存里，而内存一旦断电里边的数据就会全部丢失，这样一下系统就会丢失数据而无法往磁盘里保存数据，并且读写操作无法完成而被迫终止。-
 当你下一次开机的时候，windows就会自动检测硬盘分区上的错误，并且试图修复错误。最好不要跳过这个步骤，否则以后系统再对硬盘进行读写操作的话，会由于上次意外关机造成的隐患而导致新的读写错误。长期下去会导致硬盘频繁出现读写错误，最终影响硬盘寿命。-

-

本文转自 [https://www.eqishare.com/technology/633.html](https://www.eqishare.com/technology/633.html)，如有侵权，请联系删除。