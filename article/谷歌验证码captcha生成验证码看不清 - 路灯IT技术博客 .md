测试代码生成时，验证码就是不清楚的。-
1.从网上找了相应的配置设置也不行。-
2.而且发现配置的验证码范围：properties.setProperty("kaptcha.textproducer.char.string", "123456789");不起作用，生成的有字母。-
-
周末折腾了2天，没解决掉。重要在谷歌帮助下搜到了靠谱的解决办法。-
1.代码问题-
2.代码问题-
3.不显示是缺少字体问题-
-
**原因是Linxu系统缺少字体导致**-
解决办法：[https://www.cnblogs.com/zzzhao/p/12838039.html](https://www.eqishare.com/java/29.html)-
-
-
-

-

本文转自 [https://www.eqishare.com/java/29.html](https://www.eqishare.com/java/29.html)，如有侵权，请联系删除。