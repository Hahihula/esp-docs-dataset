

```markdown
Chapter 16 Permission Control (PMS)

Register 16.35. LP_APM_CLOCK_GATE_REG (0x00EC)
```

| 31 | Reset |
|----:|-------|
| 0  |       |

LP_APM_CLK_EN Configures whether to keep the clock always on.
- O: Enable automatic clock gating
- 1: Keep the clock always on
(R/W)

Register 16.36. LP_APM_DATE_REG (0x00FC)

| 31 | reserved | 28 | 27 |
|----|----------|----|----|
|    |          | O  | x2212160 |

LP_APM_DATE Version control register. (R/W)

## 16.9.3 CPU_APM_REG

The addresses in this section are relative to the CPU_APM base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 16.37. CPU_APM_REGION_FILTER_EN_REG (0x0000)

| 31 | reserved |
|----|----------|
|    |          |

CPU_APM_REGION_FILTER_EN Configures bit n (0-7) to enable permission checks for region n (0-7).
- O: Disable
- 1: Enable
(R/W)
```