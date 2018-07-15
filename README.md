# Tandy 1000 EX

* [System Disks](http://www.oldskool.org/guides/tvdog/system.html)
* [Forum Article where they got it working](https://torlus.com/floppy/forum/viewtopic.php?t=911)

Flash Firmware, Load up a USB drive with contents of usb/, slap it into your Tandy 1000EX, and play
classic games and use deskmate. Pretty cool stuff.


## Flashing Firmware

Purchase a Gotek SFRC922D, flash FlashFloppy Firmware on it by way of using this win32/en.stsw-stm32080.zip 
to flash the image located in win32/flashfloppy_v0.9.24a.zip. 


* [YouTube Video Explaining Procedure](https://www.youtube.com/watch?v=-K31S2xqZIk)

Set the jumpers the way outlined in the video...

```
XX0OOO
 OO0OO
```

Follow the video, pretty easy to work out.

## FlashFloppy

Installed the FlashFloppy Firmware, works very well!

## Creating 780K IMG files

* [WinImage](http://www.winimage.com/download.htm) does the trick
* * Select 720k images
* * Update manifest when you copy over or else nobody will know what is what!

## Creating 2.5M Image Files

Technically, the system can read 2.5MB images, instead of the 780k images you typically use.

* https://www.youtube.com/watch?v=Lw0JV4TypSo explains how

Basically, in order for the images to work, DOS has to be loaded with a hack or two.


### To create boot image compatible with 2.5MB disk image

* Take a DOS disk from the System Disks link above...
* Open it with imgburn, copy/inject BIOPTCH.SYS into the image
* Create a CONFIG.SYS file with the contents of `DEVICE=BIOSPTCH.SYS` and inject into image
* Save image as DSKA0000.img for booting 


### To create 2.5MB images:
* Launch win32\HxCFloppyEmulator_soft\Windows\HxCFloppyEmulator.exe
* Select 'Disk Browser'
* In 'DOS Floppy Disk Browser' window, select '3"5 2.50MB DSDD FAT32'
* Drag Files In
* Save/Export, save as DSKA0007.hfe





# No Longer Relevant

Everything below this should probably be deleted...

## Gotek SFRC922D

* [USB Floppy Format Tool for the USB Floppy Emulation V2](win32/USB_Floppy_Emulator_1.40i.exe) from [ipcas](http://www.ipcas.com/support/usb-floppy-emulation-download.html)

When I hold both buttons and turn on the device, the screen flashes with `u00` `126`
`f01`

>  I had to select the drive A first pin position for the system to see it.

* [Manual](http://cdn1.goughlui.com/wp-content/uploads/2013/05/SFR1M44-U100K-SFR1M44-U100K-R-SFR1M44-TU100K-UM.pdf)