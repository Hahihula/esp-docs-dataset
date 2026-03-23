

```markdown
Register 37.16. RMT_TX_SIM_REG (0x006C)

| Bit | Field Name       | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 3   | RMT_TX_SIM_EN    | Configures whether to enable multiple of channels to start sending data synchronously.<br>O: No effect<br>1: Enable (R/W) |
| 2   | RMT_TX_SIM_CH1   | Configures whether to enable channel `n` to start sending data synchronously with other enabled channels.<br>O: No effect<br>1: Enable (R/W) |
| 1   | RMT_TX_SIM_CH0   |                                                                             |
| 0   | Reset            |                                                                             |

Register 37.17. RMT_CHm_RX_LIM_REG (m: 2-3) (0x0058+0x4*m)

| Bit | Field Name       | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 9   | RMT_CHm_RX_LIM_REG | Configures the maximum entries that channel `m` can receive. (R/W)           |

Register 37.18. RMT_DATE_REG (0x00CC)

| Bit | Field Name       | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 28  | RMT_DATE         | Version control register. (R/W)<br>Value: `0x2006231`                        |

```
Note: The diagrams depict register bit fields with labels indicating reserved bits, reset values, and specific configuration bits for enabling synchronous transmission channels (`SIM_EN`, `SIM_CHn`) and limiting receive entries per channel (`RX_LIM_REG`). The RMT_DATE_REG contains a version identifier. All text is extracted verbatim as presented.
```