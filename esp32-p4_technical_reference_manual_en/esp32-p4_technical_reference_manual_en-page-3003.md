

```markdown
## Register 60.18. LP_ANA_TOUCH_FILTER2_REG (0x0114)

| Bit | Description |
|-----|-------------|
| 31  | LP_ANA_TOUCH_BYPASS_NN_THRES<br>LP_ANA_TOUCH_BYPASS_JOSE_THRES<br>(reserved) |
| 30  | LP_ANA_TOUCH_OUTEN |
| 29  | (reserved) |
| ... | ... |
| 15  | O |
| ... | ... |
| 0   | Reset |

### LP_ANA_TOUCH_OUTEN
Configures whether to enable output of the 14 touch pin measurement results. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
*   0: Disable
*   1: Enable (R/W)

### LP_ANA_TOUCH_BYPASS_NOISE_THRES
Configures whether to enable the bypass mode for `touch_smooth_data`.
*   0: Disable
*   1: Enable (R/W)

### LP_ANA_TOUCH_BYPASS_NN_THRES
Configures whether to enable the bypass mode for out-of-phase `noise_threshold`.
*   0: Disable
*   1: Enable (R/W)
```

```markdown
## Register 60.19. LP_ANA_TOUCH_FILTER3_REG (0x0118)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| ... | ... |
| 17  | LP_ANA_TOUCH_UPDATE_BENCHMARK_SW<br>LP_ANA_TOUCH_BENCHMARK_SW |
| 16  | O |
| ... | ... |
| 0   | Reset |

### LP_ANA_TOUCH_BENCHMARK_SW
Configures software to write the benchmark data. (R/W)

### LP_ANA_TOUCH_UPDATE_BENCHMARK_SW
Write 1 to enable the software to write the benchmark data. (WT)
```