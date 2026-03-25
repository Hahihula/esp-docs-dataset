

```markdown
Register 41.34. MCPWM_EVT_EN2_REG (0x0128)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 6   | MCPWM_EVT_OP2_TEE2_EN                                                      |
| 5   | MCPWM_EVT_OPTTEE1_EN                                                       |
| 4   | MCPWM_EVT_OPTTEE2_EN                                                       |
| 3   | MCPWM_EVT_OPn_TEE1_EN                                                     |
| 2   | MCPWM_EVT_OPn_TEE2_EN                                                     |
| 1   | MCPWM_EVT_OPn_TSTMP_E1_REG                                                |
| 0   | Reset                                                                      |

MCPWM_EVT_OPn_TEE1_EN Configures whether to generate the MCPWM_EVT_OPn_TEE1 event when the PWM generator timer equals OPn_TSTMP_E1_REG.
O: Not generate
1: Generate
(R/W)

MCPWM_EVT_OPn_TEE2_EN Configures whether to generate the MCPWM_EVT_OPn_TEE2 event when the PWM generator timer equals OPn_TSTMP_E2_REG.
O: Not generate
1: Generate
(R/W)
```