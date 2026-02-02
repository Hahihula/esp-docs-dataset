**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Register Information:**
- Register Name: IOMUX_PIN_CTRL (0x00)
- Table:
  - Columns: PIN, CTRL3, CTRL2, CTRL1, CTRL0

**Instructions for Output Clocks:**

1. **For I2S0 (I2S0_CLK):**
   - Set `CLK_OUT1` to output clock.
     ```
     CLK_OUT1, then set PIN_CTRL[3:0] = 0x0;
     CLK_OUT2, then set PIN_CTRL[3:0] = 0x0 and PIN_CTRL[7:4] = 0x0;
     CLK_OUT3, then set PIN_CTRL[3:0] = 0x0 and PIN_CTRL[11:8] = 0x0.
     ```

2. **For I2S1 (I2S1_CLK):**
   - Set `CLK_OUT1` to output clock.
     ```
     CLK_OUT1, then set PIN_CTRL[3:0] = 0xF;
     CLK_OUT2, then set PIN_CTRL[3:0] = 0xF and PIN_CTRL[7:4] = 0x0;
     CLK_OUT3, then set PIN_CTRL[3:0] = 0xF and PIN_CTRL[11:8] = 0x0.
     ```

3. **For APLL Clock Output (APLL_CLK):**
   - Set `CLK_OUT1` to output clock.
     ```
     CLK_OUT1, then set PIN_CTRL[3:0] = 0x6;
     CLK_OUT2, then set PIN_CTRL[3:0] = 0x6 and PIN_CTRL[7:4] = 0x6;
     CLK_OUT3, then set PIN_CTRL[3:0] = 0x6 and PIN_CTRL[11:8] = 0x6. (Read/Write)
     ```

**Note Section:**
- Only the above mentioned combinations of clock source are possible.
- The `CLK_OUT1 ~ 3` can be found in the IO MUX Pin Summary.

**Footer Information:**
- Page Number: 48
- Company Name: Espressif Systems
- Document Version: ESP32 TRM (Version 5.6)
- Link Texts:
  - Submit Documentation Feedback