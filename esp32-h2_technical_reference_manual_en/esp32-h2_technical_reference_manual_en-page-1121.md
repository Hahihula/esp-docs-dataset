

```markdown
Register 36.29. MCPWM_FHO_STATUS_REG (0x0070)
```

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)         |                                                                             |
| 30  |                    |                                                                             |
| 29  |                    |                                                                             |
| ... |                    |                                                                             |
| 2   | MCPWM_FHO_OST_ON   | Represents whether or not a one-shot mode action is ongoing. This field is set and reset by hardware.<br>0: No one-shot mode action is ongoing<br>1: A one-shot mode action is ongoing (RO) |
| 1   | MCPWM_FHO_CBC_ON   | Represents whether or not a cycle-by-cycle mode action is ongoing. This field is set and reset by hardware.<br>0: No cycle-by-cycle mode action is ongoing<br>1: A cycle-by-cycle mode action is ongoing (RO) |

```markdown
MCPWM_FHO_CBC_ON Represents whether or not a cycle-by-cycle mode action is ongoing. This field is set and reset by hardware.
- 0: No cycle-by-cycle mode action is ongoing
- 1: A cycle-by-cycle mode action is ongoing (RO)

MCPWM_FHO_OST_ON Represents whether or not a one-shot mode action is ongoing. This field is set and reset by hardware.
- 0: No one-shot mode action is ongoing
- 1: A one-shot mode action is ongoing (RO)
```