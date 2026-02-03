**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Register Information (APB_SARADC_CTRL2_REG):**

- **Register Name:** APB_SARADC_CTRL2_REG (0x0004)
  
- **Bit Fields Description:**
  - `31` to `25`: Reserved
  - `24`: APB_SARADC_TIMER_EN
  - `23`: APB_SARADC_SAR2_INV
  - `22`: APB_SARADC_SAR1_INV
  - `21`: APB_SARADC_MAX_MEAS_NUM
  - `20` to `9`: Reserved bits (all set as '0')
  - `8`: APB_SARADC_FILTER_CTRL1
  - `7` to `0`: Reset

- **Bit Fields Values:**
  - `31, 25, 24, 23, 22, 21, 20, 9, 8, 7, 6, 5, 4, 3, 2, 1`: All set as '0'
  - `0`: Reset

- **Bit Fields Labels:**
  - APB_SARADC_MEAS_NUM_LIMIT (Enable the limitation of SAR ADCs maximum conversion times. R/W)
  - APB_SARADC_MAX_MEAS_NUM (The SAR ADCs maximum conversion times. R/W)
  - APB_SARADC_SAR1_INV (Write 1 here to invert the data to DIG ADC1 controller. R/W)
  - APB_SARADC_SAR2_INV (Write 1 here to invert the data to DIG ADC2 controller. R/W)
  - APB_SARADC_TIMER_TARGET (Set SAR ADC timer target. R/W)
  - APB_SARADC_TIMER_EN (Enable SAR ADC timer trigger. R/W)

**Register Information (APB_SARADC_FILTER_CTRL1_REG):**

- **Register Name:** APB_SARADC_FILTER_CTRL1_REG (0x0008)
  
- **Bit Fields Description:**
  - `31` to `29`: Reserved
  - `28` and `26, 25`: Reserved bits ('0')
  - `24` onwards are reserved

- **Bit Fields Values:** All set as '0'

- **Bit Fields Labels:**
  - APB_SARADC_FILTER_FACTOR1 (The filter coefficient for SAR ADC filter 1. R/W)
  - APB_SARADC_FILTER_FACTOR0 (The filter coefficient for SAR ADC filter 0. R/W)

**Footer Information:** 
Espressif Systems
ESP32-S3 TRM (Version 1.7)