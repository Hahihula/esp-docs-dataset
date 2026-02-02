**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.25. PWM_DTO_RED_CFG_REG (0x060)

**Field Description for Register 29.25:**
- **PWM_DTO_RED**: Shadow register for RED.
- The field is a bitfield with bits labeled from `31` to `0`.

**Section Header:**
Register 29.26. PWM_CARRIERO_CFG_REG (0x064)

**Field Descriptions and Definitions in Register 29.26:**

- **PWM_CARRIERO_IN_INVERT**: When set, invert the input of PWM0A and PWM0B for this submodule.
  - The field is a bitfield with bits labeled from `31` to `0`.

- **PWM_CARRIERO_OUT_INVERT**: When set, invert the output of PWM0A and PWM0B for this submodule.
  - The field is a bitfield with bits labeled from `31` to `0`.

- **PWM_CARRIERO_OSHWTH**: Width of the first pulse, in number of periods of the carrier. (R/W)
  - The field has values ranging from `0` to `7`.

- **PWM_CARRIERO_DUTY**: Carrier duty selection.
  - Duty = PWM_CARRIERO_DUTY/8.

- **PWM_CARRIERO_PRESCALE**: PWM carrier0 clock (PC_clk) prescale value. Period of PC_clk = period of PWM_CLK * (PWM_CARRIERO_PRESCALE + 1).
  - The field is a bitfield with bits labeled from `31` to `0`.

- **PWM_CARRIERO_EN**: When set, carrier0 function is enabled.
  - When cleared, carrier0 is bypassed.

**Footer:**
Espressif Systems
693 ESP32 TRM (Version 5.6)
Submit Documentation Feedback