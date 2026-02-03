**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header (with reference to figure):**
Register 39.66, APB_SARADC_THRES1_CTRL_REG (0x0048)

**Figure Description with Labels:**
- The image shows a register layout for the specified address.
- It includes fields labeled as:
  - `APB_SARADC_THRES1频道` 
  - `APB_SARADC_THRES1_HIGH`
  - `APB_SARADC_THRES1_LOW`

**Field Descriptions:**
- **APB_SARADC_THRES1_CHANNEL:** Configure the channel for SAR ADC threshold monitor 1. (R/W)
- **APB_SARADC_THRES1_HIGH:** Set the high threshold for SAR ADC threshold monitor 1. (R/W)
- **APB_SARADC_THRES1_LOW:** Set the low threshold for SAR ADC threshold monitor 1. (R/W)

---

**Section Header:**
Register 39.67, APB_SARADC_THRES_CTRL_REG (0x0058)

**Figure Description with Labels:**
- The image shows a register layout similar to that of Register 39.66.
- It includes fields labeled as:
  - `APB_SARADC_THRES_EN`
  - `APB_SARADC_THRES_ALL_EN`

**Field Descriptions:**
- **APB_SARADC_THRES_ALL_EN:** Enable threshold monitoring for all configured channels. (R/W)
- **APB_SARADC_THRES1_EN:** Enable threshold monitor 1. (R/W)
- **APB_SARADC_THRES0_EN:** Enable threshold monitor 0. (R/W)

---

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)