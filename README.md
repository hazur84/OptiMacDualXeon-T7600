# Dell Precision T7610 Workstation Hackintosh GUIDE

## Introduction: 

Hi Everyone,

This Workstation used to be a Beast with Dual CPUs and tons of RAM, I Know it is now normal to get that much cores in a Desktop but it is still a very decent machine for me (As a Programmer), and I thought it would be a good idea to Install MacOS as the Daily Driver Rather than Linux and It turns out to be a very Great Experience (with Some Challenges ^_^).

## Specs:

CPU: 2x Xeon E5-2680 v2 2.8GHz Ten Core Processors
RAM: 128 GB 1333 MHz DDR3 ECC Memory
GPU: SAPPHIRE PULSE Radeon RX 580 8GD5
Chipset: Intel C602
Audio: Realtek ALC3220 (ALC280) High Definition Audio
SAS Drive Controllers (RAID): LSI 2308 SATA/SAS 6Gb/s controller with host based RAID 0, 1, 10 (4 
Network Controller 1: Intel 82579 Gigabit Ethernet controller with Remote Wake UP, PXE and Jumbo frames support

Network Controller 2: Intel Ethernet Controller I210

NEC USB3.0 xHCI Controller: Renesas Electronics uPD720201 & uPD720202

## Working:

Both "Xeon E5-2680 v2" and all cores with Power Management and P-States (using VoodooTSCSync & ssdtPRGen.sh)
ATI Radeon HD 4870 (Vanilla)
Realtek ALC3220 (ALC280)  (using VoodooHDA till Now - it is partially working with AppleALC using layout-id 13)
LSI 2308 SAS (using AstekFusion2)
Intel 82579 Network Controller (Vanilla)
Intel I210 Network Controller (IntelMausiEthernet)
USB 2.0

## Not Working:

NEC USB3.0 xHCI Controller (Renesas Electronics uPD720201 & uPD720202)
Sleep
