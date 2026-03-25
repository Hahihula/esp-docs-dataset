

```markdown
Chapter 9 Reset and Clock

Register 9.23. PCR_TIMERGROUP1_CONF_REG (0x0060)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                        |
| ... | ...                                |
| 5   | `PCR_TG1_TIMER1_READY`            |
| 4   | `PCR_TG1_TIMERO_READY`            |
| 3   | `PCR_TG1_WDT_READY`               |
| 2   | `PCR_TG1_RST_EN`                  |
| 1   | `PCR_TG1_CLK_EN`                  |
| 0   | Reset                             |

**PCR_TG1_CLK_EN** Configures whether or not to enable APB_CLK for Timer Group 1.  
O: Not enable  
1: Enable  
(R/W)

**PCR_TG1_RST_EN** Configures whether or not to reset Timer Group 1.  
O: Not reset  
1: Reset  
(R/W)

**PCR_TG1_WDT_READY** Represents whether or not the WDT in Timer Group 1 is released from reset.  
O: Not released  
1: Released  
(RO)

**PCR_TG1_TIMERO_READY** Represents whether or not Timer 0 in Timer Group 1 is released from reset.  
O: Not released  
1: Released  
(RO)timer_group0 Timer Omodule (RO)

**PCR_TG1_TIMER1_READY** Represents whether or not Timer 1 in Timer Group 1 is released from reset.  
O: Not released  
1: Released  
(RO)
```