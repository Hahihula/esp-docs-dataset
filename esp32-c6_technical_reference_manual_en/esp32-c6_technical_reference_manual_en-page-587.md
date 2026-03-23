

```markdown
Chapter 16 Permission Control (PMS)

Register 16.38. LP_APM_INT_EN_REG (0x00E8)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 2   | LP_APM_M1_APM_INT_EN |
| 1   | LP_APM_MO_APM_INT_EN |
| 0   | Reset |

LP_APM_MO_APM_INT_EN Configures to enable APM MO interrupt.
- 0: disable
- 1: enable (R/W)

LP_APM_M1_APM_INT_EN Configures to enable APM M1 interrupt.
- 0: disable
- 1: enable (R/W)

Register 16.39. LP_APM_CLOCK_GATE_REG (0x00EC)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 1   | LP_APM_CLK_EN |
| 0   | Reset |

LP_APM_CLK_EN Configures whether to keep the clock always on.
- 0: enable automatic clock gating
- 1: keep the clock always on (R/W)

Register 16.40. LP_APM_DATE_REG (0x00FC)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 28  | LP_APM_DATE |
| 27  | LP_APM_DATE |
| ... | ...         |
| 0   | Reset |

LP_APM_DATE Version control register. (R/W)

Espressif Systems
587
ESP32-C6 TRM (Version 1.1)
```