**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

### Registers List:

- **SENS_SAR_TOUCH_CTRL2_REG**: Touch pad control and status (0x3FF48884, RO)
- **SENS_SAR_TOUCH_ENABLE_REG**: Wakeup interrupt control and working set (0x3FF4888C, R/W)
- **SENS_SAR_TOUCHThRES1_REG**: Threshold setup for pads 0 and 1 (0x3FF4885C, R/W)
- **SENS_SAR_TOUCHThRES2_REG**: Threshold setup for pads 2 and 3 (0x3FF48860, R/W)
- **SENS_SAR TOUCHThRES3_REG**: Threshold setup for pads 4 and 5 (0x3FF48864, R/W)
- **SENS_SAR_TOUCHThRES4_REG**: Threshold setup for pads 6 and 7 (0x3FF48868, R/W)
- **SENS_SAR TOUCHThRES5_REG**: Threshold setup for pads 8 and 9 (0x3FF4886C, R/W)
- **SENS_SAR_TOUCH_OUT1_REG**: Counters for pads 0 and 1 (0x3FF48870, RO)
- **SENS_SAR TOUCH_OUT2_REG**: Counters for pads 2 and 3 (0x3FF48874, R/W)
- **SENS_SAR TOUCH_OUT3_REG**: Counters for pads 4 and 5 (0x3FF48878, RO)
- **SENS_SAR TOUCH_OUT4_REG**: Counters for pads 6 and 6 (0x3FF4887C, R/W)
- **SENS_SAR TOUCH_OUT5_REG**: Counters for pads 8 and 9 (0x3FF48880, RO)

**SAR ADC control register:**

- **SENS_SAR_START FORCE_REG**: SAR ADC1 and ADC2 control (0x3FF4882C, R/W)
- **SAR ADC1 control registers**
  - **SENS_SAR READ CTRL_REG**: SAR ADC1 data and sampling control (0x3FF48800, R/W)
  - **SENS_SAR MEAS START1_REG**: SAR ADC1 conversion control and status (0x3FF48854, RO)

**SAR ADC2 control registers:**

- **SENS_SAR READ CTRL2_REG**: SAR ADC2 data and sampling control (0x3FF48890, R/W)
- **SENS_SAR MEAS START2_REG**: SAR ADC2 conversion control and status (0x3FF48894, RO)

**ULP coprocessor configuration register:**

- **SENS_ULP_CP_SLEEP_CYCO_REG**: Sleep cycles for ULP coprocessor (0x3FF48818, R/W)
- **Pad attenuation configuration registers**
  - **SENS_SAR ATTEN1_REG**: 2-bit attenuation for each pad (0x3FF48834, R/W)
  - **SENS_SAR ATTEN2_REG**: 2-bit attenuation for each pad (0x3FF48838, R/W)

**DAC control registers:**

- **SENS_SAR_DAC_CTRL1_REG**: DAC control (0x3FF48898, R/W)
- **SENS_SAR_DAC_CTRL2_REG**: DAC output control (0x3FF4889C, RO)

---

### Section Title:
31.5.2 Advanced Peripheral Bus

**Note:** The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

---

### Common Configuration Registers:

- **APB_SARADC_CTRL_REG**: SAR ADC common configuration (0x60002610, R/W)
- **APB_SARADC_CTRL2_REG**: SAR ADC common configuration (0x60002614, R/W)
- **APB_SARADC_FSM_REG**: SAR ADC FSM sample cycles configuration (0x60002618, R/W)

**SAR ADC1 pattern table registers:**

- **APB_SARADC_SAR1_PATT_TAB1_REG**: Items 0 - 3 of pattern table (0x6000261C, R/W)
- **APB_SARADC_SAR1_PATT_TAB2_REG**: Items 4 - 7 of pattern table (0x60002620, R/W)
- **APB_SARADC_SAR1_PATT_TAB3_REG**: Items 8 - 11 of pattern table (0x60002624, R/W)

**SAR ADC2 pattern table registers:**

- **APB_SARADC_SAR1_PATT_TAB4_REG**: Items 12 - 15 of pattern table (0x60002628, R/W)

---

**Footer Information:**  
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback