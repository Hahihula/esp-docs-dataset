

```markdown
Register 14.11. RTC_WDT_INT_ST_REG (0x002C)

RTC_WDT_INT_ST    Represents the SWD whether or not generates and sends timeout interrupt to CPU.
                  O: No
                  1: Yes
                  (RO)

RTC_WDT_INT_ST    Represents the RWDT whether or not generates and sends timeout interrupt to CPU.
                  O: No
                  1: Yes
                  (RO)

Register 14.12. RTC_WDT_INT_ENA_REG (0x0030)

RTC_WDT_SUPER_WDT_INT_ENA   Configure whether or not to enable the SWD to send timeout interrupt.
                            O: Disable
                            1: Enable
                            (R/W)

RTC_WDT_INT_ENA   Configure whether or not to enable the RWDT to send timeout interrupt.
                  O: Disable
                  1: Enable
                  (R/W)
```