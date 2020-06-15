# DELL Precision T7600 + MacPro = The Dell MacPro T7600
DELL T7600 Workstation - 2x 8-Core Intel Xeon E5-2620V2 - 64GB RAM - AMD Radeon RX560

# Custom MacPro DELL T7600 Workstation Hackintosh Guide

This is a complete installation guide to install macOS Mojave 10.14.6 on your custom built hardware featuring 64GB RAM paired with 2x 8-Core Intel Xeon E5-2620v2 and SSD 960 GB. The purpose of this guide is to provide a step-by-step guide to install Mojave using Clover UEFI.

## Introduction: 

This Workstation for extreme application used to be a Beast with Dual CPUs and a lot of of RAM (64 GB), I Know it is now normal to get that much cores in a Desktop but it is still a very decent machine for me (As a Programmer), and I thought it would be a good idea to Install MOJAVE MacOS 10.14.6 as the Daily Driver, also 

It is faster than the most expensive mac pro, with a 2x1 TB raid drive speed of over 350mb/s, along with 250mb/s read write speed, and a ssd for system and applications, is configured to work with the most demanding video files, Ultra-performance video editing 3D sound system.

## Specifications

- Motherboard: DELL T7600
- Chipset: Intel C602
- CPU: 2x 8-Core Intel Xeon E5-2620V2 2GHZ
- RAM: 64 GB DDR3 1333MHz ECC Memory
- Ethernet: Intel 82579
- Ethernet: Intel I210
- Audio: Realtek ALC3220
- SAS Drive Controllers PCI (RAID): LSI 2308 SATA/SAS 6Gb/s
- NEC USB3.0 xHCI Controller: Renesas Electronics uPD720201 & uPD720202
- PSU: 1300 Watts 

# Hardware upgrades

1. WIFI: Fenvi FV-HB1200 Broadcom 94360CS2 Wifi/Bluetooth PCI Adapter AC 1300mb/s
1. Optival Drive: COMBO DVD-RW + Bluray ROM
1. Graphics: GIGABYTE AMD Radeon RX560 4GB; output 4k monitors (DVI, HDMI and Display port)
1. Monitor: LG SMART TV OLED 4K 55"
1. HD: ADATA SATA 960GB SSD
1. Keyboard: Apple USB (A1243)
1. Mouse: Apple Magic Trackpad 2 (A1535)

## Working:

1. Both "Xeon E5-2620 v2" and all cores with Power Management and P-States (using VoodooTSCSync & ssdtPRGen.sh)
1. ATI RADEON RX 560 (OOB)
1. Realtek ALC3220 (ALC280)  (using VoodooHDA till Now - it is partially working with AppleALC using layout-id 13)
1. LSI 2308 SAS (using AstekFusion2)
1. Intel 82579 Network Controller (Vanilla)
1. Intel I210 Network Controller (IntelMausiEthernet)
1. USB 2.0

## Not Working:

1. NEC USB3.0 xHCI Controller (Renesas Electronics uPD720201 & uPD720202)
1. Sleep

# Dell Precision T7600 Workstation Resources

## Dell T7600 Resources:
- Dell Precision T7600 Workstation Overview (Sales Presentation - Video)
- Dell Precision T7600 Workstation Specifications [(PDF)](https://www.dell.com/downloads/global/products/precn/en/Dell-Precision-T7600-Spec-Sheet.pdf)
- Dell T7600 documentation (dell.com): Owner's Manual [(PDF)](https://buerorechner24.de/mediafiles/Sonstiges/pdf-Dateien%20Workstations%20Spec%20Sheets%20Bedienungsanleitungen/Dell/T7600/Precision%20T7600%20Owner's%20Manual.pdf)
- Dell T7600 support (dell.com)

