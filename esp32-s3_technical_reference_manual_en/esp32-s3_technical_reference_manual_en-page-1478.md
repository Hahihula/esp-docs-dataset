**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

### Table of Contents:
- **Section Name**: 39.6.2 SENSOR (RTC_PERI) Register Summary

---

#### Section Introduction:
The addresses in this section are relative to the [Low Power Management base address + 0x800] provided in Table 4.3-3 in Chapter 4 System and Memory.

**Abbreviations:**
- **Column Access**: The abbreviations given in Column Access
- **Access Types for Registers**: Explained in Section

---

#### Configuration Register Summary:

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SENS_SAR_READER1_CTRL_REG | SAR ADC1 data and sampling control | 0x0000 | R/W |
| SENS_SAR_MEAS1_CTRL2_REG | Control SAR ADC1 conversion and status | 0x00C0 | varies |
| SENS_SAR_MEAS1_MUX_REG | Select the controller for SAR ADC1 | 0x0010 | R/W |
| SENS_SAR_ATTEN1_REG | Configure SAR ADC1 attenuation | 0x0014 | R/W |
| SENS_SAR_READER2_CTRL_REG | SAR ADC2 data and sampling control | 0x0024 | R/W |
| SENS_SAR_MEAS2_CTRL2_REG | Control SAR ADC2 conversion and status | 0x0030 | varies |
| SENS_SAR_MEAS2_MUX_REG | Select the controller for SAR ADC2 | 0x0034 | R/W |
| SENS_SAR_ATTEN2_REG | Configure SAR ADC2 attenuation | 0x0038 | R/W |
| SENS_SAR_POWER_XPD_SAR_REG | SAR ADC power control | 0x003C | R/W |
| SENS_SAR_TSENS_CTRL_REG | Temperature sensor data control | 0x0050 | varies |
| SENS_SAR_TOUCH_CONF_REG | Touch sensor configuration register | 0x005C | varies |
| SENS_SAR_TOUCH_DENOISE_REG | Denoise data register | 0x0060 | RO |
| SENS_SAR TOUCH_THRESH1_REG | Touch detection threshold for pin 1 | 0x0064 | R/W |
| SENS_SAR_TOUCH_THRESH2_REG | Touch detection threshold for pin 2 | 0x0068 | R/W |
| SENS_SAR_TOUCH_THRESH3_REG | Touch detection threshold for pin 3 | 0x006C | R/W |
| SENS_SAR TOUCH_THRESH4_REG | Touch detection threshold for pin 4 | 0x0070 | R/W |
| SENS_SAR TOUCH_THRESH5_REG | Touch detection threshold for pin 5 | 0x0074 | R/W |
| SENS_SAR_TOUCH_THRESH6_REG | Touch detection threshold for pin 6 | 0x0078 | R/W |
| SENS_SAR_TOUCH_THRESH7_REG | Touch detection threshold for pin 7 | 0x007C | R/W |
| SENS_SAR_TOUCH_THRESH8_REG | Touch detection threshold for pin 8 | 0x0080 | R/W |
| SENS_SAR_TOUCH_THRESH9_REG | Touch detection threshold for pin 9 | 0x0084 | R/W |
| SENS_SAR_TOUCH_THRESH10_REG | Touch detection threshold for pin 10 | 0x0088 | R/W |
| SENS_SAR TOUCH_THRESH11_REG | Touch detection threshold for pin 11 | 0x008C | R/W |
| SENS_SAR_TOUCH_THRESH12_REG | Touch detection threshold for pin 12 | 0x0090 | R/W |
| SENS_SAR_TOUCH_THRESH13_REG | Touch detection threshold for pin 13 | 0x0094 | R/W |
| SENS_SAR TOUCH_THRESH14_REG | Touch detection threshold for pin 14 | 0x0098 | R/W |
| SENS_SAR_TOUCH_CHN_ST_REG | Get touch channel status | 0x009C | varies |

---

**Footer:**
Espressif Systems
Page number: 1478
Document version: ESP32-S3 TRM (Version 1.7)
Feedback link for documentation submission