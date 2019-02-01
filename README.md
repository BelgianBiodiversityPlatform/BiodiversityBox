# BiodiversityBox

![screenshot](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/raw/master/screenshot.png)

BiodiversityBox is a preconfired Linux system for biodiversity informatics works. 

It is distributed as a [virtual applicance](https://en.wikipedia.org/wiki/Virtual_appliance) so it can be very easily installed within [VirtualBox](https://www.virtualbox.org/) (basically a PC-in-a-window) on any Windows / Mac or Linux machine.

# What's included

The following software is installed, configured and reay-to-use:

- [GBIF's IPT](https://www.gbif.org/ipt) (in test mode) for data publication
- [QGIS 3.4 Madeira](https://www.qgis.org/) with some plugins such as [GBIF occurrences](https://plugins.qgis.org/plugins/qgisgbifapi/)
- [R](https://www.r-project.org/) and [RStudio](https://www.rstudio.com/) with tons of installed packages (tidyverse, rgbif, sdm, readxl, SSDM, inborutils, ...)
- [OpenRefine](http://openrefine.org/), a powerful tool for working with messy data
- [Python 3](https://www.python.org/) and some useful Python packages such as [PyGBIF](https://github.com/sckott/pygbif) and [python-dwca-reader](https://python-dwca-reader.readthedocs.io).
- [Miniconda](https://conda.io/en/latest/miniconda.html) allows easy installation of data science tools (many of them are already there: [Jupyter](https://jupyter.org/), [NumPy](http://www.numpy.org/), [Pandas](https://pandas.pydata.org/), ...)
- [PostgreSQL](https://www.postgresql.org/) and [PostGIS](https://postgis.net/)
- [GDAL utilities](https://www.gdal.org/)
- [CSVKit](https://csvkit.readthedocs.io/) for CSV manipulations
- ... (full list [here](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/issues/5))

Something's missing? Don't hesitate to [report it with an issue](https://github.com/BelgianBiodiversityPlatform/BiodiversityBox/issues/new)!


# Getting started

1. Install [VirtualBox](https://www.virtualbox.org/) on your computer.
2. Download the BiodiversityBox virtual appliance and import it in VirtualBox.
3. Exectute the virtual machine
4. Tweak the configuration (see below)


# Tweak the configuration

Due to the VirtualBox platform, BiodiversityBox works like a different computer running within a window on your host machine. Therefore, some configuration is generally needed for a smoother integration between the two.

## Keyboard layout

## Network access

## Sharing files

## Speed and performance

## Copy-paste (between your "normal software" and BiodiversityBox)

# FAQ and advanced topics

## How is it made?

BiodiversityBox is based on [Arch Linux](https://www.archlinux.org/), for maximum flexibility and frequent, rolling releases.

## How can I tweak my system or add new software?

Since we're not doing anything especially fancy, you should be able to perform tasks the "Arch way" (following their wiki) and installing new packages With `Pacman` and [AUR](https://aur.archlinux.org/).

## Can I use it without VirtualBox?

