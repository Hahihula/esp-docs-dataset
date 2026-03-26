

```markdown
Register 10.66. LP_CLKRST_XTAL32K_REG (0x0030)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | ... | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|-----|---|---|
|     | LP_CLKRST_DAC_XTAL32K   | LP_CLKRST_DBUF_XTAL32K | LP_CLKRST_DGM_XTAL32K | LP_CLKRST_DRES_XTAL32K | (reserved) |
| Value | 3 | 0 | 3 | 3 | 0 | 0 | ... | 0 | 0 | 0 | Reset |

LP_CLKRST_DRES_XTAL32K Configures the bias resistor of XTAL32K_CLK.
O: Turn off internal resistor, use external resistor
1-3: Internal bias resistor value (R/W)

LP_CLKRST_DGM_XTAL32K Configures the gm of XTAL32K_CLK. (R/W)

LP_CLKRST_DBUF_XTAL32K Configures the buffer of XTAL32K_CLK.
O: Single-ended buffer
1: Differential buffer (R/W)

LP_CLKRST_DAC_XTAL32K Configures the bias current DAC of XTAL32K_CLK. (R/W)
```