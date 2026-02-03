**Chapter Title:**
Chapter 8 Chip Boot Control

**Body Text:**

- GPIO45 = 0, VDD_SPI pin is powered directly from VDD3P3_RTC via resistor RSP1. Typically this voltage is 3.3 V. For more information, see Figure: ESP32-S3 Power Scheme in ESP32-S3 Datasheet.
  
- GPIO45 = 1, VDD_SPI pin is powered from internal 1.8 V LDO.

This functionality can be overridden by setting eFuse bit EFUSE_VDD_SPI_FO to 1, in which case the EFUSE_VDD_SPI_TIEH determines the VDD_SPI voltage:

- EFUSE_VDD_SPI_TIEH = 0, VDD_SPI connects to 1.8 V LDO.
  
- EFUSE_VDD_SPI_TIEH = 1, VDD_SPI connects to VDD3P3_RTC.

**Subheading:**
8.5 JTAG Signal Source Control

**Body Text:**

GPIO3 controls the source of JTAG signals during the early boot process. This GPIO is used together with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_STRAP_JTAG_SEL, see Table 8.5-1.

**Table Title:** 
Table 8.5-1. JTAG Signal Source Control

| eFuse | eFuse | eFuse | GPIO3 | Signal Source |
|-------|-------|-------|-------|---------------|
|       | 2^2   | 3^3   | Signal    | Description                                          |
| 0     | O     | x     | JTAG signals come from USB Serial/JTAG Controller. |
| 1     |      |      |         |                                                      |
| 0     | 1     |       | JTAG signals come from corresponding pins^d.      |
| 1     | 0     | x     | JTAG signals come from corresponding pins^4.      |
| 1     | 1     | x     | JTAG is disabled.                                   |

**Footnotes:**
1 eFuse 1: EFUSE_DIS_PAD_JTAG
2 eFuse 2: EFUSE_DIS_USB_JTAG
3 eFuse 3: EFUSE_STRAP_JTAG_SEL

4 JTAG pins: MTDI, MTCK, MTMS, and MTDO.

**Footer Information:** 
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)