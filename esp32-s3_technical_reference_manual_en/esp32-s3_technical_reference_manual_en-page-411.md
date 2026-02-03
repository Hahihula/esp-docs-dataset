**Table Title:**
Table 5.3-1. Parameters in eFuse BLOCK0

| Parameters | Bit Width | Accessible by Hardware | Programming-Protection Description |
|------------|-----------|------------------------|---------------------------------------|
| EFUSE_WR_DIS | - | Y | Represents whether writing of individual eFuses is disabled. |
| EFUSE_RD_DIS | 7 | Y | Represents whether users' reading from BLOCK4 ~ 10 is disabled. |
| EFUSE_DIS_ICACHE | 1 | Y | Represents whether iCache is disabled. |
| EFUSE_DIS_DCACHE | 1 | Y | Represents whether dCache is disabled. |
| EFUSE_DIS_DOWNLOAD_ICACHE | - | N/A | Represents whether iCache is disabled in Download mode. |
| EFUSE_DIS_DOWNLOAD_DCACHE | 2 | Y | Represents whether dCache is disabled in Download mode. |
| EFUSE_DIS FORCE DOWNLOAD | 1 | Y | Represents whether the function that forces chip into download mode is disabled. |
| EFUSE_DIS_USB_OTG | - | N/A | Represents whether USB OTG function is disabled. |
| EFUSE_DIS_TWAI | 2 | Y | Represents whether TWAI Controller is disable. |
| EFUSE_DIS_APP_CPU | 1 | Y | Represents whether app CPU is disable. |
| EFUSE_SOFT_DIS JTAG | 3 | N/A | Represents whether JTAG with soft-disable is disabled. |
| EFUSE_DIS_PAD JTAG | - | N/A | Represents whether pad JTAG is permanently disabled. |
| EFUSE_DIS DOWNLOAD MANUAL ENCRYPT | 1 | Y | Represents whether flash encryption is disable in Download boot modes. |
| EFUSE_USB_EXCHG_PINS | 30 | Y | Represents whether USB D+ and D- pins are swapped. |
| EFUSE_EXT_PHY_ENABLE | - | N/A | Represents whether external USB PHY is disabled. |
| EFUSE_VDD_SPI_XPD | 1 | Y | Represents whether Flash Voltage Regulator powered up. |
| EFUSE_VDD_SPI_TIEH | 3 | Y | Represents whether Flash Voltage Regulator output short connected to VDD3P3_RTC_IO. |
| EFUSE_VDD_SPI FORCE | - | N/A | Represents whether force using EFUSE_VDD_SPI_XPD and EFUSE_VDD_SPI_TIEH to configure flash voltage LDO. |

**Footer:**
Cont’d on next page

**Side Note:** 
- "EFUSE" is a term used in the context of eFuse programming, which refers to specific fuses or configuration settings within an integrated circuit.
- The table provides detailed information about various parameters related to hardware protection and functionality control via these EFUSE blocks.