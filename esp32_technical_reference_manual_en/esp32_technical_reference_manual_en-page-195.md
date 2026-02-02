**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Table of Registers and Descriptions**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Internal power management registers** | Power-up/down configuration | 0x3FF48030 | R/W |
| RTC_CNTL_ANA_CONF_REG | Internal power distribution and control | 0x3FF4807C | R/W |
| RTC_CNTL_VREG_REG | RTC domain power management | 0x3FF48080 | R/W |
| RTC_CNTL_PWC_REG | Digital domain power management | 0x3FF48084 | R/W |
| RTC_CNTL_DIG_PWC_REG | Digital domain isolation control | 0x3FF48088 | RO |
| **RTC watchdog configuration and control registers** | WDT Configuration register O | 0x3FF4808C | R/W |
| RTC_CNTL_WDTCONFIGO_REG | WDT Configuration register 1 | 0x3FF48090 | R/W |
| RTC_CNTL_WDTCONFIG2_REG | WDT Configuration register 2 | 0x3FF48094 | R/W |
| RTC_CNTL_WDTCONFIG3_REG | WDT Configuration register 3 | 0x3FF48098 | R/W |
| RTC_CNTL_WDTCONFIG4_REG | WDT Configuration register 4 | 0x3FF4809C | R/W |
| RTC_CNTL_WDTFEED_REG | Watchdog feed register | 0x3FF480A0 | WO |
| RTC_CNTL_WDTWPROTECT_REG | Watchdog write protect register | 0x3FF480A4 | R/W |

**Miscellaneous RTC configuration registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_CNTL_EXT_XTL_CONF_REG | XTAL control by external pads | 0x3FF4805C | R/W |
| RTC_CNTL_SLP_REJECT_CONF_REG | Reject cause and enable control | 0x3FF48064 | R/W |
| RTC_CNTL_CPU_PERIOD_CONF_REG | CPU period select | 0x3FF48068 | R/W |
| RTC_CNTL_CLK_CONF_REG | Configuration of RTC clocks | 0x3FF48070 | R/W |
| RTC_CNTL_SDIO_CONF_REG | SDIO configuration | 0x3FF48074 | R/W |
| RTC_CNTL_SW_CPU_STALL_REG | Stall of CPUs | 0x3FF480AC | R/W |
| RTC_CNTL_LOW_POWER_ST_REG | RTC state register | 0x3FF480C0 | RO |
| RTC_CNTL_HOLD FORCE_REG | RTC pad hold register | 0x3FF480C8 | R/W |
| RTC_CNTL_BROWN_OUT_REG | Brownout management | 0x3FF480D4 | R/W |

**Section Title:**
9.5 Registers

**Body Text:**
The addresses in parenthesis besides register names are the register addresses relative to the Low-power Management (RTC) base address provided in Table 3-36 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 9.4 Register Summary.

**Footer Information:**
Espressif Systems  
195  
ESP32 TRM (Version 5.6)

**Link Texts:**
GoBack
Submit Documentation Feedback