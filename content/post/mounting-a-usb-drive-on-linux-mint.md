---
title: "Mounting a Usb Drive on Linux Mint"
date: 2020-02-12T17:59:30+10:00
draft: false
image: "images/linux-usb.jpg"
tags: ["linux"]
categories: ["programming"]
---

Mint usually works with NTFS USB drives but if you can't see the drive you can **mount** it yourself.

First run the command to see your hardware devices.

{{< highlight go >}}
  sudo fdisk -l                  
{{< / highlight >}}

At the Disk line

> Disk /dev/sdb: 8004 Mb 8004304896 Bytes

This is the usb disk drive

At the Device Boot line you should see something like:

> **Device   Boot Start		End		Blocks	   Id	System**
> /dev/sdb1 *		32	  1234567	1234567		7	HPFS/NTFS/exFAT

This will be another reference to the  usb drive. The **sdb1** reference is more specific and the one we will use.

We use **fdisk** to confirm the name of the USB hard disk.

We now need to create a folder so we can mount this disk.

{{< highlight go >}}
  sudo mkdir /media/usb          
{{< / highlight >}}

This will create a folder for us to use.

Finally we need to mount the disk with:

{{< highlight go >}}
  sudo mount /dev/sdb1 /media/usb
{{< / highlight >}}

mount the darware location **/dev/sdb1** in the software location **/media/usb**.

Now if this has worked correctly you should see your USB disk pop up on the screen and you now have access to the USB.
