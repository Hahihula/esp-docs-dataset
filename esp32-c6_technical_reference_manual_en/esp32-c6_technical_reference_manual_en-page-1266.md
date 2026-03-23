

```markdown
Register 36.42. MCPWM_FH1_CFG1_REG (0x00A4)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 5   | MCPWM_FH1_FORCE_OST         | Configures whether or not to trigger a one-shot mode action.<br>0: No effect<br>1: Trigger (R/W) |
| 4   | MCPWM_FH1_FORCE_CBC          | Configures whether or not to trigger a cycle-by-cycle mode action.<br>0: No effect<br>1: Trigger (R/W) |
| 3   | MCPWM_FH1_CBCPULSE           | Configures cycle-by-cycle mode action refresh moment selection.<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP (R/W) |
| 2   | MCPWM_FH1_CLR_OST            | Configures whether or not a rising edge will clear on going one-shot mode action.<br>0: No effect<br>1: Clear (R/W) |

Register 36.43. MCPWM_FH1_STATUS_REG (0x00A8)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 2   | MCPWM_FH1_CBC_ON            | Represents set and reset by hardware. If set, a cycle-by-cycle mode action is ongoing. (RO) |
| 1   | MCPWM_FH1_OST_ON            | Represents set and reset by hardware. If set, a one-shot mode action is ongoing. (RO) |
```