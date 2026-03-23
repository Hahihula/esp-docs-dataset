

```markdown
Chapter 8 Reset and Clock

Register 8.80. LP_CLKRST_CPU_RESET_REG (0x0014)

LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH configures the reset length of RTC_WDT reset CPU  
Measurement unit: LP_DYN_FAST_CLK  
(R/W)

LP_CLKRST_RTC_WDT_CPU_RESET_EN Configures whether or not RTC_WDT can reset CPU  
0: RTC_WDT could not reset CPU when RTC_WDT timeout  
1: RTC_WDT could reset CPU when RTC_WDT timeout  
(R/W)

LP_CLKRST_CPU_STALL_WAIT configure the time between CPU stall and reset  
Measurement unit: LP_DYN_FAST_CLK  
(R/W)

LP_CLKRST_CPU_STALL_EN Configures whether or not CPU entry stall state before RTC_WDT and software reset CPU  
0: CPU will not entry stall state before RTC_WDT and software reset CPU  
1: CPU will entry stall state before RTC_WDT and software reset CPU  
(R/W)

Register 8.81. LP_CLKRST_FOSC_CNTL_REG (0x0018)

LP_CLKRST_FOSC_DFREQ Configures the RC_FAST_CLK frequency, the clock frequency will increase with this field.  
(R/W)
```