

```markdown
| LP_CLKRST_FAST_CLK_SEL | Clock Source |
|-------------------------|--------------|
| 0                       | RC_FAST_CLK  |
| 1                       | XTAL_CLK     |
| 2                       | PLL_LP_CLK   |

LP_DYN_SLOW_CLK and LP_DYN_FAST_CLK can be derived from LP_SLOW_CLK or LP_FAST_CLK depending on the chip's power mode (see Chapter 14 Low-Power Management), and should be able to operate in all power modes to drive LP AON modules. These two clocks are always synchronous with each other.

*   In Active mode, select LP_FAST_CLK as the clock source. In this case, LP_DYN_SLOW_CLK has the same frequency with LP_SLOW_CLK, and the same phase with LP_FAST_CLK;
*   In Deep-sleep mode, select the clock source according to PMU configurations. If the LP CPU is off, LP_SLOW_CLK is the clock source, and has the same frequency and phase as LP_DYN_FAST_CLK in this case; if the LP CPU is on, LP_FAST_CLK is the clock source.

LP_PERI_CLK is derived from LP_DYN_FAST_CLK and drives all the buses for LP peripherals.
XTAL_D2_CLK is derived from XTAL_CLK divided by 2.

### 10.2.4.3 Peripheral Clocks

Table 10.2-4, Table 10.2-5, Table 10.2-6, and Table 10.2-7 list the derived HP/LP clock sources and HP clocks/LP clocks for each peripheral.
```