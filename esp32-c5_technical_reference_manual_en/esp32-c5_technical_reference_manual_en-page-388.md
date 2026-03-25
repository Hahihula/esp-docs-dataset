

```markdown
Note that the function of automatic frequency reduction can be disabled (already disabled by default) by configuring `APB_DECREASE_DIV_NUM` to 0.

### 9.2.4.2 LP System Clock

The LP system can operate when most other clocks are disabled. LP system clocks include `LP_SLOW_CLK` and `LP_FAST_CLK`.

The clock sources for `LP_SLOW_CLK` and `LP_FAST_CLK` are low-frequency clocks:

*   `LP_SLOW_CLK` can be derived from:
    -   `RC_SLOW_CLK`
    -   `XTAL32K_CLK`
    -   `OSC_SLOW_CLK`

*   `LP_FAST_CLK` can be derived from:
    -   20 MHz/24 MHz `XTAL_D2_CLK`, which is `XTAL_CLK` divided by 2
    -   `RC_FAST_CLK`
    -   `XTAL_CLK`

The clock source of `LP_DYN_SLOW_CLK` is `LP_SLOW_CLK`. There is no frequency change from the clock source.

The clock source of `LP_DYN_FAST_CLK` depends on the chip's power mode (see Chapter 13 Low-Power Management).

*   Select `LP_FAST_CLK` as its clock source in Active and Modem-sleep mode
*   Select `LP_SLOW_CLK` as its clock source in Light-sleep and Deep-sleep mode

### 9.2.4.3 Peripheral Clocks

Table 9.2-3, Table 9.2-4, Table 9.2-5, and Table 9.2-6 list the derived HP clock sources, HP clocks for each peripheral, derived LP clock sources and LP clocks for each peripheral.
```