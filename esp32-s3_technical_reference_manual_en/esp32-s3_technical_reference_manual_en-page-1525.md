**Related Documentation and Resources**

---

### Cont'd from previous page

#### Release notes for v1.5 (2024-04-18)

Updated the following chapters:

- **Chapter 3 GDMA Controller (GDMA):**
  - Updated descriptions of `suc_eof` and the EOF flag.

- **Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX):**
  - Updated the drive strength of GPIO17 and GPIO18.
  
- **Chapter 22 Digital Signature (DS) and Chapter 8 Chip Boot Control:**
  - Fixed some typos.

- **Chapter 26 UART Controller (UART):**
  - Updated descriptions about clearing the wake_up signal.

- **Chapter 35 LED PWM Controller (LEDC):**
  - Updated the lowest resolution in Table 35.3-1.

---

#### Release notes for v1.4 (2024-01-30)

Updated the following chapters:

- **Chapter 1 Processor Instruction Extensions (PIE):**
  - Added data exchange instruction list to Section 1.6.
  - Added descriptions for LD.QR, ST.QR, and MV.IR; fixed two typos.

- **Chapter 5 eFuse Controller:**
  - Updated the description of `EFUSE_PIN_POWER_SELECTION`.

- **Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX):**
  - Removed Debug Assist from Table 4.3-3.
  - Updated the description in Section 6.9.

- **Chapter 8 Chip Boot Control:**
  - Added SPI Download Boot mode and renamed `Download Boot mode` to Joint Download mode; fixed typo for section reference (Section 8.2).
  - Provided more details about how `FUSE_DISFORCE_DOWNLOAD` and `EFUSE_DIS_DISABLE_MODE` control chip boot mode.

- **Chapter 9 Interrupt Matrix (INTERRUPT):**
  - Removed the AS-SIST_DEBUG_INTR interrupt source.
  
- **Chapter 10 Low-Power Management (RTC_CNTL):**
  - Updated description of register `RTC_CNTL_WDT_WKEY`.

- **Chapter 12 Timer Group (TIMG):**
  - Updated the description of `TIMG_WDT_CLK PRESCALE`.

- **Chapter 15 Permission Control (PMS):**
  - Removed descriptions for access configuration in Debug Assert.

- **Chapter 17 System Registers (SYSTEM):**
  - Improved description of `SYS_TEM_CONTROL_1_MESSAGE`.

- **Chapter 26 UART Controller (UART):**
  - Updated the number of rising edges required to generate wake_up signal.
  
- **Chapter 27 I2C Controller (I2C):**
  - Updated descriptions for `I2CComdo_REG`, `I2C_SDA FORCE_OUT`, and `I2C_SCL FORCE_OUT`.

- **Chapter 36 Motor Control PWM (MCPWM):**
  - Added one note about Count-Up/Down mode configuration.

Added Section `Interrupt Configuration Registers`.