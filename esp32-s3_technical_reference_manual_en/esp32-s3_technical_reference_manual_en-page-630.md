**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.60. RTC_CNTL_INT_ENA_RTC_W1TS_REG (0x0138)

**Continuation Note:**
Continued from the previous page...

**Body Text with List Items and Descriptions for Each Field:**

- **RTC_CNTL_RTC_BROWN_OUT_INT_ENA_W1TS**: Enables the brown out interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_BROWN_OUT_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC_MAIN_TIMER_INT_ENA_W1TS**: Enables the RTC main timer interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTCMain_TIMER_INT_ENA field will be set to 1.

- **RTC_CNTL_RTC_SARADC1_INT_ENA_W1TS**: Enables the SAR ADC1 interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_SARADC1_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC_TSENS_INTE_W1TS**: Enables the temperature sensor interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_TSENS_INTE field will be set to 1.

- **RTC_CNTL_RTC_COCPU_INT_ENA_W1TS**: Enables the ULP-RISCV interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_COCPU_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC_SARADC2_INTE_W1TS**: Enables the SAR ADC2 interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_SARADC2_INTE field will be set to 1.

- **RTC_CNTL_RTC_SWD_INT_ENA_W1TS**: Enables the super watchdog interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_SWD_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC_XTAL32K_DEAD_INTE_W1TS**: Enables interrupt when the 32 kHz crystal is dead. If the value 1 is written to this bit, the RTC_CNTL_RTC_XTAL32K_DEAD_INTE field will be set to 1.

- **RTC_CNTL_RTC_COCPU_TTRAP_INT_ENA_W1TS**: Enables interrupt when the ULP-RISCV is trapped. If the value 1 is written to this bit, the RTC_CNTL_RTC_COCPU_TTRAP_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC TOUCH_TIMEOUT_INTE_W1TS**: Enables interrupt when touch sensor times out. If the value 1 is written to this bit, the RTC_CNTL_RTC_TOUCH_TIMEOUT_INTE field will be set to 1.

- **RTC_CNTL_RTC_GLITCH_DET_INT_ENA_W1TS**: Enables interrupt when a glitch is detected. If the value 1 is written to this bit, the RTC_CNTL_RTC_GLITCH_DET_INT_ENA field will be set to 1.
  
- **RTC_CNTL_RTC_TOUCH_APPROACH_LOOP_DONE_INTE_W1TS**: Enables interrupt upon completion of a touch approach loop. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH_APPROACH_LOOP_DONE_INTE field will be set to 1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)