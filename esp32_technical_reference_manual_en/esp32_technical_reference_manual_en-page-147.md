**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Back Link:**
GoBack

**Register Information:**
- **Register Name:** GPIO_FUNCn_OUT_SEL_CFG_REG
- **Address Range:** n = 0-19, 21-23, 25-27, 32-33 (0x530+0x4*n)
- **Bit Description Table:**
  - Bit Positions:
    - 31 to 8 are reserved.
    - Bits from position n down to bit s select the output value and enable.

**Field Descriptions in Register:**

1. **GPIO_FUNCn_OEN_INV SEL:** 
   - **Description:** Invert the output enable signal; 0: do not invert the output enable signal (R/W)
   - **Example Description:** [GPIO_FUNCn_OEN_SEL] Force the output enable signal to be sourced from bit n of GPIO_ENABLE_REG; 0: use output enable signal from peripheral. (R/W)

2. **GPIO_FUNCn_OUT INV SEL**
   - **Description:** Invert the output value; 0: do not invert the output value.
   - **Example Description:** [GPIO_FUNCn_OUT_SEL] Selection control for GPIO output n. A value of s selects bit n of GPIO_OUT_REG/GPIO_OUT1_REG and GPIO_ENABLE_REG/GPIO ENABLE1_REG as the output value and output enable.

**Section Title in Document:**
6.13.2 IO MUX Registers

**Footer Information:**
- **Company:** Espressif Systems
- **Page Number:** 147
- **Document Version:** ESP32 TRM (Version 5.6)
- **Link Texts:** Submit Documentation Feedback