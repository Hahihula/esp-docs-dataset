

```markdown
Register 53.5. TWAI_ERR_WARNING_LIMIT_REG (0x0034)

TWAI_ERR_WARNING_LIMIT Configures error warning threshold. When any of the error counter values (TWAI_RX_ERR_CNT or TWAI_TX_ERR_CNT) exceeds the threshold, the TWAI controller enters an error state; when all the error counter values are below the threshold, the TWAI controller exits the error state. An error warning interrupt will be triggered if the TWAI controller enters or exits an error state. (R/W)

Register 53.6. TWAI_CLOCK_DIVIDER_REG (0x007C)

TWAI_CD Configures the divisor of the external CLKOUT pin. (R/W)

TWAI_CLOCK_OFF Configures whether or not to enable the external CLKOUT pin in Reset mode.
0: Enable the external CLKOUT pin
1: Disable the external CLKOUT pin
(R/W)
```