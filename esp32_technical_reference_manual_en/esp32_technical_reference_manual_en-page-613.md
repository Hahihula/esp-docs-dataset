**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Header:**
Register 27.3. CLKSRC_REG (0x000C)

**Body Text with Details and Table:**

- **Title:** CLKSRC_REG Clock divider source for two SD cards is supported.
- Each card has two bits assigned to it.

For example:
- bit[1:0] are assigned for card 0
- bit[3:2] are assigned for card 1

Card 0 maps and internally routes clock divider [0:3] outputs to cclk_out[1:0] pins, depending on bit value.
- **Table with Values**:
  - `00`: Clock divider O;
  - `01`: Clock divider 1;
  - `10`: Clock divider 2;
  - `11`: Clock divider 3.

In MMC/Ver3.3-only controller, only one clock divider is supported.
The cclk_out is always from clock divider [0], and this register is not implemented (R/W).

**Section Header:**
Register 27.4. CLKENA_REG (0x0010)

**Body Text with Details and Table:**

- **Title:** CCLK_ENABEL Clock-enable control for two SD card clocks and one MMC card clock is supported.
- `0`: Clock disabled;
- `1`: Clock enabled.

In MMC/Ver3.3-only mode, since there is only one cclk_out, only cclk_enable[0] is used (R/W).

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Links:**
- GoBack