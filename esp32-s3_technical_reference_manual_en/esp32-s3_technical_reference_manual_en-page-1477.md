**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Body Text with Formula Explanation (partially visible):**
VALUE in the formula is the output of the temperature sensor, and the offset is determined by the temperature offset. The temperature offset varies in different actual environment (the temperature range). For details, refer to Table 39.4-1.

**Table Title:**
Table 39.4-1. Temperature Measurement Range and Offset

| Temperature Measurement Range (°C) | Temperature Offset |
|--------------------------------------|--------------------|
| 50 ~ 125                             | -2                 |
| 20 ~ 100                             | -1                 |
| -10 ~ 80                             | 0                  |
| -30 ~ 50                             | 1                  |
| -40 ~ 20                             | 2                  |

**Subsection Title:**
39.5 Interrupts

- APB_SARADC_THRESx_HIGH_INT: Triggered when the sampling value is higher than the high threshold of monitor x.
- APB_SARADC_THRESx_LOWINT: Triggered when the sampling value is lower than the low threshold of monitor x.
- APB_SARADC_ADC1_DONE_INT: Triggered when SAR ADC1 completes one data conversion.

**Additional Information about Interrupts (partially visible):**
For the interrupts routed to ULP-RISC-V, please refer to Section ULP-RISC-V Interrupts in Chapter 2 ULP Coprocessor (ULP-FSM, ULP-ISC-V).

**Subsection Title:**
39.6 Register Summary

- SENSOR (ALWAYS_ON) represents the registers, which will not be reset due to the power down of RTC_PERI domain. See Chapter 10 Low-power Management (RTC_CNTL).
- SENSOR (RTC_PERI) represents the registers, which will be reset due to the power down of RTC_PERI domain. See Chapter 10 Low-power Management (RTC_CNTL).
- SENSOR (DIG_PERI) represents the registers, which will be reset due to the power down of digital domain. See Chapter 10 Low-power Management (RTC_CNTL).

**Subsection Title:**
39.6.1 SENSOR (ALWAYS_ON) Register Summary

The addresses in this section are relative to the [Low Power Management] base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table with Register Information:**

| Name                          | Description                                    | Address       | Access |
|-------------------------------|-----------------------------------------------|--------------|--------|
| Touch control register        |                                               |              |        |
| RTC_CNTL_TOUCH_CTRL1_REG     | Touch control register 1                      | Ox0108       | R/W    |
| RTC_CNTL TOUCH_CTRL2_REG      | Touch control register 2                      | Ox010C       | R/W    |
| RTC_CNTL TOUCH_SCAN_CTRL_REG | Configure touch scanning settings              | Ox0110       | R/W    |
| RTC_CNTL_TOUCH_SLP_THRESH_REG| Configure the setting of touch sleep pin        | Ox0114       | R/W    |

**Footer:**
Espressif Systems
Page number 1477 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback