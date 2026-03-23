

# Chapter 14

## Timer Group (TIMG)

### 14.1 Overview

General-purpose timers can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. As shown in Figure 14.1-1, the ESP32-C6 chip contains two timer groups, namely timer group 0 and timer group 1. Each timer group consists of one general-purpose timer referred to as T0 and one Main System Watchdog Timer. The general-purpose timer is based on a 16-bit prescaler and a 54-bit auto-reload-capable up-down counter.

![Figure 14.1-1. Timer Group Overview](image-placeholder)

Note that while the Main System Watchdog Timer registers are described in this chapter, their functional description is included in the Chapter 15 Watchdog Timers (WDT). Therefore, the term "timer" within this chapter refers to the general-purpose timer.

### 14.2 Features

The timer's features are summarized as follows:

- A 54-bit time-base counter programmable to incrementing or decrementing
- Three clock sources: PLL_F80M_CLK or XTAL_CLK or RC_FAST_CLK
- A 16-bit clock prescaler, from 2 to 65536
- Able to read real-time value of the time-base counter
- Able to halt and resume the time-base counter
- Programmable alarm generation