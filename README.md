# dell-5400-hackintoch

Guide and EFI Folder (Clover), to how to install a fully functioning Hackintoch of macOS Catalina on Dell latitude 5400

**:warning: Important:**
- Watch the tutorial video linked below to have an idea about the process
- EFI Folder (Clover) required for this process is included in this repository
- You may risk your data or your system os, So follow instructions at your own risk !

![Image](https://i.imgur.com/OtSV3bk.png)

## Table of contents

- [Requirements](#requirements)
- [How/Tutorial](#howtutorial)
- [Recommended BIOS settings](#recommended-bios-settings)
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

## Recommended BIOS settings

**General**
- Boot Sequence:
    - Boot List Option = UEFI (-> Boot Sequence list will be set accordingly) 
- UEFI Boot Path Security:
    - Never (or whatever other value)

**System Configuration**
- SATA Operation = AHCI
- USB PowerShare:
    - Enable USB PowerShare = On 
- Keyboard illumination:
    - Bright = On (or any desired value) 
- Keyboard Backlight on AC:
    - Any desired setting 
- Keyboard Backlight on Battery:
    - Any desired setting

**Video**
- LCD Brightness = Whatever settings you prefer

**Security**
- SMM Security Mitigator = Off

**Power Management**
- Enable lid Switch = On
- Primary Battery Charge Configuration = Express Charge (or any other choice) 

**Virtualization Support**
- VT for Direct I/O = Disabled 


## Issues

:construction: Issue | :wrench: Fix
------------ | -------------
No Wifi and bluetooth | <ul><li>You will need an external wifi usb adapter (Like TL-WN725N)</li><li>or Replace the internal wifi card with a supported one</li></ul>
How can I dual boot with windows or linux | Watch the tutorial video
Can't boot after changing EFI | Copy EFI folder (in this repo) to a USB and boot from it
Audio jack Issues | <ol><li>Open EFI agent app , mount EFI</li><li>Copy all kexts that exist in: <br/>/Volumes/EFI/EFI/CLOVER/kexts/Other<br/>to:<br/>/Library/Extensions</li><li> Copy and execute this command in Terminal, to repair permissions and rebuild your cache:<br/>``` sudo chmod -Rf 755 /S*/L*/E*;sudo chmod -Rf 755 /L*/E*;sudo chown -Rf 0:0 /S*/L*/E*;sudo chown -Rf 0:0 /L*/E* ;sudo kextcache -i /  ```<br/> </li>  <li>Restart your computer for the repairs to take effect.</li></ol>
Laptop doesn't sleep after closing (lid switch) | Apply recommended bios above
Issues with trackpad (no zoom​ gesture, lag) | Use a usb mouse
Audio issues (Goes on and off randomly) | System preferences > Sound
No touch screen | N/A
No HDMI | N/A
No SD card reader | N/A

## What works

- Everything else not mentioned in the issues table, Other fixes coming soon

## Contact

- [soufiane@gouiferda.com](mailto:soufiane@gouiferda.com)
