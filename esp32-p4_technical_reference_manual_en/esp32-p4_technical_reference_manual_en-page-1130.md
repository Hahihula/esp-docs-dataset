

# 18.7 Registers

The addresses in this section are relative to RTC Timer base address provided in Table 7.3-2 in Chapter 7 *System and Memory*.

For how to program reserved fields, please refer to Section *Programming Reserved Register Field*.

## Register 18.1. RTC_TIMER_TARO_LOW_REG (0x0000)

```
RTC_TIMER_MAIN_TIMER_TAR_LOW0
31                                 0
+-----------------------------------------------+
|                                         |
+-----------------------------------------------+
Reset

RTC_TIMER_MAIN_TIMER_TAR_LOW0 Configure the low 32 bits of the target time 0 of the RTC Timer. (R/W)
```

## Register 18.2. RTC_TIMER_TARO_HIGH_REG (0x0004)

```
RTC_TIMER_MAIN_TIMER_TAR_HIGO
(reserved)                         RTC_TIMER_MAIN_TIMER_TAR_HIGO
31                                 16          15                                 0
+-----------------------------------------------+
|                                         |                                         |
+-----------------------------------------------+
Reset

RTC_TIMER_MAIN_TIMER_TAR_HIGO Configure the high 16 bits of the target time 0. (R/W)

RTC_TIMER_MAIN_TIMER_TAR_ENO Configure to enable the target time 0 of the RTC Timer. (WO)
```