---
title: "How to Mount ExFAT Drive on Ubuntu Linux"
date: 2020-02-16T20:06:00+10:00
draft: false
image: "images/mount-drive.jpg"
tags: ["linux"]
categories: ["programming"]
---

To be able to mount exFAT filesystem on Ubuntu you'll need to install the free FUSE exFAT module and tools which provide a full-featured exFAT file system implementation for Unix-like systems.

Before installing the packages make sure the Universe repository is enabled on your system. Open your terminal either by using the Ctrl+Alt+T keyboard shortcut or by clicking on the terminal icon and type:

{{< highlight go >}}
  sudo add-apt-repository universe        
{{< / highlight >}}

Once the repository is enabled update the packages index and install the exfat-fuse and exfat-utils packages using the following commands:

{{< highlight go >}}
  sudo apt update                          
{{< / highlight >}}

.

{{< highlight go >}}
  sudo apt install exfat-fuse exfat-utils
{{< / highlight >}}

That's it! You can now open your file manager and click on the USB disk to mount it.

### Conclusion

You have learned how to enable support for the exFAT file system on your Ubuntu 18.04 machine. Some people refer to exFAT as FAT64.

The USB drive will auto mount when you insert it, but in case the auto-mount fails you will have to mount the drive manually.
