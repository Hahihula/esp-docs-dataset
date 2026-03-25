

# 17.7 Registers

The addresses in this section are relative to RTC Timer base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 17.1. RTC_TIMER_TARO_LOW_REG (0x0000)

```
RTC_TIMER_MAIN_TIMER_TAR_LOW

31
+------------------------------------------+
|                                         |
|                                         | 0
+------------------------------------------+
Reset

RTC_TIMER_MAIN_TIMER_TAR_LOW Configures the low 32 bits of the target time O of the RTC Timer. (R/W)
```

## Register 17.2. RTC_TIMER_TARO_HIGH_REG (0x0004)

```
RTC_TIMER_MAIN_TIMER_TAR_ENO
(reserved) RTC_TIMER_MAIN_TIMER_TAR_HIGH

31    30                         16     15                          0
+---------------------------------------------------------------+
|                                                               | 0
+---------------------------------------------------------------+
Reset

RTC_TIMER_MAIN_TIMER_TAR_HIGH Configures the high 16 bits of the target time O. (R/W)

RTC_TIMER_MAIN_TIMER_TAR_ENO Configures to enable the target time O of the RTC Timer.
    0: Disable
    1: Enable
(WT)
```

Espressif Systems

728
Submit Documentation Feedback
ESP32-C5 TRM (Version 1.0)