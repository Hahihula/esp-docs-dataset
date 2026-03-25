

```markdown
Register 15.21. TIMG_INT_ENA_TIMERS_REG (0x0070)

TIMG_TO_INT_ENA Write 1 to enable the TIMG_TO_INT interrupt. (R/W)
TIMG_WDT_INT_ENA Write 1 to enable the TIMG_WDT_INT interrupt. (R/W)

Register 15.22. TIMG_INT_RAW_TIMERS_REG (0x0074)

TIMG_TO_INT_RAW The raw interrupt status bit of the TIMG_TO_INT interrupt. (R/SS/WTC)
TIMG_WDT_INT_RAW The raw interrupt status bit of the TIMG_WDT_INT interrupt. (R/SS/WTC)

Register 15.23. TIMG_INT_ST_TIMERS_REG (0x0078)

TIMG_TO_INT_ST The masked interrupt status bit of the TIMG_TO_INT interrupt. (RO)
TIMG_WDT_INT_ST The masked interrupt status bit of the TIMG_WDT_INT interrupt. (RO)
```