

```markdown
Chapter 37 Remote Control Peripheral (RMT)    GoBack


Register 37:15. RMT_CHn_TX_LIM_REG (n: 0-1) (0x0058+0x4*n)

| 31 | 22 | 21 | 20 | 19 | 18 | 9 | 8 | 0 |
|----|----:|----:|----:|----:|----:|---:|---:|---:|
| 0  | 0   | 0   | 0   | 0   | 0   | 0 | O | Ox80 Reset |

RMT_TX_LIM_CHn Configures the maximum entries that channel n can send out. (R/W)

RMT_TX_LOOP_NUM_CHn Configures the maximum loop count when Continuous TX mode is valid. (R/W)

RMT_TX_LOOP_CNT_EN_CHn Configures whether to enable loop count.
    0: No effect
    1: Enable
    (R/W)

RMT_LOOP_COUNT_RESET_CHn Configures whether to reset the loop count when tx_conti_mode is valid.
    0: No effect
    1: Reset
    (WT)

RMT_LOOP_STOP_EN_CHn Configures whether to enable the loop send stop function after the loop counter counts to loop number for channel n.
    0: No effect
    1: Enable
    (R/W)
```