

# 15.7 Registers

The addresses in this section are relative to RTC Timer base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 15.1. RTC_TIMER_TARO_LOW_REG (0x0000)

```
RTC_TIMER_MAIN_TIMER_TAR_LOW0
-------------------------------------------------
|                   31                                 | 0   |
------------------------------------------------- Reset

RTC_TIMER_MAIN_TIMER_TAR_LOW0 Configures the low 32 bits of the target time 0 of the RTC Timer. (R/W)
```

## Register 15.2. RTC_TIMER_TARO_HIGH_REG (0x0004)

```
RTC_TIMER_MAIN_TIMER_TAR_HIGO
-------------------------------------------------
|                   31                                 | 0   |
------------------------------------------------- Reset

RTC_TIMER_MAIN_TIMER_TAR_ENO Configures to enable the target time 0 of the RTC Timer.
    0: Disable
    1: Enable
(WT)

RTC_TIMER_MAIN_TIMER_TAR_HIGH0 Configures the high 16 bits of the target time 0. (R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-C61 TRM (Pre-release v0.5)  
PRELIMINARY