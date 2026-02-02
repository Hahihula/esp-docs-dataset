**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack**

**Section Header:**
Register 31.3. SENS_SAR_START FORCE REG (0x02c)

**Table Description:**
- The table lists various registers related to the SAR ADCs, including their names, bit widths, descriptions of what each register does.
  
**Text Content in Table:**

- **SENS_SAR1_STOP**: Stop SAR ADC1 conversion. (R/W)
- **SENS_SAR2_STOP**: Stop SAR ADC2 conversion. (R/W)
- **SENS_PC_INIT**: Initialized PC for ULP coprocessor. (R/W)
- **SENS_ULP_CP_START_TOP**: Write 1 to start ULP coprocessor; it is active only when `reg_ulp_cp_force_start_top = 1`. (R/W)
- **SENS_ULP_CP FORCE START_TOP**: ULP coprocessor is started by SW, 0: ULP coprocessor is started by timer. (R/W)
- **SENS_SAR2_PWDET_CCT**: SAR2PWDET CCT, PA power detector capacitance tuning. (R/W)
- **SENS_SAR2_EN_TEST**: SAREN_TEST is active only when `reg_sar2_dig_force = 0`. (R/W)
- **SENS_SAR2_BIT_WIDTH**: Bit width of SAR ADC2, 0: 9 bits; 01: 10 bits; 10: 11 bits; 11: 12 bits. (R/W)
- **SENS_SAR1_BIT_WIDTH**: Bit width of SAR ADC1, 0: 9 bits; 01: 10 bits; 10: 11 bits; 11: 12 bits. (R/W)

**Register Description and Values for SENS_SAR_ATTEN1_REG (0x034):**
- **Description**: 2-bit attenuation for each pad, with values as follows:
  - `11`: 1 dB
  - `10`: 6 dB
  - `01`: 3 dB
  - `00`: 0 dB

**Register Description and Values for SENS_SAR_ATTEN2_REG (0x038):**
- **Description**: 2-bit attenuation for each pad, with values as follows:
  - `[1:0]` is used for ADC2 CHO; `[3:2]` is used for ADC2 CH1, etc. The possible settings are the same.
  
**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)