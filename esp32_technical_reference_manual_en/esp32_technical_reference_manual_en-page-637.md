**Title:**
Chapter 28 LED PWM Controller (LEDC)

**Subtitle:**
28.4 Registers

**Body Text:**

The addresses in this section are relative to the LED PWM base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **28.3 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Table:**
- **Register Name:** LEDC_HSCHn_CONF0_REG (n: 0-7) (0x00+0x14*n)
- **Address:** 
  - Bits [31:20] are reserved.
  - Bits [19:0]: 
    - `LEDC_IDLE_LV_HSCHn`: This bit is used to control the output value when high-speed channel n is inactive. (R/W)
    - `LEDC_SIG_OUT_EN_HSCHn`: This is the output enable control bit for high-speed channel n. (R/W)
    - `LEDC_TIMER_SEL_HSCHn`: There are four high-speed timers. These two bits are used to select one of them for a high-speed channel n: (R/W)

**Table Description:** 
- **Register Name:** LEDC_HSCHn_HPOINT_REG (n: 0-7) (0x04+0x14*n)
- **Address:**
  - Bits [31:20] are reserved.
  - Bits [19:0]: `LEDC_HPOINT_HSCHn`: The output value changes to high when htimerx(x=[0,3]), selected by high-speed channel n, has reached LEDC_HPOINT_HSCHn[19:0]. (R/W)

**Footer Information:** 
- Page number 637
- Document version ESP32 TRM (Version 5.6)
- Company name Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback