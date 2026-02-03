**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Header:**
Register 36.30, MCPWM_GEN1_STMP_CFG_REG (0x0074)

**Table Description:**
- The table shows the binary representation of a register with various bits labeled from 'reserved' to specific bit numbers.
- Bits are numbered and separated by spaces.

**Text Content under Table 1:**

**Title:** MCPWM_GEN1_A_UPMETHOD

**Body Text:**
Update method for PWM generator 1 time stamp A's active register. When all bits are set to O: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update (R/W)

**Title:** MCPWM_GEN1_B_UPMETHOD

**Body Text:**
Update method for PWM generator 1 time stamp B's active register. When all bits are set to O: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update (R/W)

**Title:** MCPWM_GEN1_A_SHDW_FULL

**Body Text:**
Set and reset by hardware. If set, PWM generator 1 time stamp A's shadow reg is filled and waiting to be transferred to A's active reg. If cleared, A's active reg has been updated with shadow register latest value (R/W/TSC/SC)

**Title:** MCPWM_GEN1_B_SHDW_FULL

**Body Text:**
Set and reset by hardware. If set, PWM generator 1 time stamp B's shadow reg is filled and waiting to be transferred to B's active reg. If cleared, B's active reg has been updated with shadow register latest value (R/W/TSC/SC)

---

**Section Header:**
Register 36.31, MCPWM_GEN1_TSTMP_A_REG (0x0078)

**Table Description:**
- The table shows the binary representation of a register similar to Table 1.

**Text Content under Table 2:**

**Title:** MCPWM_GEN1_A

**Body Text:**
PWM generator 1 time stamp A's shadow register. (R/W)

**Title:** MCPWM_GEN1_B_STMP_B_REG (0x007C)

**Body Text:**
PWM generator 1 time stamp B's shadow register. (R/W)

---

**Footer Information:**

- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 1383

**Link Text:** Submit Documentation Feedback