**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Header:**
Register 9.1. RTC_CNTL_OPTIONSO_REG (0x0000)

**Table:**
- Columns are labeled from "31" to "0".
- Each row corresponds to a specific register bit with descriptions such as "RTC_CNTL_SW_SYS_RST", "RTC_CNTL_DG.Wrap_Force_NORST", etc.

**Descriptions of Register Bits in Markdown format:**

- **RTC_CNTL_SW_SYS_RST**: SW system reset. (WO)
- **RTC_CNTL_DG.WRAPFORCE_NORST**: The digital core forces no reset in deep sleep. (R/W)
- **RTC_CNTL_DG.WRAPFORCE_RST**: The digital core can force a reset in deep sleep. (R/W)
- **RTC_CNTL_BIAS_CORE_FUEL**: BIAS_CORE force power up. (R/W)
- **RTC_CNTL_BIAS_CORE_PD**: BIAS_CORE force power down. (R/W)
- **RTC_CNTL_BIAS_COREOLLOW_8M**: BIAS_CORE follow CK8M. (R/W)
- **RTC_CNTL_BIAS_I2C_FUEL**: BIAS_I2C force power up. (R/W)
- **RTC_CNTL_BIAS_I2C_PD**: BIAS_I2C force power down. (R/W)
- **RTC_CNTL_BIAS_I2COLLOW_8M**: BIAS_I2C follow CK8M. (R/W)
- **RTC_CNTL_BIASFORCE_NOSLEEP**: BIAS_SLEEP force no sleep. (R/W)
- **RTC_CNTL_BIASFORCE_SLEEP**: BIAS_SLEEP force sleep. (R/W)
- **RTC_CNTL_BIASLEEPOLLOW_8M**: BIAS_SLEEP follow CK8M. (R/W)
- **RTC_CNTL_XTL FORCE_PU**: Crystal force power up. (R/W)
- **RTC_CNTL_XTL FORCE_PD**: Crystal force power down. (R/W)
- **RTC_CNTL_BBPLL FORCE_FU**: BB_PLL force power up. (R/W)
- **RTC_CNTL_BBPLL FORCE_PD**: BB_PLL force power down. (R/W)
- **RTC_CNTL_BBPLL_I2C FORCEFU**: BB_PLL_I2C force power up. (R/W)
- **RTC_CNTL_BBPLL_I2C FORCEPD**: BB_PLL_I2C force power down. (R/W)
- **RTC_CNTL_BB_I2C FORCE_FU**: BB_I2C force power up. (R/W)
- **RTC_CNTL_BB_I2C FORCE_PD**: BB_I2C force power down. (R/W)

**Footer:**
Continued on the next page...

**Page Information at Bottom of Page:**
Espressif Systems
196 ESP32 TRM (Version 5.6) Submit Documentation Feedback