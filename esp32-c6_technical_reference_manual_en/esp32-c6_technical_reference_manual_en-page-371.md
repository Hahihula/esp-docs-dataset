

```markdown
Chapter 8 Reset and Clock

Register 8.82. LP_CLKRST_CLK_TO_HP_REG (0x0020)

| 31 | 30   | 29           | 28               | ... | 0 |
|----|------|--------------|------------------|-----|---|
| 1  | 1    | 1            | 0                | ... | 0 |

LP_CLKRST_ICG_HP_FOSC (reserved)
LP_CLKRST_ICG_HP_SOSC
LP_CLKRST_ICG_HP_XTAL32K

LP_CLKRST_ICG_HP_XTAL32K Configures the clk gate of XTAL32K_CLK to HP system
0: The clk could not pass to HP system
1: The clk could pass to HP system (R/W)

LP_CLKRST_ICG_HP_SOSC Configures the clk gate of RC_SLOW_CLK to HP system
0: The clk could not pass to HP system
1: The clk could pass to HP system (R/W)

LP_CLKRST_ICG_HP_FOSC Configures the clk gate of RC_FAST_CLK to HP system
0: The clk could not pass to HP system
1: The clk could pass to HP system (R/W)

Register 8.83. LP_CLKRST_LPMEM_FORCE_REG (0x0024)

| 31 | 30   | ... | 0 |
|----|------|-----|---|
| 0  | 0    | ... | 0 |

LP_CLKRST_LPMEM_CLK_FORCE_ON Configures whether or not force open the clock gate of LP MEM
0: Invalid. The clock gate controlled by hardware FSM
1: Force open clock gate of LP MEM (R/W)
```