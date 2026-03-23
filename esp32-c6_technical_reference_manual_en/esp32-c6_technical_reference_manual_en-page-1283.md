

```markdown
Register 36.63. MCPWM_CAP_CH2_CFG_REG (0x00F8)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 13  | MCPWM_CAP2_SW                  | Configures whether or not to trigger a software forced capture on channel 2. O: Not trigger<br>1: Trigger (WT) |
| 12  | MCPWM_CAP2_IN_INVERT           | Configures whether or not to invert the CAP2 from GPIO matrix before prescale.<br>O: No effect<br>1: Invert (R/W) |
| 11  | MCPWM_CAP2_PRESCALE            | Configures the value of prescaling on the rising edge of CAP2.<br>Prescale value = PWM_CAP2_PRESCALE + 1. (R/W) |
| 10  |                                |                                                                             |
| 3   | MCPWM_CAP2_MODE                | Configures the edge of capture on channel 2 after prescaling.<br>When bit0 is set to 1: enable capture on the falling edge.<br>When bit1 is set to 1: enable capture on the rising edge. (R/W) |
| 2   |                                |                                                                             |
| 1   | MCPWM_CAP2_EN                  | Configures whether or not to enable capture on channel 2.<br>O: Not enable<br>1: Enable (R/W) |

Register 36.64. MCPWM_CAP_CHO_REG (0x00FC)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  |                        |                                                                             |
|     | MCPWM_CAPO_VALUE       | Represents the value of the last capture on channel O. (RO)                  |

```
Note: The diagram for Register 36.63 shows bit positions and labels corresponding to each field as described in the text above, with "reserved" bits marked appropriately at position 31 down to certain bits not used or defined per register context. Similarly, Register 36.64's diagram reflects a single field spanning all available bits (implied by the horizontal bar labeled MCPWM_CAPO_VALUE), indicating it holds the read-only capture value for channel O.
```