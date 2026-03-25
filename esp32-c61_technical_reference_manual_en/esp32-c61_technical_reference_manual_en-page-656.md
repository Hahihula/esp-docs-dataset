

```markdown
Register 14.9. RTC_WDT_SWDPWPROTECT_REG (0x0020)

RTC_WDT_SWD_WKEY Configures this field to lock or unlock SWD's configuration registers.
0x50D83AA1: unlock the SWD configuration register.
Other values: lock the SWD configuration register which can't be modified by the software.
(R/W)
```

```markdown
Register 14.10. RTC_WDT_INT_RAW_REG (0x0024)

RTC_WDT_SWD_INT_RAW The raw interrupt status of RTC_WDT_SWD_INT interrupt.(R/WTC/SS)
RTC_WDT_INT_RAW The raw interrupt status of RTC_WDT_INT interrupt. (R/WTC/SS)
```

```markdown
Register 14.11. RTC_WDT_INT_ST_REG (0x0028)

RTC_WDT_SWD_INT_ST The masked interrupt status of RTC_WDT_SWD_INT interrupt.(RO)
RTC_WDT_INT_ST The masked interrupt status of RTC_WDT_INT interrupt.(RO)
```