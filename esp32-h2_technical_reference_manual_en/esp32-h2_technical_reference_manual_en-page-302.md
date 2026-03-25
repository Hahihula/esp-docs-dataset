

```markdown
Register 7.26. PCR_I2S_CONF_REG (0x006C)
```

| Bit | Field Name           | Description                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)           |                                                                             |
| 30  | PCR_I2S_TX_READY     | Represents whether or not I2S TX is released from reset.<br>0: Not released<br>1: Released (RO) |
| 29  | PCR_I2S_RX_READY     | Represents whether or not I2S RX is released from reset.<br>0: Not released<br>1: Released (RO) |
| 28  | PCR_I2S_RST_EN       | Configures whether or not to reset I2S.<br>0: Not reset<br>1: Reset (R/W)     |
| 27  | PCR_I2S_CLK_EN       | Configures whether or not to enable APB_CLK for I2S.<br>0: Not enable<br>1: Enable (R/W) |

```markdown
PCR_I2S_CLK_EN Configures whether or not to enable APB_CLK for I2S.
O: Not enable
1: Enable
(R/W)

PCR_I2S_RST_EN Configures whether or not to reset I2S.
O: Not reset
1: Reset
(R/W)

PCR_I2S_RX_READY Represents whether or not I2S RX is released from reset.
O: Not released
1: Released
(RO)

PCR_I2S_TX_READY Represents whether or not I2S TX is released from reset.
O: Not released
1: Released
(RO)
```