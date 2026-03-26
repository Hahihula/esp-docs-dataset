

```markdown
Register 43.16. SPI_DOUT_MODE_REG (0x002C)

Continued from the previous page...

SPI_DOUT7_MODE Configures the output mode for SPI2D7 signal.
    0: Output without delay
    1: Output with a delay of a SPI module clock cycle at its falling edge
        Can be configured in CONF state.
        (R/W)

SPI_D_DQS_MODE Configures the output mode for output SPI_DQS signal.
    0: Output without delay
    1: Output is delayed for a SPI clock cycle at its falling edge.
        Can be configured in CONF state.
        (R/W)
```