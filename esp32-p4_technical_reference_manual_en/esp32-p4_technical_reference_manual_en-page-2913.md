

```markdown
Register 5716: RMT_CHn_TX_LIM_REG (n: 0-3) (0x00A0+0x4*n)
```

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | RMT_TX_LIM_CHn               |
| 29  | RMT_TX_LOOP_NUM_CHn          |
| 28  | RMT_TX_LOOP_CNT_EN_CHn       |
| 27  | RMT_LOOP_COUNT_RESET_CHn     |
| 26  | RMT_LOOP_STOP_EN_CHn         |

```markdown
RMT_TX_LIM_CHn Configures the maximum entries that channel n can send out. (R/W)

RMT_TX_LOOP_NUM_CHn Configures the maximum loop count when Continuous TX mode is valid. (R/W)

RMT_TX_LOOP_CNT_EN_CHn Configures whether to enable loop count.
  - 0: No effect
  - 1: Enable
  (R/W)

RMT_LOOP_COUNT_RESET_CHn Configures whether to reset the loop count when continuous TX mode is enabled.
  - 0: No effect
  - 1: Reset
  (WT)

RMT_LOOP_STOP_EN_CHn Configures whether to enable the loop send stop function after the loop counter counts to loop number for channel n.
  - 0: No effect
  - 1: Enable
  (R/W)
```