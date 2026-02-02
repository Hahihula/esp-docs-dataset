**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Register Information for PWM_DT1_RED:**
- **Register Number:** 29.39.
- **Name:** PWM_DT1_RED_CFG_REG (0x0098)
- **Description:** Shadow register for RED. (R/W)
- **Bit Positions and Values:**
  - [31, 16] Reserved
  - [15, 0] Reset

**Register Information for PWM_CARRIER1_CFG:**
- **Register Number:** 29.40.
- **Name:** PWM_CARRIER1_CFG_REG (0x009c)
- **Description and Bit Positions with Values:**
  - [31, 16] Reserved
  - [15, 8] INVERT
  - [7, 4] SWTH
  - [3, 0] Reset

**Submodule Descriptions for PWM_CARRIER1:**

- **PWM_CARRIER1_IN_INVERT:** When set, invert the input of PWM1A and PWM1B for this submodule. (R/W)
  
- **PWM_CARRIER1_OUT_INVERT:** When set, invert the output of PWM1A and PWM1B for this submodule. (R/W)

- **PWM_CARRIER1_OSHWTH:** Width of the first pulse in number of periods of the carrier. (R/W)

- **PWM_CARRIER1_DUTY:** Carrier duty selection. Duty = PWM_CARRIER1_DUTY/8. (R/W)

- **PWM_CARRIER1_PRESCALE:** PWM carrier clock (PC_clk) prescale value. Period of PC_clk = period of PWM_clk * (PWM_CARRIER1_PRESCALE + 1). (R/W)

- **PWM_CARRIER1_EN:** When set, carrier function is enabled. When cleared, carrier1 is bypassed. (R/W)

**Footer:**
Espressif Systems
702 ESP32 TRM (Version 5.6)
Submit Documentation Feedback