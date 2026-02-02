Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Table:
- Name | Description | Address | Access
- RTCIO_PAD_DAC1_REG | DAC1 configuration register | 0x3FF48484 | R/W
- RTCIO_PAD_DAC2_REG | DAC2 configuration register | 0x3FF48488 | R/W
- RTCIO_XTAL_32K_PAD_REG | 32KHz crystal pins configuration register | 0x3FF4848C | R/W
- RTCIO TOUCH_CFG_REG | Touch sensor configuration register | 0x3FF48490 | R/W
- RTCIO_TOUCH_PADO_REG | Touch pin configuration register | 0x3FF48494 | R/W
- ...
- RTCIO_TOUCH_PAD9_REG | Touch pin configuration register | 0x3FF484B8 | R/W
- RTCIO_EXT_WAKEUPO_REG | External wake up configuration register | 0x3FF484BC | R/W
- RTCIO_XTL_EXT_CTR_REG | Crystal power down enable GPIO source | 0x3FF484C0 | R/W
- RTCIO_SAR_I2C_IO_REG | RTC I2C pin selection | 0x3FF484C4 | R/W

Subtitle: 6.13 Registers

Subsection Title: 6.13.1 GPIO Matrix Registers

Body Text:
The addresses in parenthesis besides register names are the register addresses relative to the GPIO base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 6.12.1 GPIO Matrix Register Summary.

Table (with binary representation):
- Register 6.1. GPIO_OUT_REG (0x0004)
  - Binary: [Binary pattern with Xs indicating unspecified bits]
  - Description: GPIO OUT output value.
  - Access Type: R/W

- Register 6.2. GPIO_OUT_WITS_REG (0x0008)
  - Binary: [Binary pattern with Xs indicating unspecified bits]
  - Description: GPIO OUT set register for every bit that is 1 in the value written here, the corresponding bit in GPIO_OUT_REG will be set.
  - Access Type: WO

- Register 6.3. GPIO_OUT_WITC_REG (0x000c)
  - Binary: [Binary pattern with Xs indicating unspecified bits]
  - Description: GPIO OUT clear register for every bit that is 1 in the value written here, the corresponding bit in GPIO_OUT_REG will be cleared.
  - Access Type: WO

Footer:
Espressif Systems
Page Number: 138
Document Version: ESP32 TRM (Version 5.6)
Link Texts: Submit Documentation Feedback