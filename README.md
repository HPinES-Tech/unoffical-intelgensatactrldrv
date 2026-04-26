# (Unoffical) Intel(R) Generic SATA controller driver


![Thumbnail Image](https://github.com/HPinES-Tech/unoffical-intelgensatactrldrv/blob/main/intelgensatactrldrv-demoimg1.png?raw=true)

This project was created to replace the official Intel(R) MSM/RST SATA AHCI/RAID driver with a simplified driver for multi-driver compatibility with various Intel variants.

Compatible with multiple configurations: MSM/RST + PCH/SoC + AHCI or MSM/RST + PCH/SoC + RAID (AHCI and RAID cannot be used interchangeably due to different Hardware IDs between CC_0106 and CC_0104).
# WARNING!
This project is still in the Unstable phase. However, if this driver works with more than 30 different Intel(R) SATA drivers (i.e., resolves and closes more than 30 issues in the [Issues](https://github.com/HPinES-Tech/unoffical-intelgensatactrldrv/issues) tab), then this project will be pushed to Stable and considered to work well across multiple devices.

Any issues related to this driver, please report them in the [Issues](https://github.com/HPinES-Tech/unoffical-intelgensatactrldrv/issues) tab like this:
- HardwareIDs: VEN_8086&&DEV_(your DEV ID)&&CC_(0106 is AHCI, 0104 is RAID)
- Issues: Describe the error you are experiencing.
- Additional description (Optional): The way you add drivers, the way you create a bootable installer, etc...

Tips: To view your controller HardwareIDs, press Windows + R -> type 'devmgmt.msc' then press enter -> expand 'IDE ATA/ATAPI controllers' -> right click to your AHCI/RAID controller -> select Properties -> 'Details' tab -> expand child option under Property -> select 'HardwareIDs', and now your controller HardwareIDs like this: VEN_8086&&DEV_xxxx&&CC_010x
# Usages
To add driver, use [Nlite](https://www.nliteos.com/) or F6 Floppy Method

Make sure you select the Textmode Driver and the Intel(R) Generic SATA AHCI/RAID controller driver when using the [Nlite](https://www.nliteos.com/) method.
# Troubleshooting & Bug Fixing
Here are some of the errors I encountered while testing on DEV_22A3 and how I've fixed them:

**1. 0x7B still appear:**
- Make sure you have added the drivers correctly.
- For **Windows 2000 and XP*: If you are using a USB drive to store the installer, use [WinNTSetup](https://taimienphi.vn/download-winntsetup-66477/64bit-phien-ban) to apply Windows to the hard drive (after extracting the ISO into a complete folder, especially one containing the I386 folder).

**2. 0xA5 BSOD**
- Unfortunately, your device uses ACPI that is too new for Windows XP to communicate. Please use [Modified ACPI for Windows XP](https://www.mediafire.com/file/wsqgptapdrxhidf/ACPI2.0_v4_x86+x64_5.1+5.2.7z/file) (there is still no solution for Windows 2000).
