同步或者提交的时候出现问题提示-
-
The working copy needs to be upgraded-
svn: Workingcopy 'E:\\JAVA\\Workspaces\\uhr' is too old (format 10,created by Subversion1.6)-
-
问题原因：项目是在svn是低版本时候检出的， 后来进行了svn版本升级 ，再更新项目就会出现如上问题。-
解决办法：更新该项目的svn-
右击项目--team--upgrade-
-

-

本文转自 [https://www.eqishare.com/programming/291.html](https://www.eqishare.com/programming/291.html)，如有侵权，请联系删除。