**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**
SO-S8 in the figure above are switches controlled by fields in register MCPWM_DTX_CFG_REG shown in Table 36.3-5.

**Table Titles and Content:**

1. **Table 36.3-5. Dead Time Generator Switches Control Fields**
   - Columns:
     - Switch
     - Field
   - Rows:
     | S0    | MCPWM_DTX_B_OUTBYPASS |
     | S1    | MCPWM_DTX_A_OUTBYPASS |
     | S2    | MCPWM_DTX_RED_OUTINVERT |
     | S3    | MCPWM_DTX_FED_OUTINVERT |
     | S4    | MCPWM_DTX_RED_INSEL |
     | S5    | MCPWM_DTX_FED_INSEL |
     | S6    | MCPWM_DTX_A_OUTSWAP |
     | S7    | MCPWM_DTX_B_OUTSWAP |
     | S8    | MCPWM_DTX_DEB_MODE |

2. **Table 36.3-6. Typical Dead Time Generator Operating Modes**
   - Columns:
     - Mode
     - Mode Description
     - SO (Switches)
     - S1, S2, S3 (Switches)
   - Rows:
     | 1    | PWMxA and PWMxB Pass Through/No Delay | X | |
     | 2    | Active High Complementary (AHC), see Figure 36.3-22 | O | O | O |
     | 3    | Active Low Complementary (ALC), see Figure 36.3-23 | - | I | O |
     | 4    | Active High (AH), see Figure 36.3-24 | X | - | - |
     | 5    | Active Low (AL), see Figure 36.3-25 | - | Y | Z |
     | 6    | PWMxA Output = PWMxA In (No Delay) | O | I | R |
     | 7    | PWMxB Output = PWMxA Input with Falling Edge Delay | X | A | B |

**Additional Text:**
All switch combinations are supported, but not all of them represent the typical modes of use. Table 36.3-6 documents some typical dead time configurations. In these configurations the position of S4 and S5 sets PWMxA as the common source of both falling-edge and rising-edge delay.

**Footer Information:**
Espressif Systems
1352 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback