

```markdown
Chapter 9 Low-power Management  
GoBack

Register 9.17. RTC_CNTL_INT_CLR_RTC_REG (0x004C)

RTC_CNTL_BBPLL_CAL_INT_CLR  
(reserved)  
RTC_CNTL_GITCH_DET_INT_CLR  
(reserved)  
RTC_CNTL_XTAL32K_DEAD_INT_CLR  
RTC_CNTL_SWD_INT_CLR  
(reserved)  
RTC_CNTL_MAIN_TIMER_INT_CLR  
RTC_CNTL_BROWN_OUT_INT_CLR  
(reserved)  
RTC_CNTL_WDT_INT_CLR  
RTC_CNTL_SLP_REJECT_INT_CLR  
RTC_CNTL_SLP_WAKEUP_INT_CLR  

Bit Field (31:0):  
31 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0  
Reset: 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0  

RTC_CNTL_SLP_WAKEUP_INT_CLR   Clears the interrupt triggered when the chip wakes up from sleep. (WO)  
RTC_CNTL_SLP_REJECT_INT_CLR    Clears the interrupt triggered when the chip rejects to go to sleep. (WO)  
RTC_CNTL_WDT_INT_CLR           Clears the RTC watchdog interrupt. (WO)  
RTC_CNTL_BROWN_OUT_INT_CLR     Clears the brownout interrupt. (WO)  
RTC_CNTL_MAIN_TIMER_INT_CLR    Clears the RTC main timer interrupt. (WO)  
RTC_CNTL_SWD_INT_CLR           Clears the super watchdog interrupt. (WO)  
RTC_CNTL_XTAL32K_DEAD_INT_CLR  Clears the RTC watchdog interrupt. (WO)  
RTC_CNTL_GITCH_DET_INT_CLR     Clears the interrupt triggered when a glitch is detected. (WO)  
RTC_CNTL_BBPLL_CAL_INT_CLR     Clears the interrupt triggered upon the ending of a bbpll call. (WO)  

Register 9.18. RTC_CNTL_STOREO_REG (0x0050)

Bit Field (31:0):  
31 0  
Reset: 0  

RTC_CNTL_SCRATCHO   Reservation register 0. (R/W)
```