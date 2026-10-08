<div align="center">

<img src="assets/logo.png" alt="Mycel logo" width="96" />

# Mycel

**AI-powered client profile management for professional services teams**

[Website](https://mycel.nemoire.tech) · [Download the latest release](https://github.com/kahankachhadiya/Mycel-Distribution/releases/latest) · [All releases](https://github.com/kahankachhadiya/Mycel-Distribution/releases)

</div>

---

This repository publishes the Mycel desktop app: installers for every release, and the update feed (`latest.json`) the app checks to update itself.

## Download

Open the [latest release](https://github.com/kahankachhadiya/Mycel-Distribution/releases/latest) and pick the file for your computer:

| System | File | Updates |
|---|---|---|
| Windows 10 / 11 (64-bit) | `Mycel_<version>_x64-setup.exe` | Automatic |
| Linux, any distribution (64-bit) | `Mycel_<version>_amd64.AppImage` | Automatic |
| Ubuntu / Debian (64-bit) | `Mycel_<version>_amd64.deb` | Automatic, asks for your password |

macOS, iPhone, iPad and Android are not supported.

The `.sig` files next to each installer are signatures the app's updater checks; you don't need to download them.

## Install

### Windows

Run `Mycel_<version>_x64-setup.exe`. It installs for your user account only, so no administrator rights are needed.

### Linux: AppImage

```bash
mkdir -p ~/Applications
mv ~/Downloads/Mycel_*_amd64.AppImage ~/Applications/
chmod +x ~/Applications/Mycel_*_amd64.AppImage
~/Applications/Mycel_*_amd64.AppImage
```

Keep the AppImage in a folder you own (like `~/Applications`) so updates can replace it. Open it once before signing in: that registers Mycel to receive the sign-in link from your browser.

If it doesn't start, install FUSE 2: `sudo apt install libfuse2t64` (Ubuntu 24.04 and newer) or `sudo apt install libfuse2` (older releases).

### Linux: Ubuntu / Debian package

```bash
sudo apt install ./Mycel_*_amd64.deb
```

Requires Ubuntu 22.04 or newer, or Debian 12 or newer.

## First run on Linux (Wayland)

Ubuntu and most current distributions use Wayland. The first time you open the clipboard overlay, GNOME asks two questions once:

1. **Allow Mycel's keyboard shortcuts** (Alt+V, Alt+↑, Alt+↓ by default). Lets the hotkeys work while another app is in front.
2. **Allow remote interaction / keyboard control.** Lets Mycel type the selected value into the app you are filling in.

Approve both. GNOME remembers the answers. To change the hotkey later, use Mycel's **Settings → Keyboard Shortcuts**; GNOME asks once to confirm a new combination.

## Updates

Mycel checks this repository when it starts and offers new versions. Each update is signed, and the app refuses one whose signature does not match.

- **Windows** and **AppImage**: the update installs and Mycel restarts.
- **.deb**: the update asks for your password, because it installs system-wide.

## Sign-in

Signing in opens Google in your browser. When it finishes, the browser asks to open Mycel; allow it (tick "Always allow" to skip the question next time).

## Help

Questions and problems: open an [issue](https://github.com/kahankachhadiya/Mycel-Distribution/issues) or visit [mycel.nemoire.tech](https://mycel.nemoire.tech).

---

<sub>Releases here are built and published automatically from the Mycel source when a version is tagged. Don't edit `latest.json` by hand: the installed apps read it to find updates.</sub>
