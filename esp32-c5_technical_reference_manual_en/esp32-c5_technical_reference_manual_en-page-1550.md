

```markdown
## Highlights for Operation of the Dead Time Generator

Options for setting up the dead time module are shown in Figure 41.3-21.

Figure 41.3-21. Options for Setting up the Dead Time Generator Module

SO-S8 in the figure above are switches controlled by fields in register `MCPWM_DTn_CFG_REG` shown in Table 41.3-5.

Table 41.3-5. Dead Time Generator Switches Control Fields

| Switch | Field |
|--------|-------|
| S0     | `MCPWM_DBn_B_OUTBYPASS` |
| S1     | `MCPWM_DBn_A_OUTBYPASS` |
| S2     | `MCPWM_DBn_RED_OUTINVERT` |
| S3     | `MCPWM_DBn_FED_OUTINVERT` |
| S4     | `MCPWM_DBn_RED_INSEL` |
| S5     | `MCPWM_DBn_FED_INSEL` |
| S6     | `MCPWM_DBn_A_OUTSWAP` |
| S7     | `MCPWM_DBn_B_OUTSWAP` |
| S8     | `MCPWM_DBn_DEB_MODE` |

All switch combinations are supported, but not all of them represent the typical modes of use. Table 41.3-6 documents some typical dead time configurations. In these configurations, the position of S4 and S5 sets PWMxA as the common source of both falling edge delay (FED) and rising edge delay (RED). The modes presented in table 41.3-6 may be categorized as follows:

*   Mode 1: Bypass delays on both FED and RED
    In this mode, the dead time module is disabled. Signals of PWMxA and PWMxB pass through without any modifications.
*   Mode 2-5: Classical Dead Time Polarity Settings
```