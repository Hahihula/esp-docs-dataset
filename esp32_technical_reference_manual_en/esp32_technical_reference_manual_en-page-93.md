**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Table of System Parameters with Protection Status**

| Name                   | Bit width | Program       | Software-Read | Description                                                                                     |
|------------------------|-----------|---------------|---------------|--------------------------------------------------------------------------------------------------|
| BLOCK2\*               | 256/192/128 | -Protection by efuse_wr_disable | -Protection by efuse_rd_disable | key for Secure Boot |
| BLOCK3\*               | 256/192/128 | 8             | 1             | key for user purposes |
| disable_app_cpu        |           | 3             | -             | disables APP CPU                                   |
| disable_bt             |           | 3             | -             | disables Bluetooth                                |
| pkg_version            | 4         | 3             | -             | packaging version                                 |
| disable_cache          | 1         | 3             | -             | disables cache                                    |
| CK8M Frequency         | 8         | 4             | -             | RC_FAST_CLK frequency                             |
| vol_level_hp_inv       |           |               | -             | stores the voltage level for CPU to run at 240 MHz, or for flash/PSRAM to run at 80 MHz     |
| dig_vol_l6             | 1         | 3             | -             | stores the difference between the digital regulator voltage at level 6 and 1.2 V           |
| uart_download_dis      |           |               | -             | permanently disables Download Boot mode when set to Valid only for ESP32 ECO V3.              |

**Section Title:**
5.3.1 System Parameter efuse_wr_disable

**Body Text:**
The system parameter efuse_wr_disable determines whether all of the system parameters are write-protected. Since efuse_wr_disable is a system parameter as well, it also determines whether itself is write-protected.

If a system parameter is not write-protected, its unprogrammed bits can be programmed from 0 to 1. The bits previously programmed to 1 will remain 1. When a system parameter is write-protected, none of its bits can be programmed: The unprogrammed bits will always remain 0 and the programmed bits will always remain 1.

The write-protection status of each system parameter corresponds to a bit in efuse_wr_disable. When the corresponding bit is set to 0, the system parameter is not write-protected. When the corresponding bit is set to 1, the system parameter is write-protected. If a system parameter is already write-protected, it will remain write-protected.

The column entitled “Program-Protection by efuse_wr_disable” in Table 5.3-1 lists the corresponding bits that determine the write-protection status of each system parameter.

**Section Title:**
5.3.1.2 System Parameter efuse_rd_disable

**Body Text:**
Of the 33 system parameters, 27 are not constrained by software-read-protection. These are marked by “-” in the column entitled “Software-Read-Protection by efuse_rd_disable” in Table 5.3-1. Those system parameters, some of which are used by software and hardware modules at the same time, can be read by software via the eFuse Controller at any time.

When not software-read-protected, the other six system parameters can both be read by software and used by hardware modules. When they are software-read-protected, they can only be used by the hardware modules.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 93  
**Document Version:** ESP32 TRM (Version 5.6)