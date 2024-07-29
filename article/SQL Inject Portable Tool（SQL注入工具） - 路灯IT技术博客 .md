-
\[attachment=332\]-
**SQL Inject Portable Tool使用说明-
**本工具是用来进行SQL注入的工具，主要针对一些没有错误返回信息的网站的表结构猜解（当然，如果有错误返回这个工具也适用，只是没必要使用这个工具了，因为有更好更快捷的工具），-
尤其是Java+Oracle，PHP+MySQL以及一部分ASP+SQLServer的网站。-
注意：测试版只有手动猜测模式（Common模式），需要Oracle和SQLServer自动模式的请注册以获取完全版本。-
Oracle、SQLServer模式使用方法如下：-
1\. Get方法：-
 a) URL中的填写与Common模式不同，这里只需要输入URL就可以了，如果可注入的参数为字符类型，请在相应的位置添加'来标明；-
 URL的填写如下：-
 [http://www.XXX.com/tsl2.jsp?pname=1'&id=1234](http://www.xxx.com/tsl2.jsp?pname=1%27&id=1234)-
 ^注意pname为字符类型的，所以添加了'。-
-
 b) 方法选择Get，在URL输入框中点击注入点-
 如：[http://www.XXX.com/tsl2.jsp?pname=1'&id=1234](http://www.xxx.com/tsl2.jsp?pname=1%27&id=1234)-
 ^鼠标点击点放在'后，用于更改Position输入框中的注入点值-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 选择Table Guess、Row Guess或者Detail Guess其中之一，注意，如果要进行Row Guess，必须在Table Name组合框中选择或者输入表名；如果要进行Detail Guess，除了输入表名之外-
，还需要输入需要猜解的列的名字，格式为：Row1|Row2|....|-
 e) 选择数据库的字符集，针对数据库的中文内容而设置，如果猜解结果存在乱码，选择适当的字符集重新猜解，其中unicode和double byte为双字节，UTF-8为3字节；-
 f) 输入猜解的条件，使用者需要熟悉SQL语句的语法；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Oracle或者SQLServer-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
-
2\. Post方法：-
 a) URL中的填写与Common模式不同，这里只需要输入URL就可以了-
 b) 方法选择Post，同时填入Post参数（如果是字符串型注入则加'），然后将鼠标放在注入点之后-
 如：Name=单荣花'&sfzh=211222198201125228&ID\_Year=2005&B1=提交-
 ^鼠标点击点放在'后，用于更改Position输入框中的注入点值-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 选择Table Guess、Row Guess或者Detail Guess其中之一，注意，如果要进行Row Guess，必须在Table Name组合框中选择或者输入表名；如果要进行Detail Guess，除了输入表名之外-
，还需要输入需要猜解的列的名字，格式为：Row1|Row2|....|-
 e) 选择数据库的字符集，针对数据库的中文内容而设置，如果猜解结果存在乱码，选择适当的字符集重新猜解，其中unicode和double byte为双字节，UTF-8为3字节；-
 f) 输入猜解的条件，使用者需要熟悉SQL语句的语法；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Oracle或者SQLServer-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
Common模式下使用方法如下：-
1\. Oracle+GET+数字猜解：-
 a) URL的填写如下：-
 [http://www.XXX.com/tsl2.jsp?pname=1'](http://www.xxx.com/tsl2.jsp?pname=1%27) and 0<nvl(length((SELECT TABLE\_NAME FROM(SELECT\*FROM(SELECT\*FROM(SELECT\*FROM USER\_TABLES ORDER BY 1ASC)WHERE ROWNUM<=1)ORDER-
BY 1DESC)WHERE ROWNUM<=1)),0) ---
 b) 方法选择Get-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 选择IsNumber-
 e) Position可由程序自动填写，将鼠标输入位置放到URL项需要做判断的数字（此处为"0"）之后，程序自动填写Position；-
 f) To填写范围，如果选择IsNumber，则为数字，否则为字符，此处为数字，如：255；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Common-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
2\. Oracle+POST+数字猜解：-
 a) URL的填写如下：-
 [http://www.XXX.com/tsl2.jsp](http://www.xxx.com/tsl2.jsp)-
 b) 方法选择POST，参数填写-
 pname=1' and 0<nvl(length((SELECT TABLE\_NAME FROM(SELECT\*FROM(SELECT\*FROM(SELECT\*FROM USER\_TABLES ORDER BY 1ASC)WHERE ROWNUM<=1)ORDER BY 1DESC)WHERE-
ROWNUM<=1)),0) --&B1=提交-
 多个参数以&间隔；-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 选择IsNumber-
 e) Position可由程序自动填写，将鼠标输入位置放到POST参数项需要做判断的数字（此处为"0"）之后，程序自动填写Position；-
 f) To填写范围，如果选择IsNumber，则为数字，否则为字符，此处为数字，如：255；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Common-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
3\. Oracle+GET+字符猜解：-
 a) URL的填写如下：-
 [http://www.XXX.com/tsl2.jsp?pname=1'](http://www.xxx.com/tsl2.jsp?pname=1%27) or 'T'=substr((SELECT TABLE\_NAME FROM(SELECT\*FROM(SELECT\*FROM(SELECT\*FROM USER\_TABLES where table\_name like '%USER%' ORDER BY-
1ASC)WHERE ROWNUM<=1)ORDER BY 1DESC)WHERE ROWNUM<=1),1,1)---
 b) 方法选择Get-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 取消IsNumber-
 e) Position可由程序自动填写，将鼠标输入位置放到URL项需要做判断的数字（此处为"T"）之后，程序自动填写Position；-
 f) To填写范围，如果选择IsNumber，则为数字，否则为字符，此处为字符，如：Z；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Common-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
2\. Oracle+POST+字符猜解：-
 a) URL的填写如下：-
 [http://www.XXX.com/tsl2.jsp](http://www.xxx.com/tsl2.jsp)-
 b) 方法选择POST，参数填写-
 pname=1' or 'T'=substr((SELECT TABLE\_NAME FROM(SELECT\*FROM(SELECT\*FROM(SELECT\*FROM USER\_TABLES where table\_name like '%USER%' ORDER BY 1ASC)WHERE ROWNUM<=1)ORDER-
BY 1DESC)WHERE ROWNUM<=1),1,1)--&B1=提交-
 多个参数以&间隔；-
 c) RefURL可填写（有些网站为防止盗链，必须填写）-
 d) 取消IsNumber-
 e) Position可由程序自动填写，将鼠标输入位置放到POST参数项需要做判断的数字（此处为"T"）之后，程序自动填写Position；-
 f) To填写范围，如果选择IsNumber，则为数字，否则为字符，此处为数字，如：Z；-
 g) Success condition为提交的URL条件成立时，网页内所含有的关键字（如果条件不成立，网页内一定不会含有），如：奶油-
 h) 模式选择Common-
 i) Fire!-
 j) 猜解的最终结果显示在最下面得Edit中-
 **点击下载：\[attachment=333\]**-

-

本文转自 [https://www.eqishare.com/redblack/630.html](https://www.eqishare.com/redblack/630.html)，如有侵权，请联系删除。