**Title: Chapter 28 I2S Controller (I2S)**

**Subtitle: Register 28.7. I2S_RX_CLKM_CONF_REG (0x0030)**

- **Field:** `I2S_RX_CLKM_DIV_NUM`
  - Description: Integral I2S RX clock divider value.
  - Access Type: Read/Write
  - Bits: [31, 30, ..., 0]

- **Field:** `I2S_RX_CLK_ACTIVE`
  - Description: Clock enable signal of I2S RX unit.
  - Access Type: Read/Write

- **Field:** `I2S_RX_CLK_SEL`
  - Description: Select clock source for I2S RX unit. 
    - Options:
      - O: XTAL_CLK
      - 1: PLL_D2_CLK
      - 2: PLL_F160M_CLK
      - 3: I2S_MCLK_in

- **Field:** `I2S_MCLK_SEL`
  - Description: Use I2S TX unit clock as I2S_MCLK_OUT.
    - Options:
      - O: Use I2S RX unit clock (R/W)

**Subtitle: Register 28.8. I2S_TX_PCM2PDM_CONF_REG (For I2S0 Only) (0x0040)**

- **Field:** `I2S_TX_PDM_SINC_OSR2`
  - Description: I2S TX PDM OSR value.
    - Access Type: Read/Write
    - Bits: [31, 26, ..., 0]

- **Field:** `I2S_TX_PDM_DAC_2OUT_EN`
  - Description:
    - Options for DAC output mode when I2S_TX_PDM_DAC_MODE_EN is set.
      - O: 1-line DAC output mode
      - 1: 2-line DAC output mode

- **Field:** `I2S_TX_PDM_DAC_MODE_EN`
  - Description: Enable bit for I2S TX PCM-to-PDM conversion.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 1064

**Navigation Links:** 
- Submit Documentation Feedback