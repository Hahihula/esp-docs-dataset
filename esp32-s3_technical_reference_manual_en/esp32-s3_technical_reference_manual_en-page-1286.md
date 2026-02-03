**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Header:**
Register 34.3. SDHOST_CLKSRC_REG (0x0000C)

**Body Text and Table Description for Register 34.3 - SDHOST_CLKSRC_REG**

- **Title:** SDHOST_CLKSRC_REG
- **Description:** Clock divider source for two SD cards is supported. Each card has two bits assigned to it.
  - For example, bit[1:0] are assigned for card 0; bit[3:2] are assigned for card 1.

**Table Description (Binary Table):**
- Columns labeled as "0x0000" and binary values from rightmost column:
  - Bit positions range from `4` to `0`
  - Values include `Reset`, `0x0`

**Body Text:**
Card O maps and internally routes clock divider[0:3] outputs to cclk_out[1:0] pins, depending on bit value. (R/W)

- **Binary Values:** 
  - OO : Clock divider 0;
  - O1 : Clock divider 1;
  - 10 : Clock divider 2;
  - 11 : Clock divider 3.

**Section Header:**
Register 34.4. SDHOST_CLKENA_REG (0x0010)

**Body Text and Table Description for Register 34.4 - SDHOST_CLKENA_REG**

- **Title:** SDHOST_CLKENA_REG
- **Description:** Clock-enable control

**Table Description (Binary Table):**
- Columns labeled as "0x000" with binary values from rightmost column:
  - Bit positions range from `18` to `0`
  - Values include `Reset`, `0x0`

**Body Text:**
SDHOST_LP_ENABLE
- **Description:** Disable clock when the card is in IDLE state. One bit per card.
  - (R/W)
  - O : Clock disabled;
  - I : Clock enabled.

SDHOST_CLK ENABLE
- **Description:** Clock-enable control for two SD card clocks and one MMC card clock supported, with a description of how each position corresponds to the enablement or disablement state:
  - One bit per card.
  - (R/W)
  - O : Clock disabled;
  - I : Clock enabled.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)