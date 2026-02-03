**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Header:**
GoBack

**Subsection with Register Information and Description:**

- **Register Name:** RMT_CHn_CARRIER_DUTY_REG (n: 0-3) (0x080+0x4*n)
  
  - **Field Descriptions:**
    - `RMT_CARRIER_LOW_CHn`:
      - Offset: 16
      - Description: This field is used to configure carrier wave's low level clock period for channel n. (R/W)

    - `RMT_CARRIER_HIGH_CHn`:
      - Offset: 15
      - Description: This field is used to configure carrier wave's high level clock period for channel n. (R/W)
  
- **Register Name:** RMT_CHn_TX_LIM_REG (n: 0-3) (0x0A0+0x4*n)

  - **Field Descriptions:**
    - `RMT_TX_LIM_CHn`:
      - Offset: 18
      - Description: This field is used to configure the maximum entries that channel n can send out. (R/W)
  
    - `RMT_TX_LOOP_NUM_CHn`:
      - Offset: 20-19, 35-34 
      - Description: This field is used to configure the maximum loop count when continuous TX mode is enabled. (R/W)

    - `RMT_TX_LOOP_CNT_EN_CHn`:
      - Offset: 36
      - Description: This bit is the enable bit for loop counting. (R/W)
  
    - `RMT_LOOP_COUNT_RESET_CHn`:
      - Offset: 17-0, 42 
      - Description: This bit is used to reset the loop count when continuous TX mode is enabled. (WT)

    - `RMT_LOOP_STOP_EN_CHn`:
      - Offset: 38
      - Description: Set this bit if the loop counting reaches the value set in RMT_TX_LOOP_CNT_EN_CHn, continuous TX mode will be stopped.

**Footer Information:** 
Espressif Systems  
1438 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback