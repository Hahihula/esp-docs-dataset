

```markdown
Register 15.6. RTC_WDT_FEED_REG (0x0014)

RTC_WDT_RTC_WDT_FEED    Configure this bit to feed the RWDT.
O: Invalid
1: Feed RWDT
(WT)
```

```markdown
Register 15.7. RTC_WDT_WPROTECT_REG (0x0018)

RTC_WDT_WKEY   Configure this field to lock or unlock RWDT's configuration registers.
0x50D83AA1: unlock the RWDT configuration register
Others value: lock the RWDT configuration register which can't be modified by software.
(R/W)
```