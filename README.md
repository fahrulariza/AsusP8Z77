# **Hackintosh-ASUS-P8Z77**

Hackintosh **macOS Big Sur 11.7.6**| **DESKTOP ASUS P8Z77** **

---

**Download EFI**

- via Terminal : \$ `git clone https://github.com/fahrulariza/AsusP8Z77.git` or [Click Here](https://github.com/fahrulariza/AsusP8Z77/archive/refs/heads/master.zip)

---

**Specification  :**

- **Processor :** [Intel Core i7-3770 @ 3.40 GHz 3 MB cache, 4 cores 8 Thread](https://www.intel.co.id/content/www/id/id/products/sku/65719/intel-core-i73770-processor-8m-cache-up-to-3-90-ghz/specifications.html#specs-1-0-1)
- **Chipset :** [Intel® Z77 Express](https://www.intel.co.id/content/www/id/id/products/sku/64024/intel-z77-express-chipset/specifications.html)  
- **Motherboard  :** [P8Z77-V (Socket LGA1155)](https://www.asus.com/id/supportonly/p8z77-v%20lx/helpdesk_cpu/) 
- **iGPU :** [Intel® HD Graphics 4000](https://www.intel.co.id/content/www/id/id/products/sku/65719/intel-core-i73770-processor-8m-cache-up-to-3-90-ghz/specifications.html#specs-1-0-4)
- **dGPU :** RX7 RX580 8GB GDDR5 2048SP 256BIT Memory(Samsung) a.k.a Ellesmere (Polaris 20) > Flash VBIOS ONLY USED [AMDVBFlash / ATI ATIFlash 2.93](dl.techpowerup.com/files/BS76uZSaTG3HUIEcHZhlhQ/1730099401/atiflash_293.zip) to [Sappire RX570 8GB GDDR5 256BIT Memory (Samsung)](https://www.techpowerup.com/vgabios/225970/sapphire-rx570-8192-191031-1)
- **Memory :** 32GB 4 x [HyperX FURY Memory Blue - 8GB Module - DDR3 1600MT/s CL10 DIMM](https://www.kingston.com/id/memory/search/discontinuedmodels?partid=HX316C10F/8)
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
- **SMbios : [iMac15,1 (Retina 5K, 27-inch, Mid 2015)](https://support.apple.com/id-id/112434)
- **OS Version :** [macOS Big Sur 11.7.6](https://support.apple.com/id-id/111980) > Installer From [Online Install from gibMacOS](https://github.com/corpnewt/gibMacOS) or [Olarila Vanilla Images - macOS Installer](https://olarila.com/topic/6278-olarila-vanilla-images-macos-installer/)
- **Bootloader :** [OpenCore 1.0.2](https://github.com/acidanthera/OpenCorePkg/releases/tag/1.0.2)

---

**What's Working **

- QE/CI of Intel® HD Graphics 4000 (1536MB) | [**ig-platform-id** : 07006201](https://dortania.github.io/OpenCore-Install-Guide/config.plist/ivy-bridge.html#deviceproperties) Used when the iGPU is only used for computing tasks and doesn't drive a display (requite kext [Lilu](https://github.com/acidanthera/Lilu/releases), [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases))
- CPU Power Management (SSDT-PLUG)
- Restart, Sleep and Shutdown
- Internal Speaker, Headphone and Internal Microphone | with layout-id 1 ([AppleALC](https://github.com/acidanthera/applealc/releases), [Lilu](https://github.com/acidanthera/Lilu/releases))
- Function FN + | in HP Keyboard
- Ethernet | [Intel(R) 82579V](https://github.com/acidanthera/IntelMausi/releases)
- Wi-Fi | TL-WN851ND V1 Wireless N Adapter chipset [Atheros AR9227](https://wikidevi.wi-cat.ru/index.php/Special:Ask?title=Special%3AAsk&q=%5B%5BChip1+model::~AR9227*%5D%5D&po=%3FInterface%0D%0A%3FFCC+ID%0D%0A%3FManuf%0D%0A%3FManuf+product+model=Manuf.+mdl%0D%0A%3FVendor+ID%0D%0A%3FDevice+ID%0D%0A%3FSubvendor+ID%0D%0A%3FSubdevice+ID%0D%0A%3FChip1+model%0D%0A%3FSupported+802dot11+protocols=PHY+modes%0D%0A%3FMIMO+config%0D%0A%3FOUI%0D%0A%3FEstimated+year+of+release=Est.+year&eq=yes&p%5Bformat%5D=broadtable&order%5B0%5D=ASC&sort_num=&order_num=ASC&p%5Blimit%5D=500&p%5Boffset%5D=&p%5Blink%5D=all&p%5Bsort%5D=&p%5Bheaders%5D=show&p%5Bmainlabel%5D=&p%5Bintro%5D=&p%5Boutro%5D=&p%5Bsearchlabel%5D=%E2%80%A6+further+results&p%5Bdefault%5D=&p%5Bclass%5D=sortable+wikitable+smwtable) - AirPortAtheros40, used [IO80211HighSierra.kext](https://github.com/khronokernel/IO80211-Patches/blob/main/10.13.6-High-Sierra-Kexts/IO80211HighSierra.kext.zip))
- Bluetooth | (Turn on in Windows setting, then restart and boot to macOS)
- HDMI Out VGA PCIE RX 580 2048SP 8Gb (Video) as RX 570 8 Gb
- HDMI Audio (Video) PCIE RX 580 2048SP 8Gb (Video) as RX 570 8 Gb 4 - LS24C36x (2- AMD High Definition Audio Device)
- Audio Internal with ALC892 [boot-args	> alcid=1](https://github.com/acidanthera/applealc/wiki/supported-codecs)
- All USB Port (USB 3.0, USB 2.0, Jack Audio)
- iMessage + facetime | (Use Real Serial Number of MacBook Pro (Sync with SMBIOS))
- Webcam USB
- SD Card Reader
- Etc..

---

**Not Working :**

-

---

**BIOS Configuration**

|                  Bios Config                  |  Setting   |
| :-------------------------------------------: | :--------: |
|            Security -> Secure Boot            |  Disabled  |
|             Intel Virtualization              |  Enabled   |
|                     VT-d                      |  Enabled   |
| Graphics Configuration ->                     |    PCIE    |
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
