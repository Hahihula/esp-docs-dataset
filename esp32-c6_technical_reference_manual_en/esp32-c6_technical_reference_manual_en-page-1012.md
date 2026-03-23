

```markdown
Register 30.16. I2S_LC_HUNG_CONF_REG (0x0060)

I2S_LC_FIFO_TIMEOUT    Configures FIFO timeout threshold.
                        I2S_RX_HUNG_INT interrupt will be triggered when FIFO hung counter is equal to this value. (R/W)

I2S_LC_FIFO_TIMEOUT_SHIFT  Configures tick counter threshold. The tick counter is reset when counter value >= 88000/2^I2S_LC_FIFO_TIMEOUT_SHIFT. (R/W)

I2S_LC_FIFO_TIMEOUT_ENA    Configures whether to enable FIFO timeout.
                            0: Disable
                            1: Enable
                        (R/W)
```

```markdown
Register 30.17. I2S_CONF_SINGLE_DATA_REG (0x0068)

I2S_SINGLE_DATA   Configures constant channel data to be sent out. (R/W)
```

```markdown
Register 30.18. I2S_STATE_REG (0x006C)

I2S_TX_IDLE    Represents the TX unit state.
               0: I2S TX unit is working
               1: I2S TX unit is in idle state
              (RO)
```