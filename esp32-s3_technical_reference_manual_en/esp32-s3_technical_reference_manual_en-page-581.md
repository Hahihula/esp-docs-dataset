**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Titles and Content:**

---

### **10.4.5 Reject Sleep**

ESP32-S3 implements a hardware mechanism that equips the chip with the ability to reject to sleep, which prevents the chip from going to sleep unexpectedly when some peripherals are still working but not detected by the CPU, thus guaranteeing the proper functioning of the peripherals.

All the wakeup sources specified in Table 10.4-3 (except UART) can also be configured as the causes to reject sleep.

Users can configure the reject to sleep option via the following registers:

- Configure the `RTC_CNTL_RTC_SLEEP_REJECT_ENA` field to enable or disable the option to reject to sleep:
  - Set `RTC_CNTL_LIGHT_SLP_REJECT_EN` to enable reject-to-light-sleep.
  - Set `RTC_CNTL_DEEP_SLP_REJECT_EN` to enable reject-to-deep-sleep.

Read `RTC_CNTL_SLP_REJECT_CAUSE_REG` to check the reason for rejecting to sleep.

---

### **10.5 Retention DMA**

ESP32-S3 can power off the CPU in the Light-sleep mode to further reduce the power consumption. To facilitate the CPU to wake up from Light-sleep and resume execution from the previous breakpoint, ESP32-S3 introduced a retention DMA.

ESP32-S3’s retention DMA stores CPU information to the Internal SRAM Block2 to Block8 before CPU enters into sleep, and restore such information from Internal SRAM to CPU after CPU wakes up from sleep, thus enabling the CPU to resume execution from the previous breakpoint.

ESP32-S3's Retention DMA:

- **Retention DMA operates on date of 128 bits**, and only supports address alignment of four words.
- **Retention DMA’s link list is specifically designed that it can be used to execute both write and read transactions**. The configuration of Retention DMA is similar to that of GDMA:
  1. First allocate enough memory in SRAM before CPU enters sleep to store 432 words*: CPU registers (428 words) and configuration information (4 words).
  2. Then configure the link list according to the memory allocated in the first step. See details in Chapter 3 GDMA Controller (GDMA).

**Note:**
* Note that if the memory allocated is smaller than 432 words, then chip can only enter the Light-sleep mode and cannot further power down CPU.

After configuration, users can enable the Retention function by configuring the `RTC_CNTL_RETENTION_EN` field in Register `RTC_CNTL_RETENTION_CTRL_REG` to:

- Use Retention DMA to store CPU information before the chip enters sleep
- Restore information from Retention DMA to CPU after CPU wakes up. 

---

**Footer:**
Espressif Systems  
581 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback