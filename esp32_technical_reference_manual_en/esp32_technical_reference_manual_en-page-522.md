**Chapter Title:**
Chapter 24. Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.43. EMACWDGTO_REG (0x10DC)

**Field Description Table for Register 24.43:**

| Bit | Name          |
|-----|--------------|
| 17-16| Reserved     |
| 15   | PWDOGEN      |
| 14   | Reserved     |
| 13   | Reserved     |
| 0    | Reset        |

**Field Details for Register 24.43:**

- **PWDOGEN**: When this bit is set and Bit[23] (WD) of EMACCONFIG_REG is reset, the WTO field (Bits[13:0]) is used as watchdog timeout for a received frame. When this bit is cleared, the watchdog timeout for a received frame is controlled by setting Bits[23] (WD) and Bit[20] (JE) in EMACCONFIG_REG.

- **WDOGTO**: When Bit[16] (WE) is set and Bit[23] (WD) of EMACCONFIG_REG is reset, this field is used as watchdog timeout for a received frame. If the length of a received frame exceeds the value of this field, such frame is terminated and declared an error frame.

**Section Header:**
Register 24.44. EMAC_EX_CLKOUT_CONF_REG (0x0800)

**Field Description Table for Register 24.44:**

| Bit | Name          |
|-----|--------------|
| 7   | Reserved     |
| 4-3 | Reserved     |
| 0   | Reset        |

**Field Details for Register 24.44:**

- **EMAC_CLK_OUT_H_DIV_NUM**: RMII CLK using internal APLL CLK, the half divider number when using RMII PHY.

- **EMAC_CLK_OUT_DIV_NUM**: RMII CLK using internal APLL CLK, the whole divider number when using RMII PHY

**Footer Information:**
Espressif Systems
Page 522 of ESP32 TRM (Version 5.6)
Submit Documentation Feedback