**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Back Navigation Link:** GoBack

---

**Register Information for Register 29.51 and 29.52**

- **Register Name**: PWM_DT2_CFG_REG (0x00c8)
- **Register Name**: PWM_DT2_FED_CFG_REG (0x00cc)

**Field Descriptions:**

- **PWM_DT2_CLK_SEL**
  - Description: Dead time generator clock selection.
  - Values:
    - 0: PWM_clk
    - 1: PT_clk

- **PWM_DT2_B_OUTBYPASS, PWM_DT2_A_OUTBYPASS**
  - Reference to Table S0 in Section 29.3-5 (Read/Write)

- **PWM_DT2_FED_OUTINVERT, PWM_DT2_RED_OUTINVERT**
  - Reference to Tables SS and S2 respectively.

- **PWM_DT2_FED_INSEL, PWM_DT2_RED_INSEL**
  - Reference to Table S5 in Section 29.3-5 (Read/Write)

- **PWM_DT2_B_OUTSWAP, PWM_DT2_A_OUTSWAP**
  - Reference to Tables SS7 and S6 respectively.

- **PWM_DT2_DEB_MODE**
  - Description: Dual-edge B mode.
  - Values:
    - FED/RED take effect on different paths separately (1)
    - FED/RED take effect on both directions

- **PWM_DT2_RED_UPMETHOD, PWM_DT2_FED_UPMETHOD**
  - Updating method for RED and FED respectively.

**Field Descriptions:**

- **PWM_DT2_RED_UPMETHOD**
  - Description:
    - When bit0 is set to 1 (TEZ)
    - When bit1 is set to TEP
    - When bit2 is set to sync

- **PWM_DT2_FED_UPMETHOD**
  - Description: Updating method for FED.

**Field Descriptions in Table Format:** 

| Field Name | Description |
|------------|-------------|
| PWM_DT2_CLK_SEL | Dead time generator clock selection. (0: PWM_clk; 1: PT_clk) |
| PWM_DT2_B_OUTBYPASS, PWM_DT2_A_OUTBYPASS | Refer to S0 in Table 29.3-5 (R/W) |
| PWM_DT2_FED_OUTINVERT, PWM_DT2_RED_OUTINVERT | Refer to SS and S2 respectively (R/W) |
| PWM_DT2_FED_INSEL, PWM_DT2_RED_INSEL | Refer to S5 in Table 29.3-5 (R/W) |
| PWM_DT2_B_OUTSWAP, PWM_DT2_A_OUTSWAP | Refer to SS7 and S6 respectively (R/W) |
| PWM_DT2_DEB_MODE | Dual-edge B mode: FED/RED take effect on different paths separately; 1 means both directions. |

**Field Descriptions in Table Format for PWM_DT2_FED_CFG_REG:** 

- **PWM_DT2_FED_UPMETHOD**
  - Description:
    - When bit0 is set to TEZ
    - When bit1 is set to TEP
    - When bit2 is set to sync

**Footer Information:**

- Company Name: Espressif Systems
- Document Version and Type: ESP32 TRM (Version 5.6)
- Page Number: 710
- Link for Submitting Documentation Feedback