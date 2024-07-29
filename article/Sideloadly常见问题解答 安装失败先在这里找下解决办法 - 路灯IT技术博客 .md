![sideloadly问题汇总.png](https://www.eqishare.com/zb_users/upload/2022/06/202206131655092531640861.png)

Sideloadly常见问题解答

-

问：Sideloadly 在连接到 Anisette 服务器时会传输哪些信息？-
答：我们仅将服务器用于 Anisette 数据。如果您使用免费的 Apple 开发者帐户，则对 Apple 服务器的每个请求都需要此数据。以下是我们的服务器可以看到的详尽信息列表：-
\- 您的 IP 地址-
\- 您的操作系统（win32、win64 或 macOS）-
\- Sideloadly 版本。

就这样。我们不会与任何人共享此信息，并且仅出于调试目的而在有限的时间内存储这些信息。您的 Apple ID 和密码只会发送到 Apple 服务器。

问：如何通过 Sideloadly 启用 Wi-Fi 侧载？-
答：要启用 Wi-Fi 侧载您的 iDevice，请确保您的计算机和 iOS 设备连接到同一网络。然后，您需要首先通过 USB 连接您的设备，并根据您的操作系统按照以下说明进行操作：-
-
Windows：打开 iTunes > 已连接设备 > 摘要 > 选项 > 启用“通过 Wi-Fi 与此 iDevice同步”选项 > 同步并完成。-
-
最新的 macOS： Finder > 在“位置”> 常规 > 启用“在 Wi-Fi 上显示此 iDevice ”选项 > 同步并完成下选择您的 iDevice。-
-
旧 macOS： 打开 iTunes > 已连接设备 > 摘要 > 选项 > 启用“" 选项 > 同步并完成。-
-
在某些情况下，如果 Sideloadly 没有无线检测到您的设备，您可能需要打开 iTunes。您还需要打开 iDevice 屏幕才能检测到它。

问：我可以使用侧载应用程序多长时间？-
答：普通且免费的 Apple Developer 帐户仅允许应用程序运行 7 天。7 天后，您可以使用相同的 Apple ID 再次旁加载它，只需确保您的进度已备份。使用付费 Apple 开发者帐户签名的 App 可以使用长达 1 年。

问：如何保存或加载我的游戏进度？-
答：您需要确保您的游戏进度在 Game Center、Facebook、Twitter 或 Google+ 上同步。如果游戏将其进度保存在本地，您将需要安装 IPA 覆盖您已经安装的IPA。为了覆盖，修改后的 IPA 必须具有相同的捆绑包 ID，并且您在旁加载时必须使用相同的 Apple ID。请参阅下面的详细信息。

问：我可以覆盖我当前的应用程序而不删除它吗？-
答：是的，这是可能的。为了实现这一点，您需要使用与之前侧载应用程序相同的 Apple ID 侧载 IPA。如果您之前手动设置了自定义捆绑 ID，则需要再次使用相同的 ID。

问：我可以侧载多少个应用程序？-
答：iOS 7、8、9：您可以在设备上加载任意数量的应用程序。但是，您的免费开发者帐户有限制，但您可以通过创建新的 Apple ID 轻松绕过这些限制。在 iOS 10、11、12、13、14 及更高版本上，您的设备上只能同时安装 3 个侧载应用程序。Apple 对此进行了限制，将不再允许免费的 Apple Developer 帐户。付费的 Apple 开发者帐户没有此类限制。

问：为什么我无法在侧载后恢复我的 Game Center 游戏进度？-
答：在最新的 iOS 版本中，Apple 已阻止免费 Apple 帐户的用户侧载与 App Store 应用具有相同捆绑 ID 的应用。为了在最新的 iOS 版本上进行旁加载，我们被迫设置唯一的捆绑包 ID，这样做时，Game Center 无法识别该应用程序，因此不会提示您恢复保存。

问：Sideloadly 不显示我的设备？-
答：如果发生这种情况，请尝试重新启动您的 PC，在您的设备连接时打开 iTunes，并确保您从 iDevice 的弹出窗口中点击“信任”。然后打开 Sideloadly。如果这没有帮助，请连接您的设备并确保它被您的 PC/iTunes 识别，然后打开 Sideloadly。您也可以尝试完全卸载然后重新安装 iTunes。此外，请确保您使用的是网络版 iTunes。

问：我如何信任该应用程序？如何修复“不受信任的开发者”？-
答：要在侧载后信任该应用程序，您需要转到 设置\->常规\->配置文件/VPN 和设备管理 ，然后点击您用于侧载的电子邮件，然后信任它。

问：Sideloadly 是否支持 iOS 7、8、9、10、11、12、13、14、15？-
A：Sideloadly 应该支持 iOS 7 到 iOS 15（以及未来的其他 iOS 版本）。如果您遇到任何 iOS 特定问题，请告诉我们，以便我们进行调查！

问：我可以将哪种 .dylibs 或 .debs 添加到我的 IPA 中？注入 dylib/deb/framework 后，应用程序在启动时崩溃。-
A: Sideloadly 支持所有 dylib/deb/framework 文件，但是，其中一些文件是专门为越狱制作的，在非越狱设备上侧载时会导致崩溃。Sideloadly 将自动尝试更新注入的文件以支持非越狱设备，但由于它们的制作方式，它并不总是 100% 工作。

问：Sideloadly 是否支持 Apple Silicon M1 Mac？-
答：是的！Sideloadly 已更新以支持 Apple Silicon MacBook、Mac Mini 和 iMac。在 Apple Silicon 设备上运行 Sideloadly 时，它会检测并在设备列表中显示 Mac 本身以安装 .IPA。我们已经在 Big Sur & Monterey 上对此进行了测试。

问：Sideloadly 是否可以在启用 SIP 的 Apple Silicon M1 Mac 上运行？-
答：是的！Sideloadly 已经过测试并与支持 SIP 的 Mac Mini 一起使用。目前还不确定是否禁用了 SIP。

问：为什么我打开侧载的 M1 iOS 应用程序时没有收到权限错误？-
答：如果您侧载的 IPA 已加密（通过 iTunes 下载或直接从您的设备下载），则会出现此问题。为了解决这个问题，您需要旁加载 IPA 的解密版本。

问：如何使用应用专用密码？-
答：特定于应用程序的密码部分通过 Sideloadly 起作用。仅当您使用已禁用茴香选项的付费 Apple Developer ID 时，应用程序专用密码才有效。

我可以在侧载应用上进行合法的应用内购买吗？-
抱歉不行。Apple 阻止应用内购买在侧载/企业安装的应用上运行。如果您想支持开发人员，请安装原始 App Store 版本并在那里进行应用内购买。

问：Sideloadly 支持哪个 Windows 版本？-
答：Sideloadly 应该可以在 Windows 7、8、10 和 11 上运行。为了获得最佳效果，建议使用 Windows 10 或更高版本。

问：Sideloadly 支持哪个 macOS 版本？-
答：Sideloadly 应该可以在 macOS 10.12 Sierra 及更高版本上运行。为获得最佳效果，建议使用 macOS Catalina、Big Sur、Monterey 及更高版本。

问：如何解决“第二次请求 2FA”？-
答：这不再是最新的 Sideloadly 的问题。

问：如何修复“错误'machineName'”？-
答：一些成员报告说更改计算机名称会有所帮助。从开始菜单中搜索“计算机名称”或“机器名称”。

问：如何解决“您的 App ID 上限已达到上限。您每 7 天最多可以创建 10 个 App ID。”？-
答：这是 Apple 对免费开发者帐户设置的限制。要解决此问题，您可以等待几天再试一次，或者使用另一个 Apple ID 进行旁加载。

问：如何解决“此设备已达到使用免费开发者配置文件安装应用程序的最大数量”？-
答：这是 Apple 对免费开发者帐户设置的限制。如果您使用免费的 Apple Developer 帐户，您的设备上只能同时安装 3 个侧载应用程序。

问：如何修复“调用lockdownd\_client\_new\_with\_handshake 失败：LOCKDOWN\_E\_INVALID\_HOST\_ID”错误？-
答：当被问及时，请确保您已从您的设备信任您的 PC。您可以尝试在保持设备插入的情况下重新启动 PC。在最新的 macOS 上，打开 Finder -> 位置 -> iDevice -> 信任。或者打开 iTunes 并同步您的设备。

问：如何修复“调用 np\_client\_new 失败：NP\_E\_CONN\_FAILED”错误？-
答：请确保您卸载 Microsoft Store 版本的 iTunes 并安装普通/网络版本 ( [x64](https://www.apple.com/itunes/download/win64) - [x32](https://www.apple.com/itunes/download/win32) )。之后，连接您的设备并进行同步，然后打开 Sideloadly。

问：如何修复“调用 afc\_file\_close 失败：AFC\_E\_MUX\_ERROR”错误？-
答：请确保您卸载 Microsoft Store 版本的 iTunes 并安装普通/网络版本 ( [x64](https://www.apple.com/itunes/download/win64) - [x32](https://www.apple.com/itunes/download/win32) )。之后，连接您的设备并进行同步，然后打开 Sideloadly。

问：如何修复“用于签署可执行文件的身份不再有效”错误？-
A: 请确保您的计算机和 iDevice 上的时间和日期是最新的并且相同。

问：如何修复“设备上没有剩余空间”错误？-
答：此错误通常意味着您的计算机上的硬盘驱动器上没有剩余空间。请检查并确保您的计算机上有足够的空间供 Sideloadly 工作。

问：如何解决“获取茴香酒失败：500 INTERNAL SERVER ERROR”-
答：这是由服务器错误引起的临时问题。如果您收到此消息，请稍后再试。

问：如何修复“无效参数 /path/to/app.ipa”-
答：当下载的 .IPA 文件已被您的防病毒软件隔离或删除时，会发生这种情况。或者可能正在被您计算机上的另一个进程使用。

问：如何解决我的 macOS 上的“Sideloadly 无法打开，因为无法验证开发者”的问题？-
答：如果您收到此消息，您需要前往系统偏好设置\->安全和隐私 ，并且您应该可以为 Sideloadly 选择“仍然打开”。

问：如何解决“用于签署可执行文件的身份不再有效。”？-
答：此消息表示您的计算机和 iOS 设备上的时间和日期可能不正确。请在您的计算机和 iOS 设备上使用正确的当前时间，然后重试。

问：如何修复“找不到此可执行文件的有效配置文件。”？-
答：我们认为此消息也与您设备的日期和时间相关联。请在您的计算机和 iOS 设备上使用正确的当前时间，然后重试。

问：如何解决“DeviceNotSupportedByThinning（设备 iPhone/iPadx，y 不在支持的设备列表中”？-
答：此消息表示您使用的设备型号不受此 .IPA 支持。但是，如果您在 Sideloadly 的高级选项下 启用“删除对受支持设备的限制”，然后重试。

问：如何修复“IncorrectArchitecture (Failed to find matching arch for 64-bit Mach-O input file)”？-
答：此消息表示您尝试安装的 .IPA 文件不支持您的设备。没有解决此问题的方法。

问：如何解决“未定义默认情况”？-
答：此消息通常表示 .IPA 中的文件已损坏或格式不正确。在继续之前，您需要从 IPA 中删除损坏的文件。在呈现给我们的大多数情况下，该文件似乎是/AppName.app/ftm.dylib。

问：如何解决“加密的版本与加载的共享对象不匹配。如果您的 Python 路径中安装了多个加密副本，可能会发生这种情况。请尝试创建新的虚拟环境来解决此问题。”？-
答：如果您收到此消息，请从最新链接重新安装 Sideloadly。

-

-

本文转自 [https://www.eqishare.com/technology/946.html](https://www.eqishare.com/technology/946.html)，如有侵权，请联系删除。