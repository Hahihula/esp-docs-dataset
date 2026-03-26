

```markdown
Register 56.34. MCPWM_EVT_EN2_REG (0x0128)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | MCPWM_EVT_OP2_TEE2_EN                                                      |
| 29  | MCPWM_EVT_OPTTEE1_EN                                                       |
| 28  | MCPWM_EVT_OPTTEE2_EN                                                       |
| 27  | MCPWM_EVT_OP2_TEE2_EN                                                      |
| 26  | MCPWM_EVT_OP1_TEE1_EN                                                      |
| 25  | MCPWM_EVT_OP2_TEE2_EN                                                      |
| 24  | MCPWM_EVT_OP1_TEE1_EN                                                      |
| 23  | MCPWM_EVT_OPn_TEE1_EN                                                     |
| 22  | MCPWM_EVT_OPn_TSTMP_E1_REG                                                |
| 21  | MCPWM_EVT_OPn_TEE1_EN                                                     |
| 20  | (R/W)                                                                      |
| 19  | O: Not generate                                                            |
| 18  | 1: Generate                                                                |
| 17  | (R/W)                                                                      |

```markdown
MCPWM_EVT_OPn_TEE1_EN Configures whether to generate the MCPWM_EVT_OPn_TEE1 event when the PWM generator timer equals OPn_TSTMP_E1_REG.
```

```markdown
O: Not generate

1: Generate

(R/W)
```

```markdown
MCPWM_EVT_OPn_TEE2_EN Configures whether to generate the MCPWM_EVT_OPn_TEE2 event when the PWM generator timer equals OPn_TSTMP_E2_REG.
```

```markdown
O: Not generate

1: Generate

(R/W)
```