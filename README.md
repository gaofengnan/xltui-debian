![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/gaofengnan/xltui-debian/total)
![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/gaofengnan/xltui-debian/latest/total)
![GitHub Release](https://img.shields.io/github/v/release/gaofengnan/xltui-debian)
![GitHub Release Date](https://img.shields.io/github/release-date/gaofengnan/xltui-debian)

<h1>
   <p align="center">
     <a href="https://xltui.org/"><img src="https://github.com/gaofengnan/xltui-debian/blob/main/xltui-logo.png" alt="xltui Logo" width="128" style="margin-right: 20px"></a>
     <a href="https://www.debian.org/"><img src="https://github.com/gaofengnan/xltui-debian/blob/main/debian-logo.png" alt="Debian Logo" width="104" style="margin-left: 20px"></a>
     <br>xltui for Debian
   </p>
</h1>
<p align="center">
 minimal Terminal UI for Excel files written in .NET.
</p>

# xltui for Debian

> Fork of [dariogriffo/xltui-debian](https://github.com/dariogriffo/xltui-debian) (MIT); the original packaging is by Dario Griffo. Served at [deb.gaofn.xyz](https://deb.gaofn.xyz) for Debian 12 (bookworm) and 13 (trixie).

This repository contains build scripts to produce the _unofficial_ Debian packages
(.deb) for [xltui](https://github.com/PDMLab/xltui/) hosted at [deb.gaofn.xyz](https://deb.gaofn.xyz)

Currently supported Debian distros are:
- Bookworm (v12)
- Trixie (v13)
- Forky (v14)
- Sid (testing)

Currently supported Ubuntu distros are:
- Jammy (22.04)
- Noble (24.04)
- Questing (25.10)
- Resolute (26.04)

One package per architecture serves every suite: xltui loads whichever ICU
library the system ships (libicu70 to libicu78).

Thanks to @ranjithrajv

Supported architectures:
- amd64 (x86_64)
- arm64 (aarch64)

This is an unofficial community project to provide a package that's easy to
install on Debian. If you're looking for the xltui source code, see
[xltui](https://github.com/PDMLab/xltui/).

## Install/Update

### The Debian way

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.gpg -o /etc/apt/keyrings/deb.gaofn.xyz.gpg
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.sources -o /etc/apt/sources.list.d/deb.gaofn.xyz.sources
# Debian 12 (bookworm): fetch deb.gaofn.xyz-bookworm.sources instead
sudo apt update
sudo apt install -y xltui
```

### Manual Installation

1. Download the .deb package for your architecture available on
   the [Releases](https://github.com/gaofengnan/xltui-debian/releases) page.
2. Install the downloaded .deb package.

```sh
sudo apt install ./<filename>.deb
```
## Updating

To update to a new version, just follow any of the installation methods above. There's no need to uninstall the old version; it will be updated correctly.

## Building

### Build for single architecture
```sh
./build.sh <xltui_version> <build_version> <architecture>
# Example: ./build.sh 0.0.3 1 arm64
```

### Build for all architectures
```sh
./build.sh <xltui_version> <build_version> all
# Example: ./build.sh 0.0.3 1 all
```

## Roadmap

- [x] Produce a .deb package on GitHub Releases
- [x] Set up a debian mirror for easier updates
- [x] Multi-architecture support (amd64, arm64)

## Disclaimer

- This repo is not open for issues related to xltui. This repo is only for _unofficial_ Debian packaging.
