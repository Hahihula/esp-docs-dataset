

```markdown
Chapter 7 Reset and Clock GoBack

Register 7.19. PCR_TIMERGROUP1_CONF_REG (0x0050)

(reserved)
PCR_TG1_TIMERx_READY
PCR_TG1_TIMERO_READY
PCR_TG1_WDT_RST_EN
PCR_TG1_CLK_EN

31
O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O 0 1 1 1 0 1 Reset

PCR_TG1_CLK_EN Configures whether or not to enable APB_CLK for Timer Group 1.  
O: Not enable  
1: Enable (R/W)

PCR_TG1_RST_EN Configures whether or not to reset Timer Group 1.  
O: Not reset  
1: Reset (R/W)

PCR_TG1_WDT_READY Represents whether or not the WDT in Timer Group 1 is released from reset.  
O: Not released  
1: Released (RO)

PCR_TG1_TIMERO_READY reset. Represents whether or not Timer 0 in Timer Group 1 is released from reset.  
O: Not released  
1: Released  
(RO)timer_group0 Timer Omodule (RO)

PCR_TG1_TIMER1_READY Represents whether or not Timer 1 in Timer Group 1 is released from reset.  
O: Not released  
1: Released (RO)
```