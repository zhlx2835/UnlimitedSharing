1.  登陆appstoreconnect -----> [https://appstoreconnect.apple.com](https://appstoreconnect.apple.com/)-
    

 2.点击用户和访问-

![iOS个人开发者账号 issID kid P8 的获取流程-后厂村路灯.png](https://www.eqishare.com/zb_users/upload/2023/04/202304111681194207306932.png)

 3.点击密钥 生成API密钥 填写相关名称信息

![iOS个人开发者账号 issID kid P8 的获取流程-后厂村路灯2.png](https://www.eqishare.com/zb_users/upload/2023/04/202304111681194230753332.png)

 4.名称随意填,访问选 管理

![iOS个人开发者账号 issID kid P8 的获取流程-后厂村路灯3.png](https://www.eqishare.com/zb_users/upload/2023/04/202304111681194230979137.png)

 5.获取到api密钥 复制iss kid

![iOS个人开发者账号 issID kid P8 的获取流程-后厂村路灯4.png](https://www.eqishare.com/zb_users/upload/2023/04/202304111681194230147981.png)

-

\----------------------------

ChatGPT回答：

要获取iOS个人开发者账号的issID、kid和P8，可以按照以下步骤进行：

1.登录到苹果开发者账号：在Safari浏览器中打开developer.apple.com，使用您的Apple ID登录到苹果开发者账号。

2.创建一个新的密钥：在“Certificates, Identifiers & Profiles”页面中，选择“Keys”选项卡，然后单击右上角的“+”按钮创建一个新的密钥。

3.为密钥提供名称：输入一个名称来标识此密钥。

4.选择密钥类型：在“Key Type”下拉菜单中，选择“Apple Pay”选项。

5.下载密钥：单击“Continue”按钮，然后单击“Download”按钮来下载您的私钥文件（.p8格式）。

6.获取issID和kid：打开您的.p8文件，使用任何文本编辑器打开它，您将在文件中看到iss和kid。iss是您的团队ID，kid是您的密钥ID。

现在，您已经成功获取了iOS个人开发者账号的issID、kid和P8，您可以使用这些信息来集成Apple Pay和其他苹果支付解决方案。

-

本文转自 [https://www.eqishare.com/technology/1066.html](https://www.eqishare.com/technology/1066.html)，如有侵权，请联系删除。