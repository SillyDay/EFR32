# EFR32 NCP Firmware
Pre-built Zigbee firmware images as binary files for Silicon Labs EFR32 SoC family, 

Firmware is built with Simplicity Studio Version: SV4.1.13.5 with EmberZNet SDK 6.7.4.0

## E180-NCP(SW FlowControl) Without BootLoader

E180-NCP are Zigbee coordinator firmware images with EmberZNet PRO Zigbee stack for the E180-ZG120A/E180-ZG120B module and E180-ZG120B-TB evualuation board from Ebyte (or any other modules using EFR32MG1B232F256GM48). 

E180-ZG120A/E180-ZG120B contains IC = EFR32MG1B232F256GM48 which has a EFR32MG12 MCU that is part of Silabs EFR32MG1 Wireless Gecko Series 1 of SoCs.

Note! Backup your original Firmware before flash! E180-NCP firmware is UNTESTED.
Pin definition: UART0 TX:PA0, RX:PA1, LED1:PF7

E180-ZG120A module links:
- http://www.ebyte.com/cn/product-view-news.aspx?id=676
  -User Manual PDF with PIN layout & listing: http://www.ebyte.com/cn/downpdf.aspx?id=676
  
E180-ZG120B module links:
- http://www.ebyte.com/en/product-view-news.aspx?id=842
  - User Manual PDF with PIN layout & listing: http://www.ebyte.com/en/downpdf.aspx?id=842

E180-ZG120B-TB evaluation board links:
- http://www.ebyte.com/en/product-view-news.aspx?id=896
  - User Manual PDF with PIN layout & listing: http://www.ebyte.com/en/downpdf.aspx?id=896

These contain a EFR32MG1 SoCs (Series 1) specifically the IC = EFR32MG1B232F256GM48
- https://www.silabs.com/wireless/zigbee/efr32mg1-series-1-socs/device.efr32mg1b232f256gm48


# How to Flash（如何刷写）
由于E180系列模块不包含能通过串口更新程序的BootLoader（就目前了解来说）推荐使用JLink进行程序更新，此外使用JFlash还可备份模块当前的程序，方便在必要时刷回。仅需备份0x0-0x3FFF程序，共256KB。同理，刷写程序时也仅需刷写Flashbank0,即0x0-0x3FFF。


# References and resources

- https://github.com/MarkDing/IoT-Developer-Boot-Camp/wiki/Zigbee-Boot-Camp
- https://github.com/MarkDing/IoT-Developer-Boot-Camp
- https://github.com/MarkDing/IoT-Developer-Boot-Camp/wiki/files/ZB-Zigbee-Boot-Camp/Silicon-Labs-ZigBee-Onboarding-Roadmap.pdf
- https://www.silabs.com/community/wireless/zigbee-and-thread/knowledge-base.entry.html/2018/04/24/how_to_form_zigbee3-zrzB
- https://www.silabs.com/support/mesh-networking-training/zigbee/zigbee-3-0-dyi-building-a-zigbee-3-0-switch-and-light-from-scratch
- https://www.silabs.com/community/wireless/zigbee-and-thread/knowledge-base.entry.html/2017/12/28/building_firmwareim-1OPr
