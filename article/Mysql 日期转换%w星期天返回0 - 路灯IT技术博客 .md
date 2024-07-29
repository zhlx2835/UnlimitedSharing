DATE\_FORMAT(date,format)直接上个例子：取出当前时间的年份-
select DATE\_FORMAT(SYSDATE(), '%Y')返回值：2020-
-
**常用格式**-
-

格式

描述

%Y

年份，4位

%y

年份，2位

%m

月份，2位，00 - 12

%c

月份，0 - 12

%d

月的天，2位，00 - 12

%e

月的天，0 - 12

%H

小时，00 - 23

%h

小时，00 - 12

%i

分钟，00 - 59

%s

秒，00 - 59

**%w**

**星期几，星期日是0**

因此，常见的日期格式化yyyy-MM-dd HH:mm:ss，用如下SQL表示：-
select DATE\_FORMAT(SYSDATE(), '%Y-%m-%d %H:%i:%s')-
输出：2020-09-02 13:53:41-

-

本文转自 [https://www.eqishare.com/db/28.html](https://www.eqishare.com/db/28.html)，如有侵权，请联系删除。