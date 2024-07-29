每逢5.12和哀悼日，各大门户网站都会把自己网站变灰色，以此来表示对逝者的哀悼。-
下面是一个java web项目网站变化的设计方案。-
思路是这样的，首先由个页面来操作网站是变灰还是不变灰，-
然后把选择的值（变灰，不变灰）传入到后台方法，存入一个静态变量中，-
让后再找到网站的公共页面加入判断代码动态显示变灰的代码。-
**第一步创建操作页面。**-
\[attachment=552\]-
代码：-
**<script>-
function yschange(){-
 var g = document.getElementById("gr").value;-
 window.location.href="webSiteServlet?action=isgray&g="+g;-
}-
 </script>-
 <body>-
 <%-
 if(com.peak.app.webSiteServlet.isgray){-
 %>-
 现在网站状态：<font color=red><b>已经变灰</b></font>。-
 <%-
 }else{-
 %>-
 现在网站状态：<font color=red><b>没有变灰</b></font>。-
 <%-
 }-
 %>-
 <br/>-
 选择是否变灰：-
 <select id="gr">-
 <option value="nogray" <%if(!com.peak.app.webSiteServlet.isgray){%> selected <%} %>>不变灰</option>-
 <option value="isgray" <%if(com.peak.app.webSiteServlet.isgray){%> selected <%} %>>变灰</option>-
 </select>-
 <input type="button" value="确定" onclick="yschange()"/>-
 </body>**-
**第二步后台接收操作的变量存入到服务期的某个txt文件中（最后新建个单独存放）。**-
代码：-
//全局变量-
**public static boolean isgray=false;-
 if(action.equalsIgnoreCase("isgray")){-
isgray = "isgray".equalsIgnoreCase(request.getParameter("g"));-
findNextPage="pagechangegray.jsp";-
 }**-
**第三步取出值来进行动态判断及显示。**-
代码：-
**<%-
if(com.peak.app.webSiteServlet.isgray){-
%>-
<style>-
html { filter:progid:DXImageTransform.Microsoft.BasicImage(grayscale=1); }-
</style>-
<%}%>**-
效果图变灰前：-
\[attachment=554\]-
-
效果图变灰后：\[attachment=553\]-
-
-
-
-
-
-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/551.html](https://www.eqishare.com/programming/551.html)，如有侵权，请联系删除。