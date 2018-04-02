# Dual Booting Ubuntu
![Laptop](https://assets.ubuntu.com/v1/b0b06642-Laptop.png?w=654)

##

# Overview

1. [Pre-Installation](##Pre-Installation)
2. [Download](##Download)
3. [Make Room](##Make-Room)
4. [Successful Boot](##Successful-Boot)
5. [Install](##Install)

## Pre-Installation
Before starting, make sure that you have the following:
- A computer with a **[UFEI boot mode](https://itsfoss.com/check-uefi-or-bios/)** and at least **16GB** of free space.
- A seperate USB stick **2GB** or more.

##

## Download
Download the files on this **[Page](linktodownload)** or follow these links:

### **[Rufus](https://rufus.akeo.ie/)** and **[Ubuntu](https://www.ubuntu.com/download/desktop)**.
Start Rufus as Administrator select the Ubuntu.iso file.

![Rufus](rufus.png)

##

## Make Room
There are multiple ways to open *Disk Partition* on Windows:
1. Open the start menu <kbd>⊞ Win</kbd> and type ***Disk Partition***.
2. Press <kbd>⊞ Win</kbd>+<kbd>R</kbd> to open the run dialog, then type `diskmgmt.msc` and hit enter.

### Find the disk for your Ubuntu installation *(Recommended to install on [SSD](https://en.wikipedia.org/wiki/Solid-state_drive) for better performance)*
Installing on the same drive as windows is perfectly normal. In this case, **Right Click** on the slice that says **"(C:)"** and `Shrink Volume...`.

![Shrink Volume](disk1.png)

### Important!
If you get the message below, go to the [solutions tab](##Cannot-shrink-volume).

![Shrink Volume error](disk3.png)

### Enter a size in MB for your Ubuntu installation. 

![Shrink Volume size](disk2.png)

*CAUTION: 1 Gigabyte is 1,024 Megabytes!*
- 16GB is 16384MB
- 30GB is 30720MB
- 50GB is 51200MB
- 64GB is 65536MB
- 100GB is 10240MB

##

## Successful Boot
1. [Fast Boot](###Disabling-Fast-Boot)
2. [Secure Boot](###Disabling-Secure-Boot)
3. [Boot Priority](###Boot-Priority)

If you already know how to boot into a USB you can **[Skip](##nextsection)** past this section.

### Disabling Fast Boot
Before you restart, you must disable **Fast Boot**.

Why?

>**DATA LOSS!!!** If you create a shared NTFS data partition, hibernation caused by Windows Fast Boot may maintain the current file structure. A problem arises when trying to save a file from Ubuntu into the NTFS partition, it will get lost on Windows reboot because the computer will remember the old file structure from when it was put in hibernation.

Navigate here to avoid this issue.

![Fast Boot](fastboot.png)

### Disabling Secure Boot
>Modern Windows PCs produced after Windows 8's release have UEFI firmware with “Secure Boot” enabled. This helps protect against rootkits and other malware infecting the Windows boot loader, but it can also prevent Ubuntu from booting.

Now you can reboot your computer and spam <kbd>F10</kbd> to get into the BIOS Setup menu.

If that doesn't work. Spam <kbd>F1</kbd> <kbd>F2</kbd> <kbd>F8</kbd> <kbd>F9</kbd> <kbd>ESC</kbd> or just google it.

![Secure Boot](bootmanager.jpg)

### Boot Priority
Before you leave that menu. Find the **Boot tab** and move **Removable Devices** to the top. *If you have the USB plugged in, move it to the top*.

![Boot Priority](boot_priority.gif)

**MAKE SURE TO SAVE CHANGES ON EXIT!!!**

##

## Install
Plug in the USB if you haven't done so already, and start your computer.

### You should see a menu similar to this. **Select** Install Ubuntu.

![Menu](menu.png)

### **Select** Language and connect to WiFi. **Check** both boxes and continue. 

![update](update.png)

### Next, **Choose** Install, Ubuntu alongside Windows. If there is no option go to this [solution](##Something-else-option)

![Dual Boot](dualboot.png)









# Solutions

## Cannot shrink volume

![solution](https://www.easeus.com/partition-manager-software/windows-cant-shrink-volume-partition.html)

## Something else option

![solution2](https://www.easeus.com/partition-manager-software/windows-cant-shrink-volume-partition.html)

