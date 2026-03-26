

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration registers**                |                                                                             |           |        |
| LP_CLKRST_LP_CLK_CONF_REG                 | LP root clock configuration register                                      | 0x0000    | R/W    |
| LP_CLKRST_LP_CLK_EN_REG                   | LP always on peripheral clock configuration register                      | 0x0008    | R/W    |
| LP_CLKRST_LP_RST_EN_REG                   | LP always on peripheral reset configuration register                       | 0x000C    | R/W    |
| LP_CLKRST_RESET_CAUSE_REG                 | HP CPU and LP CPU reset cause register                                     | 0x0010    | varies |
| LP_CLKRST_HPCPU_RESET_CTRL0_REG           | HP CPU reset configuration register 0                                      | 0x0014    | varies |
| LP_CLKRST_HPCPU_RESET_CTRL1_REG           | HP CPU reset configuration register 1                                      | 0x0018    | R/W    |
| LP_CLKRST_FOSC_CNTL_REG                   | RC_FAST_CLK frequency configuration register                               | 0x001C    | R/W    |
| LP_CLKRST_XTAL32K_REG                     | XTAL32K_CLK configuration register                                        | 0x0030    | R/W    |
| LP_CLKRST_HP_CLK_CTRL_REG                 | HP clock control register                                                  | 0x0040    | R/W    |
| LP_CLKRST_HP_USB_CLKSTR_CTRL0_REG         | USB clock and reset control register 0                                     | 0x0044    | R/W    |
| LP_CLKRST_HP_USB_CLKSTR_CTRL1_REG         | USB clock and reset control register 1                                     | 0x0048    | R/W    |
| LP_CLKRST_HP_SDMMC_EMAC_RST_CTRL_REG      | SDMMC and EMAC reset control register                                      | 0x004C    | R/W    |
| **Version register**                      | Version control register                                                   | 0x03FC    | R/W    |
```

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration registers**                |                                                                             |           |        |
| LPPERI_CLK_EN_REG                         | LP peripheral bus clock configuration register                             | 0x0000    | R/W    |
| LPPERI_CORE_CLK_SEL_REG                   | LP peripheral function clock configuration register                        | 0x0004    | R/W    |
| LPPERI_RESET_EN_REG                       | LP peripheral reset configuration register                                  | 0x0008    | varies |
| LPPERI_CPU_REG                            | LP CPU access configuration register                                       | 0x000C    | R/W    |
| LPPERI_MEM_CTRL_REG                       | LP UART miscellaneous control register                                     | 0x0028    | varies |
| LPPERI_ADC_CTRL_REG                       | LP ADC clock configuration register                                        | 0x002C    | R/W    |
| LPPERI_LP_I2S_RXCLK_DIV_NUM_REG           | LP I2S RX clock configuration register                                     | 0x0030    | R/W    |
| LPPERI_LP_I2S_RXCLK_DIV_XYZ_REG            | LP I2S RX clock configuration register                                     | 0x0034    | R/W    |
| **Version register**                      |                                                                             |           |        |
```