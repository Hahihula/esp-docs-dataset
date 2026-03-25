

```markdown
Register 34.11. I2C_CTR_REG (0x0004)

Continued from the previous page...

I2C_CLK_EN Configures whether to gate clock signal for registers.
    0: Support clock only when registers are read or written to by software
    1: Force clock on for registers
        (R/W)

I2C_ARBITRATION_EN Configures to enable I2C bus arbitration detection.
    0: No effect
    1: Enable
        (R/W)

I2C_FSM_RST Configures to reset the SCL_FSM.
    0: No effect
    1: Reset (WT)

I2C_CONF_UPGATE Configures this bit for synchronization.
    0: No effect
    1: Synchronize (WT)

I2C_SLV_TX_AUTO_START_EN Configures to enable slave to send data automatically
    0: Disable
    1: Enable
        (R/W)

I2C_ADDR_10BIT_RW_CHECK_EN Configures to check if the R/W bit of 10-bit addressing consists with I2C protocol.
    0: Not check
    1: Check (R/W)

I2C_ADDR_BROADCASTING_EN Configures to support the 7-bit general call function.
    0: Not support
    1: Support
        (R/W)
```