**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack**

**Register Information (Section):**
- **Register Name:** SENS_SAR_ATTEN2_REG (0x0038)
- **Field Description for SENS_SAR2_**ATTEN**: 
  - "SENS_SAR2_**ATTEN**" is a 2-bit attenuation setting, used to control the sensitivity of each pin in SAR ADC2. The notation [1:0] indicates that it's set up as channel 0 and [3:2] for channel 1.
- **Field Description for SENS_SAR_POWER_XPD_SAR**: 
  - "SENS_SAR_POWER_XPD_SAR" is a register used to control the power settings of SAR ADC. The fields are:
    - (reserved)
    - "SENSFORCE_XPD_SAR" which configures whether force power up/down function for the SAR ADC.
      - **Values:**
        1. Disable force power up/down
        2. Enable force power up
        3. Enable force power down

**Footer Information:** 
- Page number and document version:
  "Espressif Systems ESP32-S3 TRM (Version 1.7)"
- Link for submitting documentation feedback: [Submit Documentation Feedback](#)