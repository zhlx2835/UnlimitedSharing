-
**打印代码：**-
**<SCRIPT language="JavaScript">-
 function printdiv() {-
 var newWin = window.open('printer', '', '');-
 var titleHTML = document.getElementByIdx\_x("printdiv").innerHTML;-
 for(var i=0;i<2;i++){-
 titleHTML = titleHTML.toString().replace("border=0", "border=1");-
 }-
 for(var i=0;i<2;i++){-
 titleHTML = titleHTML.toString().replace("cellSpacing=1", "cellSpacing=0");-
 }-
 newWin.document.write(titleHTML);-
 newWin.document.location.reload();-
 newWin.print();-
 newWin.close();-
 WebBrowser.ExecWB(7, 1); //预览-
 }-
-
 </SCRIPT>-
 <body>-
-
 <input type="button" id="print" value="打印" onclick="javascript:printdiv();"/>-
 <OBJECT classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
 <div id = "printdiv">-
 <table width="80%" cellspacing="1" cellpadding="1" bgcolor="#6CA6CD" border="0">-
 <tr>-
 <td>测试</td>-
 <td>sdff</td>-
 </tr>-
 <tr>-
 <td>sdff</td>-
 <td>sdff</td>-
 </tr>-
 <tr>-
 <td>sdff</td>-
 <td>sdff</td>-
 </tr>-
 </table>-
 </div>-
 </body>**-
-
打开-
<input name=Button onClick=document.all.WebBrowser.ExecWB(1,1) type=button value=打开>-
<OBJECT classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
另存为-
<input name=Button onClick=document.all.WebBrowser.ExecWB(4,1) type=button value=另存为><OBJECT-
-
classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
属性-
<input name=Button onClick=document.all.WebBrowser.ExecWB(10,1) type=button value=属性><OBJECT-
-
classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
打印-
<input name=Button onClick=document.all.WebBrowser.ExecWB(6,1) type=button value=打印><OBJECT-
-
classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
页面设置-
<input name=Button onClick=document.all.WebBrowser.ExecWB(8,1) type=button value=页面设置><OBJECT-
-
classid=CLSID:8856F961-340A-11D0-A96B-00C04FD705A2 height=0 id=WebBrowser width=0></OBJECT>-
刷新-
<input type=button value=刷新 name=refresh onclick="window.location.reload()">-
导入收藏-
<input type="button" name="Button" value="导入收藏夹" onClick=window.external.ImportExportFavorites(true,);>-
导出收藏-
<input type="button" name="Button3" value="导出收藏夹" onClick=window.external.ImportExportFavorites(false,);>-
加入收藏-
<INPUT name=Button2 onclick="window.external.AddFavorite(location.href, document.title)" type=button value=加入收藏夹>-
整理收藏夹-
<INPUT name=Submit2 onclick="window.external.ShowBrowserUI(OrganizeFavorites, null)" type=button value=整理收藏夹>-
查看原文件-
<INPUT name=Button onclick=window.location = "view-source:" + window.location.href type=button value=查看源文件>-
语言设置-
<INPUT name=Button onclick="window.external.ShowBrowserUI(LanguageDialog, null)" type=button value=语言设置>-
前进-
<INPUT name=Submit onclick=history.go(1) type=submit value=前进>-
后退-
<INPUT name=Submit2 onclick=history.go(-1) type=submit value=后退>

-

本文转自 [https://www.eqishare.com/programming/884.html](https://www.eqishare.com/programming/884.html)，如有侵权，请联系删除。