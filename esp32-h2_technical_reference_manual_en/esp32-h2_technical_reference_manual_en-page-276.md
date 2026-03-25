

```markdown
Chapter 7 Reset and Clock

The clock source of LP_DYN_SLOW_CLK is LP_SLOW_CLK. There is no frequency change from the clock source.

The clock source of LP_DYN_FAST_CLK depends on the chip's power mode (see Chapter 11 Low-Power Management).

*   Select LP_FAST_CLK as its clock source in Active and Modem-sleep mode
*   Select LP_SLOW_CLK as its clock source in Light-sleep and Deep-sleep mode

7.2.4.3 Peripheral Clocks

Table 7.2-3, Table 7.2-4, Table 7.2-5, and Table 7.2-6 list the derived HP/LP clocks sources and HP/LP clocks for each peripheral.
```