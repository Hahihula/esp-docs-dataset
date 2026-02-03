**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Link:**
GoBack

**Register Information (Section):**

- **Register Name:** APB_SARADC_INT_RAW_REG (0x060)
- **Description:** 
  - Bit description for each bit in the register:
    - `APB_SARADC_THRES1_LOW_INT_RAW`: Raw bit of APB_SARADCThres1_low_int. (RO)
    - `APB_SARADC_THRES0_LOW_INT_RAW`: Raw bit of APB_SARADCThres0_low_int. (RO)
    - `APB_SARADC_THRES1_HIGH_INT_RAW`: Raw bit of APB_SARADCThres1_high_int. (RO)
    - `APB_SARADC_THRES0_HIGH_INT_RAW`: Raw bit of APB_SARADCThres0_high_int. (RO)
    - `APB_SARADC_ADC1_DONE_INT_RAW`: Raw bit of APB_SARADCAdc1_done_int. (RO)

- **Bit Layout Diagram:**
  - Bit positions from least significant to most significant:
    - `31`
    - `30`
    - `29`
    - `28`
    - `27`
    - `26`
    - `25`
    - (Reserved bits)
    - Reset bit

**Register Information:**

- **Register Name:** APB_SARADC_INT_ST_REG (0x064)
- **Description:**
  - Status of each interrupt:
    - `APB_SARADC_THRES1_LOW_INT`: Status of APB_SARADCThres1_low_int. (RO)
    - `APB_SARADC_THRES0_LOW_INT`: Status of APB_SARADCThres0_low_int. (RO)
    - `APB_SARADC_THRES1_HIGH_INT`: Status of APB_SARADCThres1_high_int. (RO)
    - `APB_SARADC_THRES0_HIGH_INT`: Status of APB_SARADCThres0_high_int. (RO)
    - `APB_SARADC_ADC1_DONE_INT`: Status of APB_SARADCAdc1_done_int. (RO)

- **Bit Layout Diagram:**
  - Bit positions from least significant to most significant:
    - `31`
    - `30`
    - `29`
    - `28`
    - `27`
    - `26`
    - `25`
    - (Reserved bits)
    - Reset bit

**Footer:**
- Company Name: Espressif Systems
- Document Version and Submission Information:
  - Page number: 1514
  - Document version: ESP32-S3 TRM (Version 1.7)
  - Link for feedback submission: Submit Documentation Feedback