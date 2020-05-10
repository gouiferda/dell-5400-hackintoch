# Dell-5400-hackintoch

EFI Folder (Clover), and how to install a fully functioning Hackintoch of macOS Catalina on Dell latitude 5400

**:warning: Disclaimer:**
- Always back up your data, and have another machine just in case one broke
- Watch the tutorial video linked below to have an idea about the process
- EFI Folder (Clover) required for this process is included in this repository
- This guide and anything in the repo comes with no warranty. Use at your own risk! I am not responsible if you broke your hackintosh os

<img align="right" width="300" height="250" src="https://i.imgur.com/OtSV3bk.png">

## Table of contents

- [Requirements](#requirements)
- [How/Tutorial](#howtutorial)
- [Mandatory BIOS settings](#recommended-bios-settings)
- [Issues](#issues)
- [What works](#what-works)

## Requirements

What will I need | Why
------------ | -------------
Dell 5400 or similiar models | Duh
Access to a mac computer, or a macOS virtual machine | To download macOS catalina (8 GB) from the appstore, then create a bootable catalena USB
8 GB USB | To create a bootable macOS installation from
Backup your data | macOS installation requires formatting the entire drive

## How/Tutorial

Important: The tutorial video below has the exact same process that works for the Dell Latitude 5400, the only difference is with the EFI folder used, the EFI folder and the EFI Agent app that you will need for Dell 5400 is in this github repo.

- https://www.youtube.com/watch?v=eFnZF3rgS0o

## :warning: Mandatory BIOS settings


Main Section | Option | Recommended value
------------ | ------------- | -------------
General | Boot Sequence |  Boot List Option = UEFI (-> Boot Sequence list will be set accordingly) 
General | UEFI Boot Path Security |  Never (or whatever other value)
System Configuration | SATA Operation | AHCI
System Configuration | USB PowerShare | Enable USB PowerShare = On 
System Configuration | Keyboard illumination | Bright = On (or any desired value) 
System Configuration | Keyboard Backlight on AC | Any desired setting 
System Configuration | Keyboard Backlight on Battery | Any desired setting
Video | LCD Brightness | Whatever settings you prefer
Security | SMM Security Mitigator | Off
Power Management | Enable lid Switch | On
Power Management | Primary Battery Charge Configuration | Express Charge (or any other choice) 
Virtualization Support | VT for Direct I/O |  Disabled

## Issues

:construction: Issue | :wrench: Fix
------------ | -------------
No Wifi and bluetooth | <ul><li>You will need an external wifi usb adapter (Like TL-WN725N)</li><li>or Replace the internal wifi card with a supported one</li></ul>
How can I dual boot with windows or linux | Watch the tutorial video
Can't boot after changing EFI | Copy EFI folder (exists in this repo) to a USB and rename USB "EFI" then boot from it
Laptop doesn't sleep after closing (lid switch) | Apply mandatory bios settings mentioned above
Audio jack Issues | Execute the JACK_FIX script (exists in this repo /FIXES folder) ``` cd TOOLS;sudo ./JACK_FIX ```
Audio cuts suddenly sometimes | System preferences > Sound
Issues with trackpad (no zoom​ gesture, lag) | Use a usb mouse
Mouse double clicks instead of single click sometimes | N/A
No touch screen |  Open this repo in terminal: ``` cd TOOLS;sudo ./INSTALL_TOUCH ```
No HDMI | N/A
No SD card reader | N/A

## What works

- Everything else not mentioned in the issues table, other fixes coming soon

## Contact

- [soufiane@gouiferda.com](mailto:soufiane@gouiferda.com)
