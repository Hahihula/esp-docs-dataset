

```markdown
Register 56.20. MCPWM_FHn_CFG1_REG(n: 0-2) (0x006C+0x38*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | MCPWM_TZn_CLR_OST                                                             |
| 29  | MCPWM_TZn_FORCE_OST                                                          |
| 28  | MCPWM_TZn_CBCPULSE                                                           |
| 27  | MCPWM_TZn_FORCE_CBC                                                          |
| 5   | O: No effect<br>1: Triggers a clear for ongoing one-shot mode action by software (R/W) |
| 4   | Configures the refresh moment selection of cycle-by-cycle mode action.<br>O: Select nothing, will not refresh<br>Bit0 is set to 1: TEZ<br>Bit1 is set to 1: TEP (R/W) |
| 3   | Configures whether to generate a software cycle-by-cycle mode action.<br>O: No effect<br>1: Triggers a cycle-by-cycle mode action by software (R/W) |
| 2   | Configures whether to generate a software one-shot mode action.<br>O: No effect<br>1: Triggers a one-shot mode action by software (R/W) |
| 1   | Reset                                                                      |
```