**Chapter Title:**
Chapter 11 Watchdog Timers (WDT)

**Section Heading and Subsection with Content:**

### **11.3.2 Operating Procedure**

When a watchdog timer is enabled, it will proceed in loops from stage 0 to stage 3, then back to stage 0 and start again. The expiry action and time period for each stage can be configured individually.

Every stage can be configured for one of the following actions when the expiry timer reaches the stage’s timeout value:

- Trigger an interrupt
  - When the stage expires an interrupt is triggered.
  
- Reset a CPU core
  - When the stage expires the designated CPU core will be reset. MWDT0 CPU reset only resets the PRO CPU, MWDT1 CPU reset only resets the APP CPU. The RWDT CPU reset can reset either of them, or both, or none, depending on configuration.

- Reset the main system
  - When the stage expires, the main system including the MWDTs will be reset. In this article, the main system includes the CPU and all peripherals. The RTC is an exception to this; it will not be reset.
  
- Reset the main system and RTC
  - When the stage expires the main system and the RTC will both be reset. This action is only available in the RWDT.

- Disabled
  - This stage will have no effects on the system.

When software feeds the watchdog timer, it returns to stage O and its expiry counter restarts from O.

### **11.3.3 Write Protection**

Both the MWDTs as well as the RWDT can be protected from accidental writing. To accomplish this they have a write-key register (TIMGn_WDTWPROTECT_REG for the MWDT, RTC_CNTRL_WDTWPROTECT_REG for the RWDT.) On reset these registers are initialized to the value 0x5D83AA1. When the value in this register is changed from 0x5D83AA1, write protection is enabled. Writes to any WDT register including the feeding register (but excluding the write-key register itself) will be ignored. The recommended procedure for accessing a WDT is:

1. Disable the write protection
2. Make the required modification or feed the watchdog
3. Re-enable the write protection

### **11.3.4 Flash Boot Protection**

During flash booting, the MWDT in timer group 0 (TIMG0), as well as the RWDT are automatically enabled. Stage O for the enabled MWDT is automatically configured to reset the system upon expiry: stage 0 for the RWDT resets the RTC when it expires. After booting; the register TIMERS_WDT_FLASHBOOT_MOD_EN should be cleared to stop the flash boot protection procedure for the MWDT, and RTC_CNTRL_WDT_FLASHBOOT_MOD_EN should also be cleared so do the same for the RWDT. After this, the MWDT and RWDT can be configured by software.

**Footer:**
Espressif Systems
Page number 235 (ESP32 TRM - Version 5.6)
Submit Documentation Feedback