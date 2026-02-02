**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Back Link:**
GoBack

**Register Information (Title):**
Register 31.24. APB_SARADC_CTRL_REG (0x10)

**Binary Register Diagram Description:**
The diagram shows a binary register with various fields labeled as follows:
- `APB_SARADC_DATA_TO_I2S` - I2S input data is from SAR ADC
- `APB_SARADC_DATA_SAR_SEL` 
  - `sar_sel` will be coded by the MSB of the 16-bit output data, in this case, the resolution should not contain more than 11 bits; O: using 12-bit SAR ADC resolution.
- `APB_SARADC_SAR2_PATT_P_CLEAR`
- `APB_SARADC_SAR1_PATT_P_CLEAR`
- `APB_SARADC_SAR2_PATT_LEN` - SAR ADC2, 0 - 15 means pattern table length of 1 - 16.
- `APB_SARADC_SAR1_PATT_LEN` - SAR ADC1, 0 - 15 means pattern table length of 1 - 16.

**Field Descriptions:**
- **APB_SARADC_DATA_TO_I2S**: I2S input data is from GPIO matrix. (R/W)
- **APB_SARADC_DATA_SAR_SEL**: 
  - `sar_sel` will be coded by the MSB of the 16-bit output data, in this case, the resolution should not contain more than 11 bits; O: using 12-bit SAR ADC resolution. (R/W)
- **APB_SARADC_SAR2_PATT_P_CLEAR**: Clears the pointer of pattern table for DIG ADC2 CTRL. (R/W)
- **APB_SARADC_SAR1_PATT_P_CLEAR**: Clears the pointer of pattern table for DIG ADC1 CTRL. (R/W)
- **APB_SARADC_SAR2_PATT_LEN**:
  - SAR ADC2, 0 - 15 means pattern table length of 1 - 16. (R/W)
- **APB_SARADC_SAR1_PATT_LEN**:
  - SAR ADC1, 0 - 15 means pattern table length of 1 - 16. (R/W)
- **APB_SARADC_SAR2_CLK_DIV**: SAR clock divider. (R/W)
- **APB_SARADC_SAR1_CLK_G**: Reserved. Please initialize to Ob1 (R/W)
- **APB_SARADC_SAR_SEL**:
  - `SAR1, 1: SAR2`, this setting is applicable in the single SAR mode. (R/W)
- **APB_SARADC_WORK_MODE**:
  - O: single mode; 1: double mode; 2: alternate mode. (R/W)
- **APB_SARADC_SAR2_MUX**: 
  - `SAR ADC2 is controlled by DIG ADC2 CTRL`, 0: SAR ADC2 is controlled by PWDET CTRL. (R/W)
- **APB_SARADC_START**:
  - Reserved. Please initialize to O (R/W)
- **APB_SARADC_STARTFORCE**: 
  - Reserved. Please initialize to 0 (R/W)

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)