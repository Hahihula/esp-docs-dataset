**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
Register 28.16, I2S_RX_CLKM_DIV_CONF_REG (0x0038)

**Table Description:**
- The table shows the bit layout of register `I2S_RX_CLKM_DIV_CONF_REG`.
- Bits are labeled from right to left as follows:
  - Bit 31 is reserved.
  - Bits 29, 27, and 26 have specific values (0).
  - Bits 18 through 17 contain the value `Ox0` in hexadecimal notation.

**Bit Description:**
- The table indicates that for bit positions less than or equal to a/2:
  - If b < a/2, then I2S_RX_CLKM_DIV_Z is set.
  - For other cases (b > a/2), the value of `I2S_RX_CLKM_DIV_Z` depends on `(a-b)`.

**Additional Bits:**
- Bit positions for additional values are described similarly:
  - I2S_RX_CLKM_DIV_Y
  - I2S_RX_CLKM_DIV_X

**Note Section:**
- The note explains that "a" and "b" represent the denominator and numerator of a fractional divider, respectively.
- For more information on this topic, see section `28.6`.

**Footer Information:**
- Page number: 1073
- Document title: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Link Texts:**
- "GoBack"
- "Submit Documentation Feedback"