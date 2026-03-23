

```markdown
| Name                                 | Description                          | Address   | Access |
|--------------------------------------|--------------------------------------|-----------|--------|
| PCR_GDMA_CONF_REG                   | GDMA configuration register         | 0x00BC    | R/W    |
| PCR_SPI2_CONF_REG                   | SPI2 configuration register         | 0x00C0    | R/W    |
| PCR_SPI2_CLKM_CONF_REG              | SPI2_CLKM configuration register    | 0x00C4    | R/W    |
| PCR_AES_CONF_REG                    | AES configuration register          | 0x00C8    | R/W    |
| PCR_SHA_CONF_REG                    | SHA configuration register          | 0x00CC    | R/W    |
| PCR_RSA_CONF_REG                    | RSA configuration register          | 0x00D0    | R/W    |
| PCR_RSA_PD_CTRL_REG                 | RSA power control register          | 0x00D4    | R/W    |
| PCR_ECC_CONF_REG                    | ECC configuration register          | 0x00D8    | R/W    |
| PCR_ECC_PD_CTRL_REG                 | ECC power control register          | 0x00DC    | R/W    |
| PCR_DS_CONF_REG                     | DS configuration register           | 0x00E0    | R/W    |
| PCR_HMAC_CONF_REG                   | HMAC configuration register         | 0x00E4    | R/W    |
| PCR_IOMUX_CONF_REG                  | IOMUX configuration register        | 0x00E8    | R/W    |
| PCR_IOMUX_CLK_CONF_REG              | IOMUX_CLK configuration register    | 0x00EC    | R/W    |
| PCR_MEM_MONITOR_CONF_REG            | MEM_MONITOR configuration register   | 0x00FO    | R/W    |
| PCR_TRACE_CONF_REG                  | TRACE configuration register        | 0x00FC    | R/W    |
| PCR_ASSIST_CONF_REG                 | ASSIST configuration register       | 0x0100    | R/W    |
| PCR_CACHE_CONF_REG                  | CACHE configuration register        | 0x0104    | R/W    |
| PCR_MODEM_APB_CONF_REG              | MODEM_APB configuration register     | 0x0108    | R/W    |
| PCR_TIMEOUT_CONF_REG                | TIMEOUT configuration register      | 0x010C    | R/W    |
| PCR_SYSCLK_CONF_REG                 | SYSCLK configuration register       | 0x0110    | varies |
| PCR_CPU_WAITI_CONF_REG              | CPU_WAITI configuration register     | 0x0114    | R/W    |
| PCR_CPU_FREQ_CONF_REG               | CPU_FREQ configuration register      | 0x0118    | R/W    |
| PCR_AHB_FREQ_CONF_REG               | AHB_FREQ configuration register      | 0x011C    | R/W    |
| PCR_APB_FREQ_CONF_REG               | APB_FREQ configuration register      | 0x0120    | R/W    |
| PCR_PLL_DIV_CLK_EN_REG              | SPPLL DIV clock-gating configuration register | 0x0128 | R/W    |
| PCR_CTRL_32K_CONF_REG               | 32kHz clock configuration register   | 0x0134    | R/W    |
| PCR_SRAM_POWER_CONF_REG             | HP SRAM/ROM configuration register   | 0x0138    | R/W    |
| PCR_RESET_EVENT_BYPASS_REG          | Reset event bypass backdoor configuration register | 0x0FF0 | R/W    |

Frequency Statistics Register
------------------------------
PCR_SYSCLK_FREQ_QUERY_O_REG         | SYSCLK frequency query register O   | 0x0124    | HRO

Version Register
-----------------
PCR_DATE_REG                         | Version control register            | 0x0FFC    | R/W


## 8.4.2 LP System Clock Registers

The addresses in this section are relative to the Low-power Clock/Reset Register (LP_CLKRST) base address.
For base address, please refer to Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                 | Description                          | Address   | Access |
|--------------------------------------|--------------------------------------|-----------|--------|
| Configuration Registers              |                                      |           |        |
| LP_CLKRST_LP_CLK_CONF_REG           | Configures the root clk of LP system | 0x0000    | R/W    |
```