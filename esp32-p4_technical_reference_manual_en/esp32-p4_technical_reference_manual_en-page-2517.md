

```markdown
## Register 47.12. LP_I2S_LC_HUNG_CONF_REG (0x0060)

LP_I2S_LC_FIFO_TIMEOUT Configures FIFO timeout threshold. The FIFO hung counter is incremented by one each time LP I2S is in an error state and the tick counter reaches its threshold. LP_I2S_RX_HUNG_INT interrupt will be triggered when FIFO hung counter is equal to the FIFO timeout threshold. (R/W)

LP_I2S_LC_FIFO_TIMEOUT_SHIFT Configures tick counter threshold. The tick counter is incremented by one each time LP I2S is in an error state and it is on the rising edge in each system clock (APB). The tick counter is reset when counter value >= 88000/2^LP_I2S_LC_FIFO_TIMEOUT_SHIFT. (R/W)

LP_I2S_LC_FIFO_TIMEOUT_ENA The enable bit for FIFO timeout. Configures whether to enable FIFO timeout.
O: Disable
1: Enable
(R/W)
```

```markdown
## Register 47.13. LP_I2S_CONF_SIGLE_DATA_REG (0x0068)

LP_I2S_SINGLE_DATA Configures the constant channel data to be sent out. (R/W)
```