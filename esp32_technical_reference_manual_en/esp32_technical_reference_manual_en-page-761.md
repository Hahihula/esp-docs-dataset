**Title: Chapter 31 On-Chip Sensors and Analog Signal Processing**

---

**Section Title: Register 31.25 APB_SARADC_CTRL2_REG (0x14)**

- **Field Description:** 
  - `APB_SARADC_SAR2_INV`  
    - Data to DIG ADC2 CTRL is inverted, O: data not inverted.
    - Access Type: Read/Write
  - `APB_SARADC_SAR1_INV`
    - Data to DIG ADC1 CTRL is inverted, O: data not inverted.
    - Access Type: Read/Write
  - `APB_SARADC_MAX_MEAS_NUM`
    - Max conversion number. (R/W)
  - `APB_SARADC_MEAS_NUM_LIMIT`
    - Reserved.

---

**Section Title: Register 31.26 APB_SARADC_FSM_REG (0x18)**

- **Field Description:** 
  - `APB_SARADC_SAMPLE_CYCLE`
    - Sample cycles.
    - Access Type: Read/Write
  - `Pattern tables`:
    - [0x00FF] for SAR ADC1, one byte for each pattern table.

---

**Section Title: Register 31.27 APB_SARADC_SAR1_PATT_TAB1_REG (0x1C)**

- **Field Description:** 
  - `APB_SARADC_SAR1_PATT_TAB1`
    - Pattern tables [0-3] for SAR ADC1, one byte for each pattern table.
    - Access Type: Read/Write
  - `Pattern details`:
    - [27:26] pattern0_bit_width,
    - [25:24] pattern0_attenuation,
    - [23:20] pattern1_channel, etc.

---

**Footer:** 
- Page number: 761
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems

**Link:** Submit Documentation Feedback