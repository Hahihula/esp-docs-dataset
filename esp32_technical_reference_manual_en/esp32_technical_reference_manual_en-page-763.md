**Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Section Title:**
31.6.3 RTC I/O

**Body Text with Descriptions of Registers:**

- **Register Description:** 
  - APB_SARADC_SAR2_PATT_TAB2_REG (0x30)
    - Pattern tables 4 - 7 for SAR ADC2, one byte for each pattern table:
      - [31:28] pattern4_channel,
      - [27:26] pattern4_bit_width,
      - [25:24] pattern4_attenuation,
      - [23:20] pattern5_channel, etc. (R/W)

- **Register Description:** 
  - APB_SARADC_SAR2_PATT_TAB3_REG (0x34)
    - Pattern tables 8 - 11 for SAR ADC2, one byte for each pattern table:
      - [31:28] pattern8_channel,
      - [27:26] pattern8_bit_width,
      - [25:24] pattern8_attenuation,
      - [23:20] pattern9_channel, etc. (R/W)

- **Register Description:** 
  - APB_SARADC_SAR2_PATT_TAB4_REG (0x38)
    - Pattern tables 12 - 15 for SAR ADC2, one byte for each pattern table:
      - [31:28] pattern12_channel,
      - [27:26] pattern12_bit_width,
      - [25:24] pattern12_attenuation,
      - [23:20] pattern13_channel, etc. (R/W)

**Footer Text:** 
For details, please refer to Section Registers in Chapter IO_MUX and GPIO Matrix.

**Company Information at the Bottom of Page:**
Espressif Systems
ESP32 TRM (Version 5.6)