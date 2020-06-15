# Dell Precision T7610 Workstation Hackintosh GUIDE

## Introduction: 

This Workstation used to be a Beast with Dual CPUs and a lot of of RAM (64 GB), I Know it is now normal to get that much cores in a Desktop but it is still a very decent machine for me (As a Programmer), and I thought it would be a good idea to Install MOJAVE MacOS 10.15.6 as the Daily Driver.

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

## Some pics DELL T7600

![alt text](https://www.insanelymac.com/forum/uploads/monthly_2018_08/dell_precision_t7610_462_1212_mini_1065183.jpg.708d200690c29b90ba349b695fbe2c2c.jpg)

![alt text]
(https://www.insanelymac.com/forum/uploads/monthly_2018_08/delovna-postaja-dell-precision-t7610-4492-1.jpg.a3b6e0738a01c320abf08c8c44522e03.jpg) 

