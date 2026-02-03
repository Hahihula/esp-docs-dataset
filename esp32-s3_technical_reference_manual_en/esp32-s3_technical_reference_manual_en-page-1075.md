**Title: Chapter 28 I2S Controller (I2S)**

**Section Title: Register 28.18. I2S_TX_CLKM_DIV_CONF_REG (0x03C)**

**Diagram Description:** 
- The diagram shows a register layout with labels for different bits and their corresponding values.
- Bits are labeled as follows:
  - `I2S_TX_CLKM_DIV_X` from bit positions 18 to 0
  - `I2S_TX_CLKM_DIV_Z` at position (reserved)
  - `I2S_TX_CLKM_DIV_Y` not explicitly shown in the diagram but referenced below

**Text Content:**

- **Description of I2S_TX_CLKM_DIV_Z:** 
  For b <= a/2, the value of I2S_TX_CLKM_DIV_Z is b. For b > a/2, the value of I2S_TX_CLKM_DIV_Z is (a - b). (R/W)

- **Description of I2S_TX_CLKM_DIV_Y:**
  For b <= a/2, the value of I2S_TX_CLKM_DIV_Y is s(a%b). For b > a/2, the value of I2S_TX_CLKM_DIV_Y is (a%b) - floor(a/b). (R/W)

- **Description of I2S_TX_CLKM_DIV_X:**
  For b <= a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/b) - 1. For b > a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/(a - b)) - 1. (R/W)

- **Description of I2S_TX_CLKM_DIV_YN1:**
  For b <= a/2, the value of I2S_TX_CLKM_DIV_YN1 is 0. For b > a/2, the value of I2S_TX_CLKM_DIV_YN1 is 1. (R/W)

**Note:** 
- "a" and "b" represent the denominator and the numerator of fractional divider, respectively.
- More information can be found in Section **28.6**.

**Footer:**
- Espressif Systems
- Page number: 1075
- Document version: ESP32-S3 TRM (Version 1.7)
- Link to submit documentation feedback