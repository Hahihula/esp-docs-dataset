**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Register Information:**
- Register Name: INT_ENA_PWM_REG (0x110)
- Description of the register in hexadecimal format.

**Interrupt Enable Bits Table:**

| Offset | Bit Number Range | Description |
|--------|------------------|-------------|
| 31     | 29 - 0           | Various interrupt enable bits for different PWM channels and events. |

**Interrupt Enable Bits Descriptions (continued from the image):**
- **INT_CAP2_INT_ENA:** The enable bit for the interrupt triggered by capture on channel 2.
- **INT_CAP1_INT_ENA:** The enable bit for the interrupt triggered by capture on channel 1.
- **INT_CAPO0_INT_ENA:** The enable bit for the interrupt triggered by capture on channel 0 (R/W).
- ... [Additional descriptions follow in a similar format]

**Footer:**
- "Continued on the next page..."
- Page number and version information:
  - ESP32 TRM (Version 5.6)
- Links to submit documentation feedback.

(Note: The detailed list of interrupt enable bits continues beyond what is shown, with each entry specifying which specific event or condition triggers an interrupt.)