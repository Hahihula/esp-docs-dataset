**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Heading:**
Register No.61. RTC_CNTL_INT_ENA_RTC_W1TC_REG (0x013C)

**Continuation Note:**
Continued from the previous page...

**Body Text with List Items and Descriptions for Each Register:**

- **RTC_CNTL_RTC_TOUCH_INACTIVE_INT_ENA_W1TC**: Clears the interrupt triggered when a touch is released. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH_INACTIVE_INT_CLR field will be cleared.
  
- **RTC_CNTL_RTC_BROWN_OUT_INT_ENA_W1TC**: Clears the brown out interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC BROWN_OUT_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_MAIN_TIMER_INT_ENA_W1TC**: Clears the RTIM main interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC MAIN TIMER_INT_CLR field will be cleared.
  
- **RTC_CNTL_RTC_SARADC1_INT_ENA_W1TC**: Clears the SAR ADC1 interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_SARADC1_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_TSENS_INTEA_W1TC**: Clears the temperature sensor interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_TSENS_INTEA_CLR field will be cleared.
  
- **RTC_CNTL_RTC_COCPU_INT_ENA_W1TC**: Clears the ULP-RISCV interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_COCPU_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_SARADC2_INT_ENA_W1TC**: Clears the SAR ADC2 interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_SARADC2_INT_CLR field will be cleared.
  
- **RTC_CNTL_RTC_SWD_INT_ENA_W1TC**: Clears the super watchdog interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC SWD_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_XTAL32K_DEAD_INT_ENA_W1TC**: Clears the interrupt triggered when the 32 kHz crystal is dead. If the value 1 is written to this bit, the RTC_CNTL_RTC_XTAL32K DEAD_INT_CLR field will be cleared.
  
- **RTC_CNTL_RTC_COCPU_TRAP_INT_ENA_W1TC**: Clears the interrupt triggered when the ULP-RISCV is trapped. If the value 1 is written to this bit, the RTC_CNTL_RTC_COOPU_TRAP_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_TOUCH_TIMEOUT_INT_ENA_W1TC**: Clears the interrupt triggered when touch sensor times out. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH_TIMEOUT_INT_CLR field will be cleared.
  
- **RTC_CNTL_RTC_GLITCH_DET_INT_ENA_W1TC**: Clears the interrupt triggered when a glitch is detected. If the value 1 is written to this bit, the RTC_CNTL_RTC GLITCH_DET_INT_CLR field will be cleared.

- **RTC_CNTL_RTC_TOUCH_APPROACH_LOOP_DONE_INT_ENA_W1TC**: Clears the interrupt triggered upon completion of touch approach loop. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH_APPROACH_LOOP_DONE_INT_CLR field will be cleared.
  
**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)