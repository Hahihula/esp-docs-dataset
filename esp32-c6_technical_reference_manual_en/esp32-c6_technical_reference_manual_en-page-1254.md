

```markdown
Register 36.28. MCPWM_FHO_CFG1_REG (0x006C)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 5   | MCPWM_FHO_FORCE_OST         | Configures whether or not to trigger a one-shot mode action.<br>0: No effect<br>1: Trigger a one-shot mode action (R/W) |
| 4   | MCPWM_FHO_FORCE_CBC          | Configures whether or not to trigger a cycle-by-cycle mode action.<br>0: No effect<br>1: Trigger a cycle-by-cycle mode action (R/W) |
| 3   | MCPWM_FHO_CBCPULSE           | Configures cycle-by-cycle mode action refresh moment selection.<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP (R/W) |
| 2   | MCPWM_FHO_CLR_OST            | Configures whether or not a rising edge will clear an ongoing one-shot mode action.<br>0: No effect<br>1: Clear (R/W) |

Register 36.29. MCPWM_FHO_STATUS_REG (0x0070)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 2   | MCPWM_FHO_CBC_ON            | Represents set and reset by hardware. If set, a cycle-by-cycle mode action is on going. (RO) |
| 1   | MCPWM_FHO_OST_ON            | Represents set and reset by hardware. If set, an one-shot mode action is on going. (RO) |
```