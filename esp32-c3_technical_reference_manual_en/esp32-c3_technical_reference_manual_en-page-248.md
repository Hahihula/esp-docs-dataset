

```markdown
Register 9.25. RTC_CNTL_CLK_CONF_REG (0x0070)

Continued from the previous page...

RTC_CNTL_FOSC_DFreq        Configures the FOSC frequency. (R/W)
RTC_CNTL_FOSC_FORCE_PD     Set this bit to FPD FOSC. (R/W)
RTC_CNTL_FOSC_FORCE_PU     Set this bit to FPU FOSC. (R/W)
RTC_CNTL_XTAL_GLOBAL_FORCE_GATING   Set this bit to force enable XTAL clock gating. (R/W)
RTC_CNTL_XTAL_GLOBAL_FORCE_NOGATING  Set this bit to force bypass the XTAL clock gating.
(R/W)

RTC_CNTL_FAST_CLK_RTC_SEL  Selects the RTC fast clock. 0: XTAL_DIV_CLK, 1: RC_FAST_CLK
div n. (R/W)

RTC_CNTL_ANA_CLK_RTC_SEL   Selects the RTC slow clock. 0: RC_SLOW_CLK, 1: XTAL32K_CLK,
2: RC_FAST_DIV_CLK. (R/W)


Register 9.26. RTC_CNTL_SLOW_CLK_CONF_REG (0x0074)

| Bit | Description                              |
|-----|-------------------------------------------|
| 31  | (reserved)                               |
| 30  | RTC_CNTL_ANA_CLK_DIV_VLD                 |
| 23  | RTC_CNTL_ANA_CLK_DIV                     |
| 22  | RTC_CNTL_ANA_CLK_DIV_VLD                 |
| ... | ...                                     |
| 0   | Reset                                    |

RTC_CNTL_ANA_CLK_DIV_VLD Synchronizes the reg_fosc_div_sel. Note that you have to invalidate the bus before modifying the frequency divider, and then validate the new divider clock.
(R/W)

RTC_CNTL_ANA_CLK_DIV Configures the divider for the RTC clock. (R/W)4
```