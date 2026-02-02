**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header (with backlinks):**

- **Register 31.19, SENS_SAR_TOUCH_ENABLE_REG (0x008c)**
  - **Description of Registers:**
    - `SENS_TOUCH_PAD_OUTEN1`: Bitmap defining SET1 for generating a wakeup interrupt; SET1 is considered touched if at least one of the touch pads in SET1 is touched. (R/W)
    - `SENS TOUCH PAD OUTEN2`: Bitmap defining SET2 for generating a wakeup interrupt; SET2 is considered touched if at least one of the touch pads in SET2 is touched. (R/W)
    - `SENS_TOUCH_PAD_WORKEN`: Bitmap defining the working set during measurement. (R/W)

- **Register 31.20, SENS_SAR_READ_CTRL2_REG (0x0090)**
  - **Description of Registers:**
    - `SENS_SAR2_DATA_INV`: Invert SAR ADC2 data. (R/W)
    - `SENS_SAR2_DIG FORCE`: SAR ADC2 controlled by DIG ADC2 CTRL or PWDET CTRL; O: SAR ADC2 controlled by RTC ADC2 CTRL (R/W)
    - `SENS_SAR2_SAMPLE_BIT`: Bit width of SAR ADC2, 00: for 9-bit, 01: for 10-bit, 10: for 11-bit, 11: for 12-bit. (R/W)
    - `SENS_SAR2_SAMPLE_CYCLE`: Sample cycles of SAR ADC2. (R/W)
    - `SENS_SAR2_CLK_DIV`: Clock divider. (R/W)

---

**Footer Information:** 
- **Company Name:** Espressif Systems
- **Document Version and Link:** ESP32 TRM (Version 5.6) Submit Documentation Feedback

--- 

**Note:**
The image contains a table with binary values for the registers, but it is not fully legible to transcribe accurately in this format due to resolution constraints.

---

**Navigation Links at Bottom of Page:**
- **Submit Documentation Feedback**

(Note: The text "GoBack" appears as part of navigation or interface elements and does not represent content that needs transcription.)