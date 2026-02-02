**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Header:**
Register 22.30. I2S_CONF2_REG (0x00a8)

**Binary Register Diagram Description:**
- The diagram shows a binary register with various bits labeled, such as `I2S INTER VALID EN`, `I2S EXT_ADC START EN`, etc.
- Each bit is numbered from 7 to -1.

**Register Descriptions and Values (Hexadecimal):**

1. **I2S_INTER_VALID_EN**
   - Description: Set this bit to enable camera’s internal validation.
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

2. **I2S_EXT_ADC_START_EN**
   - Description: Set this bit to enable the start of external ADC .
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

3. **I2S_LCD_EN**
   - Description: Set this bit to enable LCD mode.
   - Access Mode: Read/Write

4. **I2S_LCD_TX_SDX2_EN**
   - Description: Set this bit to duplicate data pairs (Data Frame, Form 2) in LCD mode.
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

5. **I2S_LCD_TX_WRX2_EN**
   - Description: One datum will be written twice in LCD mode.
   - Access Mode: Read/Write

6. **I2S_CAMERA_EN**
   - Description: Set this bit to enable camera mode.
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

**Section Header:**
Register 22.31. I2S_CLKM_CONF_REG (0x00ac)

**Binary Register Diagram Description for I2S_CLKM:**

- The diagram shows a binary register with various bits labeled, such as `I2S_CLKA_ENA`, `I2S_CLKM_DIV_A`, etc.
- Each bit is numbered from 7 to -1.

**Register Descriptions and Values (Hexadecimal):**

1. **I2S_CLKA_ENA**
   - Description: Set this bit to enable APLL_CLK. Default is PLL_F160M_CLK.
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

2. **I2S_CLKM_DIV_A**
   - Description: Fractional clock divider’s denominator value.
   - Access Mode: Read/Write

3. **I2S_CLKM_DIV_B**
   - Description: Fractional clock divider’s numerator value.
   - Access Mode: Read/Write
   - Value Hexadecimal: `0x00`

4. **I2S_CLKM_DIV_NUM**
   - Description: I2S clock divider's integral value.
   - Access Mode: Read/Write

**Footer Information:**
- Page Number: 446
- Company Name: Espressif Systems
- Document Title: ESP32 TRM (Version 5.6)
- Link Texts:
  - Submit Documentation Feedback