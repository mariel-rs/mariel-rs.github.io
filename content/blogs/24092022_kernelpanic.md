---
title: "Kernel panic with VirtualBox and CentOS"
date: 2022-09-24
draft: false
author: "Mariel"
tags:
  - linux
  - virtualbox
  - en
image: /images/kernelPanic.png
description: "How to solve a Kernel panic error"
toc: true
---

This week I was given a task that required me to use a CentOS virtual machine
image. Typically I use VirtualBox and it was also recommended to use this
hypervisor. Importing the image should have been a straightforward process, yet 
it was more educational.
<!--more-->

## Problem description

I followed the typical steps to create a VM and then attach the virtual disk, 
It went all fine. It got strange when I tried to turn it on. The VM showed a 
warning message saying that the hardware was unsupported.

```bash
Detected CPU family x model yyy
UNSUPPORTED HARDWARE DEVICE: Intel CPU model
```

Then came a second message:

```bash
Kernel panic - not syncing: Fatal exception
```

I came to know that **Kernel panic** is a fatal error from which the OS cannot 
recover that easy. I initially thought it might be related to the unsupported 
CPU warning thrown in the beginning. Me being also not that experienced with 
Linux errors, I didn't understand where to start troubleshooting.

## Solution

After trying so many things like passing the CPU information to the guest OS,
the final solution was to: **Increase the number of CPUs given to the VM** 
:zany_face:

It seems this VM was configured to have at least 2 CPU's and that was the reason
why the system was not able to boot. It would have been nice if I was let known
of this beforehand, yet it was a good educational experience.

As for the unsupported CPU warning, CentOS still complains about it but it does
not prevent from booting at all. After reading in several 
[forums](https://bugs.centos.org/view.php?id=8658), I understood the warning 
was being thrown because the guest OS (CentOS 6) had not been updated in a while.

This particular VM image could also be imported into VMWare and it seems that
VMWare does not suffer from this Kernel Panic problem as VMware configures 
everything and offers suggestions.