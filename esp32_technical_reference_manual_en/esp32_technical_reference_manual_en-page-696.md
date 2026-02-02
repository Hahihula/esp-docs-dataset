**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.30. PWM_GEN1_STMP_CFG_REG (0x0074)

**Table Description and Values for Register 29.30:**
- The table shows the bit positions of register 29.30 with labels such as `PWM_GEN1_B_SHDW_FULL`, `PWM_GEN1_A_SHDW_FULL`, etc.
- Each label is followed by a description:
  - **PWM_GEN1_B_SHDW_FULL**: Set and reset by hardware; if set, PWM generator 1 time stamp B's shadow register is filled to be transferred to timestamp A’s active register. If cleared, the time stamp B's active register has been updated with the shadow register latest value.
  - **PWM_GEN1_A_SHDW_FULL**: Same as above but for timestamp A instead of B.

**Additional Information:**
- `PWM_GEN1_B_UPMETHOD` and `PWM_GEN1_A_UPMETHOD`: Descriptions about updating methods when specific bits are set to certain values (TEZ, TEP).

**Section Header:**
Register 29.31. PWM_GEN1_TSTMP_A_REG (0x0078)

**Table Description for Register 29.31:**
- Similar table format as above showing bit positions and labels like `PWM_GEN1_A`.

**Additional Information:**
- Descriptions of the shadow register related to timestamp A.

**Section Header:**
Register 29.32. PWM_GEN1_TSTMP_B_REG (0x007c)

**Table Description for Register 29.32:**
- Similar table format as above showing bit positions and labels like `PWM_GEN1_B`.

**Additional Information:**
- Descriptions of the shadow register related to timestamp B.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback