

```markdown
Chapter 19 Permission Control (PMS)

Register 19.77: PMS_LP_MM_LP_PERI_PMS_REGO_REG (0x0008)

Continued from the previous page...

PMS_LP_MM_LP_MAILBOX_ALLOW Configures whether LP CPU in machine mode has permission to access LP Mailbox Controller.
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_PERICLKIRST_ALLOW Configures whether LP CPU in machine mode has permission to access LP PREICLKIRST (peripheral clock and reset).
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_UART_ALLOW Configures whether LP CPU in machine mode has permission to access LP UART.
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_I2C_ALLOW Configures whether LP CPU in machine mode has permission to access LP I2S.
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_SPI_ALLOW Configures whether LP CPU in machine mode has permission to access LP SPI.
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_I2CMST_ALLOW Configures whether LP CPU in machine mode has permission to access LP I2C master.
    O: Not allowed
    1: Allowed
        (R/W)

PMS_LP_MM_LP_I2S_ALLOW Configures whether LP CPU in machine mode has permission to access LP I2S.
    O: Not allowed
    1: Allowed
        (R/W)

Continued on the next page...
```