(I just want to download the applicance -> it's [here](https://www.dropbox.com/s/4eg9c916fxt4m9v/BiodiversityBox.ova?dl=0))

# BiodiversityBox

BiodiversityBox is a preconfired Linux system for biodiversity informatics works. 

It is distributed as a [virtual applicance](https://en.wikipedia.org/wiki/Virtual_appliance) so it can be very easily installed within [VirtualBox](https://www.virtualbox.org/) (basically a PC-in-a-window) on any Windows / Mac or Linux machine.

![general screenshot](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/raw/master/screenshot.png)

# What's included

The following software is installed, configured and reay-to-use:

- [GBIF's IPT](https://www.gbif.org/ipt) (in test mode) for data publication
- [QGIS 3.8 Zanzibar](https://www.qgis.org/) with some plugins such as [GBIF occurrences](https://plugins.qgis.org/plugins/qgisgbifapi/)
- [R](https://www.r-project.org/) and [RStudio](https://www.rstudio.com/) with tons of installed packages (tidyverse, rgbif, sdm, readxl, SSDM, inborutils, ...)
- [OpenRefine](http://openrefine.org/), a powerful tool for working with messy data
- [Python 3](https://www.python.org/) and some useful Python packages such as [PyGBIF](https://github.com/sckott/pygbif) and [python-dwca-reader](https://python-dwca-reader.readthedocs.io).
- [Miniconda](https://conda.io/en/latest/miniconda.html) allows easy installation of data science tools (many of them are already there: [Jupyter](https://jupyter.org/), [NumPy](http://www.numpy.org/), [Pandas](https://pandas.pydata.org/), ...)
- [PostgreSQL](https://www.postgresql.org/) and [PostGIS](https://postgis.net/)
- [SQLite](https://www.sqlite.org/index.html) with [DB Browser for SQLite](https://sqlitebrowser.org/)
- [GDAL utilities](https://www.gdal.org/)
- [CSVKit](https://csvkit.readthedocs.io/) for CSV manipulations
- ... (full list [here](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/issues/5))

Something's missing? Don't hesitate to [report it with an issue](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/issues/new)!


# Getting started

1. Install [VirtualBox](https://www.virtualbox.org/) (version 6) on your computer.
2. Download the [BiodiversityBox virtual appliance](https://www.dropbox.com/s/4eg9c916fxt4m9v/BiodiversityBox.ova?dl=0) and [import it in VirtualBox](https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html).
3. Run the virtual machine
4. Optionally, tweak the configuration (see below)

# How to use...

## IPT

- Installed version: 2.3.6
- The IPT is available at the http://localhost:8080/ipt address within BiodiversityBox. You'll find a shortcut to it in the launch bar at the bottom of the screen, and a bookmark in the Chromium browser's bookmarks bar.
- You can use the **bio@bio.com**/ **gbif** credentials to log in the IPT.
- Advanced use: IPT's data directory is located at `/iptdata`

## Miniconda / Python environments

To document.

## Postgresql and PostGIS

To document.

# Tweak the configuration

Due to the VirtualBox platform, BiodiversityBox works like a different computer running within a window on your host machine. Therefore, some configuration is generally needed for a smoother integration between the two.

## Keyboard layout

![keyboard configuration screenshot](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/raw/master/keyboard.png)

At first start, BiodiversityBox is configured for an American English (QWERTY) keyboard. You can configure other layouts by **right-clicking on the small flag icon** on the right on the menu bar, then **"Keyboard settings"** -> **Layout tab**. Once you've added keyboard layouts, you can switch between them by (left) clicking on the flag icon in the menu bar.

Alternatively, you can change the keyboard layout by using the `setxkbmap` command in the terminal. Example for a French layout:

![keyboard configuration screenshot - terminal](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/raw/master/keyboard_terminal.png)

## Network access

In most cases, the `NAT (Network Address Translation)` or `Bridged networking` modes should allow BiodiversityBox to access the Internet.

If not, don't hesitate to consult [the relevant documentation for Virtualbox](https://www.virtualbox.org/manual/ch06.html).

## Sharing files

To be written/fixed.

## Speed and performance

Virtual machines are, by definition, heavy (you have basically two systems running in parallel on a single computer). It's therefore important to carefully decide how to share memory between BiodiversityBox and your host operating system.

This can be configured in Virtualbox. BiodiversityBox comes configured to use 2Gb of memory. If possible (if your machine has 4Gb+ of memory), we encourage you to allocate more memory to BiodiversityBox. You should also take care of not starving the host operating system.

We also advise you to experiment with a few different values and, when working in BiodiversityBox, to close any unnecessary application (web browsers, ...) in your host operating system.

## Copy-paste between BiodiversityBox and your native applications

To be written/fixed.

# FAQ and advanced topics

## I need root/administrative access to BiodiversityBox

The following user accounts are provided:

- **username:** bio / **password:** gbif (normal user, but you can use the `sudo` command for administrative tasks)
- **username:** root / **password:** gbif (root user)

## How is it made?

BiodiversityBox is based on [Arch Linux](https://www.archlinux.org/), for maximum flexibility and frequent, rolling releases.

## How can I tweak my system or add new software?

Since we're not doing anything especially fancy, you should be able to perform tasks the "Arch way" (following their wiki) and installing new packages With `Pacman` and [AUR](https://aur.archlinux.org/).

## Can I use it without VirtualBox?

BiodiversityBox is distributed in the [Open Virtualization Format](https://en.wikipedia.org/wiki/Open_Virtualization_Format): while you can't just install it on a "physical computer", other virtualization packages such as VMWare will also work. If you cannot install any virtualization solution on your local computer, it may be possible to run this in the cloud with remote screen access (to be investigated and documented).
