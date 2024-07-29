**启动不提示 “Workspace Launcher”对话框的情况下**-
**首次启动Eclipse/MyEclipse时, 会弹出"Workspace Launcher"对话框, 提示设置Workspace路径. 设定好路径后, 倘若勾选了"Use this as the default and do not ask again", 那么以后再启动时就不会有提示, 直接进入默认工作空间.-
-
有3中方法可以更改workspace的路径设置：-
-
1\. 启动Eclipse/MyEclipse后, 打开"Window -> Preferences -> General -> Workspace", 点Workspace页上的"Startup and Shutdown", 然后勾选"Startup and Shutdown"页中的"Prompt for workspace on startup";-
-
-
-
2\. 用记事本打开"\\eclipse\\configuration\\.settings\\org.eclipse.ui.ide.prefs", 将"SHOW\_WORKSPACE\_SELECTION\_DIALOG"的值改为"true";-
-
P.S.: "RECENT\_WORKSPACES"的值表示设置过的workspace绝对路径. 第一个路径是当前设定的路径, 向后依次之前曾设置过的. 各路径之间用"\\n"分隔.-
-
-
-
3\. 删掉"\\eclipse\\configuration\\.settings\\org.eclipse.ui.ide.prefs".-
-
-
-
执行上述操作后, 再次启动, 又会弹出"Workspace Launcher"对话框, 可以重新设置了.-
**-
-

-

本文转自 [https://www.eqishare.com/programming/859.html](https://www.eqishare.com/programming/859.html)，如有侵权，请联系删除。