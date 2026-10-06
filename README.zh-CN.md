<div align="center">
  <img src="assets/dirently-icon.svg" width="96" height="96" alt="Dirently">
  <h1>Dirently</h1>
  <p><strong>低延迟远程桌面，设备之间直接连接。</strong><br>不用注册账号，画面不绕经我们的服务器。</p>
  <p>
    <a href="../../releases/latest"><img alt="最新版本" src="https://img.shields.io/github/v/release/666damn/dirently?label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC&color=25abff"></a>
    <img alt="平台" src="https://img.shields.io/badge/%E5%B9%B3%E5%8F%B0-Windows%20%7C%20macOS%20%7C%20Android-2ed9ff">
    <img alt="公测" src="https://img.shields.io/badge/%E5%85%AC%E6%B5%8B-%E5%85%8D%E8%B4%B9-ff1958">
  </p>
  <p>
    <a href="https://dirently.com"><strong>官网：dirently.com</strong></a>
    ·
    <a href="README.zh-CN.md">简体中文</a>
    ·
    <a href="README.md">English</a>
  </p>
</div>

> **公开测试中。** 测试期间免费使用。本仓库只放安装包，不含源代码。

## 下载

按设备选择下载，所有版本见 **[Releases](../../releases/latest)**。GitHub 打不开或很慢时（例如在中国大陆），点 **国内下载**，文件完全相同。

| 平台 | 下载 | 说明 |
|---|---|---|
| Windows 10 / 11（x64） | [Dirently-Setup-0.2.63.exe](../../releases/download/v0.2.63/Dirently-Setup-0.2.63.exe) · [国内下载](https://download.dirently.com/v0.2.63/Dirently-Setup-0.2.63.exe) | 可以共享这台电脑，也可以控制其他设备。 |
| macOS 13 及以上（Apple 芯片） | [Dirently-0.2.63-arm64.pkg](../../releases/download/v0.2.63/Dirently-0.2.63-arm64.pkg) · [国内下载](https://download.dirently.com/v0.2.63/Dirently-0.2.63-arm64.pkg) | 可以共享这台 Mac，也可以控制其他设备。已经过 Apple 签名和公证。 |
| Android 12 及以上 | [Dirently-0.2.63.apk](../../releases/download/v0.2.63/Dirently-0.2.63.apk) · [国内下载](https://download.dirently.com/v0.2.63/Dirently-0.2.63.apk) | 用来控制电脑，不能共享手机。 |
| iPhone / iPad（iOS / iPadOS 17 及以上） | 即将上架 App Store | 用来控制电脑。 |

每个版本都附有 [`SHA256SUMS`](../../releases/download/v0.2.63/SHA256SUMS)（[国内下载](https://download.dirently.com/v0.2.63/SHA256SUMS)），可以用来核对下载的文件：

- **Windows（PowerShell）：**`Get-FileHash .\Dirently-Setup-<版本>.exe`
- **macOS：**`shasum -a 256 Dirently-<版本>-arm64.pkg`

把算出来的值和 `SHA256SUMS` 里对应的那一行对比。

**Edge 提示"通常不会下载"？** 把鼠标移到这条下载上，点"…"→"保留"，再点"显示更多"→"仍然保留"。

**Windows 提示"Windows 已保护你的电脑"？** 测试版安装包还没有代码签名。点"更多信息"，再点"仍要运行"即可。

## 使用方法

1. 在要被连接的电脑上和你用来连接的设备上，都装好 Dirently。
2. 在其中一台上**创建小组**，设置密码。
3. 在另一台上**加入这个小组**，需要输入小组密码。
4. 两边互相能看到了，选中要连接的设备，点**连接**。

电脑默认就开启了共享，装好就能被连接（可以在这台电脑自己的卡片上关闭共享）。同一个小组的人都能看到组里的设备，所以密码只给信得过的人。

**[使用指南](GUIDE.zh-CN.md)** 里有各平台的安装方法、Mac 权限、会话菜单、手机快捷键栏、连不上时怎么办和卸载方法。

## 连接方式

- Dirently 的协调器只负责让你的设备**互相找到对方**。
- 画面、声音、键鼠输入和文件都**在设备之间直接加密传输**。
- 不经过我们的服务器中转。大多数家庭和办公网络都能直连，路由器开启 UPnP（自动端口映射）会更顺利。
- 如果两边都在限制很严的网络里，可能无法直连。这时 Dirently 会告诉你原因，不会偷偷改走中转。
- **连不上？** 在两台设备上都装免费的 [ZeroTier](https://www.zerotier.com/)，加入同一个 ZeroTier 网络。Dirently 会自动发现 ZeroTier 的地址并通过它连接，不用设置路由器。打开 ZeroTier 后先等几秒再连接。如果手机刚在 Wi-Fi 和流量之间切换过，把 ZeroTier 关掉再打开一次。（Android 同一时间只能运行一个 VPN 类应用，开 ZeroTier 时不能同时开别的 VPN。）

## 已知限制

- **没有中转服务器。** 两边都在限制很严的网络里（部分手机网络或公司网络）时，可能连不上。遇到了请告诉我们，找出这些情况正是这次测试的目的。
- **被控端：**只支持 Windows 10/11 和 Apple 芯片的 Mac，不支持 Intel Mac 和 Linux。
- **控制端：**Windows、Mac 和 Android，iPhone 和 iPad 稍后推出。
- **远程麦克风：**被控的电脑需要另外安装免费的 VB-CABLE 虚拟声卡。
- **手柄：**只有 Windows 被控端支持。
- **延迟很高的线路：**跨洲这类长距离连接下，画面仍可能偶尔短暂卡住，我们正在改进。
- **测试版：**难免有 bug，更新也会比较频繁。

## 隐私

- **不用账号：**不需要邮箱，也不用注册。
- **协调器保存的内容：**只保存让设备互相找到所需的信息，比如设备和小组的身份。
- **日志：**协调服务的安全日志保存 **30 天**后自动删除。详见[隐私政策](PRIVACY.zh-CN.md)。
- **你的数据：**屏幕内容、声音、按键和文件都不经过我们的服务器。

只连接你自己或你团队的电脑。不要因为陌生人的要求去安装 Dirently、加入小组或开启共享。

## 反馈和帮助

- **问题和建议：**在 **[Issues](../../issues)** 里提。
- **交流和答疑：**加入 **[Discord](https://discord.gg/6UeurVTxzt)**。
- **邮箱：**support [at] dirently.com

告诉我们用的是什么设备、遇到了什么问题就行。

## 法律信息

- [测试版许可协议](LICENSE.zh-CN.md)：安装或使用 Dirently 即表示同意本协议。
- [隐私政策](PRIVACY.zh-CN.md)
- [第三方许可声明](THIRD-PARTY-NOTICES.md)
- [安全问题](SECURITY.md)

中文版为译文，与英文版不一致时以英文版为准。

---

© 2026 Dirently. All rights reserved.
