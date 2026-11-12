# Dirently Privacy Policy

Effective date: 13 November 2026

This policy explains what information the developer of Dirently, based in Western Australia, Australia ("we", "us"), handles when you use the Dirently apps, the Dirently coordination service and dirently.com.

## 1. In short

- **No account.** We don't ask for your name, email address, phone number or a password to use Dirently.
- **Your screen doesn't pass through our servers.** Once two devices are connected, video, audio, input, clipboard and files travel directly between them, encrypted.
- We don't sell your information or use it for advertising.

## 2. What the coordination service handles

The coordination service helps your devices find each other and set up a connection. To do that, it handles:

| Information | Why | How long |
|---|---|---|
| Device identity: a randomly generated device ID and public key, device name, platform, app version | Identify the device and show it to your group | In memory while the device is online |
| Network addresses: source IP, public port, local IPv4 addresses | Set up a direct connection between two devices | In memory while online or in a session; shared only with the device you connect to |
| Status: displays, stream settings, frame rate, bitrate, latency | Pick suitable settings and show them to both sides of a session | In memory while online |
| Group data: group name, members' device IDs and names, roles, online/offline times, wrong-password counts, bans | Groups, permissions and protection against password guessing | Stored on our servers in Australia and Hong Kong. A group is deleted after all its members have been offline for 3 days; a member's details are removed when they leave |
| Device tag: a code the app calculates on your device for each group; it is different in every group | Enforce group bans | Stored only on our server in Australia while you are in the group, while your application to join it waits for approval and while a ban from it lasts, and for at most 7 days after a failed attempt to join it. Deleted when none of these applies any more or the group is deleted; backup copies are overwritten over time |
| Group password | Check group joins | Stored only on our server in Australia, as a one-way hash plus an encrypted copy. The group admin and we can view the current password, so don't reuse a password from elsewhere |
| Security and activity logs: time, event, source IP, a pseudonymous device reference | Investigate abuse and faults | Kept by each of our servers for 30 days, then deleted automatically (checked every hour) |
| Connection results: whether each connection succeeded or failed, the category of any failure (for example a timeout, or the other device not sharing), the kind of path used (local network, direct, hole punching, UPnP, IPv6, ZeroTier), a time bracket for how long it took, and both devices' platforms | Find out which networks and device combinations fail to connect, so we can improve direct connections | Kept only as hourly totals, with no IP address, device ID or device name, and deleted after 30 days. The record used to check a report is held in memory only, for at most 30 minutes |

**Device names:** on computers, the device name defaults to your computer's name. If it contains your real name, your group and we will see it. You can change it in Settings.

## 3. What the website handles

- dirently.com is delivered through Cloudflare, which processes visitors' IP addresses to serve and protect the site.
- A cookie named `od_visitor` counts visitors without double counting. It lasts 365 days.
- On your first visit we log the time, your IP address, the referring page (without query parameters), your browser's user agent and your language preference. We keep these records for 30 days. Older ones are deleted automatically, checked every hour, oldest first.
- The site loads no third-party analytics, ads or fonts.

## 4. What stays on your device

Your device keys, settings, trusted coordination-service certificates and diagnostic logs stay on your device; we never receive them. We receive only the connection results described in section 2, never the logs themselves. On computers the app also keeps a hash derived from the hardware ID, used only to detect a device identity copied to another machine. The device tag in section 2 is calculated on your device; what it is calculated from never leaves your device.

The Android app's "Export diagnostics" bundles your phone model, network type, settings and logs. We only receive it if you send it to us yourself. The export does not include the device tag or what it is calculated from.

## 5. Router port mapping

To make direct connections easier, the app may ask your router, via UPnP, NAT-PMP or PCP, to open a port. It only tells the router your device's local address and port. You can turn this off in Settings.

## 6. Other services we use

- **Downloads** are hosted on download.dirently.com (Cloudflare R2) and GitHub. When you download, Cloudflare or GitHub processes your IP address under its own privacy policy. The iPhone and iPad app is distributed by Apple through the App Store and TestFlight, and Apple processes your information under its own privacy policy.
- **Update checks**: the app contacts download.dirently.com to check for updates.
- **What an update check sends**: the app checks shortly after it starts, about every 6 hours while it runs, and when you choose **Check for updates**. The request contains no device ID, device name, group or account. As with any download, Cloudflare processes your IP address.
- **Downloading updates**: the Windows and Android apps download a new version only from download.dirently.com, and only when you choose **Update now** or have chosen **Automatic**. Windows has one more case: if the version you run has a security problem that must be fixed, the app downloads the update and installs it by itself once nobody is connected and the computer is idle, whichever update setting you chose. The app checks the file before installing it. The Mac app gets in-app updates in a later update. The iPhone and iPad app never downloads updates itself: they come from Apple through the App Store or TestFlight.
- **Service settings**: the app also fetches the coordination service's current connection settings from dirently.com or download.dirently.com. This request contains no device ID, device name, group or account either.
- **Our community** is on Discord, whose privacy policy applies there.
- **Email** to support [at] dirently.com is forwarded through Cloudflare to our mailbox.
- **Feedback** you send us is used only to improve Dirently and to reply to you.

## 7. Sharing

We don't share your information with anyone, except:

- as needed to run the service (for example, your device's details go to your group members or the device you connect to);
- when the law requires it;
- to protect people from serious harm such as fraud.

## 8. Where data is stored

Our servers are in Australia and Hong Kong. If you use Dirently from another country or region, including mainland China, the information above is transferred to and processed in Australia, and in Hong Kong when your app connects through our Hong Kong server. The group data in section 2 is kept on both servers. Group passwords and device tags are kept only in Australia. By using Dirently you agree to this.

## 9. Security

- Connections to the coordination service use TLS 1.3.
- Data between your devices is encrypted in transit (AES-256-GCM, with fresh keys for each session).
- Group passwords are never stored in plain text.

No system is perfectly secure.

## 10. Your choices

You can change your device name, stop sharing, leave a group or uninstall at any time. To ask about, correct or delete information about your device (such as group membership or ban records), email us with the device name and roughly when you used it. Because there are no accounts, we may ask you to confirm from that device.

## 11. Changes

We may update this policy and will publish the new version here. We will give notice of significant changes.

## 12. Contact

support [at] dirently.com

If this English version and the Chinese translation differ, the English version prevails.
