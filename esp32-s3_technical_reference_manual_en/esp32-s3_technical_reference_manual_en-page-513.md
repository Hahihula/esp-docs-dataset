**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Header:**
Register 6.35. IO_MUX_PIN_CTRL_REG (0x0000)

**Table:**
- The table shows the register layout with labels such as "IO_MUX_PAD_POWER_CTRL", "IO_MUX_SWITCH_PRT_NUM", etc., and corresponding bit positions from right to left.

**Body Text:**

1. **IO_MUX_PIN_CTRL_CLKx**: 
   - If you want to output clock for I2S0, set it (R/W).
     ```
     CLK_OUT1, then set IO_MUX_PIN_CTRL_CLK1 = 0x0;
     CLK_OUT2, then set IO_MUX_PIN_CTRL_CLK2 = 0x0;
     CLK_OUT3, then set IO_MUX_PIN_CTRL_CLK3 = 0x0.
     ```
   - If you want to output clock for I2S1:
     ```
     CLK_OUT1, then set IO_MUX_PIN_CTRL_CLK1 = 0xF;
     CLK_OUT2, then set IO_MUX_PIN_CTRL_CLK2 = 0xF;
     CLK_OUT3, then set IO_MUX_PIN_CTRL_CLK3 = 0xF.
     ```

   - Note: Only the above mentioned combinations of clock source and clock output pins are possible. The CLK_OUT1 ~ 3 can be found in `IO_MUX Pin Function List`.

2. **IO_MUX_SWITCH_PRT_NUM**:
   - GPIO pin power switch delay, delay unit is one APB clock (R/W).

3. **IO_MUX_PAD_POWER_CTRL**:
   - Select power voltage for GPIO33 ~ 37 and GPIO47 ~ 48.
     ```
     VDD_SPI 1.8V; O: select VDD3P3_CPU 3.3V. (R/W)
     ```

**Footer:**
- Page number: 513
- Company name: Espressif Systems
- Document version and type: ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- GoBack

**Additional Information:**
- Submit Documentation Feedback