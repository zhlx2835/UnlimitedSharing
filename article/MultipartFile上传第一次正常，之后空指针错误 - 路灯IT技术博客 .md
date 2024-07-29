今天刚给一人调试java上传空指针的错误。-
问题描述：MultipartFile+layui上传空指针，第一次请求时是可以上传成功，之后都失败。-
显示排查了很久初步判断后台方法没错，怀疑前端js错误，开始查了很就，第一次，第二次请求后的js，页面都是一样的，并不是这里问题。-
正当一点头绪没有时，查到第二次请求是调用了后台2次，第一次302错误，第二次是真正的空指针错误。感觉有希望了，顺着往下找。-
\[attachment=1540\]-
\[attachment=1538\]-
**查到RequestMapping的和webapp 的upload文件夹的 Url应该是冲突了，导致第二次请求失败。**-
**之后把controller的RequestMapping改成upload1就正常访问了。**-
\[attachment=1539\]-
-

-

本文转自 [https://www.eqishare.com/programming/89.html](https://www.eqishare.com/programming/89.html)，如有侵权，请联系删除。