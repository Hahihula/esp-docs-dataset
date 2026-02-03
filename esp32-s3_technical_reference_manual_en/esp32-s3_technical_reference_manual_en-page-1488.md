**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

**GoBack**

---

**Subtitle: Register 39.11. SENS_SAR_MEAS1_CTRL2_REG (0x00C)**

- **Binary Representation Diagram**
  - Bits labeled from right to left as follows:
    - `31` 
    - `30`
    - `19`
    - `18`
    - `17`
    - `16`
    - `15`
    - `14`
    - `13`
    - `12`
    - `11`
    - `10`
    - `9`
    - `8`
    - `7`
    - `6`
    - `5`
    - `4`
    - `3`
    - `2`
    - `1`
    - `0`

- **Hexadecimal Values:**
  - `0x00C` (Reset)

**Text Descriptions for Bits and Registers**

- SENS_MEAS1_DATA_SAR
  - Description: SAR ADC1 data. (RO)
  
- SENS_MEAS1_DONE_SAR
  - Description: Indicate SAR ADC1 conversion is done. (RO)
  
- SENS_MEAS1_START_SAR
  - Description: RTC ADC1 controller starts conversion, valid only when SENS_MEAS1_START FORCE = 1. (R/W)
  
- SENS_MEAS1_STARTFORCE
  - Description:
    - `0`: RTC ADC1 controller is started by software.
    - `1`: RTC ADC1 controller is started by ULP coprocessor. (R/W)
  
- SENS_SAR1_EN_PAD
  - Description: SAR ADC1 pin enable bitmap, valid only when SENS_SAR1_EN_PAD FORCE = 1. (R/W)
  
- SENS_SAR1_EN_PADFORCE
  - Description:
    - `0`: SAR ADC1 pin enable bitmap is controlled by software.
    - `1`: SAR ADC1 pin enable bitmap is controlled by ULP coprocessor.

**Subtitle: Register 39.12. SENS_SAR_MEAS1_MUX_REG (0x0010)**

- **Binary Representation Diagram**
  - Bits labeled from right to left as follows:
    - `31`
    - `30`
    - `...` (omitted for brevity)
  
- **Hexadecimal Values:**
  - `0x0010` (Reset)

**Text Descriptions**

- SENS_SAR1_DIG FORCE
  - Description: SAR ADC1 controlled by DIG ADC1 controller. (R/W)

---

**Footer Information:**
- Page number and document version:
  - "1488 ESP32-S3 TRM (Version 1.7)"
  
- Company name:
  - Espressif Systems
  
- Link for submitting documentation feedback:
  - [Submit Documentation Feedback](#)