## Dell T7610 Resources:
- Dell Precision T7610 Workstation - Product Page (specs, etc.)
- Dell Precision T7610 Workstation Specifications [(PDF)](http://i.dell.com/sites/doccontent/business/smb/merchandizing/en/Documents/Dell_Precision_T7610_Spec_Sheet.pdf)

## Dell T7600 System Board Components
![alt text](https://c528a1c3-a-9923f991-s-sites.googlegroups.com/a/dv411.com/support/home/vendors/dell/T7600%20System%20Components.png?attachauth=ANoY7crD05fCxWyc8vYAL3W96AYXQ3aqjC9F7CyhpobLtYJLvLyykVwH6jtQjKBBraFZgpcsnM0bk1NgT4O5V0QdsiFMvzpKEC2u4IN-eHjNL3cqLnFtHF7XUFtcxIqGPgnl1NkoMQN3i-bDp49Qjtj98BFwRLvxa7x4oXl7HcmtvJx_tVw9YppvzXkQerv0GBPmPxW9DLI0r_vj8LLCqchVD28Humw9ePkSF3RParOXacJBE-iN_Oa0_Q2IzPaHKMyN-XfCtB76&attredirects=0)

1. PCI slot
2. PCIe x16 slot
3. PCIe x16 slot (wired as x4)
4. PCIe x16 slot (accelerated graphics port)
5. PCIe open-ended slot (wired as x4)
6. USB 3.0 front panel connector
7. Intrusion switch connector
8. DIMM slots (available only when optional second processor is installed)
9. Processor
10. Processor fan socket
11. front panel audio connector
12. DIMM slots (available only when optional second processor is installed)
13. PCIe X16 slots (available only when optional second processor is installed)
14. HDD3 fan connector
15. HDD2 fan connector
16. system fan 1 connector
17. 24-pin power 2 connector
18. DIMM slots
19. Processor
20. DIMM slots
21. Processor fan socket
22. system fan 2 connector
23. PSWD jumper
24. System 3 fan connector
25. internal speaker connector
26. remote power enable
27. front panel & USB 2.0 connector
28. 24-pin power1 connector
29. SATA connectors
30. Internal USB 2.0 connector
31. RTCRST jumper
32. SAS0 connector
33. SAS1 connector
34. HDD temperature sensor connector
35. Internal USB 2.0 connector
36. HDD1 fan connector
37. Coin-cell battery

![alt text](https://www.insanelymac.com/forum/uploads/monthly_2018_08/dell_precision_t7610_462_1212_mini_1065183.jpg.708d200690c29b90ba349b695fbe2c2c.jpg)

![alt text](https://www.insanelymac.com/forum/uploads/monthly_2018_08/delovna-postaja-dell-precision-t7610-4492-1.jpg.a3b6e0738a01c320abf08c8c44522e03.jpg)


## Install a Supported Graphic Card Out Of The Box (OOB)

### Supported Nvidia Kepler Graphics Cards

Most people know that Nvidia has never released Web drivers for Mojave. What you may not know is that there is still support for many Nvidia Kepler cards right within Mojave. No drivers need to be installed for these cards to work in either High Sierra or Mojave. We don't know how long support will last for these but as of today they are fully supported.

The Following Cards are all Mojave and Catalina compatible:

**Kepler Gen 2:**
GTX 770,
GTX 760/ti,
GT 740,
GT 730,
GT 720,
GT 710

**Kepler Gen 1:**
GTX 680,
GTX 670,
GTX 660/TI(MUST BE RUNNING A GK 104 core, NOT GK 106),
GTX 650(MUST BE RUNNING A GK 107 core, NOT GK 106),
GTX 645(GT 645 is Fermi),
GT 640(Kepler edition, GK 107/208 core),
GT 630(Kepler edition, GK 208 core).

**Quadro:**
Quadro 410,
Quadro K420,
Quadro K600 Card (4K at 60Hz via DisplayPort, is the cheapest 4k),
Quadro K2000/D,
Quadro K4000/D,
NVS 510.

### Supported ATI graphics cards RX 5XX series.

RX 550,
RX 560 (Best option relaible, not require power connector),
RX 570,
RX 580 (NITRO SAPPHIRE),
RX 590 (NITRO SAPPHIRE).

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

## Step 2. Update BIOS to last available version (A17)

1. Download the latest BIOS A17
This is included as a mandatory step because the version that your Dell came with is likely much too old to work. 
For testing purposes, I tried the Mojave install and it worked. There were many issues that could not be resolved until you later flashed to a newer BIOS. If yours is A16 or lower, it's best to do this to get a fully functional.

1. Flashing the BIOS to a newer Revision
It's easiest by far to flash your Dell to a newer BIOS from the Windows Desktop. You simply update the BIOS from right within Windows by double clicking on the .exe file. This will initiate the flashing process. Make sure you have Internet Explorer or Edge set as your default browser. Let your Dell reboot automatically to complete the process.

1. If you don't have a Windows 7 8.1 or 10 install on the hard drive of your Dell. You could download a Windows 10 iso from Microsoft and create an install USB but that is very time consuming and tedious. Dell offers a simple way to create a DOS based USB that you can boot from and flash the BIOS without having a Windows installation on your Optiplex.

1. There is the Dell Diagnostics Deployment Package software (a free download from Dell) that you can use to make a bootable USB and then boot from that to flash the BIOS to a newer version. Follow the directions in this video.

## Step 3. Recommended BIOS Settings

If you're installing on a recommended CustoMac desktop with AMI UEFI BIOS, the options are simple. For other systems make sure to set your BIOS to Optimized Defaults, and your hard drive to AHCI mode. Here are standard AMI UEFI BIOS settings for
Gigabyte AMI UEFI BIOS, Gigabyte AWARD BIOS, ASUS AMI UEFI BIOS, and MSI AMI UEFI BIOS.

1. To access BIOS/UEFI Setup, press and hold Delete on a USB Keyboard while the system is booting up
1. Load Optimized Defaults
1. If your CPU supports VT-d, disable it
1. If your system has CFG-Lock, disable it
1. If your system has Secure Boot Mode, disable it
1. Set OS Type to Other OS
1. If your system has IO Serial Port, disable it
1. Set XHCI Handoff to Enabled
1. If you have a 6 series or x58 system with AWARD BIOS, disable USB 3.0
1. Save and exit.

## Step 4. FUll patched DSDT

It's fully described here how to patch the DSDT. **NOTE: You can NOT use my patched DSDT.aml or anyone's else. You must do it yourself!** Short story:

1. Boot into Clover. Press F4 and then boot into macOS.
1. Clone iasl to a folder of your choice (git clone https://github.com/RehabMan/Intel-iasl iasl).
1. make && sudo make install to build and put the binary at the default path for binaries.
1. Download the latest MaciASL from here.
1. Mount the EFI partition and copy over the .aml files in EFI/CLOVER/ACPI/origin that start with DSDT or SSDT to a new folder somewhere.
1. Run iasl -da -dl DSDT.aml SSDT*.aml in that directory.
1. Open MaciASL and open the outputted DSDT.dsl.
1. Apply patches. In my case, I wanted proper sleep (it was waking up by USB events):

 into_all method label _PRW  remove_entry;
 into_all all code_regex Name.*_PRW.*\n.*\n.*\n.*\n.*\}\) remove_matched;
 
1. Save as ACPI Machine Language Binary to EFI/CLOVER/ACPI/patched/DSDT.aml.
1. Reboot.

You might find other issues that you want to patch. Good luck!

# BENCHMARKING

![alt text](https://i.ebayimg.com/images/g/L9gAAOSwtjBeP-ew/s-l1600.png)

![alt text](https://i.ebayimg.com/images/g/QE8AAOSwCDxeP-e9/s-l1600.jpg)
