# Z390MPro4-i7-9700K-Sapphire-RX580
### Introduction

This repository is designed for Asrock Z390MPro4  to run Mojave 10.14.X smothly. Due to the time constraint, a step by step installation guide won't be covered in this guide. For more information (regarding installation), please check [[Guide] Creating OSX Installer by Rehabman](https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093/) or installing [Mojave 10.14.x](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/) with [Etcher](https://www.balena.io/etcher/).

### Specs

- **Asrocks Z390M Pro4** (M.2 Key B * 2 + M.2 Key A+E * 1 + PCIe 3.0 x16 * 2)
- **Intel i7-9700K** (5.0 GHz OC, SMBIOS **iMac19,1**)
- **Clover Bootloader** (r5070)
- **be quiet! Dark Rock Pro 4** (250w TDP, highly recommended)
- **Kingston HyperX Fury Black 16GB** 3200MHz DDR4 8G * 2 (3200MHz OC)
- **WD Black 2018/PC SN720 NVMe 1T SSD**
- **Sapphire RX 580 Nitro+ 8G** (*BruceX 5K* Apple Res 422 Master Exporting time **21s**)
- **BCM94331CD** Wi-Fi/Bluetooth + [M.2 NGFF Key A+E Adapter](https://www.ebay.co.uk/itm/BCM94360CS2-BCM943224PCIEBT2-12-6-Pin-WIFI-wireless-card-module-to-NGFF-M-2/223633015347?hash=item3411910233:g:clQAAOSwI7lcld~Z) 

### Performance

![](https://i.imgur.com/WpDL9K3.png)

![image-20191005011344996](https://i.imgur.com/ygmo7NY.png)

![USBs Mapping-01](https://i.imgur.com/DCBv66S.png)

### What works

- **dGPU** Hardware Accelaration  (Final Cut Pro X, VideoProc, Compressor tested)
- **AirDrop, Handoff** (Apple Wi-Fi/Bluetooth required)
- **iMessage** (complete serial required) 
- **All USB3.1 Gen1/USB2.0 ports** (few USB2.0 ports disabled) 
- **HDMI Audio** (**Sound Control** is required to adjust volume)

### Bugs 

- **USB 3.1 Gen2 Hotplugging** (type-c port only works if the device is hocked up before booting up)
- **USB Type-C has no video output** (iGPU video output has been disabled since this is required by the dGPU HW acceleration)
- **Onboard HD Audio not working** 

### BIOS Settings

* **BIOS Version P1.3** (*Please do not upgrade!* I was **NOT** able to boot up macOS with P4.X BIOSs and I had to disassemble the chip and flash P1.30 firmware.) 

  > We don't recommend users to update the BIOS if their system is already running normally.

* Download `Hackintosh-BIOS.BIN` from the release page or Clone the whole repository (the file is under /BIOS_settings) and place it in an `FAT32` USB. 

* Enter BIOS setup, `Load BIOS settings from drive`, select the one from your USB.

### Installation

#### Option 1: GUI (recommended)

- [Mojave 10.14.X Download](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/)
- [Install macOS with etcher](https://www.balena.io/etcher/)

#### Option 2: Command-line

- Download Mojave 10.14.X from App Store
- [[Guide] Creating OSX Installer by Rehabman](https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093/) 

### Changelog

#### 2019/10/05

* Initial release

