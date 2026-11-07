# VV//LIVEWIRE

**A free, unofficial desktop overlay for the Grok Bot app on Windows.**
A floating orb and panel for your Grok Bot team: see who is working, hear replies, and get pinged when a bot needs you.

By [Vinyl & Volt](https://vinylandvolt.com/skins/vv-livewire/) · [@VinylandVolt](https://x.com/VinylandVolt)

> This repository hosts **release downloads and documentation only**. It does not contain the app's source code.

---

## Download

Download the installer from the **[latest release](https://github.com/VinylandVolt/vv-livewire/releases/latest)**.

| | |
|---|---|
| Platform | Windows, x64 installer |
| Installer | `VV-Livewire-Setup-0.2.0.exe` (version 0.2.0) |
| Price | Free |

Each release lists the installer's SHA-256 in `SHA256SUMS.txt`. To check your download in PowerShell:

```powershell
Get-FileHash .\VV-Livewire-Setup-0.2.0.exe -Algorithm SHA256
# expected for 0.2.0: EEAB61D66602F61D900D1BD85DFD0B3FABE15527928948AC0BBF852466A4F636
```

## Requirements

- Windows 11, 64-bit (x64): the only Windows version tested so far.
- The Grok Bot desktop app for Windows, installed and signed in
- VV//LIVEWIRE is only a look. No Rig or bot needs it.

## Unsigned installer: what to expect

The installer is not code-signed yet, so Windows SmartScreen may show "Windows protected your PC". That warning is Windows doing its job. Only continue if you downloaded the file from this repository's Releases page and the SHA-256 matches. If you are unsure, don't install it.

## Install

1. Download `VV-Livewire-Setup-0.2.0.exe` from the [latest release](https://github.com/VinylandVolt/vv-livewire/releases/latest).
2. Run it and choose an install folder (per-user install, no admin needed).
3. VV//LIVEWIRE starts after setup and adds a desktop and Start menu shortcut.

## First run: pick your team with the [VV] marker

VV//LIVEWIRE only shows Grok Bot sidebar sections you tag. Everything else is ignored.

1. In Grok Bot, make a sidebar section with up to 6 bots.
2. Put the exact marker **[VV]** (uppercase, with brackets) at the **start or end** of the section name:
   - Works: `[VV] Crew`, `Crew [VV]`, `[VV]Crew`, `Crew[VV]`
   - Ignored: `VV Crew`, `Crew VV`, `Crew [VV] Team` (middle), `[vv] Crew` (lowercase), `(VV) Crew`, `Crew`
3. The section appears in VV//LIVEWIRE. The [VV] marker is hidden in the overlay.

VV//LIVEWIRE reads the small cache Grok Bot keeps on your PC (section names, bot names and colors, unread state). It does not change your Grok Bot setup, and it does not read or send your chats.

## Report a bug

Tray icon > **Report a bug**, or Settings > **REPORT A BUG**.

**Sent:** product name, app version, Windows version and architecture, your description, and an optional contact you type, plus a timestamp and a random report ID.
**Not sent:** your chats, bot names, Grok Bot cache, files, or account details.

If you are offline, the report is saved on your PC and retried automatically (shortly after launch, then every 10 minutes) until it gets through.

Please include what you did, what you expected, what happened, and your VV//LIVEWIRE version (Settings shows it).

## Updates

VV//LIVEWIRE checks this repository's GitHub Releases over HTTPS, about 30 seconds after launch and then periodically. You can also check from the tray or Settings.

- Nothing downloads until you click **Download**.
- Nothing installs until you click **Restart & install**. It never installs on its own when you quit.
- The download is checked against the SHA-512 in the release's `latest.yml` before it can install. Because the installer is unsigned, that check confirms the file matches this release; it is not a publisher signature.
- Installing an update over an existing copy and restarting has not been tested end to end yet. If an update ever fails, download the latest installer from Releases and run it.

## Compatibility

VV//LIVEWIRE depends on how the Grok Bot desktop app stores its local cache. A Grok Bot update can change that and break the overlay until VV//LIVEWIRE is updated. If that happens, the overlay tells you it can't read the cache. Your Grok Bot app and bots are not affected. Please report it.

## Uninstall

Windows Settings > Apps > Installed apps > **VV Livewire** > Uninstall. Uninstalling never touches your Grok Bot setup.

## Changelog

### 0.2.0
- In-app update checks against GitHub Releases. You choose when to download and when to install.
- [VV] marker is now the exact `[VV]` at the start or end of a section name.

### 0.1.1
- Report a bug from the tray and Settings, with an offline queue.

### 0.1.0
- First build: floating orb and panel, VV section marker, setup intro.

## Known limitations

- Windows x64 only.
- Installer is unsigned (SmartScreen may warn).
- Up to 6 bots per VV section.
- Unofficial: may break after Grok Bot updates.

---

Vinyl & Volt is independent and not affiliated with or endorsed by xAI / SpaceXSI. Grok is a trademark of its owner.


