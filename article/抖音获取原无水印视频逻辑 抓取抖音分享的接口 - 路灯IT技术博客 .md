抓取抖音分享的接口
=========

[](https://github.com/dxxzst/video_spider/blob/master/douyin_share/README.md#%E5%AE%9E%E7%8E%B0%E9%80%BB%E8%BE%91)实现逻辑
----------------------------------------------------------------------------------------------------------------------

注意:全程得用移动端ua才行(以下测试全程用的iPhone7UA)，chrome直接打不开。

*   1 通过分享的短链接，获取长链接
    

*   如分享短链接 [https://v.douyin.com/JPa1xhq/](https://v.douyin.com/JPa1xhq/)
    
*   直接访问获取到长链接 [https://www.iesdouyin.com/share/video/6883418578486349070/?region=CN&mid=6883418927515421454&u\_code=0&titleType=title&did=59084494265&iid=2304201954427479&utm\_source=copy\_link&utm\_campaign=client\_share&utm\_medium=android&app=aweme](https://www.iesdouyin.com/share/video/6883418578486349070/?region=CN&mid=6883418927515421454&u_code=0&titleType=title&did=59084494265&iid=2304201954427479&utm_source=copy_link&utm_campaign=client_share&utm_medium=android&app=aweme)
    

*   2 获取video\_id
    

*   直接正则获取到上图的video后面的一串数字，video\_id即上面链接中的6883418578486349070
    

*   3 拼接video\_id获取，视频信息json数据
    

*   上面video\_id拼接成如下结果
    
*   [https://www.iesdouyin.com/web/api/v2/aweme/iteminfo/?item\_ids=6883418578486349070](https://www.iesdouyin.com/web/api/v2/aweme/iteminfo/?item_ids=6883418578486349070)
    

*   4 获取上面json数据中想要的数据
    
    \# 如下视频信息播放地址(默认包含水印) { "uri": "v0300f9f0000bu3ctfaajd99kv7dbidg", "url\_list": \[ "https://aweme.snssdk.com/aweme/v1/playwm/?video\_id=v0300f9f0000bu3ctfaajd99kv7dbidg&ratio=720p&line=0" \] }
    

*   json数据基本包含了，作者信息，视频信息(封面，bgm, 视频链接)如下：
    

*   5 获取无水印的视频
    

*   第4步中获取的播放地址是包含水印的，获取无水印的也简单
    
*   把视频url参数中的`playwm`替换成`play` (wm 没猜错就是`water mark`:水印的首字母缩写)
    
*   [https://aweme.snssdk.com/aweme/v1/play/?video\_id=v0300f9f0000bu3ctfaajd99kv7dbidg&ratio=720p&line=0](https://aweme.snssdk.com/aweme/v1/play/?video_id=v0300f9f0000bu3ctfaajd99kv7dbidg&ratio=720p&line=0)
    

整理步骤：

1.找到视频id

2.替换最后的id：https://www.iesdouyin.com/web/api/v2/aweme/iteminfo/?item\_ids=6883418578486349070

3.在json中找到 url\_list 里的地址，如：https://aweme.snssdk.com/aweme/v1/playwm/?video\_id=v0300f9f0000bu3ctfaajd99kv7dbidg&ratio=720p&line=0

4.将其中的playwm替换成play，得到：https://aweme.snssdk.com/aweme/v1/play/?video\_id=v0300f9f0000bu3ctfaajd99kv7dbidg&ratio=720p&line=0

-

-

本文转自 [https://www.eqishare.com/programming/919.html](https://www.eqishare.com/programming/919.html)，如有侵权，请联系删除。