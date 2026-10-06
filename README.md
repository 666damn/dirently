<div align="center">
  <img src="assets/dirently-icon.svg" width="96" height="96" alt="Dirently">
  <h1>Dirently</h1>
  <p><strong>Low-latency remote desktop that connects your devices directly.</strong><br>No account. The picture never takes a detour through our servers.</p>
  <p>
    <a href="../../releases/latest"><img alt="release" src="https://img.shields.io/github/v/release/666damn/dirently?label=release&color=25abff"></a>
    <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Android-2ed9ff">
    <img alt="public beta" src="https://img.shields.io/badge/public%20beta-free-ff1958">
  </p>
  <p>
    <a href="https://dirently.com"><strong>Website: dirently.com</strong></a>
    ·
    <a href="README.zh-CN.md">简体中文</a>
    ·
    <a href="README.md">English</a>
  </p>
</div>

> **Beta.** Dirently is in public beta and free while the beta lasts. This repository only hosts the installers; there is no source code here.

## Download

Pick your device below, or see all versions on **[Releases](../../releases/latest)**. Where GitHub is slow or blocked (for example in mainland China), use the **mirror** link: it is the same file.

| Platform | Download | Notes |
|---|---|---|
| Windows 10 / 11 (x64) | [Dirently-Setup-0.2.63.exe](../../releases/download/v0.2.63/Dirently-Setup-0.2.63.exe) · [mirror](https://download.dirently.com/v0.2.63/Dirently-Setup-0.2.63.exe) | Can share this PC and control other devices. |
| macOS 13 or later (Apple Silicon) | [Dirently-0.2.63-arm64.pkg](../../releases/download/v0.2.63/Dirently-0.2.63-arm64.pkg) · [mirror](https://download.dirently.com/v0.2.63/Dirently-0.2.63-arm64.pkg) | Can share this Mac and control other devices. Signed and notarized by Apple. |
| Android 12 or later | [Dirently-0.2.63.apk](../../releases/download/v0.2.63/Dirently-0.2.63.apk) · [mirror](https://download.dirently.com/v0.2.63/Dirently-0.2.63.apk) | Controls your computers; it does not share the phone. |
| iPhone / iPad (iOS / iPadOS 17 or later) | Coming soon to the App Store | Controls your computers. |

Each release includes a [`SHA256SUMS`](../../releases/download/v0.2.63/SHA256SUMS) file ([mirror](https://download.dirently.com/v0.2.63/SHA256SUMS)). To check a download:

- **Windows (PowerShell):** `Get-FileHash .\Dirently-Setup-<version>.exe`
- **macOS:** `shasum -a 256 Dirently-<version>-arm64.pkg`

Compare the result with the matching line in `SHA256SUMS`.

**Edge says the installer "isn't commonly downloaded"?** Hover over the download, click **…** → **Keep**, then **Show more** → **Keep anyway**.

**Windows shows "Windows protected your PC"?** The beta installer is not code-signed yet. Click **More info**, then **Run anyway**.

## Getting started

1. Install Dirently on the computer you want to reach and on the device you connect from.
2. On one of them, **create a group** and give it a password.
3. On the other device, **join the group** (you will need its password).
4. Your devices now see each other. Pick one and click **Connect**.

Computers share themselves by default, so you can connect to them right away (you can turn this off on the computer's own card). Everyone in a group can see its devices, so only give the password to people you trust.

The **[user guide](GUIDE.md)** covers installing on each platform, Mac permissions, the in-session menu, the phone shortcut bar, connection problems and uninstalling.

## How it connects

- A small Dirently service only helps your devices **find each other**.
- The picture, sound, input and files then go **directly between your devices**, encrypted.
- Nothing is relayed through our servers. Most home and office networks work, and automatic port mapping (UPnP) on your router helps.
- When both sides sit behind very strict networks, a direct connection may not be possible. Dirently then tells you why instead of silently falling back to a relay.
- **Can't connect?** Install the free [ZeroTier](https://www.zerotier.com/) on both devices and join them to the same ZeroTier network. Dirently finds the ZeroTier addresses by itself and connects over them, with no router setup. After turning ZeroTier on, give it a few seconds before connecting. If your phone just switched between Wi-Fi and mobile data, turn ZeroTier off and on again. (On Android, only one VPN app can run at a time, so ZeroTier can't run alongside another VPN.)

## Known limits

- **No relay server.** If both sides are behind very strict networks (some mobile or corporate ones), they may not be able to connect. Please report these; finding them is what the beta is for.
- **Hosts:** Windows 10/11 and Apple Silicon Macs only. Intel Macs and Linux are not supported.
- **Controllers:** Windows, Mac and Android. iPhone and iPad are coming later.
- **Remote microphone:** the controlled computer needs the free VB-CABLE virtual audio driver installed.
- **Gamepads:** Windows hosts only.
- **Very high latency:** over long-distance links (for example across continents), the picture can still freeze for a moment. We are working on it.
- **Beta software:** expect bugs and frequent updates.

## Privacy

- **No account:** no email and no sign-up.
- **Stored by the service:** only what it needs to introduce your devices, such as device and group identities.
- **Logs:** the service's security logs are deleted after **30 days**. Details are in the [Privacy Policy](PRIVACY.md).
- **Your data:** screen content, audio, keystrokes and files never pass through our servers.

Only connect to your own or your team's computers. Never install Dirently, join a group or turn on sharing because a stranger asked you to.

## Feedback and help

- **Bugs and ideas:** open an **[issue](../../issues)**.
- **Questions and chat:** join the **[Discord](https://discord.gg/6UeurVTxzt)**.
- **Email:** support [at] dirently.com

Just tell us which devices you used and what went wrong.

## Legal

- [Beta Licence Agreement](LICENSE.md): by installing or using Dirently you agree to it.
- [Privacy Policy](PRIVACY.md)
- [Third-party notices](THIRD-PARTY-NOTICES.md)
- [Security](SECURITY.md)

---

© 2026 Dirently. All rights reserved.
