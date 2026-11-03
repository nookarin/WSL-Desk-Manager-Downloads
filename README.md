# WSL Desk Manager

A Windows app that sets up WSL and opens a Linux distro's full desktop, or a terminal, in a few
clicks. Every WSL command is a button, so you never need a command line.

This repository hosts the installer downloads.

## Download

Get the latest version from the [Releases page](https://github.com/nookarin/WSL-Desk-Manager-Downloads/releases/latest):

**WslDeskManager-Setup-1.1.0.exe** (about 52 MB)

## What it does

- **Status:** checks whether WSL is installed and ready. If it isn't, it enables WSL (one UAC
  prompt) and continues after the restart.
- **Distros:** lists installed distros with start, stop, set as default and convert to WSL 2.
  Add a distro from the online list or from a `.tar`, `.vhdx` or `.wsl` file.
- **Desktop:** installs and configures xrdp and a desktop environment (Xfce, KDE or MATE) for
  apt or dnf distros, then shows the desktop in a window, full screen, or in Windows Remote
  Desktop.
- **Terminal:** a terminal tab for each distro.
- **Settings:** display, clipboard, keyboard, performance, desktop, terminal, `.wslconfig` and
  `wsl.conf`.
- **Snapshots:** save, restore or clone a distro. A safety snapshot is taken before a restore.
- **Diagnostics:** a report you can copy for bug reports. Passwords and your Windows user name
  are masked, and nothing is sent anywhere.
- **Updates:** checks for a newer release at most once a day, verifies its SHA-256 checksum, and
  installs it in place.

## Requirements

- Windows 10 22H2 (build 19045) or Windows 11, x64, with virtualization enabled in the firmware.
- The Microsoft Edge WebView2 Runtime, used by the terminal. It comes with Windows 11 and
  current Windows 10.

The installer includes .NET, so nothing else needs to be installed.

## Install

Run `WslDeskManager-Setup-<version>.exe`. It installs for your user only, so it doesn't ask
for administrator rights. The app asks for them itself, once, if WSL needs to be enabled.

**Uninstall** from Settings > Apps. Your distros and snapshots are always kept. The uninstaller
asks whether to delete the app's settings, logs and saved desktop passwords too.

## Updates

The app checks this repository's latest release on startup and shows a banner when a newer
version exists. You can also check from **About**, where the startup check can be turned off.
Settings, distros and snapshots are kept across updates.

## Privacy

The app has no telemetry. It contacts GitHub only to check for updates and download them. The
diagnostics report stays on your machine until you copy it somewhere.

## Support

If something doesn't work, open an issue on this repository with the diagnostics report from
the app's **Diagnostics** page.
