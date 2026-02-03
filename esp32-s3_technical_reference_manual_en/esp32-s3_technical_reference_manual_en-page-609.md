**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.27. RTC_CNTL_RTC_SDIO_CONF_REG (0x007C)

**Binary Register Diagram and Description for RTC_CNTL_SDIO_REG_PD_EN:**
- **Description:** Set this bit to power down SDIO_REG when chip is in light sleep and deep sleep.
- This field only valid when RTC_CNTL_SDIO FORCE = 0. (R/W)
- Binary representation of the register with bits labeled from most significant bit at position [31] through least significant bit.

**Binary Register Diagram and Description for RTC_CNTL_SDIO_FORCE:**
- **Description:** Set this bit to allow software t1: use SW option to control SDIO_REG.
- Clear this bit to allow the state machine to control SDIO_REG. (R/W)
- Binary representation of the register with bits labeled from most significant bit at position [31] through least significant bit.

**Binary Register Diagram and Description for RTC_CNTL_SDIO_TIEH:**
- **Description:** Configure the SDIO_TIEH via software.
- This field is only valid when RTC_CNTL_SDIO FORCE = 1. (R/W)
- Binary representation of the register with bits labeled from most significant bit at position [31] through least significant bit.

**Binary Register Diagram and Description for RTC_CNTL_SDIO_REG:**
- **Description:** Set this bit to power on flash regulator.
- (R/W)

---

**Section Header:**
Register 10.28. RTC_CNTL_RTC_REG (0x0084)

**Binary Register Diagram with Labels:**
- Various labels such as RTC_CNTL_RTCReg, RTC_CNTL_DBOOST_PD, RTC_CNTL_SOCK_DCAP, etc.

**Binary Register Description for RTC_CNTL_DIG_REG_CAL_EN:**
- **Description:** Set this bit to enable calibration for the digital regulator.
- (R/W)

**Binary Register Description for RTC_CNTL_SCK_DCAP:**
- Configures the frequency of the RTC clocks. (R/W)

**Binary Register Description for RTC_CNTL_RTC_DBOOST FORCE_PD:**
- Set this bit to FPD the RTC_DBOOST. (R/W)

**Binary Register Description for RTC_CNTL_RTC_DBOOST FORCE_PU:**
- Set this bit to FPU the RTC_DBOOST. (R/W)

**Binary Register Description for RTC_CNTL_RTC_REGULATOR FORCE_PD:**
- Set this bit to FPD the RTC_REG, which means decreasing its voltage to 0.8 V or lower.
- This field is only valid when RTC_CNTL_RTCReg FORCE_PU = 1.

**Binary Register Description for RTC_CNTL_RTC_REGULATOR FORCE_PU:**
- Set this bit to FPU the RTC_REG. (R/W)

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)