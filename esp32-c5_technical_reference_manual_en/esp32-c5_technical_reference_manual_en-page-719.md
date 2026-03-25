

```markdown
Register 16.6. RTC_WDT_FEED_REG (0x0014)

RTC_WDT_FEED    Configures this bit to feed the RWDT.
O: Invalid
1: Feed RWDT
(WT)
```

```markdown
Register 16.7. RTC_WDT_WPROTECT_REG (0x0018)

RTC_WDT_WKEY    Configures this field to lock or unlock RWDT's configuration registers.
0x50D83AA1: unlock the RWDT configuration register
Other values: lock the RWDT configuration register which can't be modified by software.
(R/W)
```