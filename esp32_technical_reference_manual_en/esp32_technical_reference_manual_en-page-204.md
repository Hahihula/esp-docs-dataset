**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Header:**
GoBack

**Register Information:**
- **Register Name:** RTC_CNTL_INT_RAW_REG (0x0040)
- **Description:** The raw interrupt status bit for various interrupts.

**Interrupt Status Bits Description Table:**

| Offset | Bit Number | Register Name                          |
|--------|-----------|----------------------------------------|
| 31     | -         | Reserved                               |
| ...    | ...       | ...                                    |

**Interrupt Status Bits List with Descriptions and Access Type (RO for Read-Only):**
- RTC_CNTL_MAIN_TIMER_INT_RAW
- RTC_CNTLMainTimerIntRaw: The raw interrupt status bit for the RTC_CNTL_MAIN_TIMER_INT interrupt. (RO)
- RTC_CNTL_BROWN_OUT_INT_RAW
- RTC_CNTLBrownOutIntRaw: The raw interrupt status bit for the RTC_CNTL_BROWN_OUT_INT interrupt. (RO)
- RTC_CNTL_TOUCH_INTEGR原材料
- RTC_CNTLTouchIntRaw: The raw interrupt status bit for the RTC_CNTL_TOUCH_INTEGR原材料 interrupt. (RO)
- RTC_CNTL_ULP_CP_INT_RAW
- RTCUNCTLULPCPIRaw: The raw interrupt status bit for the RTC_CNTL_ULP_CP_INT interrupt. (RO)
- RTC_CNTL_TIME_VALID_INTEGR原材料
- RTCUNCTLTimeValidIntRaw: The raw interrupt status bit for the RTC_CNTL_TIME_VALID_INTEGR原材料 interrupt. (RO)
- RTC_CNTL_WDT_INTEGR原材料
- RTCUNCTLWDTIRRaw: The raw interrupt status bit for the RTC_CNTL_WDT_INTEGR原材料 interrupt. (RO)
- RTC_CNTL_SDIO_IDLE_INT_RAW
- RTCUNCTLSDIOTERRaw: The raw interrupt status bit for the RTC_CNTL_SDIO_IDLE_INT interrupt. (RO)
- RTC_CNTL_SLP_REJECT_INTEGR原材料
- RTCUNCTLSLRPRejectIntRaw: The raw interrupt status bit for the RTC_CNTL_SLP_REJECT_INTEGR原材料 interrupt. (RO)
- RTC_CNTL_SLP_WAKEUP_INTEGR原材料
- RTCUNCTLSLPRWakeUpIntRaw: The raw interrupt status bit for the RTC_CNTL_SLP_WAKEUP_INTEGR原材料 interrupt. (RO)

**Footer Information:**
Espressif Systems  
Page 204 ESP32 TRM (Version 5.6)  

**Link:**
Submit Documentation Feedback