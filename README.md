# Introduction

This project would be an upgrade to the [Paragon NTFS driver for Linux](https://www.paragon-software.com/home/ntfs-linux-professional/).

That driver comes with a [Free Limited Version](https://www.paragon-software.com/home/ntfs-linux-professional/#comparison) which can be downloaded by [this official link](http://dl.paragon-software.com/free/Paragon-715-FRE_NTFS_Linux_9.5_Express.tar.gz).

## State of the art

At the time I am writing (September 7, 2018) it supports kernel up to the 4.12.

## Goals

The goal of this project is to support kernels 4.15 and newer.

## License

In order to publish this project I received the explicit authorization from Paragon which asked me to publish the [Paragon End User License](https://github.com/antonio-petricca/paragon-ufsd-ntfs-driver-porting/Paragon-End-User-License.txt).

## How to build

The `apply-patches` script downloads the [free limited version](http://dl.paragon-software.com/free/Paragon-715-FRE_NTFS_Linux_9.5_Express.tar.gz) of the driver, then patches it to work on newer kernel releases.

```bash
$ ./apply-patches
$ cd sources
$ ./configure
$ make driver
$ sudo make driver_install
```