

```markdown
## Register 8.63. PCR_SYSCLK_CONF_REG (0x0110)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)            |                                                                             |
| 30  | POR_CLK_XTAL_FREQ     | Represents the frequency of XTAL. Measurement unit: MHz (RO)                 |
| 24  |                        |                                                                             |
| 18  | PCR_SOC_CLK_SEL       | Configures to select clock source.<br>0: Select XTAL_CLK<br>1: Select PLL_CLK<br>2: Select RC_FAST_CLK<br>3: Reserved (R/W) |
| 17  |                        |                                                                             |
| 16  |                        |                                                                             |
| 8   | PCR_HS_DIV_NUM        | Represents HP_ROOT_CLK is derived from a high-speed clock source (such as SPLL) divided by 3. (HRO) |
| 7   |                        |                                                                             |
| 2   |                        |                                                                             |
| 1   |                        |                                                                             |
| 0   | PCR_LS_DIV_NUM        | Represents HP_ROOT_CLK is derived from a low-speed clock source (such as XTAL/FOSC) divided by 1. (HRO) |

PCR_LS_DIV_NUM: Represents HP_ROOT_CLK is derived from a low-speed clock source (such as XTAL/FOSC) divided by 1. (HRO)

PCR_HS_DIV_NUM: Represents HP_ROOT_CLK is derived from a high-speed clock source (such as SPLL) divided by 3. (HRO)

PCR_SOC_CLK_SEL: Configures to select clock source.
- 0: Select XTAL_CLK
- 1: Select PLL_CLK
- 2: Select RC_FAST_CLK
- 3: Reserved (R/W)

PCR_CLK_XTAL_FREQ: Represents the frequency of XTAL. Measurement unit: MHz (RO)
```

```markdown
## Register 8.64. PCR_CPU_WAITI_CONF_REG (0x0114)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 29  | POR_CPU_WAITI_DELAY_NUM       | Configures delay cycle when CPU enters WAITI mode. After delay, waiti_clk will close. (R/W) |
| 8   | PCR_CPU_WAIT_MODE_FORCE_ON    | Configures whether or not to force enable cpu_waiti_clk.<br>0: Not force enable<br>1: Force enable (R/W) |
| 7   | (reserved)                    |                                                                             |
| 4   | (reserved)                    |                                                                             |
| 3   | (reserved)                    |                                                                             |
| 2   | (reserved)                    |                                                                             |
| 1   | PCR_CPU_WAITI_DELAY_NUM       | Configures delay cycle when CPU enters WAITI mode. After delay, waiti_clk will close. (R/W) |
| 0   | Reset                         |                                                                             |

PCR_CPU_WAIT_MODE_FORCE_ON: Configures whether or not to force enable cpu_waiti_clk.
- 0: Not force enable
- 1: Force enable (R/W)

PCR_CPU_WAITI_DELAY_NUM: Configures delay cycle when CPU enters WAITI mode. After delay, waiti_clk will close. (R/W)
```