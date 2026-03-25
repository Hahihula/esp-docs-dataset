

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PCR_CPU_WAITI_CONF_REG                    | Configuration register for gating CPU clock in wait for interrupt mode                           | 0x0110    | R/W    |
| PCR_CPU_FREQ_CONF_REG                     | CPU_CLK frequency configuration register                                                      | 0x0114    | R/W    |
| PCR_AHB_FREQ_CONF_REG                     | AHB_CLK frequency configuration register                                                     | 0x0118    | R/W    |
| PCR_APB_FREQ_CONF_REG                     | APB_CLK frequency configuration register                                                     | 0x011C    | R/W    |
| PCR_PLL_DIV_CLK_EN_REG                    | Configuration register for gating PLL divided clocks                                         | 0x0124    | R/W    |
| PCR_CTRL_TICK_CONF_REG                    | Clock divisor configuration register                                                          | 0x012C    | R/W    |
| PCR_CTRL_32K_CONF_REG                     | 32 kHz clock configuration register                                                           | 0x0130    | R/W    |
| PCR_SRAM_POWER_CONF_O_REG                 | HP SRAM/ROM configuration register                                                            | 0x0134    | R/W    |
| PCR_SRAM_POWER_CONF_1_REG                 | HP SRAM/ROM configuration register                                                            | 0x0138    | R/W    |
| PCR_SEC_CONF_REG                          | Clock source configuration register for External Memory Encryption and Decryption              | 0x013C    | R/W    |
| PCR_BUS_CLK_UPDATE_REG                    | Configuration register for applying updated high-performance system clock sources             | 0x0148    | R/W/WTC|
| PCR_SAR_CLK_DIV_REG                       | SAR ADC clock divisor configuration register                                                 | 0x014C    | R/W    |
| Frequency Data Register                   |                                                                                                  |           |        |
| PCR_SYSCLK_FREQ_QUERY_O_REG               | System clock frequency query 0 register                                                       | 0x0120    | HRO    |
| Version Register                          |                                                                                                  |           |        |
| PCR_DATE_REG                              | Version control register                                                                       | 0x0FFC    | R/W    |

### 7.4.2 LP System Clock Register Summary

The addresses of the last two registers with the LPPERI prefix in this section are relative to the Low-power Peripheral Register (LPPERI) base address. The addresses of the third and fourth to last registers with the LP_AON prefix in this section are relative to the Low-power Always-on Register (LP_AON) base address. The other addresses in this section are relative to the Low-power Clock/Reset Register (LP_CLKRST) base address. For base address, please refer to Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Configuration Registers                    |                                                                                                  |           |        |
| LP_CLKRST_LP_CLK_CONF_REG                 | LP system clock source configuration register                                                  | 0x0000    | R/W    |
| LP_CLKRST_LP_CLK_PO_EN_REG                | Configuration register for gating clock signals to pins                                       | 0x0004    | R/W    |
```