

```markdown
Register 53.32. TWAI_TIMESTAMP_DATA_REG (0x0094)

TWAI_TIMESTAMP_DATA    The timestamp of the TWAI frame indicated by the RX FIFO read pointer corresponds to the time when the current TWAI frame was received. Valid only when TWAI_TS_ENABLE is enabled. (RO)

Register 53.33. TWAI_TIMESTAMP_PRESCALER_REG (0x0098)

TWAI_TS_DIV_NUM    Configures the clock divisor of the timestamp counter. (R/W)

Register 53.34. TWAI_TIMESTAMP_CFG_REG (0x009C)

TWAI_TS_ENABLE    Configures whether to enable the timestamp collection function.
0: Disable
1: Enable
(R/W)
```