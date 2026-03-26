

```markdown
Register 1013. HP_SYS_CLKRST_PERI_CLK_CTRL00_REG (0x0030)

| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                  | -                                                                                                                                          |
| 30  | HP_SYS_CLKRST_EMAC_RX_CLK_EN                                               | -                                                                                                                                          |
| 29  | HP_SYS_CLKRST_EMAC_RX_CLK_SRC_SEL                                          | -                                                                                                                                          |
| 28  | HP_SYS_CLKRST_RMII_CLK_SRC_SEL                                             | -                                                                                                                                          |
| 27  | HP_SYS_CLKRST_PAD_EMAC_REF_CLK_EN                                          | -                                                                                                                                          |
| 26  | HP_SYS_CLKRST_PSRAM_CORE_CLK_DIV_NUM                                      | -                                                                                                                                          |
| 25  | HP_SYS_CLKRST_PSRAM_CORE_CLK_EN                                            | -                                                                                                                                          |
| 24  | HP_SYS_CLKRST_PSRAM_PLL_CLK_SRC_SEL                                       | -                                                                                                                                          |
| 23  | HP_SYS_CLKRST_FLASH_CLK_SRC_SEL                                           | Configures the clock source for FLASH_CLK. <br> O: XTAL_CLK<br> 1: SPLL_CLK (480 MHz)<br> 2: CPLL_CLK (360 MHz)<br> 3: Invalid (R/W) |
| 22  | HP_SYS_CLKRST_FLASH_PLL_CLK_EN                                            | Configures whether to enable FLASH_PLL_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                         |
| 21  | HP_SYS_CLKRST_FLASH_CORE_CLK_EN                                           | Configures whether to enable FLASH_CORE_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                         |
| 20  | HP_SYS_CLKRST_FLASH_CORE_CLK_DIV_NUM                                     | Configures the clock divisor of FLASH_CORE_CLK. (R/W)                                                                                     |
| 19  | HP_SYS_CLKRST_PSRAM_CLK_SRC_SEL                                          | Configures the clock source for PSRAM_CLK. <br> O: XTAL_CLK<br> 1: MPLL_CLK<br> 2: SPLL_CLK (480 MHz)<br> 3: CPLL_CLK (360 MHz) (R/W) |
| 18  | HP_SYS_CLKRST_PSRAM_PLL_CLK_EN                                           | Configures whether to enable PSRAM_PLL_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                         |
| 17  | HP_SYS_CLKRST_PSRAM_CORE_CLK_EN                                          | Configures whether to enable PSRAM_CORE_CLK. <br> O: Disable<br> 1: Enable (R/W)                                                         |

Reset value for bits:
- Bit 30–24: All 0
- Bit 23: 1
- Bit 22: 1
- Bit 21: 1
- Bit 20: 1
- Bit 19: 3
- Bit 18: 1
- Bit 17: 1

Continued on the next page...
```