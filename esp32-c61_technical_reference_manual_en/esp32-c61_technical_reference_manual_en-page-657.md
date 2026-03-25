

```markdown
Register 14.12. RTC_WDT_INT_ENA_REG (0x002C)

RTC_WDT_INT_ENA
RTC_WDT_SWD_INT_ENA

(reserved)

31   30    29
+-----------------------------+
|                               |
|                               | Reset
+-----------------------------+

RTC_WDT_SWD_INT_ENA Write 1 to enable RTC_WDT_SWD_INT. (R/W)
RTC_WDT_INT_ENA     Write 1 to enable RTC_WDT_INT. (R/W)

Register 14.13. RTC_WDT_INT_CLR_REG (0x0030)

RTC_WDT_INT_CLR
RTC_WDT_SWD_INT_CLR

(reserved)

31   30    29
+-----------------------------+
|                               |
|                               | Reset
+-----------------------------+

RTC_WDT_SWD_INT_CLR Write 1 to clear RTC_WDT_SWD_INT. (WT)
RTC_WDT_INT_CLR     Write 1 to clear RTC_WDT_INT. (WT)

Register 14.14. RTC_WDT_DATE_REG (0x03FC)

RTC_WDT_CLK_EN
RTC_WDT_DATE

31   30
+-----------------------------+
|                               |
|                               | Reset
+-----------------------------+

0x2112080

RTC_WDT_DATE Version control register. (R/W)
RTC_WDT_CLK_EN Reserved. (R/W)
```