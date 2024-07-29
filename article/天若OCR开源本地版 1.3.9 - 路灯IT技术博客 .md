**天若ocr开源版本**的本地版，采用Chinese-lite和paddle-ocr识别，再也不用网络啦

推荐paddle-ocr识别，可以在识别结果里面切换接口

本软件离不开以下仓库、软件的帮助，在此表达崇高的感谢：

> [https://gitee.com/ZZK-1989/tianruoocr](https://gitee.com/ZZK-1989/tianruoocr)

> [https://github.com/DayBreak-u/chineseocr\_lite/tree/onnx/dotnet\_projects/OcrLiteOnnxCs](https://github.com/DayBreak-u/chineseocr_lite/tree/onnx/dotnet_projects/OcrLiteOnnxCs)

> [https://github.com/RapidAI/RapidOCR](https://github.com/RapidAI/RapidOCR)

软件为64位系统使用，win10/win7都行，没有测试win11，需要.net4.7.2

本程序主要靠粘贴复制，要是有大佬帮忙改改就好了

中文识别率还是很舒服的

线程设的4，可以修改

本软件不具备任何捐赠的地方，也欢迎大家传播使用，软件作者是机械专业学生，不具备太多编程能力，大部分问题都是自己百度谷歌解决，有问题欢迎交流。

**注意：**-

1.  编译的话需要引用Microsoft.ML.OnnxRuntime.dll，如果是为了win7能用可以引用我编译好的（在dll和runtime文件夹），也可以自己编译，需要把对应onnxruntime.dll放在运行文件夹中。如果不使用win7，可以直接使用nuget安装即可。
    
2.  更改nuget包管理为PackageReference，应该不要packages了，编译之前请先安装nuget的一堆包
    
3.  编译的话注意AdvRichTextBox.Designer.cs文件，必须重写，这个文件在切换的过程中有可能会被系统自动覆盖，需要复制回来
    

![天若OCR开源本地版 1.3.9快捷键.png](https://www.eqishare.com/zb_users/upload/2023/09/202309131694567469259319.png)

![天若OCR开源本地版 1.3.9设置.png](https://www.eqishare.com/zb_users/upload/2023/09/202309131694567469834856.png)

![天若OCR开源本地版 1.3.9识别文字.png](https://www.eqishare.com/zb_users/upload/2023/09/202309131694567469255640.png)

下载地址：-

github地址1：[https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle/releases/download/v1.3.9/tianruoocr-cl-v1.3.9v2.7z](https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle/releases/download/v1.3.9/tianruoocr-cl-v1.3.9v2.7z)

github地址2：[https://git.xfj0.cn/https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle/releases/download/v1.3.9/tianruoocr-cl-v1.3.9v2.7z](https://git.xfj0.cn/https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle/releases/download/v1.3.9/tianruoocr-cl-v1.3.9v2.7z)

蓝奏云：[https://wwuc.lanzouj.com/iGDPR17gtw4f](https://wwuc.lanzouj.com/iGDPR17gtw4f)

官方作者GitHub：[https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle](https://github.com/wangfreexx/wangfreexx-tianruoocr-cl-paddle)

-

本文转自 [https://www.eqishare.com/softwaretool/1112.html](https://www.eqishare.com/softwaretool/1112.html)，如有侵权，请联系删除。