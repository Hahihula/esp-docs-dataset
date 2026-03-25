

```markdown
Register 41.15. MCPWM_DTn_CFG_REG(n: 0-2) (0x0058+0x38*n)

Continued from the previous page...

MCPWM_DBn_FED_OUTINVERT Configures the S3 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_A_OUTBYPASS Configures the S1 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_B_OUTBYPASS Configures the SO switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_CLK_SEL Configures dead time generator n clock selection.
0: PWM_CLK
1: PT_CLK
(R/W)
```

```markdown
Register 41.16. MCPWM_DTn_FED_CFG_REG(n: 0-2) (0x005C+0x38*n)

MCPWM_DBn_FED Configures the shadow register for FED. (R/W)
```

```markdown
Register 41.17. MCPWM_DTn_RED_CFG_REG(n: 0-2) (0x0060+0x38*n)

MCPWM_DBn_RED Configures the shadow register for RED. (R/W)
```