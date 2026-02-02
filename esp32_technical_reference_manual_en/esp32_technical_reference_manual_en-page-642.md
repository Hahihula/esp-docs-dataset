**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Section Header:**
Register 28.11. LEDC_HSTIMERx_CONF_REG

**Table Description:**
- **Columns:** 
  - Offset in hex (e.g., "0x00", "0x00")
  - Bit positions and names
- The table shows the bit layout for Register 28.11, including bits like LEDC_HSTIMERx, LEDC_CLK_DIV_NUM_HSTIMERx, etc.

**Bit Description:**
- **LEDC_TICK_SEL_HSTIMERx:** This is used to select APB_CLK or REF_TICK for high-speed timer.
  - Values:
    - `0`: APB_CLK
    - `1`: REF_TICK

- **LEDC_HSTIMERx_RST:** This bit is used to reset the high-speed timer. The counter value will be 'zero' after reset.

- **LEDC_HSTIMERx_PAUSE:** This bit is used to suspend the counter in a high-speed timer.
  - Values:
    - `0`: Not paused
    - `1`: Paused

- **LEDC_CLK_DIV_NUM_HSTIMERx:** This register is used to configure the division factor for the divider in high-speed timer. The least significant eight bits represent the fractional part.

- **LEDC_HSTIMERx_DUTY_RES:** This register is used to control the range of the counter in a high-speed timer.
  - Counter range: `[0, 2^LEDC_HSTIMERx_DUTY_RES]`
  - The maximum bit width for this counter is `20`.

**Additional Register Description:**
- **Register 28.12. LEDC_HSTIMERx_VALUE_REG:** This register can be read to get the current counter value of high-speed timer.

**Footer Information:**
- Page number and document version:
  - "642 ESP32 TRM (Version 5.6)"
  
- Company information at bottom left corner:
  - Espressif Systems

- Links for additional actions or feedback, such as submitting documentation.
  - Text links like “Submit Documentation Feedback”