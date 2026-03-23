

```markdown
| Bit | Description |
|-----|-------------|
| 31-24 | (reserved) |
| 23 | RTC_CNTL_XTAL32K_WDT_EN Set this bit to enable the XTAL32K watchdog. (R/W) |
| 22 | RTC_CNTL_XTAL32K_WDT_CLK_FO Set this bit to FPU the XTAL32K watchdog clock. (R/W) |
| 21 | RTC_CNTL_XTAL32K_WDT_RESET Set this bit to reset the XTAL32K watchdog by SW. (R/W) |
| 20 | RTC_CNTL_XTAL32K_EXT_CLK_FO Set this bit to FPU the external clock of XTAL32K. (R/W) |
| 19-17 | RTC_CNTL_XTAL32K_AUTO_BACKUP Set this bit to switch to the backup clock when the XTAL32K is dead. (R/W) |
| 16-14 | RTC_CNTL_XTAL32K_AUTO_RESTART Set this bit to restart the XTAL32K automatically when the XTAL32K is dead. (R/W) |
| 13-11 | RTC_CNTL_XTAL32K_AUTO_RETURN Set this bit to switch back to XTAL32K when the XTAL32K is restarted. (R/W) |
| 10-9 | RTC_CNTL_XTAL32K_XPD_FORCE Set this bit to allow the software to FPD the XTAL32K; Reset this bit to allow the FSM to FPD the XTAL32K. (R/W) |
| 8 | RTC_CNTL_ENCKINIT_XTAL_32K Set this bit to apply an internal clock to help the XTAL32K to start. (R/W) |
| 7-6 | RTC_CNTL_DBUF_XTAL_32K 0: single-end buffer 1: differential buffer. (R/W) |
| 5-4 | RTC_CNTL_DGM_XTAL_32K Configures the xtal_32k gm control. (R/W) |
| 3-2 | RTC_CNTL_DRES_XTAL_32K Configures DRES_XTAL_32K. (R/W) |
| 1-0 | RTC_CNTL_XPD_XTAL_32K Configures XPD_XTAL_32K. (R/W) |
|     | RTC_CNTL_DAC_XTAL_32K Configures DAC_XTAL_32K. (R/W) |
|     | RTC_CNTL_WDT_STATE Indicates the 32 kHz watchdog timer state. (RO) |
|     | RTC_CNTL_XTAL32K_GPIO_SEL Set this bit to select the XTAL32K. Clear this bit to select external XTAL32K. (R/W) |
```