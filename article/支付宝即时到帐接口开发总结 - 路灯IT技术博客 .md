支付宝即时到帐接口总结：-
付款：-
1.配置AlipayConfig.java文件里的partner、key、seller\_email信息。（商户提供）-
2.支付页面：需要传入商品名称、金额、商品说明等说明。-
3.跳转到alilpayto.jsp中处理支付参数。（注意编码格式）-
4.登录自己的支付宝进行支付。-
5.返回-
return\_url.jsp(同步)可以处理业务逻辑并可写入html代码。-
notify\_url.jsp(异步)可以处理业务逻辑，有且只有输出success，且必须保证为空白页面，无任何HTML标签、空格、回车换行等字符。-
退款：-
在notify\_url.jsp中直接解析result\_details退款结果明细-
//格式：第一笔交易#第二笔交易#第三笔交易-
//第N笔交易格式：交易退款信息-
//交易退款信息格式：原付款支付宝交易号^退款总金额^处理结果码^结果描述-
-
双项接口中没有退款功能，需手动退款。-

-

本文转自 [https://www.eqishare.com/programming/468.html](https://www.eqishare.com/programming/468.html)，如有侵权，请联系删除。