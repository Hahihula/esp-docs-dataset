**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section Header:**
Register 31.21. SENS_SAR_meas_START2_REG (0x0094)

**Binary Diagram Description for SENS_SAR2_EN_PAD FORCE:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 31
  - Bit 30 and onwards

**Text Explanation under SENS_SAR2_EN_PAD FORCE:**
SENS_SAR2_EN_PAD FORCE: 1: SAR ADC2 pad enable bitmap is controlled by SW, O: SAR ADC2 pad enable bitmap is controlled by ULP coprocessor. (R/W)

**Register Description for SENS_SAR2_EN_PAD FORCE:**
SENS_SAR2_EN_PAD: SAR ADC2 pad enable bitmap; active only when reg_sar2_en_pad_force = 1. (R/W)

**Binary Diagram Description for SENS_meas2_START FORCE:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_meas2_START FORCE:**
SENS_meas2_START FORCE: 1: SAR ADC2 controller (in RTC) is started by SW, O: SAR ADC2 controller is started by ULP coprocessor. (R/W)

**Register Description for SENS_meas2_START FORCE:**
SENS_meas2_START FORCE: SAR ADC2 controller (in RTC) starts conversion; active only when reg_meas2_start_force = 1. (R/W)

**Binary Diagram Description for SENS_meas2_DONE_SAR:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_meas2_DONE_SAR:**
SENS_meas2_DONE_SAR: SAR ADC2-conversion-done indication. (RO)

**Binary Diagram Description for SENS_meas2_DATA_SAR:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_meas2_DATA_SAR:**
SENS_meas2_DATA_SAR: SAR ADC2 data. (RO)

---

**Section Header:**
Register 31.22. SENS_SAR_DAC_CTRL1_REG (0x0098)

**Binary Diagram Description for SENS_DAC_CLK_INV:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 31
  - Bit 30 and onwards

**Text Explanation under SENS_DAC_CLK_INV:**
SENS_DAC_CLK_INV: 1: inverts PDAC_CLK, O: no inversion. (R/W)

**Binary Diagram Description for SENS_DAC_CLK FORCE_HIGH:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_DAC_CLK FORCE_HIGH:**
SENS_DAC_CLK FORCE_HIGH forces PDAC_CLK to be 1. (R/W)

**Binary Diagram Description for SENS_DAC_CLK FORCE_LOW:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_DAC_CLK FORCE_LOW:**
SENS_DAC_CLK FORCE_LOW forces PDAC_CLK to be O. (R/W)

**Binary Diagram Description for SENS_DAC_DIG FORCE:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_DAC_DIG FORCE:**
SENS_DAC_DIG FORCE: 1: DAC1 & DAC2 use DMA, O: DAC1 & DAC2 do not use DMA. (R/W)

**Binary Diagram Description for SENS_SW_TONE_EN:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_SW_TONE_EN:**
SENS_SW_TONE_EN: 1: enable CW generator, O: disable CW generator. (R/W)

**Binary Diagram Description for SENS_SW_FSTEP:**
- Binary representation of the register with bits labeled from right to left.
- Bits are numbered as follows:
  - Bit 30
  - Bit 29 and onwards

**Text Explanation under SENS_SW_FSTEP:**
SENS_SW_FSTEP Frequency step for CW generator; can be used to adjust the frequency. (R/W)

---

**Footer Information:** 
Espressif Systems  
758  
ESP32 TRM (Version 5.6)  

**Link Text at Bottom of Page:** Submit Documentation Feedback