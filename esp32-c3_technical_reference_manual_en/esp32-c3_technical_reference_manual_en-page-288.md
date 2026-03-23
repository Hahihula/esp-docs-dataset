

# Chapter 11

## Timer Group (TIMG)

### 11.1 Overview

General purpose timers can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. As shown in Figure 11.1-1, the ESP32-C3 chip contains two timer groups, namely timer group 0 and timer group 1. Each timer group consists of one general purpose timer referred to as TO and one Main System Watchdog Timer. All general purpose timers are based on 16-bit prescalers and 54-bit auto-reload-capable up-down counters.

![Figure 11.1-1. Timer Units within Groups](image-placeholder)

Note that while the Main System Watchdog Timer registers are described in this chapter, their functional description is included in the Chapter 12 Watchdog Timers (WDT). Therefore, the term 'timers' within this chapter refers to the general purpose timers.

The timers’ features are summarized as follows:

- A 16-bit clock prescaler, from 2 to 65536
- A 54-bit time-base counter programmable to incrementing or decrementing
- Able to read real-time value of the time-base counter
- Halting and resuming the time-base counter
- Programmable alarm generation
- Timer value reload (Auto-reload at alarm or software-controlled instant reload)
- Level interrupt generation