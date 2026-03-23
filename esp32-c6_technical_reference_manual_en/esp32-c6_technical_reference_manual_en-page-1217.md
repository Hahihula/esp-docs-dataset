
```markdown
## Highlights for Operation of the Dead Time Generator

Options for setting up the dead time module are shown in Figure 36.3-23.

Figure 36.3-23. Options for Setting up the Dead Time Generator Module

S0-S8 in the figure above are switches controlled by fields in register `MCPWM_DTx_CFG_REG` shown in Table 36.3-5.

Table 36.3-5. Dead Time Generator Switches Control Fields

| Switch | Field |
|--------|-------|
| S0     | MCPWM_DTx_B_OUTBYPASS |
| S1     | MCPWM_DTx_A_OUTBYPASS |
| S2     | MCPWM_DTx_RED_OUTINVERT |
| S3     | MCPWM_DTx_FED_OUTINVERT |
| S4     | MCPWM_DTx_RED_INSEL |
| S5     | MCPWM_DTx_FED_INSEL |
| S6     | MCPWM_DTx_A_OUTSWAP |
| S7     | MCPWM_DTx_B_OUTSWAP |
| S8     | MCPWM_DTx_DEB_MODE |

All switch combinations are supported, but not all of them represent the typical modes of use. Table 36.3-6 documents some typical dead time configurations. In these configurations, the position of S4 and S5 sets PWMxA as the common source of both falling edge delay (FED) and rising edge delay (RED). The modes presented in table 36.3-6 may be categorized as follows:

Table 36.3-6. Typical Dead Time Generator Operating Modes

| Mode | Mode Description | S0 | S1 | S2 | S3 |
|------|-------------------|----|----|----|----|
| 1    | PWMxA and PWMxB Pass Through/No Delay | 1 | 1 | X | X |
| 2    | Active High Complementary (AHC), see Figure 36.3-24 | O | O | O | 1 |
| 3    | Active Low Complementary (ALC), see Figure 36.3-25 | O | O | 1 | O |
| 4    | Active High (AH), see Figure 36.3-26 | O | O | O | O |
| 5    | Active Low (AL), see Figure 36.3-27 | O | O | 1 | 1 |
```