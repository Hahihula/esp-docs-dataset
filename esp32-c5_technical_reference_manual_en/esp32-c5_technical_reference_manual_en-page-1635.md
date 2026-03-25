

```markdown
Register 42.15. RMT_CHn_TX_LIM_REG (n: 0-1) (0x0058+0x4*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   |    |    |    |    |    |    |    |    |    |    |    |    | O   |     | Reset |
|     |    |    |    |    |    |    |    |    |    |    |    |    | Ox80|      |       |

RMT_TX_LIM_CHn Configures the maximum entries that channel n can send out. (R/W)

RMT_TX_LOOP_NUM_CHn Configures the maximum loop count when Continuous TX mode is valid. (R/W)

RMT_TX_LOOP_CNT_EN_CHn Configures whether to enable loop count.
  O: No effect
  1: Enable
  (R/W)

RMT_LOOP_COUNT_RESET_CHn Configures whether to reset the loop count when tx_conti_mode is valid.
  O: No effect
  1: Reset
  (WT)

RMT_LOOP_STOP_EN_CHn Configures whether to enable the loop send stop function after the loop counter counts to loop number for channel n.
  O: No effect
  1: Enable
  (R/W)
```