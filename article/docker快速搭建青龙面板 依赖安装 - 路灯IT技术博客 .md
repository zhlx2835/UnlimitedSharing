![](https://user-images.githubusercontent.com/22700758/191449379-f9f56204-0e31-4a16-be5a-331f52696a73.png)

支持python3、javaScript、shell、typescript 的定时任务管理面板

**功能：**

功能支持多种脚本语言（python3、javaScript、shell、typescript）

支持在线管理脚本、环境变量、配置文件

支持在线查看任务日志

支持秒级任务设置

支持系统级通知

支持暗黑模式

支持手机端操作

-

官方github：[https://github.com/whyour/qinglong](https://github.com/whyour/qinglong)

-

一、拉去最新镜像

docker pull whyour/qinglong

二、启动镜像

docker run -dit \\ -v $pwd/ql/config:/ql/config \\ -v $pwd/ql/log:/ql/log \\ -v $pwd/ql/db:/ql/db \\ -v $pwd/ql/scripts:/ql/scripts \\ -v $pwd/ql/jbot:/ql/jbot \\ -p 5700:5700 \\ -e ENABLE\_HANGUP=true \\ -e ENABLE\_WEB\_PANEL=true \\ --name qinglong \\ --hostname qinglong \\ --restart always \\ whyour/qinglong:latest

使用docker ps查看服务使用启动

三、服务器开发对应端口5700

http://ip:5700/

进入首页设置账号后可进入系统！

-

**常用Cron表达式:**

在线Cron表达式生成器：[https://www.pppet.net/](https://www.pppet.net/ "在线克隆表达式")

 （1）0 0 2 1 \* ? 表示在每月的1日的凌晨2点调整任务   （2）0 15 10 ? \* MON-FRI 表示周一到周五每天上午10:15执行作业   （3）0 15 10 ? 6L 2002-2006 表示2002-2006年的每个月的最后一个星期五上午10:15执行作   （4）0 0 10,14,16 \* \* ? 每天上午10点，下午2点，4点   （5）0 0/30 9-17 \* \* ? 朝九晚五工作时间内每半小时   （6）0 0 12 ? \* WED 表示每个星期三中午12点   （7）0 0 12 \* \* ? 每天中午12点触发   （8）0 15 10 ? \* \* 每天上午10:15触发   （9）0 15 10 \* \* ? 每天上午10:15触发   （10）0 15 10 \* \* ? 每天上午10:15触发   （11）0 15 10 \* \* ? 2005 2005年的每天上午10:15触发   （12）0 \* 14 \* \* ? 在每天下午2点到下午2:59期间的每1分钟触发   （13）0 0/5 14 \* \* ? 在每天下午2点到下午2:55期间的每5分钟触发   （14）0 0/5 14,18 \* \* ? 在每天下午2点到2:55期间和下午6点到6:55期间的每5分钟触发   （15）0 0-5 14 \* \* ? 在每天下午2点到下午2:05期间的每1分钟触发   （16）0 10,44 14 ? 3 WED 每年三月的星期三的下午2:10和2:44触发   （17）0 15 10 ? \* MON-FRI 周一至周五的上午10:15触发   （18）0 15 10 15 \* ? 每月15日上午10:15触发   （19）0 15 10 L \* ? 每月最后一日的上午10:15触发   （20）0 15 10 ? \* 6L 每月的最后一个星期五上午10:15触发   （21）0 15 10 ? \* 6L 2002-2005 2002年至2005年的每月的最后一个星期五上午10:15触发   （22）0 15 10 ? \* 6#3 每月的第三个星期五上午10:15触发

-

依赖安装

NodeJS依赖

crypto-js prettytable dotenv jsdom date-fns tough-cookie tslib ws@7.4.3 ts-md5 jsdom -g jieba fs form-data json5 global-agent png-js @types/node require typescript js-base64 axios

Python3

requests canvas ping3 jieba

Linux依赖

bizCode bizMsg lxml

-

-

本文转自 [https://www.eqishare.com/technology/1030.html](https://www.eqishare.com/technology/1030.html)，如有侵权，请联系删除。