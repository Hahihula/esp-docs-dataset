
```markdown
## Highlights for Operation of the Dead Time Generator

Options for setting up the dead time module are shown in Figure 56.3-21.

Figure 56.3-21. Options for Setting up the Dead Time Generator Module

SO-S8 in the figure above are switches controlled by fields in register `MCPWM_DTn_CFG_REG` shown in Table 56.3-5.

Table 56.3-5. Dead Time Generator Switches Control Fields

| Switch | Field |
|--------|-------|
| S0     | MCPWM_DBn_B_OUTBYPASS |
| S1     | MCPWM_DBn_A_OUTBYPASS |
| S2     | MCPWM_DBn_RED_OUTINVERT |
| S3     | MCPWM_DBn_FED_OUTINVERT |
| S4     | MCPWM_DBn_RED_INSEL |
| S5     | MCPWM_DBn_FED_INSEL |
| S6     | MCPWM_DBn_A_OUTSWAP |
| S7     | MCPWM_DBn_B_OUTSWAP |
| S8     | MCPWM_DBn_DEB_MODE |

All switch combinations are supported, but not all of them represent the typical modes of use. Table 56.3-6 documents some typical dead time configurations. In these configurations, the position of S4 and S5 sets PWMxA as the common source of both falling edge delay (FED) and rising edge delay (RED). The modes presented in table 56.3-6 may be categorized as follows:

Table 56.3-6. Typical Dead Time Generator Operating Modes

| Mode | Mode Description                                                                 | S0 | S1 | S2 | S3 |
|------|-----------------------------------------------------------------------------------|----|----|----|----|
| 1    | PWMxA and PWMxB Pass Through/No Delay                                             | 1  | 1  | X  | X  |
| 2    | Active High Complementary (AHC), see Figure 56.3-22                               | O  | O  | O  | 1  |
| 3    | Active Low Complementary (ALC), see Figure 56.3-23                                | O  | O  | 1  | O  |
| 4    | Active High (AH), see Figure 56.3-24                                             | O  | O  | O  | O  |
```