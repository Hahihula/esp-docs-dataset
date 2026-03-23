

```markdown
Register 15.11. RTC_WDT_INT_ST_REG (0x0028)

RTC_WDT_INT_ST    RTC_WDT_SWD_INT_ST

RTC_WDT_SWD_INT_ST Represents the SWD whether or not generates and sends timeout interrupt to CPU.
O: No
1: Yes
(RO)

RTC_WDT_INT_ST Represents the RWDT whether or not generates and sends timeout interrupt to CPU.
O: No
1: Yes
(RO)

Register 15.12. RTC_WDT_INT_ENA_REG (0x002C)

RTC_WDT_INT_ENA    RTC_WDT_SWD_INT_ENA

RTC_WDT_SWD_INT_ENA Configure whether or not to enable the SWD to send timeout interrupt.
O: Disable
1: Enable
(R/W)

RTC_WDT_INT_ENA Configure whether or not to enable the RWDT to send timeout interrupt.
O: Disable
1: Enable
(R/W)
```