

```markdown
Register 7.23. PCR_I2S_CONF_REG (0x0060)
```

| Bit | Field Name           | Description                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)          |                                                                             |
| 4   | `PCR_I2S_TX_READY`    | Represents whether or not I2S TX is released from reset.                    |
| 3   | `PCR_I2S_RX_READY`    | Represents whether or not I2S RX is released from reset.                    |
| 2   | `PCR_I2S_RST_EN`      | Configures whether or not to reset I2S.                                     |
| 1   | `PCR_I2S_CLK_EN`      | Configures whether or not to enable APB_CLK for I2S.                        |
| 0   | (Reset)              |                                                                             |

**PCR_I2S_CLK_EN**
- O: Not enable
- 1: Enable
(R/W)

**PCR_I2S_RST_EN**
- O: Not reset
- 1: Reset
(R/W)

**PCR_I2S_RX_READY**
- O: Not released
- 1: Released
(RO)

**PCR_I2S_TX_READY**
- O: Not released
- 1: Released
(RO)
```