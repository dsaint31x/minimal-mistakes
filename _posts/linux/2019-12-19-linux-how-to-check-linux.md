---
title:  "[linux] How to check my linux version"
last_modified_at:   2019-12-19
author: dsaint31
categories: 
  - linux
use_math: false
tags: 
  - linux 
---

# How to determine which linux distriubtion is running

## Linux Distriubtion and Linux Kernel.

The command below will show you the information of your linux syste.
```bash
grep . /etc/*-release
``` 

The output of the above command on my system is as follow;

```bash
/etc/lsb-release:DISTRIB_ID=LinuxMint
/etc/lsb-release:DISTRIB_RELEASE=19.2
/etc/lsb-release:DISTRIB_CODENAME=tina
/etc/lsb-release:DISTRIB_DESCRIPTION="Linux Mint 19.2 Tina"
/etc/os-release:NAME="Linux Mint"
/etc/os-release:VERSION="19.2 (Tina)"
/etc/os-release:ID=linuxmint
/etc/os-release:ID_LIKE=ubuntu
/etc/os-release:PRETTY_NAME="Linux Mint 19.2"
/etc/os-release:VERSION_ID="19.2"
/etc/os-release:HOME_URL="https://www.linuxmint.com/"
/etc/os-release:SUPPORT_URL="https://forums.ubuntu.com/"
/etc/os-release:BUG_REPORT_URL="http://linuxmint-troubleshooting-guide.readthedocs.io/en/latest/"
/etc/os-release:PRIVACY_POLICY_URL="https://www.linuxmint.com/"
/etc/os-release:VERSION_CODENAME=tina
/etc/os-release:UBUNTU_CODENAME=bionic
grep: /etc/upstream-release: Is a directory
```
As you can see, my linux distibution name is **Linux Mint 19.2 Tina**.

You can also use the following mehtod to find out your linux distribution and version.

```bash
lsb_release -a
```

Sample output from my system:
```bash
No LSB modules are available.
Distributor ID:	LinuxMint
Description:	Linux Mint 19.2 Tina
Release:	19.2
Codename:	tina
```

If you want to know the version of kernel, the command below can be used.

```bash
hostnamectl | grep Kernel
```

or

```bash
uname -r
```

The each same out is as follows:
* `hostnamectl`
	```bash
	            Kernel: Linux 4.15.0-66-gener
	```
* `uname`
	```bash
4.15.0-66-generic
	```

## Window mananger (which is currently running)

I prefer to use `environment variable` as follows.

```bash
echo $XDG_CURRENT_DESKTOP
```

The output is as follows

```bash
X-Cinnamon
```

Another environment variable `GDMSESSIONI`

```bash
echo $GDMSESSION
```
