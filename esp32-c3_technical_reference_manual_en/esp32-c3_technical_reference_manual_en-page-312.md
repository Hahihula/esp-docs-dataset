

# Chapter 13

## XTAL32K Watchdog Timers (XTWDT)

### 13.1 Overview

The XTAL32K watchdog timer on ESP32-C3 is used to monitor the status of external crystal XTAL32K_CLK. This watchdog timer can detect the oscillation failure of XTAL32K_CLK, change the clock source of RTC, etc.

When XTAL32K_CLK works as the clock source of RTC_SLOW_CLK (for clock description, see Chapter 6 Reset and Clock) and stops vibrating, the XTAL32K watchdog timer first switches to BACKUP32K_CLK derived from RC_SLOW_CLK and generates an interrupt (if the chip is in Light-sleep and Deep-sleep mode, the CPU will be woken up), and then switches back to XTAL32K_CLK after it is restarted by software.

![Figure 13.1-1. XTAL32K Watchdog Timer](image)

### 13.2 Features

#### 13.2.1 Interrupt and Wake-Up

When the XTAL32K watchdog timer detects the oscillation failure of XTAL32K_CLK, an oscillation failure interrupt RTC_XTAL32K_DEAD_INT (for interrupt description, please refer to Chapter 9 Low-power Management) is generated. At this point, the CPU will be woken up if in Light-sleep and Deep-sleep mode.

Espressif Systems
Submit Documentation Feedback
ESP32-C3 TRM (Version 1.3)
312