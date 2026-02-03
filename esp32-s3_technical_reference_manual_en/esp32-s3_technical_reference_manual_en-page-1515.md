**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Register Information (Section Title):**
- **Register Name**: APB_SARADC_INT_CLR_REG (0x068)
- **Description**: Register bits for clearing interrupts.

**Bit Description Table:**

| Bit Number | Bit Name                          |
|------------|-----------------------------------|
| 31         | APB_SARADC_ADC1_DONE_INT_CLR     |
| 30         | APB_SARADC_THRES0_HIGH_INT_CLR   |
| 29         | APB_SARADC_THRES0_LOW_INT_CLR    |
| 28         | (reserved)                        |
| 27         | APB_SARADC_THRES1_HIGH_INT_CLR   |
| 26         | APB_SARADC_THRES1_LOW_INT_CLR    |
| 25-3       | Reserved                           |

**Bit Clearing Instructions:**
- **APB_SARADC_THRES1_LOW_INT_CLR**: Clear bit of APB_SARADCThres1_Low_Int. (WO)
- **APB_SARADC_THRES0_LOW_INT_CLR**: Clear bit of APB_SARADCThres0_Low_Int. (WO)
- **APB_SARADC_THREST_HIGH_INT_CLR**: Clear bit of APB_SARADCThrest_High_Int. (WO)
- **APB_SARADC_THRESO_HIGH_INT_CLR**: Clear bit of APB_SARADCThreso_High_Int. (WO)
- **APB_SARADC_ADC1_DONE_INT_CLR**: Clear bit of APB_SARADCAdc1_Done_Int. (WO)

**Register Information:**
- **Register Name**: APB_SARADC_APB_CTRL_DATE_REG (0x03FC)
- **Description**: Version control register.

**Bit Description Table for Register 39.76:**

| Bit Number | Bit Name                          |
|------------|-----------------------------------|
| 31         | APB_SARADC_APB_CTRL_DATE         |

**Version Control Information:** 
- **Register Name**: APB_SARADC_APB_CTRL_DATE
- **Description**: Version control register.
- **Access Mode**: (R/W)

**Footer:**
- Page Number: 1515
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Information: Espressif Systems

**Link:** Submit Documentation Feedback