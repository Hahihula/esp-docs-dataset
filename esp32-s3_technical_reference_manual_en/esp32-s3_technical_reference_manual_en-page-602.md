**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Link:**
GoBack

**Subtitle:**
Register 10.17. RTC_CNTL_INT_CLR_RTC_REG (0x04C)

**Body Text:**
Continued from the previous page...

- **RTC_CNTL_RTC_MAIN_TIMER_INTEGR_CLR**: Clears the RTC main timer interrupt.
- **RTC_CNTL_RTC_SARADC1_INTEGR_CLR**: Clears the SAR ADC1 interrupt.
- **RTC_CNTL_RTC_TSENS_INTEGR_CLR**: Clears the temperature sensor interrupt.
- **RTC_CNTL_RTC_COCPU_INTEGR_CLR**: Clears the ULP-RISCV interrupt.
- **RTC_CNTL_RTC_SARADC2_INTEGR_CLR**: Clears the SAR ADC2 interrupt.
- **RTC_CNTL_RTC_SWD_INTEGR_CLR**: Clears the super watchdog interrupt.
- **RTC_CNTL_RTC_XTAL32K_DEAD_INTEGR_CLR**: Clears the interrupt triggered when the 32 kHz crystal is dead.
- **RTC_CNTL_RTC_COCPU_TRAP_INTEGR_CLR**: Clears the interrupt triggered when the ULP-RISCV is trapped.
- **RTC_CNTL_RTC_TOUCH_TIMEOUT_INTEGR_CLR**: Clears the interrupt triggered when touch sensor times out.
- **RTC_CNTL_RTC_GLITCH_DET_INTEGR_CLR**: Clears the interrupt triggered when a glitch is detected.
- **RTC_CNTL_RTC TOUCH_APPROACH_LOOP_DONE_INTEGR_CLR**: Clears the interrupt triggered upon completion of a touch approach loop.

**Register 10.18: RTC_CNTL_RTC_STOREO_REG (0x050)**
- **Description:** RTC_CNTL_RTC_SCRATCHIO Retention register

**Footer Information:**
Espressif Systems
602 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback