

```markdown
Chapter 18 Permission Control (PMS)

Register 18.61. CPU_APM_FUNC_CTRL_REG (0x00C4)
| bit | Description |
|-----|-------------|
| 31-2 | reserved |
| 1   | Reset |

CPU_APM_MO_FUNC_EN Configures whether to enable permission management for CPU_APM_CTRL MO.
- 0: Disable
- 1: Enable (R/W)

CPU_APM_M1_FUNC_EN Configures whether to enable permission management for CPU_APM_CTRL M1.
- 0: Disable
- 1: Enable (R/W)

Register 18.62. CPU_APM_MO_STATUS_REG (0x00C8)
| bit | Description |
|-----|-------------|
| 31-2 | reserved |
| 1   | Reset |

CPU_APM_MO_EXCEPTION_STATUS Represents exception status.
- bit0: 1 represents permission restrictions
- bit1: 1 represents address out of bounds (RO)
```