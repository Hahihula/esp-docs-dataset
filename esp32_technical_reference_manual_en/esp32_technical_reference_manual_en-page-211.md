**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Header:**
Register 9.25. RTC_CNTL_SDIO_CONF_REG (0x074)

**Binary Register Table Description:**
- The table shows a binary register with bits labeled from '31' to '0'.
- Each bit is associated with specific functions related to SDIO control.

**Text Descriptions and Comments for the Binary Bits:**

- **RTC_CNTL_XPD_SDIO_VREG**: SW option for XPD_SDIO_VREG; active only when `reg_rtc_cntl_sdio_force == 1. (R/W)`
  
- **RTC_CNTL_DREFH_SDIO**: SW option for DREFH_SDIO; active only when `reg_rtc_cntl_sdio_force == 1. (R/W)`

- **RTC_CNTL_DREFM_SDIO**: SW option for DREFM_SDIO; active only when `reg_rtc_cntl_sdio_force == 1. (R/W)`

- **RTC_CNTL_DREFL_SDIO**: SW option for DREFL_SDIO; active only when `reg_rtc_cntl_sdio_force == 1. (R/W)`

- **RTC_CNTL_REG1P8 READY**: Read-only register for REG1P8READY. (RO)

- **RTC_CNTL_SDIO_TIEH**: SW option for SDIO_TIEH; active only when `reg_rtc_cntl_sdio_force == 1. (R/W)`

- **RTC_CNTL_SDIOFORCE**: 
  - `1`: use SW option to control SDIO_VREG
  - `0`: use state machine to control SDIO_VREG. (RO)

- **RTC_CNTL_SDIO_VREG_PD_EN**: Power down SDIO_VREG in sleep; active only when `reg_rtc_cntl_sdio_force == 0. (R/W)`

**Footer:**
Espressif Systems
211 ESP32 TRM (Version 5.6)
Submit Documentation Feedback