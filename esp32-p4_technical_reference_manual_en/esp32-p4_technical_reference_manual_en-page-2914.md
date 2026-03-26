

```markdown
Chapter 57 Remote Control Peripheral (RMT) GoBack


Register 57.17. RMT_TX_SIM_REG (0x00C4)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| ... | ...         |
| 5   | RMT_TX_SIM_EN |
| 4   | RMT_TX_SIM_CH3 |
| 3   | RMT_TX_SIM_CH2 |
| 2   | RMT_TX_SIM_CH1 |
| 1   | RMT_TX_SIM_CHO |
| 0   | Reset       |

RMT_TX_SIM_CHn (n: 0-3) Configures whether to enable channel n to start sending data synchronously with other enabled channels.
O: No effect
1: Enable
(R/W)

RMT_TX_SIM_EN Configures whether to enable multiple of channels to start sending data synchronously.
O: No effect
1: Enable
(R/W)


Register 57.18. RMT_CHm_RX_LIM_REG (m: 4-7) (0x00B0, 0x00B4, 0x00B8, 0x00BC)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| ... | ...         |
| 9   | RMT_CHm_RX_LIM_REG |
| 8   | Ox80        |
| 0   | Reset       |

RMT_CHm_RX_LIM_REG Configures the maximum entries that channel m can receive. (R/W)


Register 57.19. RMT_DATE_REG (0x00CC)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| ... | ...         |
| 28  | RMT_DATE    |
| 27  | Ox2201111   |
| 0   | Reset       |

RMT_DATE Version control register. (R/W)
```