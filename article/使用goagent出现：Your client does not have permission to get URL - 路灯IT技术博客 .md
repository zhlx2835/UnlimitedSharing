如图使用goagent出现：-
**403\.** That’s an error.-
**Your client does not have permission to get URL /2 from this server. **That’s all we know.-
\[attachment=1205\]-
-
-
解决办法：-
打开goagent目录找到proxy.ini文件-
打开文件找到\[gae\]下边的-
**profile = google\_cn**-
**改**-
**profile = google\_hk**-
重启goagent就可以了！-
-

-

本文转自 [https://www.eqishare.com/technology/254.html](https://www.eqishare.com/technology/254.html)，如有侵权，请联系删除。