

```markdown
| Name | Description | Address | Access |
|:-------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------|:-------|
| **TO Control and configuration registers** |  |  |  |
| TIMG_TOCONFIG_REG | Timer 0 configuration register | 0x0000 | varies |
| TIMG_TOLO_REG | Timer 0 current value, low 32 bits | 0x0004 | RO |
| TIMG_TOHI_REG | Timer 0 current value, high 22 bits | 0x0008 | RO |
| TIMG_TOUPDATE_REG | Write to copy current timer value to TIMG_TOLO_REG or TIMG_TOHI_REG | 0x000C | R/W/SC |
| TIMG_TOALARMLO_REG | Timer 0 alarm value, low 32 bits | 0x0010 | R/W |
| TIMG_TOALARMHI_REG | Timer 0 alarm value, high 22 bits | 0x0014 | R/W |
| TIMG_TOLOADLO_REG | Timer 0 reload value, low 32 bits | 0x0018 | R/W |
| TIMG_TOLOADHI_REG | Timer 0 reload value, high 22 bits | 0x001C | R/W |
| TIMG_TOLOAD_REG | Write to reload timer from TIMG_TOLOADLO_REG or TIMG_TOLOADHI_REG | 0x0020 | WT |
| **T1 Control and configuration registers** |  |  |  |
| TIMG_T1CONFIG_REG | Timer 1 configuration register | 0x0024 | varies |
| TIMG_T1LO_REG | Timer 1 current value, low 32 bits | 0x0028 | RO |
| TIMG_T1HI_REG | Timer 1 current value, high 22 bits | 0x002C | RO |
| TIMG_T1UPDATE_REG | Write to copy current timer value to TIMG_T1LO_REG or TIMG_T1HI_REG | 0x0030 | R/W/SC |
| TIMG_T1ALARMLO_REG | Timer 1 alarm value, low 32 bits | 0x0034 | R/W |
| TIMG_T1ALARMHI_REG | Timer 1 alarm value, high 22 bits | 0x0038 | R/W |
| TIMG_T1LOADLO_REG | Timer 1 reload value, low 32 bits | 0x003C | R/W |
| TIMG_T1LOADHI_REG | Timer 1 reload value, high 22 bits | 0x0040 | R/W |
| TIMG_T1LOAD_REG | Write to reload timer from TIMG_T1LOADLO_REG or TIMG_T1LOADHI_REG | 0x0044 | WT |
| **WDT Control and configuration registers** |  |  |  |
| TIMG_WDTCONFIG0_REG | Watchdog timer configuration register | 0x0048 | varies |
| TIMG_WDTCONFIG1_REG | Watchdog timer prescaler register | 0x004C | varies |
| TIMG_WDTCONFIG2_REG | Watchdog timer stage 0 timeout value | 0x0050 | R/W |
| TIMG_WDTCONFIG3_REG | Watchdog timer stage 1 timeout value | 0x0054 | R/W |
| TIMG_WDTCONFIG4_REG | Watchdog timer stage 2 timeout value | 0x0058 | R/W |
| TIMG_WDTCONFIG5_REG | Watchdog timer stage 3 timeout value | 0x005C | R/W |
| TIMG_WDTFEED_REG | Write to feed the watchdog timer | 0x0060 | WT |
| TIMG_WDTWPROTECT_REG | Watchdog write protect register | 0x0064 | R/W |
| **RTC CALI Control and configuration registers** |  |  |  |
| TIMG_RTCCALICFG_REG | RTC calibration configure register | 0x0068 | varies |
| TIMG_RTCCALICFG1_REG | RTC calibration configure register 1 | 0x006C | RO |
| TIMG_RTCCALICFG2_REG | RTC calibration configure register 2 | 0x0080 | varies |
```