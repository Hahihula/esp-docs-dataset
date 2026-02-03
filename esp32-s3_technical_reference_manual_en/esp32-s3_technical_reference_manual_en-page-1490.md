**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Section Header (Register):**
Register 39.15. SENS_SAR_MEAS2_CTRL2_REG (0x0030)

**Binary Representation Diagram for Register 39.15:**

- Bits are labeled from right to left as follows:
  - Bit 31
  - ...
  - Bit 4

**Register Description and Values in Text Format:**
```
SENS_MEAS2_DATA_SAR SAR ADC2 data. (RO)
```

```
SENS_MEAS2_DONE_SAR Indicate SAR ADC2 conversion is done. (RO)
```

```
SENS_MEAS2_START_SAR RTC ADC2 controller starts conversion. valid only when
SENS_MEAS2_START FORCE = 1. (R/W)

SENS_MEAS2_START FORCE: 1: RTC ADC2 controller is started by software. 0: RTC ADC2 controller 
is started by ULP coprocessor. (R/W)
```

```
SENS_SAR2_EN_PAD SAR ADC2 pin enable bitmap. Valid only when SENS_SAR2_EN_PADFORCE
= 1. (R/W)

SENS_SAR2_EN_PAD FORCE: 1: SAR ADC2 pin enable bitmap is controlled by software. 0: SAR 
ADC2 pin enable bitmap control is handled by ULP coprocessor. (R/W)
```

**Section Header (Register):**
Register 39.16. SENS_SAR_MEAS2_MUX_REG (0x0034)

**Binary Representation Diagram for Register 39.16:**

- Bits are labeled from right to left as follows:
  - Bit 31
  - ...
  - Bit 4

**Register Description and Values in Text Format:**
```
SENS_SAR2_RTC FORCE In sleep, force to use RTC to control ADC. (R/W)
```

**Footer Information:** 
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

**Link for Submitting Documentation Feedback:** Submit Documentation Feedback