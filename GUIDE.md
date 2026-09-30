<div align="center">
  <a href="GUIDE.zh-CN.md">简体中文</a> · <a href="GUIDE.md">English</a>
</div>

# Dirently user guide

Control your own computers from another computer or a phone. Your devices
connect directly to each other. No account needed.

[Getting started](#getting-started) ·
[macOS](#macos-first-launch) ·
[Windows](#windows-first-launch) ·
[Android](#android) ·
[Remote microphone](#remote-microphone) ·
[Shortcuts](#keyboard-shortcuts) ·
[Can't connect?](#cant-connect) ·
[Uninstall](#uninstall)

## Getting started

1. **Install Dirently** on the computer you want to control and on the device
   you connect from. Get it from [Releases](../../releases/latest).
2. **Create a group** on one of them: on the **Devices** page, click
   **Create group**. Enter a **Group name** and a **Group password** (at least
   8 characters), keep **Private group**, and click **Create and Join**.
3. **Join the group** on the other device: click **Find group**, search for the
   name, click **Join**, type the password and click **Join group**.
4. **Check that the computer is shared.** Sharing is on by default: the
   computer's own card then shows **Stop sharing**. If it shows
   **Share this device**, click it.
5. **Connect:** on the other device, click **Connect** on that computer's card.

Good to know:

- Anyone can find a group by name with **Find group**. Use a strong password
  and share it only with people you trust.
- After 10 wrong passwords, a device is blocked from that group until the
  group's administrator unbans it (**Manage group** → **Bans** → **Unban**).
- Keep all your devices on the same Dirently version.

## macOS first launch

You need an Apple Silicon Mac with macOS 13 or later.

1. Open `Dirently-<version>-arm64.pkg` and follow the installer. The package is
   signed and notarized by Apple, so macOS opens it without a warning.
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

1. Download the `.apk` from [Releases](../../releases/latest) on the phone and
   open it. Allow your browser or file manager to install apps
   (**Allow from this source**), then tap **Install**. If Play Protect warns
   about an unknown app, you can still install it.
2. Create or join a group as in [Getting started](#getting-started). Computers
   that are online and shared appear in the list. Tap **Connect**.
3. In a session, tap the small tab at the top for the session menu:
   **Keyboard**, **Input** (touch, trackpad or virtual mouse),
   **Microphone passthrough**, **Files** and **Disconnect**.

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
2. **Turn on UPnP on the router.** In Dirently, keep **Enable UPnP automatic
   port mapping** on (Settings → Network, on by default). The **NAT** box there
   shows the result, for example **Port mapping: UDP …**.
3. **Mapping table full.** If you see **Port mapping: the router refused; its
   mapping table may be full (restarting the router clears it)**, restart the
   router and try again. If it comes back, use a port forward.
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
5. **Port forward (last resort).** On the computer you want to control, set
   **Sharing start port** (Settings → Network) to a fixed number from 1025 to
   65534 (0 means random) and save. On its router, forward that **UDP** port to
   the computer, and give the computer a fixed local IP. If the strict network
   is on the side you connect from, do the same there with **Client port**.
6. **Strict networks.** If Dirently says you are behind your provider's NAT
   (CGNAT), open the port on the other side instead. If both sides are on
   strict networks (mobile data, office, school, hotel, some VPNs), a direct
   connection may be impossible; move one side to a home network.
7. **Firewall.** Allow Dirently in any third-party firewall or security app.

**No picture?** If you see **The remote device sent no video**, set **Display**
to **Virtual display** in Settings → Sharing on that Windows computer.

**Report a problem:** tell us which devices you used (for example "Windows 11
PC → MacBook"), what went wrong, and the message Dirently showed. On Android
you can attach **Settings → General → Diagnostics → Export diagnostics** (it leaves out
passwords, keys, IDs and IP addresses).
[Discord](https://discord.gg/6UeurVTxzt) · support@dirently.com ·
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
