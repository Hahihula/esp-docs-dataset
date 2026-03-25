

```markdown
Register 7.6. PCR_UART1_PD_CTRL_REG (0x0014)

PCR_UART1_MEM_FORCE_PU Configures whether or not to force power up UART1 memory.
- O: Not force power up UART1 memory
- 1: Force power up UART1 memory
(R/W)

PCR_UART1_MEM_FORCE_PD Configures whether or not to force power down UART1 memory.
- O: Not force power down UART1 memory
- 1: Force power down UART1 memory
(R/W)
```

```markdown
Register 7.7. PCR_UART2_CONF_REG (0x0018)

PCR_UART2_CLK_EN Configures whether or not to enable APB_CLK for UART2.
- O: Not enable
- 1: Enable
(R/W)

PCR_UART2_RST_EN Configures whether or not to reset UART2.
- O: Not reset
- 1: Reset
(R/W)

PCR_UART2_READY Represents whether or not UART2 is released from reset.
- O: Not released
- 1: Released
(RO)
```