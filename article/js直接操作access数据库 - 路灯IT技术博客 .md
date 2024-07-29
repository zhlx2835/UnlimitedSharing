**<html>-
 <head><titel>jstest</title></head>-
 <body>-
<script>-
 //connection-
 var con = new ActiveXObject("Adodb.Connection");-
 //var strConn= "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=c:\\\\jstest\\\\jstest.mdb";-
 var strConn = "DRIVER={Microsoft Access Driver (\*.mdb)};PWD=Storm\_LZS;UID=Storm\_LZS; DBQ=D:\\\\person.mdb";-
 con.open(strConn);-
-
 var rs=new ActiveXObject("ADODB.Recordset");-
 var sqlSel="select userid,password from Userlib";-
 //rs.LockType=rs.CursorType=1;-
 rs.Open(sqlSel,con);-
-
 //excute-
 //var sqlUpt="update Clients set name='saqsss';"-
 // con.execute(sqlUpt);**-
 **document.write('<table><tr><td>客户名称</td><td>电话</td></tr>');-
 while(!rs.EOF){-
 var userid=rs('userid');-
 var password=rs('password');-
-
 document.write('<tr><td>',userid,'</td><td>',password,'</td></tr>');-
 rs.moveNext();-
 }-
 rs.close;-
 con.close;-
 document.write('</table>');-
</script>-
 </body>-
</html>**-

-

本文转自 [https://www.eqishare.com/programming/883.html](https://www.eqishare.com/programming/883.html)，如有侵权，请联系删除。