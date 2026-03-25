

```markdown
## Register 9.93. LP_CLKRST_CLK_TO_HP_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_ICG_HP_FOSC                                                       |
|     | (reserved)                                                                  |
| 30  | LP_CLKRST_ICG_HP_SOSC                                                      |
| 29  | LP_CLKRST_ICG_HP_XTAL32K                                                   |

LP_CLKRST_ICG_HP_XTAL32K Configures whether to gate the XTAL32K_CLK signals to HP system.
- 0: Disable the clock gate
- 1: Enable the clock gate (R/W)

LP_CLKRST_ICG_HP_SOSC Configures whether to gate the RC_SLOW_CLK signals to HP system.
- 0: Disable the clock gate
- 1: Enable the clock gate (R/W)

LP_CLKRST_ICG_HP_FOSC Configures whether to gate the RC_FAST_CLK signals to HP system.
- 0: Disable the clock gate
- 1: Enable the clock gate (R/W)
```

```markdown
## Register 9.94. LP_CLKRST_LPMEM_FORCE_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31  | LP_CLKRST_LPMEM_CLK_FORCE_ON |

LP_CLKRST_LPMEM_CLK_FORCE_ON Configures whether to force enable the gate of LP Memory.
- 0: Invalid. The clock gate controlled by hardware FSM
- 1: Force open clock gate of LP Memory (R/W)
```