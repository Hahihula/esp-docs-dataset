**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** (Located at top right corner)

---

**Section Header - Register Information for APB_SARADC:**

- **Register Name**: APB_SARADC_APB_SARADC1_DATA_STATUS_REG
- **Address**: 0x0040
  
  **Description**: Raw sample data from SAR ADC1. (RO)
  
  **Binary Representation**:
  ```
  31    17   16     0
  0 0 0 0 0 0 0 0 0 0 0 0 0 Reset
  ```

- **Register Name**: APB_SARADC_APB_SARADC2_DATA_STATUS_REG
- **Address**: 0x0078
  
  **Description**: Raw sample data from SAR ADC2. (RO)
  
  **Binary Representation**:
  ```
  31    17   16     0
  0 0 0 0 0 0 0 0 0 0 0 0 Reset
  ```

- **Register Name**: APB_SARADC_ADC2_DATA
- **Address**: (Not specified in the visible text)
  
  **Description**: Raw sample data from SAR ADC2. (RO)

---

**Section Header - Register Information for Interrupt Enable:**

- **Register Name**: APB_SARADC_INT_ENA_REG
- **Address**: 0x005C
  
  **Description and Bit Definitions**:
  
  ```
  31    30   29     28    27   26      25       (reserved)
  0 0 0 0 0 0 0 0 0 0 0 0 0 Reset
  ```

  **Bit Definitions**:
  
  - APB_SARADC_THRES1_LOW_INT_ENA: Enable bit of THRESH1 LOW INT. (R/W)
  - APB_SARADC_THRES0_LOW_INT_ENA: Enable bit of THRESH0 LOW INT. (R/W)
  - APB_SARADC_THRES1_HIGH_INT_ENA: Enable bit of THRESH1 HIGH INT. (R/W)
  - APB_SARADC_THRES0_HIGH_INT_ENA: Enable bit of THRESH0 HIGH INT. (R/W)
  - APB_SARADC_ADC1_DONE_INT_ENA: Enable bit of ADC1 DONE INT. (R/W)

---

**Footer Information:**
- **Company**: Espressif Systems
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Page Number and Link**: Page number not visible, "Submit Documentation Feedback" link at the bottom.

(Note: The binary representations are shown as they appear in the image with spaces between bits for clarity.)