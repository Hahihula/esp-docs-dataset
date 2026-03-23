

```markdown
Chapter 33 Remote Control Peripheral (RMT)
GoBack

Register 33.16. RMT_CHn_TX_LIM_REG (n = 0, 1) (0x0058, 0x005C)

| 31 | 21 | 20 | 19 | 18 | 9 | 8 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
| 0  | 0  | 0  | 0  | 0  | O |   | Reset |
|    |     |     |     |     |   |   | 0x80 |

RMT_TX_LIM_CHn This field is used to configure the maximum entries that channel n can send out. (R/W)

RMT_TX_LOOP_NUM_CHn This field is used to configure the maximum loop count when continuous TX mode is enabled. (R/W)

RMT_TX_LOOP_CNT_EN_CHn This bit is the enable bit for loop counting. (R/W)

RMT_LOOP_COUNT_RESET_CHn This bit is used to reset the loop count when continuous TX mode is enabled. (WT)

Register 33.17. RMT_TX_SIM_REG (0x006C)

| 31 | ... | 3 | 2 | 1 | 0 |
|----:|-----|---:|---:|---:|---:|
| 0  | 0   | O | O | O | Reset |

RMT_TX_SIM_CHO Set this bit to enable channel 0 to start sending data synchronously with other enabled channels. (R/W)

RMT_TX_SIM_CH1 Set this bit to enable channel 1 to start sending data synchronously with other enabled channels. (R/W)

RMT_TX_SIM_EN This bit is used to enable multiple of channels to start sending data synchronously. (R/W)
```