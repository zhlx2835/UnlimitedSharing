-
Sub 测试word到excel()-
Dim excel As Object-
Dim workbook As Object-
Dim worksheet As Object-
-
-
Dim i As Integer-
Dim row As Integer-
Dim str As String-
-
-
-
-
Set excel = CreateObject("excel.application")-
Set workbook = excel.WorkBooks.Open("c:\\temp.xls")-
Set worksheet = workbook.WorkSheets(1)-
-
-
-
-
row = 2-
-
-
For i = 1 To ActiveDocument.Tables(1).Rows.count-
-
-
-
-
str = ActiveDocument.Tables(1).Cell(i, 3).Range.Text-
-
-
worksheet.Cells(row, 1).Value = str-
-
-
MsgBox "行:" & i & " 内容：" & str-
-
-
row = row + 1-
-
-
Next-
-
-
excel.Visible = True-
-
-
End Sub

-

本文转自 [https://www.eqishare.com/technology/295.html](https://www.eqishare.com/technology/295.html)，如有侵权，请联系删除。