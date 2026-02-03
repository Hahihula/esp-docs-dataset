**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Title:**
12.4 Register Summary

**Body Text:**
The addresses in this section are relative to Timer Group base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Subsection Title (Timer O configuration and control registers):**

| Name | Description | Address | Access |
| --- | --- | --- | --- |
| TIMG_TOCONFIG_REG | Timer 0 configuration register | 0x0000 | varies |
| TIMG_TOLO_REG | Timer 0 current value, low 32 bits | 0x0004 | RO |
| TIMG_TOHI_REG | Timer 0 current value, high 22 bits | 0x0008 | RO |
| TIMGTOUPDATE_REG | Write to copy current timer value to TIMG_TOLO_REG or TIMG_TOHI_REG | 0x000C | R/W/SC |
| TIMG_TOALARMLO_REG | Timer 0 alarm value, low 32 bits | 0x0010 | R/W |
| TIMG_TOALARMHI_REG | Timer 0 alarm value, high bits | 0x0014 | R/W |
| TIMG_TOLOADLO_REG | Timer 0 reload value, low 32 bits | 0x0018 | R/W |
| TIMG_TOLOADHI_REG | Timer 0 reload value, high 22 bits | 0x001C | R/W |
| TIMG_TOLOAD_REG | Write to reload timer from TIMG_TOLADLO_REG or TIMG_TOLADHI_REG | 0x0020 | WT |

**Subsection Title (Timer 1 configuration and control registers):**

| Name | Description | Address | Access |
| --- | --- | --- | --- |
| TIMG_T1CONFIG_REG | Timer 1 configuration register | varies | RO |
| TIMG_T1LO_REG | Timer 1 current value, low 32 bits | 0x0028 | R/W |
| TIMG_T1HI_REG | Timer 1 current value, high 22 bits | 0x002C | RO |
| TIMG_T1UPDATE_REG | Write to copy current timer value to TIMG_T1LO_REG or TIMG_T1HI_REG | 0x0030 | R/W/SC |
| TIMG_T1ALARMLO_REG | Timer 1 alarm value, low 32 bits | 0x0034 | R/W |
| TIMG_T1ALARMHI_REG | Timer 1 alarm value, high bits | 0x0038 | R/W |
| TIMG_T1LOADLO_REG | Timer 1 reload value, low 32 bits | 0x003C | R/W |
| TIMG_T1LOADHI_REG | Timer 1 reload value, high 22 bits | 0x0040 | R/W |
| TIMG_T1LOAD_REG | Write to reload timer from TIMG_T1LOADLO_REG or TIMG_T1LOADHI_REG | varies | WT |

**Subsection Title (Configuration and control registers for WDT):**

| Name | Description | Address | Access |
| --- | --- | --- | --- |
| TIMG_WDTCONFIGO_REG | Watchdog timer configuration register | 0x0048 | R/W |
| TIMG_WDTCONFIG1_REG | Watchdog timer prescaler register | 0x004C | R/W |
| TIMG_WDTCONFIG2_REG | Watchdog timer stage 0 timeout value | 0x0050 | R/W |
| TIMG_WDTCONFIG3_REG | Watchdog timer stage 1 timeout value | 0x0054 | R/W |
| TIMG_WDTCONFIG4_REG | Watchdog timer stage 2 timeout value | 0x0058 | R/W |
| TIMG_WDTCONFIG5_REG | Watchdog timer stage 3 timeout value | 0x005C | R/W |
| TIMG_WDTFEED_REG | Write to feed the watchdog timer | varies | WT |
| TIMG_WDTPROTECT_REG | Watchdog write protect register | 0x0064 | R/W |

**Subsection Title (Configuration and control registers for RTC frequency calculation):**

(Note: The text under this subsection is not fully visible in the image provided.)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)