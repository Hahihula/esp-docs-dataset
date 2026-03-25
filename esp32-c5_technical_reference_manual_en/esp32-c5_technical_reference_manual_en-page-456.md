

```markdown
Chapter 9 Reset and Clock

Register 9.87. LP_CLKRST_LP_CLK_PO_EN_REG (0x0004)

Continued from the previous page...

LP_CLKRST_CORE_EFUSE_OEN Configures whether to gate the EFUSE_CTRL clock.
    0: Disable the clock gate
    1: Enable the clock gate
    (R/W)

LP_CLKRST_SLOW_OEN Configures whether to gate the LP_SLOW_CLK signals to pad.
    0: Disable the clock gate
    1: Enable the clock gate
    (R/W)

LP_CLKRST_FAST_OEN Configures whether to gate the LP_FAST_CLK signals to pad.
    0: Disable the clock gate
    1: Enable the clock gate
    (R/W)

LP_CLKRST_RNG_OEN Configures whether to gate the RNG clock signals to pad.
    0: Disable the clock gate
    1: Enable the clock gate
    (R/W)

LP_CLKRST_LPBUS_OEN Configures whether to gate the LP bus clock signals to pad.
    0: Disable the clock gate
    1: Enable the clock gate
    (R/W)

Register 9.88. LP_CLKRST_LP_CLK_EN_REG (0x0008)
```

```markdown
LP_CLKRST_FAST_ORI_GATE Configures the clock gate to LP_FAST_CLK.
    0: Invalid. The clock gate controlled by hardware FSM
    1: Force the clock to pass the clock gate
    (R/W)
```