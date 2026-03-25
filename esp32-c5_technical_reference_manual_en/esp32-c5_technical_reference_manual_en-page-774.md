

```markdown
Chapter 18 Permission Control (PMS)

Register 18.33. LP_APM_FUNC_CTRL_REG (0x00C4)
```

| bit | description |
|-----|-------------|
| 31  | (reserved) |
| 2   | LP_APM_M1_FUNC_EN |
| 1   | LP_APM_MO_FUNC_EN |
| 0   | Reset |

LP_APM_MO_FUNC_EN Configures to enable permission management for LP_APM_CTRL MO. (R/W)

LP_APM_M1_FUNC_EN Configures to enable permission management for LP_APM_CTRL M1. (R/W)

Register 18.34. LP_APM_MO_STATUS_REG (0x00C8)
```

| bit | description |
|-----|-------------|
| 31  | (reserved) |
| 2   | LP_APM_MO_EXCEPTION_STATUS |

LP_APM_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)

Register 18.35. LP_APM_MO_STATUS_CLR_REG (0x00CC)
```

| bit | description |
|-----|-------------|
| 31  | (reserved) |
| 1   | LP_APM_MO_EXCEPTION_STATUS_CLR |

LP_APM_MO_EXCEPTION_STATUS_CLR Configures to clear exception status. (WT)

Espressif Systems
774
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```