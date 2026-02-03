**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Back Link:**
GoBack

**Register Information (Title):**
Register 39.56, APB_SARADC_CTRL_REG (0x000)

**Bitfield Table Description:**

- **APB_SARADC_WAIT_ARB_CYCLE:** Reserved
- **APB_SARADC_XPD_SAR FORCE:** Reserved
- **APB_SARADC_SAR1_PATT LEN:** Reserved
- **APB_SARADC_SAR_CLK_DIV:** Reserved
- **APB_SARADC_SAR_CLK GATED:** Reserved

**Bitfield Table:**

| Bit 31 | ... | Bit 20 | ... | Bit 9 | ... | Bit 8 | ... | Bit 7 | ... | Bit 6 | ... | Bit 5 | ... | Bit 4 | ... | Bit 3 | ... | Bit 2 | ... | Bit 1 | ... | Bit 0 |
|--------|-----|--------|-----|-------|-----|-------|-----|-------|-----|-------|-----|-------|-----|-------|-----|-------|-----|
| 1      |     | 0      |     | 25    |     | 24    |     | 23    |     | 22    |     | 21    |     | 20    |     | 19    |     | 18    |     | 17    |
|        |     |        |     |       |     |       |     |       |     |       |     |       |     |       |     |       |     |       |     |

**Bitfield Descriptions:**

- **APB_SARADC_START FORCE:** 
  - Value (0): SAR ADC is started by software.
  - Value (1): SAR ADC starts SAR ADC by software, only valid when APB_SARADC_START FORCE = I. 

- **APB_SARADC START**
  - Enable SAR ADC clock gate when SAR ADC is in idle.

- **APB_SARADC_SAR_CLK GATED**
  - SAR clock divider.
  
- **APB_SARADC_SAR1_PATT_LEN**
  - Configure how many pattern table entries will be used for SAR ADC. If this field is set to I, then pattern table entries (cmd0) and (cmd1) will be used.

- **APB_SARADC_SAR1_PATT P_CLEAR**
  - Clear the pointer of pattern table entry for DIG ADC1 controller.
  
- **APB_SARADC_XPD_SAR FORCE**
  - Force select XPD SAR. 

- **APB_SARADC_WAIT_ARB_CYCLE**
  - The clock cycles of waiting arbitration signal stable after SAR DONE.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback