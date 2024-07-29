那么怎么做才能保证之前的配置不丢失呢？这时想到启动停止时显示的状态:"Loading workbench"，看来和这个workbench插件有关。查看工作空间中的.metadata/.plugins目录，在众多文件夹中-
发现了两个： org.eclipse.ui.workbench 和org.eclipse.ui.workbench.texteditor。删了这两个目录，重新启动eclipse。正常启动且原项目信息正确加载。-

-

本文转自 [https://www.eqishare.com/programming/349.html](https://www.eqishare.com/programming/349.html)，如有侵权，请联系删除。