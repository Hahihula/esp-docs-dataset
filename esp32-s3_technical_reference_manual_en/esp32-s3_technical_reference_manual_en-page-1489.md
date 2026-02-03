**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Register Information (Section):**

- **Register Name**: SENS_SAR1_ATTEN (0x0014)
  - Description: "2-bit attenuation for each pin of SAR ADC1. [1:0] is used for channel 0, [3:2] is used for channel 1, etc." 
  - Access Type: Read/Write
  - Example Value in Hexadecimal (Hex): Oxfffffff

- **Register Name**: SENS_SAR2_CTRL_REG (0x0024)
  - Description:
    - "SENS_SAR2_INTE_N" (reserved)
    - "SENS_SAR2_DATA_INV" (reserved)
    - "SENS_SAR2_INT_EN" Enable SAR ADC2 to send out interrupt. 
      - Access Type: Read/Write
      - Bits and their functions are listed as follows:
        - 31-0, all bits reserved.
        - Bit positions for specific settings from bit 28 down (e.g., SENS_SAR2_CLK_DIV).
    - "SENS_SAR2_CLK_DIV" Clock divider. 
      - Access Type: Read/Write
    - "SENS_SAR2_WAIT_ARB_CYCLE" Wait arbiter stable after SAR_DONE.
      - Access Type: Read/Write
    - "SENS_SAR2_DATA_INV" Invert SAR ADC2 data.
      - Access Type: Read/Write

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Link for Feedback:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback