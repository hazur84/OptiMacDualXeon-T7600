# Dell Precision T7610 Workstation Hackintosh GUIDE

## Introduction: 

Hi Everyone,

This Workstation used to be a Beast with Dual CPUs and tons of RAM, I Know it is now normal to get that much cores in a Desktop but it is still a very decent machine for me (As a Programmer), and I thought it would be a good idea to Install MacOS as the Daily Driver Rather than Linux and It turns out to be a very Great Experience (with Some Challenges ^_^).

## Specs:

1. CPU: 2x Xeon E5-2620 v2 2GHz Eight Core Processors
1. RAM: 64 GB 1333 MHz DDR3 ECC Memory
1. GPU: GYGABYTE Radeon RX 560 4GB
1. HD SATA SSD 960 GB
1. BLUETOOTH USB BT400 ASUS
1. Chipset: Intel C602
1. Audio: Realtek ALC3220 (ALC280) High Definition Audio
1. SAS Drive Controllers (RAID): LSI 2308 SATA/SAS 6Gb/s controller with host based RAID 0, 1, 10 (4 
1. Network Controller 1: Intel 82579 Gigabit Ethernet controller with Remote Wake UP, PXE and Jumbo frames support
1. Network Controller 2: Intel Ethernet Controller I210
1. NEC USB3.0 xHCI Controller: Renesas Electronics uPD720201 & uPD720202

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
