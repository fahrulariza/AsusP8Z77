# **Hackintosh-ASUS-P8Z77**

Hackintosh **macOS Big Sur 11.7.6**| **DESKTOP ASUS P8Z77** **

---

**Download EFI**

- via Terminal : \$ `git clone https://github.com/fahrulariza/HP-Pavilion-14-V205TX.git` or [Click Here](https://github.com/fahrulariza/HP-Pavilion-14-V205TX/archive/refs/heads/master.zip)

---

**Specification  :**

- **Processor :** [Intel Core i7-3770 @ 3.40 GHz 3 MB cache, 4 cores 8 Thread](https://www.intel.co.id/content/www/id/id/products/sku/65719/intel-core-i73770-processor-8m-cache-up-to-3-90-ghz/specifications.html) 
- **Motherboard  :** [P8Z77-V (Socket LGA1155)](https://www.asus.com/id/supportonly/p8z77-v%20lx/helpdesk_cpu/) 
- **iGPU :** Intel® HD Graphics 4000
- **dGPU :** RX7 RX580 8GB GDDR5 2048SP 256BIT Memory(Samsung) Flash BIOS to [Sappire RX570 8GB GDDR5 256BIT Memory (Samsung)](https://www.techpowerup.com/vgabios/225970/sapphire-rx570-8192-191031-1)
- **Memory :** 32GB 4x8GB DDR3 1333/1600
- **Storage :** [1x PNY CS900 2.5'' SATA III SSD 250GB (Windows 10)](https://www.pny.com/ssd-cs900?sku=SSD7CS900-240-RB)
- **Storage :** [1x HXY SSD 120GB (MacOS)](https://linux-hardware.org/?id=ide:hxy-ssd-120g)
- **Storage :** [2x WDC 500GB HDD (Media)](https://smarthdd.com/database/WDC-WD5000AZLX-60K2TA0/01.01A01/)
- **Ethernet :** [1x Intel(R) 82579V Gigabit Network Connection](https://www.intel.com/content/www/us/en/products/sku/52963/intel-82579v-gigabit-ethernet-phy/specifications.html)
- **Wi-Fi :** [TL-WN851ND V1 Wireless N Adapter / Atheros AR9227](https://www.tp-link.com/id/support/download/tl-wn851nd/) PCI\VEN_168C&DEV_002D&SUBSYS_0300168C&REV_01
- **Bluetooth :** 
- **Camera :** Iriun Webcam USB
- **USB :** [Intel(R) 7 Series/C216 Chipset Family PCI Express Root Port](https://www.intel.com/content/www/us/en/products/sku/66416/intel-c216-chipset/specifications.html)
- **External Ports :** 1x SDCard Reader + 2x USB 3.0 + 2 USB 2.0 + 1x HDMI + 1x RJ45
- **Audio Codec :** [Realtek High Definition Audio codec ALC892 (1, 2, 3, 4, 5, 7, 11, 12, 15, 16, 17, 18, 20, 21, 22, 23, 28, 31, 32, 90, 92, 97, 99, 100)](https://www.realtek.com/Product/Index?id=699&cate_id=195)
- **Display Size and Model :** [24" Essential Monitor S3 S33GC](https://www.samsung.com/id/monitors/flat/essential-monitor-s3-24-inch-fhd-ips-100hz-ls24c330gaexxd/)
- **Monitor Resolution :** HD 1920 x 1080 100Hz Refresh Rate HDMI Port
- **Boot Mode :** [UEFI GPT](https://wiki.restarters.net/UEFI_and_GPT)
- **BIOS Manufacturer :** [P8Z77-V LX BIOS 2501](https://www.asus.com/id/supportonly/p8z77-v%20lx/helpdesk_bios/)
- **SMbios : [iMac15,1](https://support.apple.com/id-id/112434)
- **OS Version :** [macOS Big Sur 11.7.6](https://github.com/corpnewt/gibMacOS)
- **Bootloader :** [OpenCore 0.9.1](https://github.com/acidanthera/OpenCorePkg/releases)

---

**What's Working **

- QE/CI of Intel HD Graphics 5500 (1536MB) | **ig-platform-id** : 06002616 + SMBIOS MBP12,1 ([Lilu](https://github.com/acidanthera/Lilu/releases), [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases))
- CPU Power Management (SSDT-PLUG)
- Restart, Sleep and Shutdown
- Internal Speaker, Headphone and Internal Microphone | with layout-id 4 ([AppleALC](https://github.com/acidanthera/applealc/releases), [Lilu](https://github.com/acidanthera/Lilu/releases), SSDT-IRQFix)
- Touchpad with Gestures
- Brightness | (SSDT-PNLF)
- FN + Brightness Button Up/Down | (SSDT-PNLF)
- Ethernet | ([RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases))
- Wi-Fi | (AirPortAtheros40, [HS80211Family](https://www.insanelymac.com/forum/files/file/1008-io80211family-modif/))
- Bluetooth | (Turn on in Windows setting, then restart and boot to macOS)
- HDMI Out (Video)
- HDMI Audio (Video)
- Battery Indicator | ([VirtualSMC](https://github.com/acidanthera/virtualsmc/releases), SMCBatteryManager)
- All USB Port (USB 3.0, USB 2.0, Jack Audio)
- iMessage + facetime | (Use Real Serial Number of MacBook Pro (Sync with SMBIOS))
- Webcam
- SD Card Reader
- Etc..

---

**Not Working :**

- dGPU : Nvidia GeForce 840M (disable from SSDT)
- AirDrop ??? not tested

---

**BIOS Configuration**

|                  Bios Config                  |  Setting   |
| :-------------------------------------------: | :--------: |
|            Security -> Secure Boot            |  Disabled  |
|             Intel Virtualization              |  Enabled   |
|                     VT-d                      |  Enabled   |
| Graphics Configuration -> DVMT Pre-Allocation |    64M     |
|    USB Configuration -> XHCI Pre-Boot Mode    | Smart Auto |
|                   SATA Mode                   |    AHCI    |
|              Boot -> Launch CSM               |  Disabled  |

---

**Tutorial**

[OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

---

**Special Thanks and Credits to :**

[Apple](https://www.apple.com) | [OpenCore](https://github.com/acidanthera/OpenCorePkg) | [corpnewt](https://github.com/corpnewt/gibMacOS) | [doesprintfwork](https://github.com/doesprintfwork/MakeInstallmacOS) | [Acidanthera](https://github.com/acidanthera) | [RehabMan](https://github.com/RehabMan/Laptop-DSDT-Patch) | [Mieze](https://github.com/Mieze/RTL8111_driver_for_OS_X) | [InsanelyMac](https://www.insanelymac.com/forum) | [Andres ZeroCross](https://github.com/andreszerocross) | Other Developers.

---
