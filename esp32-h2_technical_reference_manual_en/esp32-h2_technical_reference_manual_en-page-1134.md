

```markdown
Register 36.43. MCPWM_FH1_STATUS_REG (0x00A8)

| 31 | 30 | ... | 2 | 1 | 0 |
|----:|----:|-----|---:|---:|---:|
|    ||reserved||||
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

MCPWM_FH1_CBC_ON Represents whether or not a cycle-by-cycle mode action is ongoing. This field is set and reset by hardware.
- O: No cycle-by-cycle mode action is ongoing
- 1: A cycle-by-cycle mode action is ongoing (RO)

MCPWM_FH1_OST_ON Represents whether or not a one-shot mode action is ongoing. This field is set and reset by hardware.
- O: No one-shot mode action is ongoing
- 1: A one-shot mode action is ongoing (RO)
```