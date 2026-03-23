

```markdown
Chapter 8 Reset and Clock

Register 8.76. LP_CLKRST_LP_CLK_PO_EN_REG (0x0004)

Continued from the previous page...

LP_CLKRST_CORE_EFUSE_OEN Configures the clock gate to pad of the EFUSE_CTRL clock.
    0: Disable the clk pass clock gate
    1: Enable the clk pass clock gate
    (R/W)

LP_CLKRST_SLOW_OEN Configures the clock gate to pad of the LP_SLOW_CLK.
    0: Disable the clk pass clock gate
    1: Enable the clk pass clock gate
    (R/W)

LP_CLKRST_FAST_OEN Configures the clock gate to pad of the LP_FAST_CLK.
    0: Disable the clk pass clock gate
    1: Enable the clk pass clock gate
    (R/W)

LP_CLKRST_RNG_OEN Configures the clock gate to pad of the RNG clk.
    0: Disable the clk pass clock gate
    1: Enable the clk pass clock gate
    (R/W)

LP_CLKRST_LPBUS_OEN Configures the clock gate to pad of the LP bus clk.
    0: Disable the clk pass clock gate
    1: Enable the clk pass clock gate
    (R/W)

Register 8.77. LP_CLKRST_LP_CLK_EN_REG (0x0008)
```

```markdown
LP_CLKRST_FAST_ORI_GATE Configures the clock gate to LP_FAST_CLK
    0: Invalid. The clock gate controlled by hardware fsm
    1: Force the clk pass clock gate
    (R/W)
```