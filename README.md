# Custom MacPro DELL T7600 Workstation Hackintosh Guide

## Introduction: 

This Workstation for extreme application used to be a Beast with Dual CPUs and a lot of of RAM (64 GB), I Know it is now normal to get that much cores in a Desktop but it is still a very decent machine for me (As a Programmer), and I thought it would be a good idea to Install MOJAVE MacOS 10.15.6 as the Daily Driver, also 

It is faster than the most expensive mac pro, with a 2x1 TB raid drive speed of over 350mb/s, along with 250mb/s read write speed, and a ssd for system and applications, is configured to work with the most demanding video files, Ultra-performance video editing 3D sound system.

## Specs:

1. CPU: 2x Xeon E5-2620 v2 2GHz Eight Core Processors
1. RAM: 64 GB 1333 MHz DDR3 ECC Memory
1. GPU: GYGABYTE Radeon RX 560 4GB, OUTPUT 4K MONITORS (DVI, HDMI and Display port)
1. HD SATA SSD 960 GB
1. WIFI AC 1300mb/s
1. BLUETOOTH 4.1 USB BT400  (Fully compatible with apple wireless devices)
1. Chipset: Intel C602
1. Built-in Speakers, Optical Drive
1. Audio: Realtek ALC3220 (ALC280) High Definition Audio
1. SAS Drive Controllers (RAID): LSI 2308 SATA/SAS 6Gb/s controller with host based RAID 0, 1, 10 (4 
1. Network Controller 1: Intel 82579 Gigabit Ethernet controller with Remote Wake UP, PXE and Jumbo frames support
1. Network Controller 2: Intel Ethernet Controller I210
1. NEC USB3.0 xHCI Controller: Renesas Electronics uPD720201 & uPD720202
1. Power Supply 1300 Watts 

## Working:

1. Both "Xeon E5-2620 v2" and all cores with Power Management and P-States (using VoodooTSCSync & ssdtPRGen.sh)
1. ATI RADEON RX 560
1. Realtek ALC3220 (ALC280)  (using VoodooHDA till Now - it is partially working with AppleALC using layout-id 13)
1. LSI 2308 SAS (using AstekFusion2)
1. Intel 82579 Network Controller (Vanilla)
1. Intel I210 Network Controller (IntelMausiEthernet)
1. USB 2.0

## Not Working:

1. NEC USB3.0 xHCI Controller (Renesas Electronics uPD720201 & uPD720202)
1. Sleep

## Pictures DELL T7600

![alt text](https://www.insanelymac.com/forum/uploads/monthly_2018_08/dell_precision_t7610_462_1212_mini_1065183.jpg.708d200690c29b90ba349b695fbe2c2c.jpg)

![alt text](https://www.insanelymac.com/forum/uploads/monthly_2018_08/delovna-postaja-dell-precision-t7610-4492-1.jpg.a3b6e0738a01c320abf08c8c44522e03.jpg)

![alt text](https://i.ebayimg.com/images/g/QE8AAOSwCDxeP-e9/s-l1600.jpg)

![alt text](https://i.ebayimg.com/images/g/L9gAAOSwtjBeP-ew/s-l1600.png)

# Hardware upgrades

1. Fenvi FV-HB1200 Broadcom 94360CS2 Wifi/BT Adapter

# Dell Precision T7600 + MacPro = The Dell MacPro

## Install a Supported Graphic Card Out Of The Box (OOB)

### Supported Nvidia Kepler Graphics Cards

Most people know that Nvidia has never released Web drivers for Mojave. What you may not know is that there is still support for many Nvidia Kepler cards right within Mojave. No drivers need to be installed for these cards to work in either High Sierra or Mojave. We don't know how long support will last for these but as of today they are fully supported.

The Following Cards are all Mojave Compatible:

Kepler Gen 2:
GTX 770
GTX 760/ti
GT 740
GT 730
GT 720
GT 710

Kepler Gen 1:
GTX 680
GTX 670
GTX 660/TI(MUST BE RUNNING A GK 104 core, NOT GK 106)
GTX 650(MUST BE RUNNING A GK 107 core, NOT GK 106)
GTX 645(GT 645 is Fermi)
GT 640(Kepler edition, GK 107/208 core)
GT 630(Kepler edition, GK 208 core)

Quadro:
Quadro 410
Quadro K420
Quadro K600 Card (4K at 60Hz via DisplayPort, is the cheapest 4k)
Quadro K2000/D
Quadro K4000/D
Dell or HP NVS 510

### Supported ATI Graphics Cards

1. RX 550
1. RX 560 (Best option relaible, not require power connector)
1. RX 570
1. RX 580 (NITRO SAPPHIRE)
1. RX 590 (NITRO SAPPHIRE)

## Preliminary Steps

1. Replace the Existing Thermal Paste on the CPU IHS (Integrated Heat Spreader)
Even if you bought your Dell from a professional refurbisher, it's highly unlikely that they took the time to replace the thermal compound between the CPU and heatsink. After four or five years, it needs to have the old compound removed and a fresh coat applied. Use 99% isopropyl alcohol and some guaze pads to remove it. Then apply some new paste like the Arctic MX4 which is available on Amazon or Newegg. If you don't have experience doing this look for some online video tutorials that show you how. A new coat of thermal paste will help keep temps much lower when you are pushing your CPU during gaming or video/photo editing.

1. Replace the CMOS Battery
These Dell Optiplex PCs are about 5 years old and may have sat on a shelf for two years unplugged from power. When Lithium batteries stay in a fully discharged state for long periods it greatly reduces their ability to hold a charge. My 9020 MT model had a battery like this. I kept getting a black screen at boot up. Was not able to even access the BIOS until I removed the battery for a minute and reseated it. I had checked the battery with a multimeter and it read 3.0v. Should be good right ? Even if it reads 3.0 volts it still may not be able to provide adequate voltage under load. When I test new CR2032 batteries the reading is often from 3.4 to 3.5 volts. That's how a good battery should test out.

Replace yours with a fresh new one before you make the BIOS changes in Step #2. Once you remove it from your board, all BIOS setting changes will be lost and you'll have to reapply them. Link to amazon to purchase a 2 pack is found above.
source: https://www.computerhope.com/issues/ch000239.htm

1. Remove any Add in Cards
If your Dell has any kind of wireless adapter installed (USB, PCIe or Mini PCIe) remove it before attempting the installation of macOS. Use Ethernet until after you've got everything else working properly. Then you can work on Wifi function after that. If you have a supported Broadcom card like the Fenvi FV-HB1200 you can keep that in a PCIe Slot during initial install.


## Step 1. Create your Mojave Unibeast Installer
Download Mojave from the Mac App Store on a Apple computer or whatever Hackintosh with Mojave OS.x

## If you don't have access to a Mac capable of making the Unibeast Installer

Create your UniBeast installer by following the standard tonymacx86 guide. Use a 16 or 32GB USB flash drive. Anything larger than 32GB in size must be partitioned to less than 32GB. Use UniBeast for Mojave only. Version 9.2.0.

There is one critical step to remember when formatting your USB or other drives in Disk Utility. Always click View and then Show All Devices instead of leaving it at "Show Only Volumes" when using High Sierra or Mojave to make the installer. After you select the Parent name, click on the Erase tab and format the USB as directed in the tonymacx86 guide.

Once creation of the UniBeast installer has completed, you will need to replace the UniBeast created config.plist with the custom one attached below. Do this before ejecting the UniBeast installer or you'll have to mount the EFI manually later. Now go to Finder -> Preferences and then select the "Show Hard Disks on the Desktop" option.

A. There will be an external drive on your desktop that represents the UniBeast USB's EFI partition
B. Double click that EFI drive icon to open it up and reveal the EFI folder on that partition
C. Now open the Clover folder inside of that EFI folder
D. Download the Custom Clover config.plist (zip file) Attached below
E. Delete the existing config.plist and then add in the new Custom one you just downloaded
F. Open up the kexts/other folder and drag and drop the release version USBInjectAll.kext into that folder
G. Download "SSDTs" zip file from the end of this post and place those files in the /Clover/ACPI/patched folder
H. Add the HFSPlus.efi driver to the Drivers64-UEFI folder. This is also attached below.

## Step 2. Update your BIOS and Change the Settings

Download the latest Optiplex 7020 BIOS A18 - Download the latest Optiplex 9020 BIOS A25
This is included as a mandatory step because the version that your Dell came with is likely much too old to work. Mine came with A05 from late 2015. For testing purposes, I tried the Mojave install and it worked. There were many USB related issues that could not be resolved until I later flashed to a newer 2018 BIOS. If yours is A10 or lower for the 7020 or A18 for the 9020 or lower, it's best to do this to get a fully functional OptiMac. Especially if you want working USB 3.0 ports.

If you do flash to A18 or A25 and want to downgrade later to an older BIOS that is an option you have. If you don't want the latest Intel Spectre and Meltdown updates to the CPU microcode then flash only up to A13 instead of A18. For the 9020, the newest BIOS without the Intel security patches would be A20. In my testing the A18/A25 BIOS versions don't significantly slow down i5 or i7 CPUs so consider flashing to the latest versions.

Flashing the BIOS to a newer Revision

It's easiest by far to flash your Dell to a newer BIOS from the Windows Desktop. You simply update the BIOS from right within Windows by double clicking on the .exe file. This will initiate the flashing process. Make sure you have Internet Explorer or Edge set as your default browser. Let your Dell reboot automatically to complete the process.

If you don't have a Windows 7 8.1 or 10 install on the hard drive of your Dell. You could download a Windows 10 iso from Microsoft and create an install USB but that is very time consuming and tedious. Dell offers a simple way to create a DOS based USB that you can boot from and flash the BIOS without having a Windows installation on your Optiplex.

There is the Dell Diagnostics Deployment Package software (a free download from Dell) that you can use to make a bootable USB and then boot from that to flash the BIOS to a newer version. Follow the directions in this video.
