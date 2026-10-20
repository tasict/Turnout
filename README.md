<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/logo-dark.svg">
    <img src="assets/logo.svg" alt="Turnout" width="260">
  </picture>
</p>

Turnout is a VPN client for macOS that connects to WireGuard servers the way `wg-quick` does, in a native app: your `PreUp`/`PostUp` hooks run, your routes stay yours, and you choose which network interface the tunnel leaves through. It lives in the menu bar, follows the network as it changes, can connect by schedule or Wi-Fi network, and cleans up after itself.

Turnout's source code is not published here. This repository holds:

- the website, <https://turnout.ctsite.cc/>
- the installer downloads, under [Releases](https://github.com/tasict/Turnout/releases)
- the [issue tracker](https://github.com/tasict/Turnout/issues)

## Installing

<!-- download:soon -->
**Coming soon.** The first public release is being prepared; until then there is nothing to download. Watch this repository, or its [Releases](https://github.com/tasict/Turnout/releases) page, for the first one.
<!-- /download:soon -->

Turnout needs macOS 15 or later, on Apple silicon or Intel.

1. Download `Turnout-<version>.pkg` from the [latest release](https://github.com/tasict/Turnout/releases/latest).
2. Open it and follow the steps. Turnout is installed in `/Applications` and opens when the installer finishes.
3. In Turnout's window, install the background service, then allow it when macOS asks, in System Settings › General › Login Items & Extensions.

The installer is signed with a Developer ID but not yet notarized by Apple, so macOS may refuse to open it. If it does, go to System Settings › Privacy & Security, choose Open Anyway, and open the installer again.

What the background service does to your Mac, and how to check it, is on [What Turnout does to your Mac](https://turnout.ctsite.cc/how-it-works.html).

## Reporting a problem

[Open an issue](https://github.com/tasict/Turnout/issues/new?template=bug_report.md). It helps to include:

- your macOS version, and Turnout's version from Turnout › About Turnout
- what you did, what you expected, and what happened instead
- the lines of the background service's log from around that time, in `/Library/Logs/cc.ctsite.wggui.daemon.log`
- the app's own log:

  ```sh
  /usr/bin/log show --predicate 'subsystem == "cc.ctsite.wggui"' --last 1h
  ```

Issues are public: leave out private keys, preshared keys, server addresses and whole config files.

## The website

Plain static HTML and one stylesheet, in English and 繁體中文, served by GitHub Pages from this repository's `main` branch as it stands, at <https://turnout.ctsite.cc/>; there is no build step. The screenshots in `assets/` are taken from the app itself.

- [Turnout](https://turnout.ctsite.cc/)
- [What Turnout does to your Mac](https://turnout.ctsite.cc/how-it-works.html)
- [Privacy policy](https://turnout.ctsite.cc/privacy.html)

© 2026 tasict
