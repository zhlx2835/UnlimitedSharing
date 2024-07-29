不支持iframe标签插入视频网页链接的方式，只支持video标签插入视频文件链接的方式。

适配UEditor类编辑器插入的video视频播放，停用插件也没有影响，开启后前端不论新旧文章内的视频都是使用DPlayer播放器。

全局设置文章内的视频默认的大小显示，自适应高度，视频播放界面可以设置左边或者右边显示指定的logo图片。

来这体验视频播放效果：[https://www.lyplugin.com/post/59](https://www.lyplugin.com/post/59)

![image.png](https://www.lyplugin.com/zb_users/upload/2023/03/202303021677738168460939.png)

编辑器插入有些视频文件链接是不能直接识别的，我们需要伪装成mp4视频文件链接

如直实的m3u8视频文件链接：https://qianniureplay.alicdn.com/circles/10632264.m3u8

在视频文件链接后面加?.mp4伪装：https://qianniureplay.alicdn.com/circles/10632264.m3u8?.mp4

如直实的webm视频文件链接：https://media.st.dl.eccdnx.com/steam/apps/256893883/movie480\_vp9.webm

在视频文件链接后面加?.mp4伪装https://media.st.dl.eccdnx.com/steam/apps/256893883/movie480\_vp9.webm?.mp4

![image.png](https://www.lyplugin.com/zb_users/upload/2022/07/202207151657865778792538.png)

参考代码：

 <video id="tmpVideo0" class="edui-video-video" controls="" preload="none" width="420" height="420" src="https://cache.m3u8.bdcdss.com/ufile/347cc860a70a83560d4ab7b81d7d58a5/e83b8da3f5f0a961984490c027f6a916.m3u8?.mp4" data-setup="{}"> <source src="https://cache.m3u8.bdcdss.com/ufile/347cc860a70a83560d4ab7b81d7d58a5/e83b8da3f5f0a961984490c027f6a916.m3u8?.mp4" type="video/mp4"/> </video>

-

-

本文转自 [https://www.eqishare.com/technology/1038.html](https://www.eqishare.com/technology/1038.html)，如有侵权，请联系删除。