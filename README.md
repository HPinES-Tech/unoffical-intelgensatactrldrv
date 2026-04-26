# (Unoffical) Intel(R) Generic SATA controller driver


![Thumbnail Image](https://github.com/HPinES-Tech/unoffical-intelgensatactrldrv/blob/main/intelgensatactrldrv-demoimg1.png?raw=true)

This project was created to replace the official Intel(R) MSM/RST SATA AHCI/RAID driver with a simplified driver for multi-driver compatibility with various Intel variants.

Compatible with multiple configurations: MSM/RST + PCH/SoC + AHCI or MSM/RST + PCH/SoC + RAID (AHCI and RAID cannot be used interchangeably due to different Hardware IDs between CC_0106 and CC_0104).
# WARNING!
This project is still in the Unstable phase. However, if this driver works with more than 30 different Intel(R) SATA drivers (i.e., resolves and closes more than 30 issues in the Issues tab), then this project will be pushed to Stable and considered to work well across multiple devices.

Any issues related to this driver, please report them in the Issue tab like this:
- HardwareIDs: VEN_8086&&DEV_(your DEV ID)&&CC_(0106 is AHCI, 0104 is RAID)
- Issues: Describe the error you are experiencing.
- Additional description (Optional): The way you add drivers, the way you create a bootable installer, etc...
# Usages
To add driver, use 
