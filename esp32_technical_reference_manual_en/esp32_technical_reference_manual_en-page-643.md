**Title: Chapter 28 LED PWM Controller (LEDC)**

**Subtitle: Register 28.13. LEDC_LSTIMERx_CONF_REG**

- **Field Description:** 
  - `LEDCLSTIMERx PARA_UP`
    - **Description:** Set this bit to update LEDC_CLK_DIV_NUM_LSTIMERx and LEDC_LSTIMERx DUTY_RES.
    - **Access:** (R/W)
  
  - `LEDC_TICK_SEL_LSTIMERx`
    - **Description:** This bit is used to select RTC_SLOW_CLK or REF_TICK for low-speed timer x. 
      - `1: RTC_SLOW_CLK;`
      - `0: REF_TICK.`

  - `LEDC_LSTIMERx_RST`
    - **Description:** This bit is used to reset the low-speed timer.
      - The counter will show 0 after reset.

  - `LEDC_LSTIMERx_PAUSE`
    - **Description:** This bit is used to suspend the counter in a low-speed timer x. 

  - `LEDCLK_DIV_NUM_LSTIMERx`
    - **Description:** This register is used to configure the division factor for the divider in a low-speed timer.
      - The least significant eight bits represent the fractional part.

  - `LEDC_LSTIMERx_DUTY_RES`
    - **Description:** This register is used to control the range of the counter in a low-speed timer x. 
      - The counter range is [0, 2^LEDCLSTIMERx_DUTY_RES], with max bit width for counter being 20.

**Register 28.14. LEDC_LSTIMERx_VALUE_REG**

- **Field Description:**
  - `LEDC_LSTIMERx_CNT`
    - **Description:** Software can read this register to get the current counter value of a low-speed timer x.
      - **Access:** (RO)

**Footer Information:**
- Page number: "643"
- Document version and company information:
  - ESP32 TRM (Version 5.6)
  - Espressif Systems
  - Submit Documentation Feedback

**Diagram Description in the Image:**

The image contains a diagram showing bit positions for various fields within registers related to LEDC configuration, including `LEDCLSTIMERx PARA_UP`, `LEDC_LSTIMERx_DUTY_RES`, and others. The bits are labeled with their respective functions as described above.

- **Bit Positions:** 
  - Bits from the top: `31` down to `0`
  - Specific bit positions for fields like `LEDCLSTIMERx PARA_UP`, `LEDC_LSTIMERx_DUTY_RES`, etc., have specific labels indicating what each set or reset value does.

- **Reset Values:** 
  - The diagram shows the values that correspond with a "reset" state, such as `0x00` for certain fields. 

This detailed description should help in understanding and referencing this section of documentation without needing to view the image directly.