**Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Subtitle:**
Register 2.5. SENS_SAR_COOPU_INT_RAW_REG (0x00E8)

**Body Text/Table:**

- **Table Header:** 
  - Bits | Description
  - 31 to 0

- **Table Content:**
  - Bit 31, Reserved.
  - Bit 30 down to bit 24:
    - SENS_COOPU_TOUCH_SCAN_DONE_INT_RAW (reserved)
  - Bit 23 and below are interrupt raw bits for various touch-related events with corresponding descriptions such as:
    - TOUCH DONE INT
    - TOUCH ACTIVE INT
    - TOUCH START INT
    - SWI INT
    - TSENS DONE INT
    - RISCV START INT
    - SWI RAW
    - SWD INT
    - TOUCH TIME OUT INT
    - TOUCH APPROACH LOOP DONE INT

- **Interrupt Raw Bits:**
  - SENS_COOPU_TOUCH_DOINE_INT_RAW (interrupt raw bit. (RO))
  - SENS_COOPU_TOUCH_INACTIVE_INT_RAW (interrupt raw bit. (RO))
  - SENS_COOPU_TOUCH_ACTIVE_INT_RAW (interrupt raw bit. (RO))
  - SENS_COOPU_SARADC1_INT_RAW
  - SENS_COOPU_SARADC2_INT_RAW
  - SENS_COOPU_TSENS_INT_RAW
  - SENS_COOPU_START_INT_RAW
  - SENS_COOPU_SW_INT_RAW
  - SENS_COOPU_SWD_INT_RAW

- **Interrupt Raw Bits (continued):**
  - SENS_COOPU_TOUCH_TIME_OUT_INT
  - SENS_COOPU TOUCH SCAN DONE INT
  - SENS_COOPU TOUCH START INT
  - SENS_COOPU TOUCH ACTIVE INT
  - SENS_COOPU TOUCH INACTIVE INT

**Footer:**
Espressif Systems  
337  
ESP32-S3 TRM (Version 1.7)  

**Link:**
Submit Documentation Feedback