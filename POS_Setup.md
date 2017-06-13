POS Terminal Setup
=======================

These instructions will guide you through the process of setting up one of the PAR POS terminals with touch capabilities. It will also list details for installing specific software relevant to the makerspace.



## Download
1. Download the latest Ubuntu Mate 64bit iso from the link below:
[https://ubuntu-mate.org/](https://ubuntu-mate.org/)

## Burn
These POS terminals won't boot from a USB thumb drive, only have 2 USB 2.0 ports, and lack an optical disk drive. In order to install anything, both a USB optical DVD drive and a USB hub are required to have enough I/O for the drive, mouse, and keyboard.

1. Use whatever tools are available to burn the ISO to a blank DVD.

## Boot
During the POS Boot up, there is a short window of time to choose [1. Boot]  [2. Setup]  [3. No]

1. Press [1.Boot] 
2. Choose the number of the device that corresponds to the USB Optical Drive

## Install
Follow the standard guided installation:

1. Wipe everything and use entire disk
2. check install updates during install (requires network access)
3. check install additional software drivers
3. User - rcl
4. Hostname - make it machine specific ex: "laser-station"


## Configure
These steps will ensure all makerspace POS terminals will provide the same interface at each station

1. Update the OS via either terminal or System > Administration > Software Updater
2. Reboot

### Touchscreen
 [Download](http://solutions.3m.com/wps/portal/3M/en_US/Electronics_NA/Electronics/Tools_Support/Support/) the Linux (Single Touch)(64-bit) Driver from 3M website
 
 Open a terminal and enter the following commands:
 `mkdir Documents/touchscreen_driver`
 
 `mv Downloads/MT7.14.4.bin64 Documents/touchscreen_driver`

`cd Documents/touchscreen_driver`

`chmod +x MT7.14.4.bin64`

`./MT7.14.4.bin64`

Hold the `page down` key until it stops scrolling

press `y` to blindly accept the agreement

`tar xzf twscreen.7.14.4.tar.gz`

`cd twscreen`

`sudo ./Install`

`sudo service TWDrvStartup start`

`sudo service TWDrvStartup status`

verify the service is running

Touch the screen like a child in wonderment

Dont' close the terminal

### Calibration
`sudo ./TwCalib`

follow prompts on the screen to calibrate the touch functions


### Look and Feel
Go to System > Preferences > Look and Feel > Mate Tweak

Desktop Tab

1. Uncheck Show Desktop Icons

Interface tab

1. Change panel to "Mutiny"
2. Change Toolbar>Style to "Test beside Items"
3. Save Panel Layout

Go to System > Preferences > Look and Feel > Appearance
Go to Background Tab
Select No Background (blue to green gradient)

Change Date/Time settings to 12 hour clock

Install Chromium browser via System > Administration > Software Boutique

Remove any unnecessary programs from the dock

Pin chromium to the dock
Pin Caja file manager to the dock



