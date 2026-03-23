

```markdown
|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|
|:----|:----|:-----|:----|:----|:----|:----|:----|:-------|:--------|:---------|:----------|:-----------|:------------|:-------------|:--------------|:---------------|:-----------------|:------------------|:-------------------|:--------------------|:----------------------|:-----------------------|
|0|0x0| | | | | | | | | | | | | | | | |1|0|0|1|0|0| |
||Reset||
```

RTC_CNTL_WDT_PAUSE_IN_SLP Set this bit to pause the watchdog in sleep. (R/W)

RTC_CNTL_WDT_PROCPU_RESET_EN enable WDT reset CPU (R/W)

RTC_CNTL_WDT_FLASHBOOT_MOD_EN Set this bit to enable watchdog when the chip boots from flash. (R/W)

RTC_CNTL_WDT_SYS_RESET_LENGTH Sets the length of the system reset counter. (R/W)

RTC_CNTL_WDT_CPU_RESET_LENGTH Sets the length of the CPU reset counter. (R/W)

RTC_CNTL_WDT_STG3 1: enable at the interrupt stage, 2: enable at the CPU stage, 3: enable at the system stage, 4: enable at the system and RTC stage. (R/W)

RTC_CNTL_WDT_STG2 1: enable at the interrupt stage, 2: enable at the CPU stage, 3: enable at the system stage, 4: enable at the system and RTC stage. (R/W)

RTC_CNTL_WDT_STG1 1: enable at the interrupt stage, 2: enable at the CPU stage, 3: enable at the system stage, 4: enable at the system and RTC stage. (R/W)

RTC_CNTL_WDT_STGO 1: enable at the interrupt stage, 2: enable at the CPU stage, 3: enable at the system stage, 4: enable at the system and RTC stage. (R/W)

RTC_CNTL_WDT_EN Set this bit to enable the RTC watchdog. (R/W)

Register 9.32. RTC_CNTL_WDTCONFIG1_REG (0x0094)
```markdown
|31| | | | | | | | | | | | | | | | | | | | | | |
|:----|:-----|:------|:-------|
||Reset||
|200000| |
```

RTC_CNTL_WDT_STGO_HOLD Configures the hold time of RTC watchdog at level 1. (R/W)
```