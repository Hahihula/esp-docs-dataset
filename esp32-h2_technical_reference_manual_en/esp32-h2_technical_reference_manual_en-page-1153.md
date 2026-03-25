

```markdown
Register 36.65. MCPWM_CAP_CH1_REG (0x0100)

MCPWM_CAP1_VALUE Represents the value of the last capture on channel 1. (RO)

Register 36.66. MCPWM_CAP_CH2_REG (0x0104)

MCPWM_CAP2_VALUE Represents the value of the last capture on channel 2. (RO)

Register 36.67. MCPWM_CAP_STATUS_REG (0x0108)

(reserved) | MCPWM_CAP2_EDGE | MCPWM_CAP1_EDGE | MCPWM_CAPO_EDGE
-----------|-----------------|-----------------|---------------
31         | 3               | 2               | 1               | 0

MCPWM_CAPO_EDGE Represents the edge of the last capture trigger on channel 0.
0: Rising edge
1: Falling edge
(RO)

MCPWM_CAP1_EDGE Represents the edge of the last capture trigger on channel 1. See details in MCPWM_CAPO_EDGE. (RO)

MCPWM_CAP2_EDGE Represents the edge of the last capture trigger on channel 2. See details in MCPWM_CAPO_EDGE. (RO)
```