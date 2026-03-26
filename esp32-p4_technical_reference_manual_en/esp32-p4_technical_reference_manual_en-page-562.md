

```markdown
## 9.13 LP Peripheral Signal List

Table 9.13-1 shows the peripheral input/output signals via LP GPIO matrix.

Please pay attention to the configuration of the bit `LP_GPIO_FUNCn_OE_SEL`:

*   `LP_GPIO_FUNCn_OE_SEL = 1`: the output enable is controlled by the corresponding bit `n` of `LP_GPIO_ENABLE_REG`:
    -   `LP_GPIO_ENABLE_REG = 0`: output is disabled.
    -   `LP_GPIO_ENABLE_REG = 1`: output is enabled.

*   `LP_GPIO_FUNCn_OE_SEL = 0`: use the output enable signal from peripheral, for example `lp_spi_clk_pad_oe` in the column "Output enable signal when LP_GPIO_FUNCn_OE_SEL = 0" of Table 9.13-1. Note that the signals such as `lp_spi_clk_pad_oe` can be 1 ('1d1') or 0 ('1'd0), depending on the configuration of corresponding peripherals. If it's '1'd1 in column "Output enable signal when LP_GPIO_FUNCn_OE_SEL = 0", it indicates that once `LP_GPIO_FUNCn_OE_SEL` is cleared, the output signal is always enabled by default.

**Note:**
Signals are numbered consecutively, but not all signals are valid.
*   Only the signals with a name assigned in the column "Input signal" in Table 9.13-1 are valid input signals.
*   Only the signals with a name assigned in the column "Output signal" in Table 9.13-1 are valid output signals.
```