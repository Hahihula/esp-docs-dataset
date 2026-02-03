**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
GoBack

**Register Information Section:**

- **Register Name:** MCPWM_DT2_RED_CFG_REG (0x0D0)
  - **Description:** Shadow register for RED. (R/W)
  - **Bit Description Table:**
    - Bit 31 to bit 0 are all set as '0'.
    - The label "Reset" is associated with the rightmost column.

- **Register Name:** MCPWM_CARRIER2_CFG_REG (0x0D4)
  - **Description and Bit Labels for each field in hexadecimal format:**
    - `0x0000_0000_0000_0000`
      - `0` to `31`: Reserved bits.
    - Fields:
      - `MCPWM_CARRIER2_IN_OFS` (bit 8)
        - Description: INVERT
      - `MCPWM_CARRIER2_OUT_OFS` (bit 7)
        - Description: TWTH
      - `MCPWM_CARRIER2_DUTY` (bit 6)
        - Description: DUTY
      - `MCPWM_CARRIER2_EN` (bit 5)
        - Description: EN
      - `MCPWM_CARRIER2 PRESCALE` (bits 4 to 0)
        - Description:
          - When set, carrier2 function is enabled. When cleared, carrier2 is bypassed.
          - Prescale value for PWM carrier clock.

- **Fields in MCPWM_CARRIER2_CFG_REG:**
  - `MCPWM_CARRIER2_EN` (bit 5): When set, carrier2 function is enabled; when cleared, it's by-passed. (R/W)
  - `MCPWM_CARRIER2 PRESCALE` (bits 4 to 0): PWM carrier clock prescale value.
    - Period of PC_clk = period of PWM_clk * (PWM_CARRIER_PRESCALE + 1). (R/W)

- **Additional Fields:**
  - `MCPWM_CARRIER2_DUTY`: Carrier duty selection. Duty = PWM_CARRIER_DUTY/8. (R/W)
  - `MCPWM_CARRIER2_OSHTWTH`: Width of the first pulse in number of periods of the carrier.
    - When set, invert the output of PWMA and PWA for this sub-module.

- **More Fields:**
  - `MCPWM_CARRIER2_OUT_INVERT`: Invert the input of PWMA and PWMAB for this sub-module. (R/W)

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback