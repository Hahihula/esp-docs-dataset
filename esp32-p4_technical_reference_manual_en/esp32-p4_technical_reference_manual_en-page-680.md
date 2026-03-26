

```markdown
Chapter 10 Reset and Clock

Register 10.15. HP_SYS_CLKRST_PERI_CLK_CTRL02_REG (0x0038)

Continued from the previous page...

HP_SYS_CLKRST_SDIO_LS_DRV_CLK_EN Configures whether to enable SDIO_DRV_CLK.
    0: Disable
    1: Enable
    (R/W)

HP_SYS_CLKRST_SDIO_LS_SAM_CLK_EN Configures whether to enable SDIO_SAM_CLK.
    0: Disable
    1: Enable
    (R/W)

HP_SYS_CLKRST_MIPI_DSI_DPHY_CLK_SRC_SEL Configures the clock source for DSI_DPHY_CFG_CLK and DSI_DPHY_PLL_PEECLK.
    0: PLL_F20M_CLK
    1: RC_FAST_CLK
    2: PLL_F25M_CLK
    3: Invalid
    (R/W)
```