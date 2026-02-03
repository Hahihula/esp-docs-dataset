**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Table of Status Register Addresses**

| Name                                      | Description                                                                                   | Address   | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|----------|--------|
| SENS_SAR_PERI_CLK_GATE_CONF_REG          | Clock gate of RTC peripherals                                                                | 0x0104   | R/W    |
| SENS_SAR_PERI_RESET_CONF_REG             | Reset register of RTC peripherals                                                           | 0x0108   | R/W    |
| Status register                           |                                                                                              |          |        |

- **SENS_SAR_TOUCH_STATUSO_REG** - Get touch scan status
- **SENS_SAR_TOUCH_STATUS1_REG** - Channel status of touch pin 1 (RO)
- **SENS_SAR TOUCH STATUS2_REG** - Channel status of touch pin 2 (RO)
- **SENS_SAR_TOUCH_STATUS3_REG** - Channel status of touch pin 3 (RO)
- **SENS_SAR_TOUCH_STATUS4_REG** - Channel status of touch pin 4 (RO)
- **SENS_SAR_TOUCH_STATUS5_REG** - Channel status of touch pin 5 (RO)
- **SENS_SAR_TOUCH_STATUS6_REG** - Channel status of touch pin 6 (RO)
- **SENS_SAR TOUCH STATUS7_REG** - Channel status of touch pin 7 (RO)
- **SENS_SAR_TOUCH_STATUS8_REG** - Channel status of touch pin 8 (RO)
- **SENS_SAR_TOUCH_STATUS9_REG** - Channel status of touch pin 9 (RO)
- **SENS_SAR_TOUCH_STATUS10_REG** - Channel status of touch pin 10 (RO)
- **SENS_SAR TOUCH STATUS11_REG** - Channel status of touch pin 11 (RO)
- **SENS_SAR TOUCH STATUS12_REG** - Channel status of touch pin 12 (RO)
- **SENS_SAR TOUCH STATUS13_REG** - Channel status of touch pin 13 (RO)
- **SENS_SAR_TOUCH_STATUS14_REG** - Channel status of touch pin 14 (RO)
- **SENS_SAR TOUCH STATUS15_REG** - Channel status of sleep pin in proximity mode
- **SENS_SAR TOUCH APPR STATUS_REG** - Channel status of touch pins

---

**Section Title:**
39.6.3 SENSOR (DIG_PERI) Register Summary

**Note:** The addresses mentioned are relative to the [ADC controller base address] provided in Table 4.3-3.

**Table of Configure Register Addresses**

| Name                                      | Description                                                                                   | Address   | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|----------|--------|
| APB_SARADC_CTRL_REG                      | Configuration register for DIG ADC controller                                               | 0x0000   | R/W    |
| APB_SARADC_CTRL2_REG                     | Configuration register for DIG ADC controller                                                | 0x0004   | R/W    |
| APB_SARADC_FILTER_CTRL1_REG              | Configuration register 1 for SAR ADC filter                                                 | 0x0008   | R/W    |
| APB_SARADC_SAR1_PATT_TAB1_REG            | Pattern table register 1 for SAR ADC1                                                      | 0x0012   | R/W    |
| APB_SARADC_SAR1_PATT_TAB2_REG            | Pattern table register 2 for SAR ADC1                                                      | 0x0018   | R/W    |
| APB_SARADC_SAR1_PATT_TAB3_REG            | Pattern table register 3 for SAR ADC1                                                      | 0x0024   | R/W    |
| APB_SARADC_SAR1_PATT_TAB4_REG            | Pattern table register 4 for SAR ADC1                                                      | 0x0030   | R/W    |
| APB_SARADC_ADC_ARB_CTRL_REG              | Configuration register for SAR ADC2 arbiter                                                 | 0x0038   | R/W    |
| APB_SARADC_FILTER_CTRL0_REG              | Configuration register 0 for SAR ADC filter                                                | 0x003C   | R/W    |
| APB_SARADC_THRESO_CTRL_REG               | Sampling threshold control register 0                                                      | 0x0040   | R/W    |
| APB_SARADC_THRES1_CTRL_REG               | Sampling threshold control register 1                                                      | 0x0048   | R/W    |
| APB_SARADC_THRES3_CTRL_REG               | Sampling threshold enable register                                                          | 0x0052   | R/W    |

**Footer:**
Espressif Systems
Page number and document version information:
ESP32-S3 TRM (Version 1.7)