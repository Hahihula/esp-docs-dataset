

```markdown
## Register 9.3. PCR_UART0_PD_CTRL_REG (0x0008)

PCR_UART0_MEM_FORCE_PU Configures whether or not to force power up UART0 memory.
- O: Not force power up UART0 memory
- 1: Force power up UART0 memory
(R/W)

PCR_UART0_MEM_FORCE_PD Configures whether or not to force power down UART0 memory.
- O: Not force power down UART0 memory
- 1: Force power down UART0 memory
(R/W)
```

```markdown
## Register 9.4. PCR_UART1_CONF_REG (0x000C)

PCR_UART1_CLK_EN Configures whether or not to enable APB_CLK for UART1.
- O: Not enable
- 1: Enable
(R/W)

PCR_UART1_RST_EN Configures whether or not to reset UART1.
- O: Not reset
- 1: Reset
(R/W)

PCR_UART1_READY Represents whether or not UART1 is released from reset.
- O: Not released
- 1: Released
(RO)
```