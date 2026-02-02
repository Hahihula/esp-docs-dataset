**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**GoBack Link:** GoBack

---

### Table of Contents:

- **Timer O configuration and control registers**
  - TIMGn_TOCONFIG_REG
    - Description: Timer O configuration register
    - TIMGO, TIMG1, ACC Values:
      - TIMGO: 0x3FF5F000
      - TIMG1: 0x3FF60000 (R/W)
- **TIMGn_TLO_REG**
  - Description: Timer O current value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F004
    - TIMG1: 0x3FF60004 (RO)
- **TIMGn_TOHI_REG**
  - Description: Timer O current value, high 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F008
    - TIMG1: 0x3FF60008 (RO)
- **TIMGn_TOUPDATE_REG**
  - Description: Write to copy current timer value to TIMGn_TLO/THI_REG
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F00C
    - TIMG1: 0x3FF6000C (WO)
- **TIMGn_TOALARMLO_REG**
  - Description: Timer O alarm value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F010
    - TIMG1: 0x3FF60010 (R/W)
- **TIMGn_TOALARMHI_REG**
  - Description: Timer O alarm value, high bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F014
    - TIMG1: 0x3FF60014 (R/W)
- **TIMGn_TOLOADLO_REG**
  - Description: Timer O reload value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F018
    - TIMG1: 0x3FF60018 (R/W)
- **TIMGn_TOLOADHI_REG**
  - Description: Timer O reload value, high 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F01C
    - TIMG1: 0x3FF6001C (R/W)
- **TIMGn_TOLOAD_REG**
  - Description: Write to reload timer from TIMGn_TO(LOADLOADHI)_REG
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F020
    - TIMG1: 0x3FF60020 (WO)

---

### Timer 1 configuration and control registers

- **TIMGn_T1CONFIG_REG**
  - Description: Timer 1 configuration register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F024
    - TIMG1: 0x3FF60024 (R/W)
- **TIMGn_TLO_REG**
  - Description: Timer current value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F028
    - TIMG1: 0x3FF60028 (RO)
- **TIMGn_THI_REG**
  - Description: Timer current value, high 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F02C
    - TIMG1: 0x3FF6002C (RO)
- **TIMGn_TUPDATE_REG**
  - Description: Write to copy current timer value to TIMGn_T(LO/HI)_REG
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F030
    - TIMG1: 0x3FF60030 (WO)
- **TIMGn_T1ALARMLO_REG**
  - Description: Timer 1 alarm value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F034
    - TIMG1: 0x3FF60034 (R/W)
- **TIMGn_T1ALARMHI_REG**
  - Description: Timer 1 alarm value, high bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F038
    - TIMG1: 0x3FF60038 (R/W)
- **TIMGn_T1LOADLO_REG**
  - Description: Timer 1 reload value, low 32 bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F03C
    - TIMG1: 0x3FF6003C (R/W)
- **TIMGn_T1LOADHI_REG**
  - Description: Timer 1 reload value, high bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F040
    - TIMG1: 0x3FF60040 (R/W)
- **TIMGn_T1LOAD_REG**
  - Description: Write to reload timer from TIMGn_T(LOADLOADHI)_REG
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F044
    - TIMG1: 0x3FF60044 (WO)

---

### System watchdog timer configuration and control registers

- **TIMGn_WDTCONFIG0_REG**
  - Description: Watchdog timer configuration register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F048
    - TIMG1: 0x3FF60048 (R/W)
- **TIMGn_WDTCONFIG1_REG**
  - Description: Watchdog timer prescaler register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F04C
    - TIMG1: 0x3FF6004C (R/W)
- **TIMGn_WDTCONFIG2_REG**
  - Description: Watchdog timer stage 0 timeout value
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F050
    - TIMG1: 0x3FF60050 (R/W)
- **TIMGn_WDTCONFIG3_REG**
  - Description: Watchdog timer stage 1 timeout value
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F054
    - TIMG1: 0x3FF60054 (R/W)
- **TIMGn_WDTCONFIG4_REG**
  - Description: Watchdog timer stage 2 timeout value
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F058
    - TIMG1: 0x3FF60058 (R/W)
- **TIMGn_WDTCONFIG5_REG**
  - Description: Watchdog timer stage 3 timeout value
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F05C
    - TIMG1: 0x3FF6005C (R/W)
- **TIMGn_WDTFEED_REG**
  - Description: Write to feed the watchdog timer
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F060
    - TIMG1: 0x3FF60060 (WO)
- **TIMGn_WDTWPROTECT_REG**
  - Description: Watchdog write protect register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F064
    - TIMG1: 0x3FF60064 (R/W)

---

### Configuration and Control Register for RTC CALI

- **TIMGn_RTCCALCFG_REG**
  - Description: RTC calibration configuration register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F068
    - TIMG1: 0x3FF60068 (varies)
- **TIMGn_RTCCALCFG1_REG**
  - Description: RTC calibration configuration register
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F06C
    - TIMG1: 0x3FF6006C (RO)

---

### Interrupt registers

- **TIMGn_INT_ENA_REG**
  - Description: Interrupt enable bits
  - TIMGO, TIMG1, ACC Values:
    - TIMGO: 0x3FF5F098
    - TIMG1: 0x3FF60098 (R/W)

---

**Footer Information:** 
- Page Number: 225
- Document Version: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Link for Feedback Submission:** Submit Documentation Feedback