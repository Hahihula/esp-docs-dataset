**Chapter Title:**
Chapter 11 Watchdog Timers (WDT)

**GoBack Link:** [GoBack](#)

---

## Introduction

The ESP32 has three watchdog timers: one in each of the two timer modules (called Main System Watchdog Timer, or MWDT) and one in the RTC module (which is called the RTC Watchdog Timer, or RWDT). These watchdog timers are intended to recover from an unforeseen fault, causing the application program to abandon its normal sequence. A watchdog timer has four stages. Each stage may take one out of three or four actions upon the expiry of a programmed period of time for this stage, unless the watchdog is fed or disabled. The actions are: interrupt, CPU reset, core reset and system reset. Only the RWDT can trigger the system reset, and is able to reset the entire chip and the main system including the RTC itself. A timeout value can be set for each stage individually.

During flash boot, the RWDT and the first MWDT start automatically in order to detect and recover from booting problems.

---

## Features

- Four stages, each of which can be configured or disabled separately
- Programmable time period for each stage
- One out of three or four possible actions (interrupt, CPU reset, core reset and system reset) upon the expiry of each stage
- 32-bit expiry counter
- Write protection, to prevent the RWDT and MWDT configuration from being inadvertently altered.
- Flash boot protection

If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system.

---

## Functional Description

### Clock (Section 11.3.1)

The RWDT is clocked from the RTC slow clock RTC_SLOW_CLK. The MWDT clock source is derived from the APB clock APB_CLK via a pre-MWDT 16-bit configurable prescaler. For either watchdog, the clock source is fed into the 32-bit expiry counter. When this counter reaches the timeout value of the current stage, the action configured for the stage will execute; the expiry counter will be reset and the next stage will become active.

---

**Footer:**
Espressif Systems  
Page number: 234  
Document version: ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)