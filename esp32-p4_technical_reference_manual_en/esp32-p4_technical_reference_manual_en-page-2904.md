

```markdown
Register 57.6. RMT_CHm_RX_CARRIER_RM_REG (m: 4-7) (0x0090, 0x0094, 0x0098, 0x009C)

| 31 | 16   | 15       | 0 |
|----|------|----------|---|
|    |      |          | Reset |
| 0x00 |      |          |

RMT_CARRIER_LOW_THRES_CHm Configures the low level period in a carrier modulation mode for channel m, which is equal to (RMT_CARRIER_LOW_THRES_CHm + 1). (R/W)

RMT_CARRIER_HIGH_THRES_CHm Configures the high level period in a carrier modulation mode for channel m, which is equal to (RMT_CARRIER_HIGH_THRES_CHm + 1). (R/W)

Register 57.7. RMT_SYS_CONF_REG (0x00C0)

| 31 | 30   | 27    | 26 | 25 | 24 | 23 | 18 | 17 | 12 | 11 | 4 | 3 | 2 | 1 | 0 |
|----|------|-------|----|----|----|----|----|----|----|----|---|---|---|---|---|
| RMT_CLK_EN | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | RMT_APB_FIFO_MASK |
| 0 | 0 | 0 | 0 | 1 | 0x1 | 0x0 | 0x0 | 0x0 | 0x1 | 0 | 0 | 0 | 0 | Reset |

RMT_APB_FIFO_MASK Configures the memory access mode.
0: Access memory by FIFO
1: Access memory directly
(R/W)

RMT_CLK_EN Configures whether to enable signal of RMT register clock gate.
0: Power down the drive clock of registers
1: Power up the drive clock of registers
(R/W)
```