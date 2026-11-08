<div align="center">
  <a href="GUIDE.zh-CN.md">简体中文</a> · <a href="GUIDE.md">English</a>
</div>

# Dirently user guide

Control your own computers from another computer, a phone or a tablet. Your
devices connect directly to each other. No account needed.

[Getting started](#getting-started) ·
[macOS](#macos-first-launch) ·
[Windows](#windows-first-launch) ·
[Android](#android) ·
[iPhone and iPad](#iphone-and-ipad) ·
[Remote microphone](#remote-microphone) ·
[Shortcuts](#keyboard-shortcuts) ·
[Can't connect?](#cant-connect) ·
[Uninstall](#uninstall)

## Getting started

1. **Install Dirently** on the computer you want to control and on the device
   you connect from. Download the Windows, Mac and Android versions from
   [dirently.com](https://dirently.com/#download) (they are also on
   [Releases](../../releases/latest)). For iPhone and iPad, see
   [iPhone and iPad](#iphone-and-ipad).
2. **Create a group** on one of them: on the **Devices** page, click
   **Create group**. Enter a **Group name** and a **Group password** (at least
   10 characters and not a common one; **Generate strong password** makes one), keep
   **Private group**, and click **Create and join**.
3. **Join the group** on the other device: click **Find group**, search for the
   name, click **Join**, type the password and click **Join group**. With a
   one-time invitation from the group's administrator, click **Use an
   invitation** in **Find group** instead and paste the code or link.
4. **Check that the computer is shared.** Sharing is on by default: the
   computer's own card then shows **Stop sharing**. If it shows
   **Share this device**, click it.
5. **Connect:** on the other device, click **Connect** on that computer's card.

Good to know:

- Anyone can find a group by name with **Find group**. Use a strong password
  and share it only with people you trust.
- To add a device without giving out the password, open **Manage group** →
  **Invitations and protection** → **Invite a new device**. Each invitation
  (code, link or QR code) admits one device once. There you can also turn on
  **Require administrator approval**: a correct password then only sends an
  application, which an administrator approves. If someone keeps guessing the
  password, administrators see a warning there.
- After 10 wrong passwords, a device is blocked from that group until the
  group's administrator unbans it (**Manage group** → **Bans** → **Unban**).
- Keep all your devices on the same Dirently version.

## macOS first launch

You need an Apple Silicon Mac with macOS 13 or later.

1. Open `Dirently-<version>-arm64.pkg` and follow the installer. The package is
   signed with our Developer ID and notarized by Apple, so macOS opens it
   without a warning.
2. Dirently then starts in the background. Click its menu bar icon and choose
   **Show Dirently**, or open it from Applications.
3. Turn on these permissions in **System Settings → Privacy & Security**. A Mac
   that only controls other devices does not need the first two.

| Permission | Why |
|---|---|
| Screen Recording (macOS 15 and later: Screen & System Audio Recording) | To send this Mac's screen and sound. |
| Accessibility | So the other device's mouse and keyboard can control this Mac, and for the F12 emergency disconnect. |
| Input Monitoring | Recommended: makes the F12 emergency disconnect more reliable and avoids stuck keys after a session. macOS does not ask for it; click **+** below the list and add Dirently yourself. |
| Microphone | Only to send this Mac's microphone to a computer you control. |
| Local Network | To connect directly to devices on your network. Allow it when asked. |

If macOS asks you to quit and reopen Dirently, do it. The lists show it as
Dirently; if you also see dirently-host, turn that on too.

Closing the window does not quit Dirently; it stays in the menu bar so the Mac
stays reachable. To quit, choose **Exit** from the menu bar icon.

## Windows first launch

You need Windows 10 or 11, 64-bit.

1. Run `Dirently-Setup-<version>.exe`.
2. If you see **Windows protected your PC**, click **More info**, then
   **Run anyway**. The beta installer is not code-signed yet.
3. Click **Yes** to allow changes. Setup adds a background service, firewall
   rules, a virtual display driver (so a PC without a monitor can be shared)
   and, if missing, the ViGEmBus driver for remote gamepads.
4. Dirently opens and from now on starts with Windows (**Settings → Sharing →
   Start Dirently with Windows**). Closing the window keeps it running in the
   notification area.

## Android

The Android app controls your computers. The phone itself can't be controlled.
You need Android 12 or later.

1. On the phone, download the `.apk` from
   [dirently.com](https://dirently.com/#download) (it is also on
   [Releases](../../releases/latest)) and open it. Allow your browser or file
   manager to install apps (**Allow from this source**), then tap **Install**. If Play Protect warns
   about an unknown app, you can still install it.
2. Create or join a group as in [Getting started](#getting-started). Computers
   that are online and shared appear in the list. Tap **Connect**.
3. In a session, tap the small tab at the top for the session menu:
   **Keyboard**, **Input** (touch, trackpad or virtual mouse),
   **Microphone passthrough**, **Files** and **Disconnect**.

## iPhone and iPad

The iPhone and iPad app controls your computers. The iPhone or iPad itself
can't be controlled. You need iOS or iPadOS 17 or later; the same app works on
both.

1. Install Dirently from the
   [App Store](https://apps.apple.com/app/id6817623617). The App Store version
   is not yet available in mainland China: there, install Apple's TestFlight
   app first, then join the
   [public beta on TestFlight](https://testflight.apple.com/join/cQFb6pPh).
2. Open Dirently. When iOS asks to find devices on your local network, allow
   it.
3. Create or join a group as in [Getting started](#getting-started). Computers
   that are online and shared appear in the list. Tap **Connect**.
4. In a session, tap the small tab at the top for the session menu:
   **Input** (direct touch, trackpad or virtual mouse), **Keyboard** with the
   [phone shortcut bar](#keyboard-shortcuts), **Gamepad** (on-screen, Windows
   computers only), **Files**, **Microphone passthrough** and **Disconnect**.
   You can also change the resolution, refresh rate, codec and bandwidth there.

Good to know:

- The clipboard is shared with the computer.
- In **Files** you can upload photos, videos and documents to the computer.
  Files you download from it are saved in the Files app, under
  **On My iPhone** (or **On My iPad**) → **Dirently**.
- Hardware keyboards, mice and trackpads work too. Game controllers work with
  Windows computers.
- After you switch to another app, iOS keeps the session for only about 30
  seconds.

## Remote microphone

You can send your microphone to the computer you control, so its apps (a call,
a game) hear you. That computer, Windows or Mac, needs the free **VB-CABLE**
driver. Dirently does not include it.

1. On the computer you control, install VB-CABLE from
   https://vb-audio.com/Cable/ and restart. VB-CABLE is donationware under
   VB-Audio's own license.
2. There, **Settings → Sound → Virtual microphone bridge** should say
   **VB-CABLE detected: …**. If it says **VB-CABLE was not detected on this
   device.**, finish the install, restart, and click **Check again**.
3. On the device you control from, turn on **Microphone passthrough** in
   **Settings → Sound** or in the session menu.

In the session menu, **Microphone - Ready** means it works. With
**(remote default input)**, Dirently also made VB-CABLE the remote default
microphone for the session. **Remote virtual microphone missing** means
VB-CABLE is not installed there: use **Get VB-CABLE**, then
**Retry detection**. If an app still can't hear you, pick the VB-CABLE
microphone in that app (on Windows: **CABLE Output**).

## Keyboard shortcuts

In the session window:

| Action | Windows | Mac |
|---|---|---|
| Disconnect | F12 | ⌘W |
| Fullscreen on/off | F11 | **Fullscreen** in the session menu |
| Release mouse and keyboard | Ctrl+Alt+Z | ⌃⌥Z (Control+Option+Z) |

- To change these shortcuts or the emergency-disconnect key below, open
  **Settings → Shortcuts**.
- The session menu is the movable Dirently icon in the session window.
- Release is for when **Immersive mode** (Settings → Remote picture) or a game
  holds the mouse and keyboard. Click in the window to capture them again.
- On a Mac, F11 and F12 go to the remote computer like other keys.

**Emergency disconnect.** If someone is controlling your computer, press
**F12** on that computer's own keyboard (Mac: usually **fn+F12**; needs the
Accessibility permission). It ends every incoming session at once. It only
disconnects, so they can connect again: to keep everyone out, click
**Stop sharing** or turn on **Block all remote control** (Settings → Sharing).
It does not work on the Windows lock screen or admin prompts, or in Mac
password fields.

**Phone shortcut bar.** In a session, open the session menu and tap
**Keyboard**. A bar above the keyboard adds keys that phones lack, matching the
computer you control:

| | Windows computer | Mac |
|---|---|---|
| Held keys (tap, then the next key) | Ctrl, Alt, Shift, Win | ⌃ Control, ⌥ Option, ⌘ Command, ⇧ Shift |
| Keys | Esc, Tab, Del, arrows | Esc, Tab, Del, arrows |
| Shortcuts | Win, Ctrl+Alt+Del, Ctrl+Shift+Esc, Alt+Tab, Copy, Paste | ⌘Space, ⌥⌘Esc, ⌘Tab, Copy, Paste |

Tap **Shift** twice (on, then off) with no key in between to switch the
computer's input method between Chinese and English (if it switches on Shift).

## Can't connect?

Dirently has no relay. Our server only helps your devices find each other;
picture, sound and input go straight between them, never through our servers,
not even as a fallback. So the two networks must be able to reach each other.
Most home networks can. When they can't, Dirently explains why, starting with
"The two networks cannot reach each other directly."

1. **Basics.** Both devices are online, in the same group and on the same
   version. The computer shows **Stop sharing**, and **Block all remote
   control** is off (Settings → Sharing).
2. **Automatic port mapping.** In Dirently, keep **Enable UPnP automatic port
   mapping** on (Settings → Network, on by default). Dirently then asks the
   router for its own port mapping. The **NAT** box there shows the result,
   for example **Port mapping: UDP …**.
3. **Mapping table full.** If you see **Port mapping: the router refused; its
   mapping table may be full. Review mappings you no longer need.**, click
   **Review router mappings** (Settings → Network) and delete the mappings you
   no longer need. If the message comes back, use ZeroTier (next step).
4. **Use ZeroTier (easiest).** Install the free [ZeroTier](https://www.zerotier.com/)
   on both devices and join them to the same ZeroTier network. Dirently finds
   the ZeroTier addresses by itself and connects over them, with no router
   setup. After turning ZeroTier on, give it a few seconds before connecting.
   If your phone just switched between Wi-Fi and mobile data, turn ZeroTier
   off and on again.
   ZeroTier usually connects the devices directly, so latency stays the
   same; only when it can't get through either does it relay through its own
   servers, which adds delay (`zerotier-cli peers` shows DIRECT or RELAY). On
   Android only one VPN app can run at a time, so ZeroTier can't run alongside
   another VPN.
5. **Strict networks.** If Dirently says one side is behind its provider's NAT
   (CGNAT), the connection relies on the other side: keep automatic port
   mapping on there (step 2). If both sides are on strict networks (mobile
   data, office, school, hotel, some VPNs), a direct connection may be
   impossible; use ZeroTier, or move one side to a home network.
6. **Firewall.** Allow Dirently in any third-party firewall or security app.

**No picture?** If you see **The remote device sent no video**, set **Display**
to **Virtual display** in Settings → Sharing on that Windows computer.

**Report a problem:** tell us which devices you used (for example "Windows 11
PC → MacBook"), what went wrong, and the message Dirently showed. On Android
you can attach **Settings → General → Diagnostics → Export diagnostics** (it leaves out
passwords, keys, IDs and IP addresses).
[Discord](https://discord.gg/6UeurVTxzt) · support [at] dirently.com ·
[GitHub Issues](../../issues)

## Uninstall

**Windows:** Settings → Apps → Installed apps (Windows 10: Apps & features) →
**Dirently** → **Uninstall**. This removes the app, its service, firewall rules
and virtual display driver. It keeps the ViGEmBus driver (other apps may use
it; remove it from the same list if not), VB-CABLE if you installed it, and
this PC's identity and settings in `C:\ProgramData\Dirently` (so a reinstall
is back in its group; delete the folder for a clean removal).

**macOS:** choose **Exit** from the menu bar icon, then drag **Dirently** from
Applications to the Trash. You can also remove it from the lists in System
Settings → Privacy & Security. Its identity and settings stay in
`~/Library/Application Support/dirently`; delete that folder for a clean removal.

**Android:** touch and hold the Dirently icon and choose **Uninstall**. This
deletes the phone's identity; after reinstalling, join your group again.

**iPhone and iPad:** touch and hold the Dirently icon and choose
**Remove App** → **Delete App**. The device's key can stay in the iOS
keychain after the app is deleted, so a reinstall on the same iPhone or iPad
may still be in its groups. To take the device out of a group, use
**Leave group** before deleting the app.
