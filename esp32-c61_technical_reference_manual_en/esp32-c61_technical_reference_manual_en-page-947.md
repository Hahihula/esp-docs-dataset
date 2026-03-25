

```markdown
Chapter 26 SPI Controller (SPI) GoBack

Register 26.16. SPI_DOUT_MODE_REG (0x002C)

(reserved)
31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
                                                         SPI_DQS_MODE
                                                         SPI_DOUT7_MODE
                                                         SPI_DOUT6_MODE
                                                         SPI_DOUT5_MODE
                                                         SPI_DOUT4_MODE
                                                         SPI_DOUT3_MODE
                                                         SPI_DOUT2_MODE
                                                         SPI_DOUT1_MODE
                                                         SPI_DOUT0_MODE

SPI_DOUT0_MODE Configures the output mode for FSPID signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

SPI_DOUT1_MODE Configures the output mode for FSPIQ signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

SPI_DOUT2_MODE Configures the output mode for FSPIWP signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

SPI_DOUT3_MODE Configures the output mode for FSPIHD signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

SPI_DOUT4_MODE Configures whether the output signal DOUT4 is delayed by one SPI module clock cycle at its falling edge.  
0: No delay.  
1: Delayed by one SPI module clock cycle (falling edge).  
Can be configured in CONF state.  
(HRO)

SPI_DOUT5_MODE Configures whether the output signal DOUT5 is delayed by one SPI module clock cycle at its falling edge.  
0: No delay.  
1: Delayed by one SPI module clock cycle (falling edge).  
Can be configured in CONF state.  
(HRO)

Continued on the next page...
```