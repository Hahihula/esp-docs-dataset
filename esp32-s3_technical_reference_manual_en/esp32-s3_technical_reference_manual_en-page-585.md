**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Table of Contents with Descriptions, Addresses, and Access Types**

- **Name:** RTC_CNTL_RTC_WDTWPROTECT_REG  
  **Description:** RTC watchdog write protection register  
  **Address:** 0x00B0  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_SWD_CONF_REG  
  **Description:** Super watchdog configuration register  
  **Address:** 0x00B4  
  **Access:** varies

- **Name:** RTC_CNTL_RTC_SWD_WPROTECT_REG  
  **Description:** Super watchdog write protection configuration register  
  **Address:** 0x00B8  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_SW_CPU_STALL_REG  
  **Description:** CPU stall configuration register  
  **Address:** 0x00BC  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_LOW_POWER_ST_REG  
  **Description:** Indicates the RTC is ready to be triggered by any wakeup source  
  **Address:** 0x00D0  
  **Access:** RO

- **Name:** RTC_CNTL_RTC_PAD_HOLD_REG  
  **Description:** Configures the hold options for RTC GPIOs  
  **Address:** 0x00D8  
  **Access:** R/W

- **Name:** RTC_CNTL_DIG_PAD_HOLD_REG  
  **Description:** Configures the hold option for digital GPIOs  
  **Address:** 0x00DC  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_EXT_WAKEUP_REG  
  **Description:** EXT1 wakeup configuration register  
  **Address:** 0x00E0  
  **Access:** varies

- **Name:** RTC_CNTL_RTC_BROWN_OUT_REG  
  **Description:** Brownout configuration register  
  **Address:** 0x00E8  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_XTAL32K_CLK_FACTOR_REG  
  **Description:** Configures the divider factor for the backup clock of 32 kHz crystal oscillator  
  **Address:** 0x00F4  
  **Access:** varies

- **Name:** RTC_CNTL_RTC_XTAL32K_CONF_REG  
  **Description:** 32 kHz crystal oscillator configuration register  
  **Address:** 0x00F8  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_USB_CONF_REG  
  **Description:** USB configuration register  
  **Address:** 0x0120  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_OPTION1_REG  
  **Description:** RTC option register  
  **Address:** 0x012C  
  **Access:** varies

- **Name:** RTC_CNTL_INT_ENA_RTC_WITS_REG  
  **Description:** RTC interrupt enabling register (WITS)  
  **Address:** 0x0138  
  **Access:** WO

- **Name:** RTC_CNTL_INT_ENA_RTC_WITC_REG  
  **Description:** RTC interrupt clear register (WITC)  
  **Address:** 0x013C  
  **Access:** WO

- **Name:** RTC_CNTL_RETENTION_CTRL_REG  
  **Description:** Retention Configuration Register  
  **Address:** 0x0140  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_FIB_SEL_REG  
  **Description:** Brownout detector configuration register  
  **Address:** 0x0148  
  **Access:** WO

**Status Registers**

- **Name:** RTC_CNTL_RTC_TIME_LOWOReg  
  **Description:** Stores the lower 32 bits of RTC timer 0  
  **Address:** 0x0010  
  **Access:** RO

- **Name:** RTC_CNTL_RTC_TIME_HIGHOReg  
  **Description:** Stores the higher 16 bits of RTC timer 0  
  **Address:** 0x0014  
  **Access:** R/W

- **Name:** RTC_CNTL_RESET_STATE_REG  
  **Description:** Indicates the CPU reset source  
  **Address:** 0x0038  
  **Access:** varies

- **Name:** RTC_CNTL STOREOReg  
  **Description:** Retention register  
  **Address:** 0x0050  
  **Access:** R/W

- **Name:** RTC_CNTL_STORE1Reg  
  **Description:** Retention register  
  **Address:** 0x0054  
  **Access:** varies

- **Name:** RTC_CNTL_STORE2Reg  
  **Description:** Retention register  
  **Address:** 0x0058  
  **Access:** R/W

- **Name:** RTC_CNTL STORE3Reg  
  **Description:** Retention register  
  **Address:** 0x005C  
  **Access:** varies

- **Name:** RTC_CNTL_STORE4Reg  
  **Description:** Retention register 4  
  **Address:** 0x0060  
  **Access:** R/W

- **Name:** RTC_CNTL STORE5Reg  
  **Description:** Retention register 5  
  **Address:** 0x0064  
  **Access:** varies

- **Name:** RTC_CNTL_STORE6Reg  
  **Description:** Retention register 6  
  **Address:** 0x0068  
  **Access:** R/W

- **Name:** RTC_CNTL_STORE7Reg  
  **Description:** Retention register 7  
  **Address:** 0x006C  
  **Access:** varies

- **Name:** RTC_CNTL_RTC_EXT_WAKEUP1_STATUS_REG  
  **Description:** EXT1 wakeup source register  
  **Address:** 0x00E4  
  **Access:** RO

- **Name:** RTC_CNTL_RTC_TIME_LOW1Reg  
  **Description:** Stores the lower 32 bits of RTC timer 1  
  **Address:** 0x00EC  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_TIME_HIGH1Reg  
  **Description:** Stores the higher 16 bits of RTC timer 1  
  **Address:** 0x00F0  
  **Access:** RO

- **Name:** RTC_CNTL_RTC_SLP_REJECT_CAUSE_REG  
  **Description:** Stores the reject-to-sleep cause  
  **Address:** 0x0128  
  **Access:** R/W

- **Name:** RTC_CNTL_RTC_SLP_WAKEUP_CAUSE_REG  
  **Description:** Stores the sleep-to-wakeup cause  
  **Address:** 0x0130  
  **Access:** RO

**Interrupt Registers**

- **Name:** RTC_CNTL_INT_ENA_RTC_REG  
  **Description:** RTC interrupt enabling register  
  **Address:** 0x0040  
  **Access:** R/W

**Footer:**
Espressif Systems
Page number: 585
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback