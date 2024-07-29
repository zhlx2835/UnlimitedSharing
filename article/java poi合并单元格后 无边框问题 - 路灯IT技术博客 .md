![POI合并后没有边框.png](https://www.eqishare.com/zb_users/upload/2022/08/202208291661757127802739.png)

使用POI导出合并单元格时出现，右侧无边框现象，代码如下：

Row row0 = sheet.createRow(0); Cell cell\_0 = row0.createCell(0); cell\_0.setCellStyle(style); cell\_0.setCellValue("教师业务档案登记表"); //合并第一行 sheet.addMergedRegion(new CellRangeAddress(0, 0, 0, 6));

解决办法很简单，也很巧妙，因为只在第一个格中写了数据，其他格没有写数据，那可以在最右侧的单元格写上个空数据，然后再加上边框，在合并就可以了。

**最终解决：**

Row row0 = sheet.createRow(0); Cell cell\_0 = row0.createCell(0); cell\_0.setCellStyle(style); cell\_0.setCellValue("教师业务档案登记表"); Cell cell\_6 = row0.createCell(6); //最右侧加个空的格设置上样式 cell\_6.setCellStyle(style); //最右侧加个空的格设置上样式 cell\_6.setCellValue(""); //最右侧加个空的格设置上样式 //合并第一行 sheet.addMergedRegion(new CellRangeAddress(0, 0, 0, 6));

![POI合并后没有边框-1.png](https://www.eqishare.com/zb_users/upload/2022/08/202208291661757453527333.png)

-

本文转自 [https://www.eqishare.com/programming/986.html](https://www.eqishare.com/programming/986.html)，如有侵权，请联系删除。