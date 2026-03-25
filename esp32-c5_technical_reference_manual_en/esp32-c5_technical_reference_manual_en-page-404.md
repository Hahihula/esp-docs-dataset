

```markdown
## Register 9.6. PCR_UART1_PD_CTRL_REG (0x0014)

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
## Register 9.7. PCR_I2C_CONF_REG (0x0020)

PCR_I2C_CLK_EN Configures whether or not to enable APB_CLK for I2C.
- O: Not enable
- 1: Enable
(R/W)

PCR_I2C_RST_EN Configures whether or not to reset I2C.
- O: Not reset
- 1: Reset
(R/W)

PCR_I2C_READY Represents whether or not I2C is released from reset.
- O: Not released
- 1: Released
(RO)
```