**Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Subtitle:**
Register 2.6. SENS_SAR_COCPU_INT_ENA_REG (0x00EC)

**Body Text/Table:**

- **Table Header:** 
  - Bits 31 to 0

- **Table Content:**
  - Bit 31: Reserved
  - Bit 30 down to bit 24:
    - SENS_COCPU_TOUCH_DONE_INT_ENA (interrupt enable bit. (R/W))
    - SENS_COCPU_TOUCH_INACTIVE_INT_ENA (interrupt enable bit. (R/W))
    - SENS_COCPU TOUCH_ACTIVE_INT_ENA (interrupt enable bit. (R/W))
  - Bit 23:
    - SENS_COCPU_SARADC1_INT_ENA (interrupt enable bit. (R/W))
  - Bit 22 to bits 0: 
    - SENS_COCPU_SARADC2_INT_ENA
    - SENS_COCPU_TSENS_INT_ENA TSENSDONE_INT (interrupt enable bit. (R/W))
    - SENS_COCPU_START_INT_ENA RISCV START_INT (interrupt enable bit. (R/W))
    - SENS_COCPU_SW_INT_ENA SW_INT (interrupt enable bit. (R/W))
    - SENS_COCPU_SWD_INT_ENA SWDINT (interrupt enable bit. (R/W))
  - Bit 19:
    - SENS_COCPU_TOUCH_TIME_OUT_INT_ENA TOUCH TIME OUT interrupt enable bit. (R/W)
  - Bit 18 to bits 0: 
    - SENS_COCPU_TOUCH_APPROACH LOOP DONE INT TOUCH APPROACH LOOP DONE INT interrupt enable bit. (R/W)

**Footer:**
Espressif Systems
338 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback