# dell-5400-hackintoch

EFI Folder (Clover) and config required for dell latitude 5400 Hackintosh wiith macOS Catalina

![Image](https://i.imgur.com/OtSV3bk.png)

## Table of contents

- [Issues](#issues)
- [What works](#what-works)
- [Requirements](#requirements)
- [Tutorial](#tutorial)

## Issues

:x: Issue | :wrench: Fix
------------ | -------------
Wifi doesn't work | You will need an external wifi usb adapter (Like TL-WN725N)
Bluetooth doesn't work | Replace the internal wifi card with a supported one
How can I dual boot with windows or linux | Watch the tutorial (from bottom link)
Messing with clover efi files might be risky | Copy what's in this repo to a USB and boot from it
Audio jack Issues | <ul><li>Open EFI agent app , mount EFI</li><li>Copy all kexts that exist in: <br/>/Volumes/EFI/EFI/CLOVER/kexts/Other<br/>to:<br/>/Library/Extensions</li><li> Copy and execute this command in Terminal, to repair permissions and rebuild your cache:<br/>``` sudo chmod -Rf 755 /S*/L*/E*;sudo chmod -Rf 755 /L*/E*;sudo chown -Rf 0:0 /S*/L*/E*;sudo chown -Rf 0:0 /L*/E* ;sudo kextcache -i /  ```<br/> </li>  <li>Restart your computer for the repairs to take effect.</li></ul>
Updating the system might be risky | N/A
No detection of laptop lid closing | N/A
HDMI port doesn't work | N/A


## What works

- Everything else not mentioned in issues

## Requirements

What | Why
------------ | -------------
Dell 5400 or similiar models | Duh
Access to a mac computer, or a macOS virtual machine | To download macOS catalina (8 GB) and copy to usb
8 GB USB | To boot macOS installation from
Backup your data | macOS installation requires formatting the entire drive

## Tutorial

- https://www.youtube.com/watch?v=eFnZF3rgS0o

