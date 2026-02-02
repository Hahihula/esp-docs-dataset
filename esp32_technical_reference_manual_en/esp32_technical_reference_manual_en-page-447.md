**Title:**
Chapter 22 I2S Controller (I2S)

**Header:**
Register 22.32. I2S_SAMPLE_RATE_CONF_REG (0x00b0)

**Diagram Description:**
- A register diagram with labeled fields:
  - `I2S_RX BITS MOD`
  - `I2S_TX BITS MOD`
  - `I2S_RX BCK DIV NUM` [Bit clock configuration bit in receiver mode. (R/W)]
  - `I2S_TX BCK DIV NUM` [Bit clock configuration bit in transmitter mode. (R/W)]

**Field Descriptions:**
- **31:** Reserved
- **24, 23, 18, 17, 16, 16, 12, 11, 6, 5, 0:** Bits of the register with corresponding labels as mentioned above.
- **Reset:** A bit labeled "Reset" at position `6`.

**Field Access Modes:**
- I2S_RX BITS_MOD [Set the bits to configure the bit length of I2S receiver channel. (R/W)]
- I2S_TX BITS_MOD [Set the bits to configure the bit length of I2S transmitter channel. (R/W)]
- I2S_RX BCK DIV_NUM [Bit clock configuration bit in receiver mode. (R/W)]
- I2S_TX BCK DIV_NUM [Bit clock configuration bit in transmitter mode. (R/W)]

**Footer:**
Espressif Systems
447 ESP32 TRM (Version 5.6)
Submit Documentation Feedback