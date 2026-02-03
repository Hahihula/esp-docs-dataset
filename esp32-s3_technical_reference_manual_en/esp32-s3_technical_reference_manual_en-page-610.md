**Title: Chapter 10 Low-power Management (RTC_CNTL)**

**Header: Register 10.29. RTC_CNTL_RTC_PWC_REG (0x088)**

**Binary Diagram Description:**  
A binary diagram is provided showing the layout of bits in a register, with labels for each bit from "RTC_CNTL_RTC_PAD_FORC_HLD" to "RTC_CNTL_RTC_FORCE_ISO". The positions are numbered 31 down to 0.

**Body Text:**

- **Field Name**: RTC_CNTL_RTC FORCE ISO  
  - Description: Set this bit to force isolate the RTC peripherals. (R/W)

- **Field Name**: RTC_CNTL_RTC FORCE NOISO  
  - Description: Set this bit to disable the force isolation on the RTC peripherals. (R/W)

- **Field Name**: RTC_CNTL_RTC FASTMEM FOLLOW CPU  
  - Description: Set 1 to FPD the RTC slow memory when the CPU is powered down. Set 0 to FPD the RTC slow memory when the RTC main state machine is powered down. (R/W)

- **Field Name**: RTC_CNTL_RTC FASTMEM FORCE LPD  
  - Description: Set this bit to force not retain the RTC fast memory. (R/W)

- **Field Name**: RTC_CNTL_RTC FASTMEM FOLLOW LPU  
  - Description: Set this bit to force retain the RTC fast memory. (R/W)

- **Field Name**: RTC_CNTL_RTC SLOWMEM FOLLOW CPU  
  - Description: 
    - "1": RTC memory PD following CPU
    - "0": RTC memory PD following RTC state machine

- **Field Name**: RTC_CNTL_RTC SLOWMEM FORCE LPD  
  - Description: Set this bit to force not retain the RTC slow memory. (R/W)

- **Field Name**: RTC_CNTL_RTC SLOWMEM FORCE LPU  
  - Description: Set this bit to force retain the RTC slow memory. (R/W)

- **Field Name**: RTC_CNTL_RTC FORCE PD  
  - Description: Set this bit to FPD the RTC peripherals. (R/W)

- **Field Name**: RTC_CNTL_RTC FORCE PU  
  - Description: Set this bit to FPU the RTC peripherals. (R/W)

- **Field Name**: RTC_CNTL_RTC PAD_EN  
  - Description: Set this bit to enable PD for the RTC peripherals in sleep. (R/W)

- **Field Name**: RTC_CNTL_RTC PAD FORCE HOLD  
  - Description: Set this bit the force hold the RTC GPIOs. (R/W)

**Footer:**  
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)