---
title: "How to Setup a Permanent Doskeys Macro File"
date: 2020-07-12T10:09:23+10:00
draft: false
image: "images/beach.jpg"
tags: ["computer"]
categories: ["programming"]
---

I needed to recreate my doskeys.macro file on a new computer. The following commands show how to setup permanent doskey commands.

Open **Regedit**.

Go to the following regedit directory.

```
    HKEY_CURRENT_USER\Software\Microsoft\Command Processor
```

Create a new key named **Autorun**.

```	
    REG_SZ
```

Value

```
    doskey /macrofile="d:\util\macros.doskey"
```

#### My macros.doskey

These are short key commands that I use every day.

```
    cr=createcmd
    cu=cleanup
    dl=dlist
    no="C:\Program Files\Notepad++\notepad++.exe" $1
    mp=D:\Util\BuildMp3Tag.exe
```
