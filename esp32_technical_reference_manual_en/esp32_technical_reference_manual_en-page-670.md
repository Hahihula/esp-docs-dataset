**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Table of Switches and Registers:**

| Switch | Register |
|--------|----------|
| S1     | PWM_DTxA_OUTBYPASS |
| S2     | PWM_DTxB_OUTINVERT |
| S3     | PWM_DTxFED_OUTINVERT |
| S4     | PWM_DTx_RED_INSEL |
| S5     | PWM_DTxFED_INSEL |
| S6     | PWM_DTxA_OUTSWAP |
| S7     | PWM_DTxB_OUTSWAP |
| S8     | PWM_DTxB_DEB_MODE |

**Body Text:**
All switch combinations are supported, but not all of them represent the typical modes of use. Table 29.3-6 documents some typical dead time configurations. In these configurations the position of S4 and S5 sets PWMxAs the common source of both falling-edge and rising-edge delay.

**Subsection: Dead Time Configurations**
The following table (Table 29.3-6) may be categorized as follows:

1. **Mode 1:** Bypass delays on both falling (FED) as well as raising edge (RED)
   - In this mode the dead time submodule is disabled. Signals PWMxAs and PWMxBs pass through without any modifications.

2. **Mode 2-5:** Classical Dead Time Polarity Settings
   - These modes represent typical configurations of polarity and should cover the active-high/low modes in available industry power switch gate drivers. The typical waveforms are shown in Figures 29.3-22 to 29.3-25.

3. **Modes 6 and 7:** Bypass delay on falling edge (FED) or rising edge (RED)
   - In these modes, either RED (Rising Edge Delay) or FED (Falling Edge Delay) is bypassed. As a result, the corresponding delay is not applied.

**Table: Typical Dead Time Generator Operating Modes**

| Mode | Mode Description |
|------|------------------|
| 1    | PWMxAs and PWMxB Pass Through/No Delay |
| 2    | Active High Complementary (AHC), see Figure 29.3-22 |
| 3    | Active Low Complementary (ALC), see Figure 29.3-23 |
| 4    | Active High (AH), see Figure 29.3-24 |
| 5    | Active Low (AL), see Figure 29.3-25 |
| 6    | PWMxAs Output = PWMxA In (No Delay) <br> PWMxB Output = PWMxA Input with Falling Edge Delay |
| 7    | PWMxAs Output = PWMxA Input with Rising Edge Delay <br> PWMxB Output = PWMxB Input with No Delay |

**Note:**
For all the modes above, the position of the binary switches S4 to S8 is set to 0.

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback