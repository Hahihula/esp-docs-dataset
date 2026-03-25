

```markdown
Register 36.56. MCPWM_FH2_CFG1_REG (0x00DC)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 5   | MCPWM_TZ2_FORCE_OST         | Configures whether or not a rising edge will clear an ongoing one-shot mode action. O: Not clear<br>1: Clear<br>(R/W) |
| 4   | MCPWM_TZ2_CBCPULSE          | Configures cycle-by-cycle mode action refresh moment selection.<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP<br>(R/W) |
| 3   | MCPWM_TZ2_FORCE_CBC         | Configures whether or not to trigger a cycle-by-cycle mode action.<br>O: No effect<br>1: Trigger a cycle-by-cycle mode action<br>(R/W) |
| 2   | MCPWM_TZ2_FORCE_OST         | Configures whether or not to trigger a one-shot mode action.<br>O: No effect<br>1: Trigger a one-shot mode action<br>(R/W) |
```