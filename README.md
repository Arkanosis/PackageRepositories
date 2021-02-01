# Arkanosis' package repositories

This git repository contains the necessary files to populate the following package repositories:
 * [apk.arkanosis.net](https://apk.arkanosis.net) Android package repository;
 * [apt.arkanosis.net](https://apt.arkanosis.net) Debian & Kubuntu package repository;
 * [pkg.arkanosis.net](https://pkg.arkanosis.net) Arch Linux package repository.

Software authors and packagers are most of the time third parties but packages are all curated, reviewed and built by [myself](https://arkanosis.net) for my personal use.

Any package I don't use anymore may be removed at any time, *except packages of software I've written myself*. Support for distros I don't use anymore may be discontinued at any time — this usually means versions of Debian older than stable and versions of Kubuntu older than the latest LTS. Therefore, if you ever depend on a third-party package being available from here, update your distro and drop me an email so that I can at least tell you in advance, should I plan to retire it.

Any package made available in the official repositories of a distro (or in the official F-Droid repository, for Android) may be removed at any time, *including packages for software I've written myself*. This shouldn't cause any issue for you.

## Installation

### On Arch Linux

You can enable this repository on your up to date Arch Linux as follow:

```sh
sudo pacman-key --recv-keys FA490B15D054C7E83F70B0408C145ABAC11FA702
sudo pacman-key --lsign FA490B15D054C7E83F70B0408C145ABAC11FA702
echo '\n[arkanosis]\nInclude = /etc/pacman.d/arkanosis.list' | sudo tee -a /etc/pacman.conf
echo 'Server = https://pkg.arkanosis.net/$repo/os/$arch' | sudo tee /etc/pacman.d/arkanosis.list
sudo pacman -Sy
```

### On Debian and Kubuntu

You can enable this repository your Debian 10 (Buster), your Kubuntu 16.04 LTS (Xenial) or your Kubuntu 18.04 (Bionic) as follow:

```sh
curl -s https://arkanosis.net/jroquet.pub.asc | sudo apt-key add -
echo "deb https://apt.arkanosis.net/ stable software" | sudo tee /etc/apt/sources.list.d/arkanosis.list
sudo apt update
```

### On Android

You can enable this repository on your Android 4.4+ with [F-Droid](https://f-droid.org/) as follow:
 * Scan [this QR code](https://apk.arkanosis.net/fdroid/qr.png), or
 * Manually add the repository with the following information:
   * Address: https://apk.arkanosis.net
   * Fingerprint: 655955660F34A4DB7CC2B30D96B8B546759D6AEABC83D34AE682B73A7C24FE62

## Packages

The following packages are currently available:
 * **bamrescue**: a command line tool to check BAM files for corruption and repair them ([sources](https://github.com/Arkanosis/bamrescue), [PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=bamrescue))
 * **wmrc**: an application to follow recent changes on Wikimedia projects in real time ([sources](https://github.com/arkanosis/wmrc))

The following packages are currently being considered for addition:
 * **batzconverter**: a command line tool to display the current or future time in different timezones ([sources](https://github.com/chmouel/batzconverter))
 * **chars**: a command line tool to display information about unicode characters ([sources](https://github.com/antifuchs/chars), [PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=chars))
 * **csvfix**: a command line tool to deal with CSV data ([sources](https://bitbucket.org/neilb/csvfix/src/default/), [PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=csvfix))
 * **delta**: a syntax-highlighting pager for git ([sources](https://github.com/dandavison/delta))
 * **desed**: a debugger for sed ([sources](https://github.com/SoptikHa2/desed/))
 * **fdroidserver**: command line tools to manage a F-Droid repository ([sources](https://gitlab.com/fdroid/fdroidserver), [PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=fdroidserver))
 * **hotspot**: graphical profiler based on Linux perf ([sources](https://github.com/KDAB/hotspot), [PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=hotspot))
 * **tmux-thumbs**: a tmux plugin for efficient, keyboard-only copy and paste in the terminal ([sources](https://github.com/fcsonline/tmux-thumbs))
 * **urlencode**: a simple url-encoder / decoder ([sources](https://github.com/dead10ck/urlencode))
