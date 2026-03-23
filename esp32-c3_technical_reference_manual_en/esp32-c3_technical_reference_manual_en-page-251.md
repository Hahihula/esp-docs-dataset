

```markdown
Register 9.30. RTC_CNTL_DIG_ISO_REG (0x008C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | PTC_CNTL_DG_WRAP_FORCE_NOISO | PTC_CNTL_WIFI_FORCE_ISO | PTC_CNTL_CPU_TOP_FORCE_ISO | (reserved) | PTC_CNTL_DG_PAD_FORCE_NOISO | PTC_CNTL_DG_PERI_FORCE_ISO | (reserved) | PTC_CNTL_DG_PAD_HOLD | PTC_CNTL_DG_PAD_UNHOLD | PTC_CNTL_DG_PAD_AUTOHOLD | RTC_CNTL_CLR_DG_PAD_AUTOHOLD | RTC_CNTL_DG_PAD_AUTOHOLD_EN | RTC_CNTL_DG_PAD_FORCE_NOISO | RTC_CNTL_DG_PAD_FORCE_ISO | RTC_CNTL_DG_PAD_FORCE_UNHOLD | RTC_CNTL_DG_PAD_FORCE_HOLD | RTC_CNTL_DG_PERI_FORCE_ISO | RTC_CNTL_DG_PERI_FORCE_NOISO | RTC_CNTL_CPU_TOP_FORCE_ISO | RTC_CNTL_CPU_TOP_FORCE_NOISO | RTC_CNTL_WIFI_FORCE_ISO | RTC_CNTL_WIFI_FORCE_NOISO | RTC_CNTL_DG_WRAP_FORCE_ISO | RTC_CNTL_DG_WRAP_FORCE_NOISO |
| Value (Reset) | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
```

RTC_CNTL_DG_PAD_AUTOHOLD Indicates the auto-hold status of the digital GPIOs. (RO)

RTC_CNTL_CLR_DG_PAD_AUTOHOLD Set this bit to clear the auto-hold enabler for the digital GPIOs. (WO)

RTC_CNTL_DG_PAD_AUTOHOLD_EN Set this bit to allow the digital GPIOs to enter the auto-hold status. (R/W)

RTC_CNTL_DG_PAD_FORCE_NOISO Set this bit to disable the force isolation of the digital GPIOs. (R/W)

RTC_CNTL_DG_PAD_FORCE_ISO Set this bit to force isolation of the digital GPIOs. (R/W)

RTC_CNTL_DG_PAD_FORCE_UNHOLD Set this bit the force unhold the digital GPIOs. (R/W)

RTC_CNTL_DG_PAD_FORCE_HOLD Set this bit the force hold the digital GPIOs. (R/W)

RTC_CNTL_DG_PERI_FORCE_ISO Set this bit to force isolation of the digital peripherals. (R/W)

RTC_CNTL_DG_PERI_FORCE_NOISO Set this bit to disable the force isolation of the digital peripherals. (R/W)

RTC_CNTL_CPU_TOP_FORCE_ISO Set this bit to force hold the CPU. (R/W)

RTC_CNTL_CPU_TOP_FORCE_NOISO Set this bit to force unhold the CPU. (R/W)

RTC_CNTL_WIFI_FORCE_ISO Set this bit to force isolation of the wireless circuits. (R/W)

RTC_CNTL_WIFI_FORCE_NOISO Set this bit to disable the force isolation of the wireless circuits. (R/W)

RTC_CNTL_DG_WRAP_FORCE_ISO Set this bit to force isolation of the digital system. (R/W)

RTC_CNTL_DG_WRAP_FORCE_NOISO Set this bit to disable the force isolation of the digital system. (R/W)
```