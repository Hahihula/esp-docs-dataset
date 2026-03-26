

```markdown
Register 16.21. TIMG_INT_ENA_TIMERS_REG (0x0070)

TIMG_Tx_INT_ENA (x: 0-1)    Write 1 to enable the TIMG_Tx_INT interrupt. (R/W)
TIMG_WDT_INT_ENA            Write 1 to enable the TIMG_WDT_INT interrupt. (R/W)

Register 16.22. TIMG_INT_RAW_TIMERS_REG (0x0074)

TIMG_Tx_INT_RAW (x: 0-1)    The raw interrupt status bit of the TIMG_Tx_INT interrupt. (R/SS/WTC)
TIMG_WDT_INT_RAW            The raw interrupt status bit of the TIMG_WDT_INT interrupt. (R/SS/WTC)

Register 16.23. TIMG_INT_ST_TIMERS_REG (0x0078)

TIMG_Tx_INT_ST (x: 0-1)     The masked interrupt status bit of the TIMG_Tx_INT interrupt. (RO)
TIMG_WDT_INT_ST             The masked interrupt status bit of the TIMG_WDT_INT interrupt. (RO)
```