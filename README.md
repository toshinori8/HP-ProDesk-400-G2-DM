![HP Prodesk 400 G2 DM](OC/Resources/Image/HP-ProDesk-400-G2.webp)
# HP ProDesk 400 G2 DM 
## Big Sur 11.5.2 (20G95)

## Configuration

| Specifications | Details                                          |
| ------------------- | ------------------------------------------- |
| Computer model      | HP Prodesk 400 G2 DM      					|
| Processor           | Intel(R) Core(TM) i3-6100T CPU @ 3.20GHz    |
| SMBIOS           | iMac19/2     |
| Graphics			  | Intel HD Graphics 530 fake [Intel Skylake GT2 [HD Graphics 520] 2048  MB]                 		|
| Sound Card          | Realtek ALC221 (layout-id:88)            |
| Ethernet		      | Realtek RTL8111 PCIE                        |
| WiFi		          | Intel 7265 m.2                          	|
| RAM		          | 16GB                                     	|


![m.2 ssd and Prodesk mainboard wiht two m.2 slots](OC/Resources/Image/ssd.jpg)


## Improvements

- This version was prepared using OpenCore 0.7.5 for MacOS Big Sur.
- SSDT was generated for i3-6100T. Use https://github.com/Piker-Alpha/ssdtPRGen.sh to optimize yours CPU power management and then paste it into EFI/OC/ACPI/ssdt.aml
- Used SSDTTime Script to fix irq issues for sound and generate dsdt-hpet.aml 



## Working / Fixed; 



+ Intel HD 530 blnking screen - fix by inject Intel Iris 520 
+ USB
+ Sound / for internal speaker and lineOut bootargs alcid=88
+ Fixed Airplay screen mirroring - black screen with mouse cursor (Skylake isue) 
+ iMessages
+ Wifi and Ethernet
+ M.2 Pcie SSD 
+ Fixed RTC error on restart 

GeekBench 5.3.2 Score 1919
https://browser.geekbench.com/v5/cpu/compare/9719494?baseline=8259325

## Installation




- Durning installation if you nead ethernet and is disconected use terminal to set proper media type. Script is located under /EFI/network_UP_script 


### Issues
+ Display Port Audio output isn't working with enabled internal speaker and lineout / remove alcid=88 boot args 
+ Sleep 